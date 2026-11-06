```aura width=860 height=180
<div style={{
  width: '100%', height: '100%', background: '#08080c',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter',
  position: 'relative', overflow: 'hidden', borderRadius: 16,
  border: '1px solid rgba(255,255,255,0.14)'
}}>
  <style>{`
    @keyframes drift-right { 0%, 100% { transform: translateX(0px); opacity: 0.75; } 50% { transform: translateX(320px); opacity: 1; } }
    @keyframes drift-left { 0%, 100% { transform: translateX(0px); opacity: 0.7; } 50% { transform: translateX(-260px); opacity: 1; } }
    @keyframes drift-short { 0%, 100% { transform: translateX(0px); opacity: 0.9; } 50% { transform: translateX(180px); opacity: 0.55; } }
    @keyframes breathe { 0%, 100% { opacity: 0.85; } 50% { opacity: 0.35; } }
    #orb-1 { animation: drift-right 9s ease-in-out infinite; }
    #orb-2 { animation: drift-left 12s ease-in-out infinite; }
    #orb-3 { animation: drift-short 10s ease-in-out infinite; }
    #orb-4 { animation: drift-right 13s ease-in-out infinite reverse; }
    #orb-5 { animation: breathe 7s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="ga" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(255,80,90,0.30)" />
        <stop offset="45%" stopColor="rgba(220,50,60,0.14)" />
        <stop offset="70%" stopColor="rgba(220,50,60,0)" />
      </radialGradient>
      <radialGradient id="gb" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(255,130,135,0.20)" />
        <stop offset="45%" stopColor="rgba(220,60,70,0.10)" />
        <stop offset="70%" stopColor="rgba(220,60,70,0)" />
      </radialGradient>
      <radialGradient id="gc" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(230,110,115,0.15)" />
        <stop offset="70%" stopColor="rgba(230,110,115,0)" />
      </radialGradient>
    </defs>
    <ellipse id="orb-1" cx="180" cy="215" rx="260" ry="170" fill="url(#ga)" />
    <ellipse id="orb-2" cx="320" cy="220" rx="220" ry="150" fill="url(#gb)" />
    <ellipse id="orb-3" cx="450" cy="220" rx="180" ry="130" fill="url(#gc)" />
    <ellipse id="orb-4" cx="600" cy="230" rx="160" ry="110" fill="url(#gb)" />
    <ellipse id="orb-5" cx="760" cy="230" rx="130" ry="100" fill="url(#gc)" />
  </svg>

  <div style={{
    position: 'absolute', left: 48, top: 42, width: 96, height: 96,
    borderRadius: 48, background: 'linear-gradient(135deg, #6b1e25, #111118)',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
  }}>
    <img src="data:image/jpeg;base64,/9j/2wBDAAQEBAQFBAUGBgUHCAcIBwoKCQkKChALDAsMCxAYDxEPDxEPGBUZFRMVGRUmHhoaHiYsJSMlLDUvLzVDP0NXV3X/2wBDAQQEBAQFBAUGBgUHCAcIBwoKCQkKChALDAsMCxAYDxEPDxEPGBUZFRMVGRUmHhoaHiYsJSMlLDUvLzVDP0NXV3X/wgARCACwALADASIAAhEBAxEB/8QAHQAAAAYDAQAAAAAAAAAAAAAAAQQFBgcIAAIDCf/EABoBAAIDAQEAAAAAAAAAAAAAAAAEAQIDBQb/2gAMAwEAAhADEAAAACrzoF6V0a8ygmOHZxlH0L8pfTkuy6Beo3ltbDoAL4N4H4aCOBdaGBHAEMzMDAEAtTU+xsHU3yzDLJRpMlKvRDzvtkN8aH3HCyvmpfOkt8dN2O5sWOqkqcFm2ymvhsXyII5hUbRbOb6hrmBIZsBXeSKav5FYc/V3l7zuu3SS2O9waeyoQ8GBHzlg4qdz5h5nY80inqImWjy5Nejcb1KPKMhxR0eV3SlJM1w2DMkzMEOnpbErjyarHDeDbHaQDblprE9zohlzj9zWUYWjerFzD8M5g3LLeqsl6q2nqBNqLGdYSCol+g8vsOu164IZB6I0BTi1dR20sMQ8IsvnSRV2VCctOLiegqF1nZY3pkc2IjRZus74VWS4i5j6oaW0pWoKBDv+aSBAd1RzXYOGKVrK7RfebrXQjSLYRsngzZhfYbv896w63l6HZvJDarmV2XtaeIKKzfGOnZENlYhieYIe9B5wMHGuZghsHp6mVGheJmiEdsmNVxDCL3fk+v05+a9Yox2koVWlhq8m6xpaYjCMop5pEcOiOXEG1D9t5L7XC8/Dvpku6YeZHf0xwPKkdRtjtgAAgZKhJNsqBWh5XYnaP3C/uV3aeys+i2kpaVzZguoWgqTbvscEyAY9zh1xBjVwgyNov5vYA2wzbm7Q6Mg24o2QZ9rBZ1JyJXyZh6t5rb8RmbUfjgRpaVbZpohDbSdoohjDVxU8n7ZOWCAzTrmuEn3H1RJDSd0KWESztUrPIdFcbMjNDmddgIbyiB/mHHG1JFe5xRHcnKlo3PdyW+BbiucIlKHbWDZccRC8GG8qI9Z4cSnORPd7d2i1oEOundN11o3GYnEXgmz5UgoqR2qsOlzR4oa2oZOEDYG5QiE9XX//xAAoEAABBQACAQQCAgMBAAAAAAAEAQIDBQYABxEIEBIgExQVIRYiMEH/2gAIAQEAAQUA6V7Xlv4+28BHrc0qKi86d065/eKipzuqlS065T/rVyf5H6ZuAHFgHYvTwabMd5ZVlDueIrmrkrlLvL2ATD61GuZxF4HnLAhsGYrGukz9GqEZ8XyVWHDIi/b07X4sWj0tCVn7/S0RVBf+me9e6H1IU7Scgnt0BYKV1xF/Uh9I5+ijeOAr7wGHkGmr3Mi1tHC5ljXHzlW1nVkSJWlMLEeM9PoEYUEZ23AJssx6j61g279PJL4uxe5Rmz9Y/wDvPTPO52a3O1HzFYdanmytjuppx8pSPaNnuuY4X5nDPkZ1YBYx2WZ0+fjpSHNidGGU2SN8b+Knv1tumZmx9S5Ucmx9PIzpexe4yGwdY/8AvPTQz4Z/aX493qdBfK6KMqaRUB0LmtqdK7hNfes4+RPMJxMbWSt/cejHNPiV0afXsbTJptr6ZqJ7YfUfcNFxacXlbqz6HIG3hhiYrAWepJxuArqaIYFzI0SJiGMY9C6WpIZd9XYg9N31Ta0rRDWTqSrkh+tdXmWJ+MzA+ZzXemtZf7hOMRVdvcdosw/JZiW5tM+NW0ACd0iAz02/rrQf+Wie6MsZVPsQmK+6p3yWrI1i7NxbRbFJ0JF+vTPU7s5F3B2JFks9/arzqPNLe7bt+7O0U/SNe2eN61wy29Wp4tcM6nPp7GUgex0f6cel0N/aEVtJo1fT3pgMHZUSOzdikaz/AF7C7Ko8WBodBa6G4T2zmXNy2U7FtYbQbpupeNh7ct9ZLedq6GKcac04/rqjR9d2EHJAbFaVg5IlvnDkGNkfJq2fPHjfml5PTWUAnPK+3nhpxhxfPPOjutH3J8w8RDNKRHPN15WILkrWhHIgfgxknhzIQzaOBRxb0FSCSuvRmDDdWzDvqMQ8RmoBRmfrM5bGl2VoWZD9uq+oDtTMIKMIN3b2k2ugAqxHZepnbGE2VXoqNa00sUdzd9VNDIuq6x4FGyWH9VjXS/jY3XkNjqQqxjqnyq+ye9VT2tub196fhhXMjYxnaXdY9ayRz3v6Ap7EyzryPikEvnieXr2xTWZQw9RYhg0K3tRcUznOrJZlVTy0ZzbmkzVGtjJo8V9E5TUFJRiaja5nLj7/ALsvdGxE9qnTXtUNgy/2s5B5Rp15W1MGv0RtrAlKhFbmreFhAUkX6M8zvjZlu8WehCrT+27WpNI58k5BX2BHIshrJU/wfaJzRd+be0Qgggmf6dPWjSMuMTGqbTK3OhNj67mlQrr65RThNDXJ1zpbGayMK+MZ86y8teudns7Sn9MwzErOkOtwEAzGbARv+qeXLzyv0VffrLRtqrsUtJWwlyI3WxXEbY9Nr4yqJpUzCFEjUmwWThpckktSDBX1nn/kGGUaU7+l+St4DpZqiXM6uqsGyzV6wTU9G95QgDYi5R4FtrmKBmVuqultxSxixvaRUjaVq8sJyTszr2NY+y+vJPfzyOOSWSeQGrCHjcjTI469FgjucY23sak8PtE90a9lSLOb2KQ6AfYnlPqQyTiO0GINjeke1wcyDfepjlx3R2RZqbaWZz/i3ie3n2VeAJ/DVLIZJXJ+Oujl/K2Tr2T9vE6HPCntPzFoNItZcIo1FZzLRUkA6UtckadsufPWQgqtU9it+/nlaDNYH38sFhop5WtQmVUZOrSF6+rX1tJbQujnLhRyFQ/HhlhGGz+duZH1+60gS32vFLEyhaWVPAvlHhCo2WCWJfdV555iGrATX+Io3SIqluX5ROVZsvo2WTLaFro5Rmry9cMCKTJITPANNNMJmI4R4qwKPmdyQkNrcPFlt2SeZFOR3FChm5JG+N/ERVUahJcjpJa8CGRiDum/uaRHPgTxNQXK1R8W5yhleumo2re28tkcnMf1yTWh6UuBhPz8Jb3XzlGkV0TU8JCvx4x6eYvxGPpcV1LaDxtCBY4lZHST/A0mFI5nSqjpJUckcSrMXGivWJ6IFH4k/Iqr0xUBEafs/aVlVloi2rzS2iwN/wBlQaNE4jvKtXyss8LGslKk5G5Wx//EAEYQAAIBAwICBQgGBwYGAwAAAAECAwAEEQUhEjEiQVFhcQYQExQyUnKBFSAjkaHRJDNCQ2KxwTBjc4KSsiU2RIOiw1OTlP/aAAgBAQAGPwBdC1ebOoxJm3nbncovU394tSmGMfSdmrS2jdb9bReD0QQQesHYjzaa7vw212fVJ+zhm2U/Jqwa1ghMyWfBeR/9k9L/AMSf7bVLRelPo07HHYsMgmH/AIP5ra7tZjFcQSrJE45q6HINabq8ICmeL7RB+7mTZ1+RqeaGPgtdRT1qMDkHJxKv+rzAqcMDkHsI5GtF1MHe6sopG+PGH/EVfWbjK3FtNCR/iIVrgb2l6J8RsfMHcLBGd+KTY4+Eb0PS3E77jJChBj8TSERTKCh/eHc5wKIhuWDdSlS/4gCi0kLcA/aG4+vqXk5fEep63aNFg9cyKf8AchIrU9JuAfSWdy8JPvBT0W+Ywa1PSrjeS0uHjJ94D2WHiN617RnbZDHdwj4ug9afqIXp2V+FJ/guBw/zA89tCTk2l7cw/IkSD/dSH+IVras3oraDUrpGkxnlK2FQdbUkVjpr+mZQQzjikwxwHc4PAtPJPNHcuMAxAkR8XXyOWxQ9PBMZQ3REThU4fdwc+JqSf0dy03soCQscY7AtNHbXwgnK/ZicEozZyekoGCeQzsBQjuiM8+KN+MEH8KWR0aLj9meMZRj3jbfuoAsrqwyjryYfVt7u2laKeCVJYpBzR0PEprR/L/TYgHKJZ6xCn7idNlY1bXSjHrmmxO3e0TGOkjB2m066Q/IB68pB7kEco8Y5FPn1+LqTUoz/AK4qEgCPeS5FvExwNubt/CtXF3HA8qtK8kkpXhwztxH2cBQxq49JMIxK+ZZZHCAgcgSeoUjTeVFkj49hVlbh8W4aAfyltncDpngl3+Ho0zQ+UtnwEnhyzJw+PEKc6Z5RadK3IJ6dDxVLDfafx2hBIk4ONc9WGFPHnKgdJTuo+Icj3UYOIRMekhPscXd2Z66ZHUhlOCD1EfVura/gN1oepRer6la8+KM7CRB76VpEA9qHSgW/7sjEUkgG0OnXTn5gJXlMT+3bJGPF5FHn8pZSQF9fh3P8MVazdzH1i3jmEFomeh6JNgwII2PPvr0PrNomQCyAgDblgYoLFOHJIIRI3bn8K0cW9+ynckWkxz4nFAixv9uRFjNgUzT2l0meZe2mUHHitESiA8tmwpOPiAo+ie4iU52hlbg+5SRQkDK3pWIlOME7d21Yxsdxk5IzSz5HECEffc7dE/hj62samhJgkm4Lf/BiHAla9rLps5jtIj8PTerLTw3Tvr9D/ktxxnz3mkpdRQ2t1L6S5IXilkMihfR/DgchRAdo4ATgZ6TE9ppSAUtEYcczcz3JSi3s04sDpHc0A0SmjhQPlRGOfVRE1nA/xxq38xTE6Rbxy+/CPRP96Yo3unSPd26HJjcZlTwPWKKvseWDzBFSKeor9a2srSEy3FxKscSDmzscAVpukQkN6CL7Rx+8lfd2+ZqaGCTitdNQ2sZHJnBzK33+ZQF4iSML291SHWhEVuYwbMxN0CG/WADmpXk2atIJAeBhx8I6k7/Gh9mMKoEca82oJNFwjljHKhJbzowPPDZwaHTxk0Mmhh1rgNzDxd7CiDuhoX+nqEMpPFHyBNPzDou4PPon+Y+sNY1aIfSssZEUXP1VG/8AY1NBbSj6VvUZLZeuJOTTHw6qJJJPmsA8JktrL9MuB2rDuq+LGoJbpHWCMt8t/wCtaxqUsWcOI08EWs3IEk7nib+g8BThdPQxgHcKNhXFbu0QzunMVxh98CiC54gOVMkNwYIQcAg7mhIt+HHusxGaeC8/V52B3wesqalnXdkIIq3u4eU8REw/vAu5+f1iZmE+oSITb2anpN2M/upVzqWozmW5mbc8lUDkiDqUdQ89k91bPFJeRiW5bi4XQc0T5Vbw2KyvBEymTEb4Rm5cTYwTTuV6U1xMw+W1SXTWE1wVbkNl+Zqay+g9PClhgguWxjIIevVJ4OGTg4g2eNTgZI4qf1iPkDzrhhWmWeRcoftGOcLjtwCa4bDVbGVhjCAtE/3SU0E0fI9Y66vh2W5p4FBJBJAoXMtu6RdbMMYJOAN+s9n1Zrq7uJJ55W4pJZGLOx7ST549e1KD/h1rJm3RhtcTJ/NEpo5EVw2RhhkEnbka15dMuOLTILy4WQocxMsYXdOfXsK0aEjB9URiO+Qcf9aKnAFEpcy5OxVUUVGvCdjnhJzvVwQMLwYApzIOvZusVcQwQARzriWNW4S+/FkMc75q4VbeRRIMDiVW4BnOxGKhJnkYAbh9/uNahGOu2cfhVxJZwqywjHSkEfE3Uo76t45ZSViGFTGAv14tR1FHg0dG8Husfsx/w9rVDb28KRQQoEjjQcKoq7AAVP5O6TP+myrwXsyH9Qjc4h/eN19grV9ItEDzfRxvfTJuJTCy5X7jVsi9USAY7AKwcUaM87cMUfPvJ6qdAoCnrzvX6PKDNn2aXI6udbtkVjatQOP+nl2/y1ZXYmzwtdXBzsI1gjz95NAnn9VLTT7Ka5uG5RxKWPiewd5qG+8pik8owyWKHMS/4rft+ApEjQKqgKqqMAAcgAKn0nyeuElvd0mvEPElv3R9TSfgKZ3ZmZiSWJySTuSSeZNajqHqsJsYbT1P0kspUK0hDsAo57UqcQwrFe7o7ebFQx2z3KpJGQ7wnBXBpIY7meULnEkr5ankfUzNA46KMmHB8RVpIRjijViD5iwq7jgR5JpVEaKNyS5xWk6ewdZrqSUzZ2wi4Yr4E4+sLbTNPgtYetYk4c/EeZr0mq6gkTEZSBenPJ8MY3qWx05X0/TmyGAb7eYdkjjkP4R57m2stQmghn3kVDsWxji8a0eVmLF7KHLHrYDBJoZNCa7nVc8hUSaehEHBkvnh50syXMJ+zXm4yHA3Wja6lHwDmhYcJG9RhGyqjbHZRx30+a0/1lwondwCTsOEDetISyuUkZI53nCnOHkIwSe8DzYyK+xs7iT4Inb+QrKeT+psO61k/Kv+W9V//JJ+VPHZGDTIT/8AAOOb/wCx6knnmkllkOXkkYu7HvJyT9WKFm6drPJF/lJ41/nQB6qSa2uI4hH0VMilhjwpBfeUNy0g2AiRQieANMI9ZiWJeReMgk9/CazdwpfxqMI8WfSoB3HmKuIJpHa2KHg4lIKnvBo55Yo5OBUUlhZxpYRRejW5mlCRls5bHMmlOq6+7nrjtIgo/wBclAnRzdN71zM8v4bCgLTRbCDHuW8YP34rC9Edg2rma5n67QTPiC6AXuEi+zSshzmiuDTy2nGrke0NjTQySO4Q75GeKlluXblStGihgeytzzqK2gQvNNIscag7s7HAFWlpEpCRRKozzyOef7OK3t4y8rnCqNuW5JJ2AA3JNEZBwSMg5Bx2GuIdW/3VBFMxNvJCkkTnrVhnHiKRfSDJzzP86YYRtjvivSiGPHvCgyTqFAolnBzy37achtxsKttf1x3jtI5hGmFLlGlBAdh2VDcW8ySwyoHjkRgyOrcipHMefikIRe1jwj7zWLjXtMi+K6jH9aw3lVpfynBrC+VWl/OcD6iRxozu7BUVRlmZjgADrJq40qGT9OnRku7pW6Ckb+rIetCRh26z3UBuWYjbvPICuG4HFcn9wD7H+IR1/wAIrSZXUcZsoiCOpwMbUyNKyskoJ7Cvd3Glh9ORg880qCQiMoxI7yDSENk9e/dzFPHI7PjdOvANJJcknpZVD1VEg5tew/gGNajp2t3E4sMCa0KxmUxyn2owB1PTJoug+E14/wD646YNrklsh/YtUEA+8b0Wu765uGPXLK0n+4mtlH1l1HOL67DpZdsMQ6Elx8R9iP5msRpnq7qZbPgkuimGui2AjH9mEHl8Z3PVUokJ484Oa09Sd4xIn+lzREgw65w/WKIXMi5O60PsSaHGwjGc7nNAKCXPNjzNBiuKhtk6n4wPhr1gBuFfREk0OsEf2FraRfrJ5kjXxY4q4iiYraw/o8GBnENsOAffjNcCKFRTsBXjmuEbSL19oq3tJWy7xCfw9N0sVnBonFbCskZY+yvbWVuniGdljPCBSr64849yUCT8eYqO6khKTYdRAff7c+7Wo6XIQHAZ4/BvyNOkoYYYjvVhtQxK+TjcgYFdJduojcHwP1tT1Thz9H6fNKh/vXHAn4mriQnJ4VQfPc1nNEdlE5rT7g4EvoRDMB1NHt+I3pXwPGjg0ZZT3Io5s3ZTSycz9wHYKjihj45HOFUfzPdWHAZsZd+0/lTfYq/Ft0hxbeBq+vjeCCGID0Sc8mQciPcq5kg9ni6Xxj2qB6hRQQoVPPIzX2I4H7Ccqfyoo6kMOYPmAAyTyFB7k+gTsYZkPgv51eRWTtHHNEY7hc8RliJBwx7iAadevjzntyKNeIzXgcUGYt6MkFgO6lVtUiR8ey+UNEfSduezD5NPKchB0Y191fzPXQ5nfGAMkk9QFCe+hIvZ1BZSP1SdUfj71NaQYIjOJWHWw/ZHhXeeWeXz7hUq27McBl9MWOX8ByC0B156VAZ3NbVxseiD99Rme3kaJSR9mwRvkxyKb03lZqOmXKKC8VwkUo/yMg6VYt4gpA3kO7n5/lXPOTSo+6vHjFXJR19GGXgXO+GGaNDurjHI8/GsDtremkP7I28TRpNSvUV4NPIMSnk1wfZJ+DnXFb8P0heOYoO1BzeX5DzNZxnErDExB9ke5+dEgEgDfu8xNACl+yBI5ZNA58BRCnpY3b+lf//EADARAAIBAgQDBQcFAAAAAAAAAAECAAMRBBIhMRBBkTJCUWFxBRMUICKBoRUwUrHB/9oACAECAQE/ALd3pFNxBo/qP2NnPmJ3V8Q3+2g7TdYe0vrwqMR4/YQ1DzWp0MSul7BvsdD8jC403ndHm1/zeDtN0hGq+seqlNSzGwn6oWY5aekPtFgOwIPatPZqZ63lGtSqpdD8l+90gFhDUAa0xdQ1KxVuyvKA0yugsYGOafD021LATD56FdbHQmI2YA8QDuYxtKlPIQ176x6l67m1xmj1aWS4QAiZrZWgNArqxBmce8W3iIj/AFWBHnxLchqYBzO8xRtTv4azvGGxKiNSBB+vbaDaUlu6+swo0Z/E6eg4gAbDgyqwsQCJikK1X8jKS09DmGaZLggkGMhR8t7zDUg72O1pSUpTCgE25nSfX5D8yz+I6fJj6GZlYbkf1PdujjSVKl9AgESmZgUARjzvbgWUbkCZ6f8ANevEA3JufSY64Smw5NFajVAzWBgo0F1uJWqKL5RMFf3HnczKOdzAANhxHDHBjTFtr6xDMPRz6naGlTy2yL0lJFS4EAFoV4BZ3jwKhlIO0+Bpjm0VQAAI5toIBxKAnn1M/8QAOREAAgECAwQGBwYHAAAAAAAAAQIDABEEEiExQVGBBRAgYXGRExQiMpKxwRUjUlNy0iQwM0JUk6H/2gAIAQMBAT8Az6CUAXBtINzA7+e+pUCOQDcaEHuOoo+1AD+BsvJtR8j/ACD7WHU70Yg+DaigB6aQAWV4i1vFc4FPrFCeAK+Rv9ai/pz/AKAeeYdUKA6+zzIFCEC1ni+IVJhZLElea6jsROqsQ18rCzVsmkO5IipPeFyfOn0hhHHM3mbfSo2ASYHegA+IGo4XlYKi3NfY6qozS68BQ6JjJ99qboZxqk3mLVPh5oXIcc+PYyWHogRcm8jbgBUrh3JAsNAB3DQUIfuVO9iTyGldHw5IQy+82+gJVf2iGFMi5dtHEODZYyRxrFhJ4GuNQKdcrEdbuuXIlwu8na1RR521NlGrHgKik9MXXLaykjfoN1RREQRgGxyio4Js5zSlge6shIYA7LUwxSuMqKRThjGxI/tNSRkLmYHXZ1pCSuZjlTid/gN9SSAgIgsg8yeJro8ZsQF/ECD4Ea1GRkFDQGkmGYAJt22NEA1iCBG1uFdIsAYYhtRBm8W62Zna7MSeJNz1I7owZWIPEG1YOTNFGb7QKSKaeQqNFrEYGaAB1GzmDUc2eO9rGsROyDMACQd5sKxBSWZ5HkUX2qt2I+lfww/MbyX91ZsN+VJ/sH7ex0biCqMp2A/OklV0uG17qBlAOed2HAmnlUA610hIzOg3Wv1JDK4ukbsO4E16piv8eX4D1vKGijTIoK3uwFiwOwHw410dYvIh3pTLPCxy3Io4jEtpZqgidrZzWPI9Y2XAAr1hx7gVP0jUc9tO7ubuxbxN6sOx0cyCY3220pwL1iphHoPeoTyhr+ka/jUsryWLHsXrd1KxVgQdRX2jMdqrTuSSxNyaTXU0ATs60mdBYBOaK3/SK//Z" width={88} height={88} style={{ borderRadius: 44 }} />
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', marginLeft: 168, gap: 8 }}>
    <div style={{ display: 'flex', fontSize: 38, fontWeight: 800, color: '#ffffff', letterSpacing: '-1px', lineHeight: 1 }}>
      Eduardo Staudt
    </div>
    <div style={{ display: 'flex', fontSize: 15, color: 'rgba(220,220,220,0.80)', fontWeight: 400, letterSpacing: '0.3px' }}>
      Graduando em Ciência da Computação (UTFPR) e Ciências Econômicas (Uninter)
    </div>
    <div style={{ display: 'flex', fontSize: 14, color: 'rgba(255,115,122,0.95)', fontWeight: 700, letterSpacing: '0.3px' }}>
      Dev Fullstack · Deep Learning
    </div>
    <div style={{ display: 'flex', gap: 20, marginTop: 4 }}>
      {[
        ((github && github.stats && github.stats.totalRepos) || 0) + ' Repositórios',
        ((github && github.user && github.user.followers) || 0) + ' Seguidores',
        ((github && github.stats && github.stats.totalStars) || 0) + ' Estrelas',
        ((github && github.stats && github.stats.totalCommits) || 0) + ' Commits',
      ].map(function(txt) {
        return (
          <div key={txt} style={{ display: 'flex', alignItems: 'center', gap: 5 }}>
            <div style={{ width: 8, height: 8, borderRadius: 4, background: '#ff5a64' }} />
            <span style={{ fontSize: 12, color: 'rgba(220,220,220,0.72)', fontWeight: 600 }}>{txt}</span>
          </div>
        );
      })}
    </div>
  </div>
</div>
```

```aura width=860 height=84
<div style={{
  width: '100%', height: '100%', background: '#08080c',
  display: 'flex', alignItems: 'center', justifyContent: 'space-around',
  fontFamily: 'Inter', borderRadius: 16,
  border: '1px solid rgba(255,255,255,0.06)', padding: '0 28px', boxSizing: 'border-box',
}}>
  {[
    { label: 'Pesquisa', sub: 'Em redes neurais' },
    { label: 'Sistemas', sub: 'Do início ao fim' },
    { label: 'Mente de empresário', sub: 'Tecnologia como negócio' },
    { label: 'Aprender fazendo', sub: 'Projetos de verdade' },
  ].map(function(item) {
    return (
      <div key={item.label} style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 6, width: 180 }}>
        <div style={{ width: 10, height: 10, borderRadius: 5, background: '#ff5a64' }} />
        <span style={{ fontSize: 13, fontWeight: 700, color: '#ffffff', textAlign: 'center' }}>{item.label}</span>
        <span style={{ fontSize: 11, color: 'rgba(235,235,235,0.82)', textAlign: 'center' }}>{item.sub}</span>
      </div>
    );
  })}
</div>
```

```aura width=860 height=180
(function() {
  var layers = [3, 5, 6, 5, 2];
  var xs = [150, 290, 430, 570, 710];
  var cy = 78, gap = 24;
  var nodes = layers.map(function(n, l) {
    var arr = [];
    for (var i = 0; i < n; i++) arr.push({ l: l, i: i, x: xs[l], y: cy - (n - 1) * gap / 2 + i * gap });
    return arr;
  });
  var edges = [];
  for (var l = 0; l < layers.length - 1; l++) {
    for (var a = 0; a < nodes[l].length; a++) {
      for (var b = 0; b < nodes[l + 1].length; b++) {
        var p = nodes[l][a], q = nodes[l + 1][b];
        edges.push({ id: 'ed' + l + '-' + a + '-' + b, x1: p.x, y1: p.y, x2: q.x, y2: q.y, delay: l * 0.5 + ((a * 3 + b) % 4) * 0.12 });
      }
    }
  }
  var all = [];
  nodes.forEach(function(layer) { layer.forEach(function(n) { all.push(n); }); });
  var css = '@keyframes sig { from { stroke-dashoffset: 0; } to { stroke-dashoffset: -210; } } '
    + '@keyframes pulse { 0%, 100% { opacity: 0.15; } 50% { opacity: 0.9; } } '
    + edges.map(function(e) {
        return '#' + e.id + ' { animation: sig 2.4s linear infinite ' + e.delay.toFixed(2) + 's; }';
      }).join(' ') + ' '
    + layers.map(function(n, l) {
        return '[id^="nd' + l + '-"] { animation: pulse 2.4s ease-in-out infinite ' + (l * 0.5) + 's; }';
      }).join(' ');

  return (
    <div style={{ width: '100%', height: '100%', display: 'flex', position: 'relative', overflow: 'hidden', background: '#08080c', borderRadius: 16, border: '1px solid rgba(255,255,255,0.14)', fontFamily: 'Inter' }}>
      <style>{css}</style>
      <svg width="860" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="gn" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(255,80,90,0.16)" />
            <stop offset="70%" stopColor="rgba(220,50,60,0)" />
          </radialGradient>
        </defs>
        <ellipse cx="430" cy="80" rx="380" ry="110" fill="url(#gn)" />
        {edges.map(function(e) {
          return <line key={'b' + e.id} x1={e.x1} y1={e.y1} x2={e.x2} y2={e.y2} stroke="rgba(255,90,100,0.16)" strokeWidth="1" />;
        })}
        {edges.map(function(e) {
          return <line key={e.id} id={e.id} x1={e.x1} y1={e.y1} x2={e.x2} y2={e.y2} stroke="#ff7b84" strokeWidth="2" strokeLinecap="round" strokeDasharray="6 204" />;
        })}
        {all.map(function(n) {
          return <circle key={'h' + n.l + n.i} id={'nd' + n.l + '-' + n.i} cx={n.x} cy={n.y} r="12" fill="rgba(255,90,100,0.45)" />;
        })}
        {all.map(function(n) {
          var out = n.l === layers.length - 1, inp = n.l === 0;
          return <circle key={'c' + n.l + n.i} cx={n.x} cy={n.y} r="6.5" fill={out ? '#ff5a64' : '#14080a'} stroke={inp ? '#f5f5f5' : '#ff5a64'} strokeWidth="2" />;
        })}
      </svg>
      {[
        { x: 150, t: 'ENTRADA' },
        { x: 430, t: 'CAMADAS OCULTAS' },
        { x: 710, t: 'SAÍDA' },
      ].map(function(lb) {
        return (
          <div key={lb.t} style={{ position: 'absolute', left: lb.x - 90, top: 152, width: 180, display: 'flex', justifyContent: 'center' }}>
            <span style={{ fontSize: 10, fontWeight: 700, color: 'rgba(210,210,210,0.45)', letterSpacing: '2px' }}>{lb.t}</span>
          </div>
        );
      })}
    </div>
  );
})()
```

```aura width=276 height=150 link="https://nnadsorption-app.web.app/" inline align=center
<div style={{ width: '100%', height: '100%', display: 'flex', padding: '0 6px', boxSizing: 'border-box', fontFamily: 'Inter', position: 'relative' }}>
  <div style={{ display: 'flex', flexDirection: 'column', width: '100%', height: '100%', gap: 6, padding: '16px 18px', boxSizing: 'border-box', background: '#08080c', borderRadius: 14, border: '1px solid rgba(255,255,255,0.14)', position: 'relative' }}>
    <span style={{ fontSize: 10, fontWeight: 700, color: '#ff5a64', letterSpacing: '1.5px' }}>PESQUISA</span>
    <span style={{ fontSize: 17, fontWeight: 700, color: '#ffffff' }}>NNAdsorption</span>
    <span style={{ fontSize: 12, color: 'rgba(235,235,235,0.78)', lineHeight: 1.5 }}>Redes neurais que modelam adsorção. Apresentada no CNMAC 2026 e SICITE 2026.</span>
  </div>
  <svg width="276" height="150" style={{ position: 'absolute', top: 0, left: 0 }}>
    <path d="M243 27 L249 21 M244 21 H249 V26" stroke="rgba(255,255,255,0.6)" strokeWidth="1.6" fill="none" strokeLinecap="round" strokeLinejoin="round" />
  </svg>
</div>
```

```aura width=276 height=150 link="https://glazzy.pages.dev" inline align=center
<div style={{ width: '100%', height: '100%', display: 'flex', padding: '0 6px', boxSizing: 'border-box', fontFamily: 'Inter', position: 'relative' }}>
  <div style={{ display: 'flex', flexDirection: 'column', width: '100%', height: '100%', gap: 6, padding: '16px 18px', boxSizing: 'border-box', background: '#08080c', borderRadius: 14, border: '1px solid rgba(255,255,255,0.14)', position: 'relative' }}>
    <span style={{ fontSize: 10, fontWeight: 700, color: '#ff5a64', letterSpacing: '1.5px' }}>SISTEMA</span>
    <span style={{ fontSize: 17, fontWeight: 700, color: '#ffffff' }}>Glazzy</span>
    <span style={{ fontSize: 12, color: 'rgba(235,235,235,0.78)', lineHeight: 1.5 }}>ERP para vidraçarias com desenho técnico, orçamentos, recibos e financeiro.</span>
  </div>
  <svg width="276" height="150" style={{ position: 'absolute', top: 0, left: 0 }}>
    <path d="M243 27 L249 21 M244 21 H249 V26" stroke="rgba(255,255,255,0.6)" strokeWidth="1.6" fill="none" strokeLinecap="round" strokeLinejoin="round" />
  </svg>
</div>
```

```aura width=276 height=150 link="https://thefenexy.itch.io/hero-maze" inline align=center
<div style={{ width: '100%', height: '100%', display: 'flex', padding: '0 6px', boxSizing: 'border-box', fontFamily: 'Inter', position: 'relative' }}>
  <div style={{ display: 'flex', flexDirection: 'column', width: '100%', height: '100%', gap: 6, padding: '16px 18px', boxSizing: 'border-box', background: '#08080c', borderRadius: 14, border: '1px solid rgba(255,255,255,0.14)', position: 'relative' }}>
    <span style={{ fontSize: 10, fontWeight: 700, color: '#ff5a64', letterSpacing: '1.5px' }}>JOGO</span>
    <span style={{ fontSize: 17, fontWeight: 700, color: '#ffffff' }}>Hero Maze</span>
    <span style={{ fontSize: 12, color: 'rgba(235,235,235,0.78)', lineHeight: 1.5 }}>Jogo educativo em Godot 4 com pixel art. Fui vice-líder e artista principal.</span>
  </div>
  <svg width="276" height="150" style={{ position: 'absolute', top: 0, left: 0 }}>
    <path d="M243 27 L249 21 M244 21 H249 V26" stroke="rgba(255,255,255,0.6)" strokeWidth="1.6" fill="none" strokeLinecap="round" strokeLinejoin="round" />
  </svg>
</div>
```

```aura width=860 height=160
(function() {
  var categories = [
    { title: 'Linguagens', color: '#f5f5f5', items: ['Python', 'Java', 'Flutter', 'SQL', 'Dart'] },
    { title: 'Machine Learning', color: '#ff5a64', items: ['PyTorch', 'TensorFlow', 'Keras', 'NumPy', 'Pandas', 'MLPs', 'PINNs'] },
    { title: 'Estudando', color: '#b8b8b8', items: ['Next.js', 'Programação Funcional', 'Plataformas de Hospedagem', 'Visão Computacional'] },
  ];

  return (
    <div style={{
      width: '100%', height: '100%', background: '#08080c',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter', padding: '18px 32px', gap: 14, boxSizing: 'border-box',
      borderRadius: 16, border: '1px solid rgba(255,255,255,0.14)',
      position: 'relative', overflow: 'hidden',
    }}>
      <style>{`
        @keyframes stack-right { 0%, 100% { transform: translateX(0px); opacity: 0.8; } 50% { transform: translateX(300px); opacity: 1; } }
        @keyframes stack-left { 0%, 100% { transform: translateX(0px); opacity: 0.7; } 50% { transform: translateX(-240px); opacity: 1; } }
        #stack-1 { animation: stack-right 10s ease-in-out infinite; }
        #stack-2 { animation: stack-left 13s ease-in-out infinite; }
      `}</style>
      <svg width="860" height="160" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="gs" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(255,80,90,0.20)" />
            <stop offset="45%" stopColor="rgba(220,50,60,0.08)" />
            <stop offset="70%" stopColor="rgba(220,50,60,0)" />
          </radialGradient>
        </defs>
        <ellipse id="stack-1" cx="200" cy="190" rx="260" ry="130" fill="url(#gs)" />
        <ellipse id="stack-2" cx="650" cy="190" rx="220" ry="110" fill="url(#gs)" />
      </svg>

      <div style={{ display: 'flex', fontSize: 10, fontWeight: 700, color: 'rgba(210,210,210,0.5)', letterSpacing: '3px' }}>
        STACK
      </div>
      <div style={{ display: 'flex', flexDirection: 'column', gap: 12 }}>
        {categories.map(function(cat) {
          return (
            <div key={cat.title} style={{ display: 'flex', alignItems: 'center', gap: 16 }}>
              <div style={{ display: 'flex', fontSize: 10, fontWeight: 700, color: cat.color, letterSpacing: '1px', width: 124 }}>
                {cat.title.toUpperCase()}
              </div>
              <div style={{ display: 'flex', flexWrap: 'wrap', gap: 7 }}>
                {cat.items.map(function(item) {
                  return (
                    <div key={item} style={{
                      display: 'flex', padding: '4px 13px', borderRadius: 6,
                      background: 'rgba(255,255,255,0.05)', border: '1px solid rgba(255,255,255,0.12)',
                      color: 'rgba(235,235,235,0.82)', fontSize: 12, fontWeight: 600,
                    }}>{item}</div>
                  );
                })}
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

```aura width=120 height=44 link="https://www.linkedin.com/in/eduardo-andrei-staudt/" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZwogIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICB3aWR0aD0iNDgiCiAgaGVpZ2h0PSI0OCIKICB2aWV3Qm94PSIwIDAgMjQgMjQiCiAgZmlsbD0ibm9uZSIKICBzdHJva2U9IiNmZmZmZmYiCiAgc3Ryb2tlLXdpZHRoPSIyIgogIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIKICBzdHJva2UtbGluZWpvaW49InJvdW5kIgogIGNsYXNzPSJpY29uIGljb24tdGFibGVyIGljb25zLXRhYmxlci1vdXRsaW5lIGljb24tdGFibGVyLWJyYW5kLWxpbmtlZGluIgo+CiAgPHBhdGggc3Ryb2tlPSJub25lIiBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIiAvPgogIDxwYXRoIGQ9Ik04IDExdjUiIC8+CiAgPHBhdGggZD0iTTggOHYuMDEiIC8+CiAgPHBhdGggZD0iTTEyIDE2di01IiAvPgogIDxwYXRoIGQ9Ik0xNiAxNnYtM2EyIDIgMCAxIDAgLTQgMCIgLz4KICA8cGF0aCBkPSJNMyA3YTQgNCAwIDAgMSA0IC00aDEwYTQgNCAwIDAgMSA0IDR2MTBhNCA0IDAgMCAxIC00IDRoLTEwYTQgNCAwIDAgMSAtNCAtNGwwIC0xMCIgLz4KPC9zdmc+"
  text="LinkedIn"
  backgroundColor="#111111"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#ff5a64' },
    { offset: '60%', color: '#ffffff' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#8c2a31' },
  ]}
/>
```

```aura width=12 height=44 inline align=center
<div style={{ width: '100%', height: '100%', display: 'flex' }} />
```

```aura width=128 height=44 link="https://www.instagram.com/eduardo_staudt_/" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZwogIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICB3aWR0aD0iNDgiCiAgaGVpZ2h0PSI0OCIKICB2aWV3Qm94PSIwIDAgMjQgMjQiCiAgZmlsbD0ibm9uZSIKICBzdHJva2U9IiNmZmZmZmYiCiAgc3Ryb2tlLXdpZHRoPSIyIgogIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIKICBzdHJva2UtbGluZWpvaW49InJvdW5kIgogIGNsYXNzPSJpY29uIGljb24tdGFibGVyIGljb25zLXRhYmxlci1vdXRsaW5lIGljb24tdGFibGVyLWJyYW5kLWluc3RhZ3JhbSIKPgogIDxwYXRoIHN0cm9rZT0ibm9uZSIgZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIgLz4KICA8cGF0aCBkPSJNMyA3YTQgNCAwIDAgMSA0IC00aDEwYTQgNCAwIDAgMSA0IDR2MTBhNCA0IDAgMCAxIC00IDRoLTEwYTQgNCAwIDAgMSAtNCAtNGwwIC0xMCIgLz4KICA8cGF0aCBkPSJNOC41IDEyYTMuNSAzLjUgMCAxIDAgNyAwYTMuNSAzLjUgMCAwIDAgLTcgMCIgLz4KICA8cGF0aCBkPSJNMTcgN3YuMDEiIC8+Cjwvc3ZnPg=="
  text="Instagram"
  backgroundColor="#111111"
  width={128}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#ff5a64' },
    { offset: '60%', color: '#ffffff' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#8c2a31' },
  ]}
/>
```

```aura width=12 height=44 inline align=center
<div style={{ width: '100%', height: '100%', display: 'flex' }} />
```

```aura width=120 height=44 link="https://www.youtube.com/@EduardoAndreiStaudt" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZwogIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICB3aWR0aD0iNDgiCiAgaGVpZ2h0PSI0OCIKICB2aWV3Qm94PSIwIDAgMjQgMjQiCiAgZmlsbD0ibm9uZSIKICBzdHJva2U9IiNmZmZmZmYiCiAgc3Ryb2tlLXdpZHRoPSIyIgogIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIKICBzdHJva2UtbGluZWpvaW49InJvdW5kIgogIGNsYXNzPSJpY29uIGljb24tdGFibGVyIGljb25zLXRhYmxlci1vdXRsaW5lIGljb24tdGFibGVyLWJyYW5kLXlvdXR1YmUiCj4KICA8cGF0aCBzdHJva2U9Im5vbmUiIGQ9Ik0wIDBoMjR2MjRIMHoiIGZpbGw9Im5vbmUiIC8+CiAgPHBhdGggZD0iTTIgOGE0IDQgMCAwIDEgNCAtNGgxMmE0IDQgMCAwIDEgNCA0djhhNCA0IDAgMCAxIC00IDRoLTEyYTQgNCAwIDAgMSAtNCAtNHYtOCIgLz4KICA8cGF0aCBkPSJNMTAgOWw1IDNsLTUgM2wwIC02IiAvPgo8L3N2Zz4="
  text="YouTube"
  backgroundColor="#111111"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#ff5a64' },
    { offset: '60%', color: '#ffffff' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#8c2a31' },
  ]}
/>
```

```aura width=12 height=44 inline align=center
<div style={{ width: '100%', height: '100%', display: 'flex' }} />
```

```aura width=110 height=44 link="mailto:programadorstaudt@gmail.com" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZwogIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICB3aWR0aD0iNDgiCiAgaGVpZ2h0PSI0OCIKICB2aWV3Qm94PSIwIDAgMjQgMjQiCiAgZmlsbD0ibm9uZSIKICBzdHJva2U9IiNmZmZmZmYiCiAgc3Ryb2tlLXdpZHRoPSIyIgogIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIKICBzdHJva2UtbGluZWpvaW49InJvdW5kIgogIGNsYXNzPSJpY29uIGljb24tdGFibGVyIGljb25zLXRhYmxlci1vdXRsaW5lIGljb24tdGFibGVyLW1haWwiCj4KICA8cGF0aCBzdHJva2U9Im5vbmUiIGQ9Ik0wIDBoMjR2MjRIMHoiIGZpbGw9Im5vbmUiIC8+CiAgPHBhdGggZD0iTTMgN2EyIDIgMCAwIDEgMiAtMmgxNGEyIDIgMCAwIDEgMiAydjEwYTIgMiAwIDAgMSAtMiAyaC0xNGEyIDIgMCAwIDEgLTIgLTJ2LTEwIiAvPgogIDxwYXRoIGQ9Ik0zIDdsOSA2bDkgLTYiIC8+Cjwvc3ZnPg=="
  text="E-mail"
  backgroundColor="#111111"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '10%', color: '#111111' },
    { offset: '50%', color: '#ff5a64' },
    { offset: '60%', color: '#ffffff' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#8c2a31' },
  ]}
/>
```

```aura width=860 height=96
<div style={{
  width: '100%', height: '100%', background: '#08080c',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', gap: 10,
  fontFamily: 'Inter', position: 'relative', overflow: 'hidden', borderRadius: 16,
  border: '1px solid rgba(255,255,255,0.14)'
}}>
  <style>{`
    @keyframes foot-right { 0%, 100% { transform: translateX(0px); opacity: 0.8; } 50% { transform: translateX(300px); opacity: 1; } }
    @keyframes foot-left { 0%, 100% { transform: translateX(0px); opacity: 0.7; } 50% { transform: translateX(-280px); opacity: 1; } }
    #foot-1 { animation: foot-right 11s ease-in-out infinite; }
    #foot-2 { animation: foot-left 14s ease-in-out infinite; }
  `}</style>
  <svg width="860" height="96" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="gf" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(255,80,90,0.28)" />
        <stop offset="50%" stopColor="rgba(220,50,60,0.10)" />
        <stop offset="75%" stopColor="rgba(220,50,60,0)" />
      </radialGradient>
    </defs>
    <ellipse id="foot-1" cx="220" cy="128" rx="260" ry="80" fill="url(#gf)" />
    <ellipse id="foot-2" cx="640" cy="128" rx="240" ry="74" fill="url(#gf)" />
  </svg>
  <div style={{ display: 'flex', alignItems: 'center', gap: 16, width: 600 }}>
    <div style={{ display: 'flex', flex: 1, height: 1, background: 'linear-gradient(90deg, rgba(255,90,100,0), rgba(255,90,100,0.55))' }} />
    <span style={{ fontSize: 11, fontWeight: 700, color: 'rgba(230,230,230,0.75)', letterSpacing: '4px' }}>OBRIGADO PELA VISITA</span>
    <div style={{ display: 'flex', flex: 1, height: 1, background: 'linear-gradient(90deg, rgba(255,90,100,0.55), rgba(255,90,100,0))' }} />
  </div>
  <span style={{ fontSize: 11, color: 'rgba(210,210,210,0.45)', letterSpacing: '0.5px' }}>{'Eduardo Staudt · ' + new Date().getFullYear()}</span>
</div>
```
