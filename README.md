# 🛒 Desafio Fullstack – Softcom

Este repositório apresenta minha solução para o **Desafio Fullstack da Softcom**, com implementação tanto de **backend (Node.js + Express + Sequelize + MySQL)** quanto de **frontend (React)**.

A proposta foi criar uma lojinha virtual para pequenos empreendedores, com funcionalidades de cadastro, autenticação e gerenciamento de itens à venda.

---

## 🔧 Tecnologias Utilizadas

### 📦 Backend
- Node.js
- Express
- Sequelize ORM
- MySQL
- JWT (Autenticação)
- Bcrypt
- Joi (validações)
- Dotenv
- Arquitetura MVC

### 🎨 Frontend
- React
- React Router DOM
- Axios
- Context API (para autenticação)
- Styled Components / CSS Modules

---

## ✅ Funcionalidades

### Backend
- Cadastro de usuários (nome, e-mail, CNPJ, senha)
- Autenticação por e-mail ou CNPJ + senha
- Criação, leitura, edição e exclusão de itens por usuário
- Proteção de rotas com JWT
- Rota extra: `/api/v1/verify` para verificação de token JWT

> ⚠️ **Nota:** A lógica de **desconto de 5% para pagamento em dinheiro** ainda **não foi implementada** (extra opcional do desafio).

### Frontend
- Tela de login e cadastro
- Dashboard com listagem de itens
- Cadastro, edição e exclusão de itens
- Visualização de item individual
- Gerenciamento de autenticação com Context API
- Proteção de rotas privadas

---

## 📡 Rotas da API

| Método | Rota                                        | Descrição                            |
|--------|---------------------------------------------|--------------------------------------|
| POST   | `/api/v1/user`                              | Cadastrar novo usuário               |
| GET    | `/api/v1/user/:id`                          | Buscar usuário por ID                |
| POST   | `/api/v1/auth/sign_in`                      | Autenticação do usuário              |
| POST   | `/api/v1/user/:id/item`                     | Cadastrar novo item                  |
| GET    | `/api/v1/user/:id/item/:itemId`             | Buscar item específico               |
| PUT    | `/api/v1/user/:id/item/:itemId`             | Atualizar item                       |
| DELETE | `/api/v1/user/:id/item/:itemId`             | Remover item                         |
| GET    | `/api/v1/verify`                            | Verificar validade do token JWT      |

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Node.js
- MySQL
- npm ou yarn

### 1. Clonar o repositório
```bash
git clone https://github.com/pedrinhoas7/challenge.git
cd challenge
```

### 2. Configurar e rodar o backend
```bash
cd backend
cp .env.example .env    # configure o banco de dados e JWT_SECRET
npm install
npx sequelize db:migrate
npm run dev
```

### 3. Rodar o frontend
```bash
cd ../frontend
npm install
npm start
```

---

## ✅ Requisitos Atendidos

### Requisitos Funcionais
- [x] Cadastro de conta (nome, e-mail, CNPJ, senha)
- [x] Autenticação via e-mail ou CNPJ
- [x] Cadastro e gerenciamento de itens
- [x] Validação de e-mail e CNPJ únicos
- [x] Listagem de itens por usuário

### Requisitos Não Funcionais
- [x] Uso de banco de dados relacional (MySQL)
- [x] Separação em camadas (MVC)
- [x] Uso de ORM (Sequelize)

### Diferenciais (Plus)
- [x] JWT implementado para autenticação e autorização
- [ ] Regra de desconto de 5% (não implementada)
- [ ] Testes unitários (não implementados)

---

## 🧠 Considerações

Este projeto foi uma excelente oportunidade para aplicar práticas de desenvolvimento web fullstack, como:

- Organização de código em camadas
- Gerenciamento de estado com Context API
- Integração frontend-backend com segurança via JWT
- Consistência nas validações e tratativas de erro

---

## 📬 Contato

Fique à vontade para entrar em contato:

- 📧 pedrinhoas7@gmail.com 

Agradeço à equipe da **Softcom** pela oportunidade 🙌  
