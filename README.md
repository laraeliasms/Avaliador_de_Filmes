[README (1).md](https://github.com/user-attachments/files/29349558/README.1.md)
# Site de Avaliação de Filmes — Projeto Full Stack (ABP)

Projeto dividido em **3 Marcos de Entrega**, conforme `Projeto_Full_Stack_Apresentacao_ABP.pdf`.

## Sobre o Projeto

O **Site de Avaliação de Filmes** é uma aplicação web full stack que
permite aos usuários cadastrar, visualizar e excluir avaliações de filmes,
informando o nome do filme, uma nota de 1 a 5 e um comentário/crítica.

O projeto foi desenvolvido como parte de uma Atividade Baseada em Projeto
(ABP), seguindo uma evolução incremental em três marcos de entrega:

1. **Marco 1** — validação da arquitetura cliente-servidor com dados
   mockados em memória, sem persistência real.
2. **Marco 2** — implementação de persistência real dos dados utilizando
   SQLite e Prisma ORM, com rotas completas de CRUD (criar, listar e
   excluir avaliações).
3. **Marco 3** — blindagem da aplicação contra vulnerabilidades de
   segurança (XSS), utilizando `textContent` no frontend e o middleware
   `helmet` no backend, além da documentação técnica final do projeto.

A stack utilizada é HTML5 e JavaScript puro no frontend, e Node.js com
Express, Prisma e SQLite no backend.

## Alunos

- Lara Geovana — RA: 22502104
- Gabriel Rios — RA: 22505812
- Camilla Valenzuela — RA: 22502503

## Estrutura de Diretórios

```
movie-review-app/
├── backend/
│   ├── server.js              # Servidor Express (versão final, com Prisma + Helmet)
│   ├── package.json
│   ├── prisma/
│   │   └── schema.prisma      # Modelagem do banco SQLite
│   └── dev.db                 # Gerado automaticamente após migração (SQLite)
├── frontend/
│   ├── index.html
│   └── script.js
├── MARCO_1_server_mock.js     # Versão do server.js só com dados em memória (referência histórica)
├── RELATORIO.md
└── README.md
```

> Observação: o arquivo `backend/server.js` já está na **versão final** (Marco 3: CRUD com Prisma + Helmet + proteção XSS).
> O arquivo `MARCO_1_server_mock.js` foi mantido separado apenas como referência do código inicial do Marco 1 (dados mockados em memória), para você mostrar a evolução do projeto na apresentação.

## Como rodar (resumo — detalhes completos no RELATORIO.md)

```bash
cd backend
npm install
npx prisma migrate dev --name init
node server.js
```

Depois abra `frontend/index.html` no navegador (ou sirva com uma extensão como "Live Server").
