# API Escola

A API Escola é uma API RESTful desenvolvida para gerenciar informações relacionadas a uma instituição de ensino. Ela fornece funcionalidades para manipulação de alunos, usuários, autenticação e upload de fotos.

## Tecnologias Utilizadas

- Node.js
- Express.js
- Sequelize (ORM para MySQL)
- JSON Web Token (JWT) para autenticação
- Multer para upload de imagens

## Rotas Disponíveis

### 1. Alunos (/alunos)
- GET /alunos - Lista todos os alunos
- POST /alunos - Cria um novo aluno
- GET /alunos/:id - Retorna um aluno específico
- PUT /alunos/:id - Atualiza informações de um aluno
- DELETE /alunos/:id - Remove um aluno

### 2. Usuários (/users)
- POST /users - Cria um novo usuário
- GET /users/:id - Retorna um usuário específico
- PUT /users/:id - Atualiza um usuário
- DELETE /users/:id - Remove um usuário

### 3. Autenticação (/tokens)
- POST /tokens - Gera um token de acesso com base nas credenciais fornecidas

### 4. Home (/home)
- GET / - Rota pública de boas-vindas

### 5. Fotos (/fotos)
- POST /foto - Faz o upload de uma foto associada a um aluno

---
# Proteção de Rotas
- Para proteger qualquer rota, basta adicionar o middleware loginRequired antes da rota desejada.
---
# Configuração do Ambiente

### Para rodar a API localmente, é necessário configurar um arquivo .env na raiz do projeto com as seguintes variáveis:
DATABASE="api_database"
DATABASE_HOST="127.0.0.1"
DATABASE_PORT=3306
DATABASE_USERNAME="root"
DATABASE_PASSWORD="root"

TOKEN_SECRET="token_secret_key"
TOKEN_EXPIRATION=7d

APP_PORT=3001
APP_URL=http://localhost:3001
---

# Como Executar o Projeto

### Clone o repositório: 
- git clone https://github.com/seu-usuario/api-escola.git

### Instale as dependências:
- npm install

### Configure o arquivo .env conforme descrito acima.
- Rode as migrações do banco de dados:
- npx sequelize db:migrate

### Configure o CORS
- Abra o arquivo app.js e procure a variável whitelist
- Adicione no array de strings whitelist todas URL das origens que forem consumir a API

### Inicie o servidor:
- npm start

### A API estará disponível em http://localhost:3000
---

## Contribuição
### Fique à vontade para abrir issues e pull requests para melhorias e correções no projeto!
## Créditos:
**Projeto feito com fins práticos acadêmicos com as orientações do professor Luiz Otávio Miranda.**
