# Rocketseat-back (Projeto let me ask com integração de ia)

Este é um projeto backend baseado em Fastify, desenvolvido durante um curso da **Rocketseat**, com algumas funcionalidades **extras adicionadas** posteriormente por mim.

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Fastify**: Framework web de alto desempenho para Node.js
- **Zod**: Validação de esquemas e tipagens
- **Drizzle ORM**: ORM moderno e leve para SQL
- **Postgres**: Banco de dados utilizado
- **@google/genai**: Integração com a API de IA da Google
- **Fastify CORS & Multipart**: Plugins de CORS e upload de arquivos
- **Typescript**: Tipagem estática para JavaScript
- **Drizzle-kit**: CLI para geração e gerenciamento de migrations
- **fastify-type-provider-zod**: Integração entre Zod e Fastify

## 📁 Estrutura do Projeto

Organizado com padrão MVC simplificado e utilização de migrations via Drizzle.

```
Rocketseat-back/
├── src/
│   ├── routes/
│   ├── lib/
│   ├── server.ts
├── drizzle.config.ts
├── docker-compose.yml
├── .env.example
```

## 📦 Padrões de Projeto Utilizados

- **Type-safe API**: Utilizando Zod para validação de dados
- **Injeção de dependência implícita**
- **Modularização por rotas**

## ⚙️ Setup e Configuração

### Pré-requisitos

- Node.js >= 18.x
- Docker e Docker Compose (opcional para banco)
- PostgreSQL local (caso não use Docker)

### Passos para rodar:

### 1. Clone o repositório
```bash
git clone <url-do-repositorio>
cd server
```

### 2. Configure o arquivo `.env` baseado no `.env.example`.

### 3. Instale as dependências:
```bash
npm install
```

### 4. Suba o banco com Docker:
```bash
docker-compose up -d
```

### 5. Execute as migrações do banco
```bash
npx drizzle-kit migrate
```

### 6. (Opcional) Popule o banco com dados de exemplo
```bash
npm run db:seed
```

### 7. Inicie o servidor:
```bash
npm run dev
```

