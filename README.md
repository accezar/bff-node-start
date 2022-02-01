# BFF Node Starter

Boilerplate de um bff utilizando Nodejs, Typescript e Express.

### Setup
- Clone o projeto
- Instale as dependências e inicie o servidor através do comando `yarn && yarn dev`
- A API estará disponível em `localhost:3000`.
- Swagger disponível em `localhost:3000/api-docs`

### Ferramentas, bibliotecas e afins
- Dev Server: Nodemoon
- API Docs: Swagger 
- Builder & Compiler: SWC https://swc.rs/
- Container: Docker
- Process Manager: PM2 https://pm2.keymetrics.io/
- Testes: Jest https://jestjs.io/pt-BR/
- Tokens and Crypto: jsonwebtoken, bcrypt
- Proxy: NGINX
- Logger: Para lidar com logs, implementado Winston https://github.com/winstonjs/winston

### Fluxo

**Routes** direciona request para uma rota, que passa por um **Middleware** 
Um **Middleware** efetua tratativas na requisição http (cada middleware lida com seu contexto).
**Routes** utilizam de **Controllers** que orquestram as chamadas de **Services** 
**Services** usam de **DTOs** para validar o objeto de requisição e de **Interfaces** para modelar e representar o formato da resposta.