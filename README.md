name: Generate README

on:
  push:
    branches: [main]
    paths:
      - 'readme.source.md'
      - '.github/workflows/readme-aura.yml'
  schedule:
    - cron: '0 6 * * *'
  workflow_dispatch:

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      # Busca o calendário de contribuições e coloca no bloco "ATIVAÇÕES".
      # Só muda a cópia usada no build (o readme.source.md do repo não é commitado).
      - name: Fetch contributions
        shell: python
        env:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          LOGIN: ${{ github.repository_owner }}
        run: |
          import json, os, re, pathlib, urllib.request
          q = 'query($l:String!){user(login:$l){contributionsCollection{contributionCalendar{weeks{contributionDays{date contributionLevel}}}}}}'
          req = urllib.request.Request('https://api.github.com/graphql',
              data=json.dumps({'query': q, 'variables': {'l': os.environ['LOGIN']}}).encode(),
              headers={'Authorization': 'bearer ' + os.environ['GH_TOKEN'], 'Content-Type': 'application/json'})
          try:
              d = json.load(urllib.request.urlopen(req, timeout=30))
              weeks = d['data']['user']['contributionsCollection']['contributionCalendar']['weeks']
              days = [x for w in weeks for x in w['contributionDays']]
              L = {'NONE': 0, 'FIRST_QUARTILE': 1, 'SECOND_QUARTILE': 2, 'THIRD_QUARTILE': 3, 'FOURTH_QUARTILE': 4}
              cal = {'start': days[0]['date'], 'levels': [L.get(x['contributionLevel'], 0) for x in days]}
              p = pathlib.Path('readme.source.md'); s = p.read_text(encoding='utf-8')
              s, n = re.subn(r'var CAL = .*?; // CONTRIB', lambda m: 'var CAL = ' + json.dumps(cal, separators=(',', ':')) + '; // CONTRIB', s)
              p.write_text(s, encoding='utf-8')
              print('contribuições:', len(days), 'dias, blocos atualizados:', n)
          except Exception as e:
              print('::warning::não consegui buscar as contribuições, mantendo as anteriores:', e)

      - name: Generate README
        uses: collectioneur/readme-aura@main
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          auto_commit: 'false'

      # Limpa máscaras que o gerador cria e não usa (SVGs mais leves) e deixa as larguras em %,
      # pra os blocos e as fileiras (projetos, redes) terem sempre as mesmas bordas, em qualquer tela.
      - name: Post-process
        shell: python
        run: |
          import re, pathlib, math
          # 1) remove máscaras e clip-paths que o gerador cria e não usa (deixa os SVGs bem mais leves)
          for f in pathlib.Path('.github/assets').glob('*.svg'):
              s = f.read_text(encoding='utf-8')
              used = set(re.findall(r'url\(#([^)]+)\)', s))
              def drop(m):
                  return m.group(0) if m.group(2) in used else ''
              s2 = re.sub(r'<(mask|clipPath) id="([^"]+)">.*?</\1>', drop, s, flags=re.S)
              if s2 != s:
                  f.write_text(s2, encoding='utf-8')
                  print(f.name, len(s), '->', len(s2))
          # 2) larguras em %, pra blocos e fileiras (projetos, redes) manterem as mesmas bordas em qualquer tela
          p = pathlib.Path('README.md'); s = p.read_text(encoding='utf-8')
          BASE = 860
          s = re.sub(r'\[!\[([^\]]*)\]\(([^ )]+)(?: "[^"]*")?\)\]\(([^)]+)\)', r'<a href="\3"><img src="\2" alt="\1" width="100%"></a>', s)
          s = re.sub(r'!\[([^\]]*)\]\(([^ )]+)(?: "[^"]*")?\)', r'<img src="\2" alt="\1" width="100%">', s)
          def pct(m):
              v = math.floor(int(m.group(1)) / BASE * 100 * 1000) / 1000
              return f'width="{v:g}%"'
          s = re.sub(r'width="(\d+)" height="\d+"', pct, s)
          p.write_text(s, encoding='utf-8')

      - name: Commit and push
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add README.md .github/assets
          if git diff --cached --quiet; then
            echo "Sem mudanças."
          else
            git commit -m "regenerate README via readme-aura"
            git push
          fi
