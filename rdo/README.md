# RDO Rio Tanque

App do Relatório Diário de Obra, publicado em https://rdo-cvv.web.app (projeto Firebase `rdo-cvv`).
O app inteiro é o arquivo `public/index.html`.

O site https://projetos-vv.pages.dev/rdo/ busca a versão publicada aqui; ele lê os RDOs (coleção `rdos`)
no Reporte Semanal. Não mude os nomes dos campos gravados no Firestore.

## Publicar (do seu computador)

Precisa do Node.js (https://nodejs.org, versão LTS) e de uma conta Google com acesso ao projeto `rdo-cvv`.

```
npm install -g firebase-tools
firebase login
git clone https://github.com/FabianoBarross/Engenharia.git
cd Engenharia/rdo
firebase deploy --only hosting
```

`--only hosting` publica só a página; não mexe nas regras nem nos dados do Firestore.
Para voltar à versão anterior: console do Firebase → Hosting → histórico de versões → "Reverter".
