# Server

Este é um projeto desenvolvido durante um evento da Rocketseat. Ele consiste em uma API simples para gerenciar salas, utilizando PostgreSQL como banco de dados e Drizzle ORM para manipulação de dados.

## Tecnologias Utilizadas

- **Node.js**: Versão 22 (definida em `.nvmrc`).
- **Fastify**: Framework web rápido e leve.
- **Drizzle ORM**: ORM para manipulação de banco de dados.
- **PostgreSQL**: Banco de dados relacional.
- **Zod**: Biblioteca para validação de dados.
- **Biome**: Ferramenta de formatação e análise de código.

## Padrões de Projeto

- **ORM**: Utilização do Drizzle ORM para manipulação de tabelas e consultas.
- **Modularização**: Código organizado em módulos (`src/db`, `src/http/routes`, etc.).
- **Configuração baseada em ambiente**: Variáveis de ambiente gerenciadas com `zod` e `.env`.

## Setup e Configuração

### Pré-requisitos

- Node.js versão 22.
- PostgreSQL instalado e configurado.

### Instalação

1. Clone o repositório:
   ```sh
   git clone <url-do-repositorio>
   cd server

2. Instale as dependências:

```bash
npm install
 ```

3. Configure o banco de dados:

- Certifique-se de que o PostgreSQL está rodando.
- Crie um banco de dados chamado agents.
- Execute o script de configuração inicial:

```bash
docker-compose up -d
```

4. Configure o arquivo .env: Copie o arquivo .env.example para .env e preencha as variáveis:

```bash
PORT=3333
DATABASE_URL="postgres://<usuario>:<senha>@localhost:5432/agents"
```

Rodando o Projeto:

Para rodar em modo de desenvolvimento:
```bash
npm run dev
```

Para rodar em produção:
```bash
npm start
```

Seed do Banco de Dados
Para popular o banco de dados com dados iniciais:

```bash
npm run db: seed
```

Endpoints
- Health Check: GET /health
- Listar Salas: GET /rooms
