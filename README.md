# 📚 Books Server - BACKEND em NODE

> Uma API RESTful para gerenciamento de livros, desenvolvida com Node.js e Express para treinar competências em backend.

---

## 🎯 Visão Geral

Este projeto é uma API simples porém completa para gerenciar uma coleção de livros. Pode ser utlizada de forma simples servindo seus dados para um projeto FRONT-END utilizando AXIOS. Foi criada com o objetivo de praticar e desenvolver habilidades em desenvolvimento backend com Node.js, focando especialmente em:

- Criação de rotas RESTful
- Manipulação de requisições HTTP (GET, POST, PATCH, DELETE)
- Integração com banco de dados (simulado com JSON)
- Estrutura de projeto MVC (Model-View-Controller)

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|------------|-----------|
| **Node.js** | Runtime JavaScript assíncrono baseado no motor V8 |
| **Express** | Framework web rápido e minimalista para Node.js |
| **Nodemon** | Utilitário que monitora alterações e reinicia o servidor automaticamente |

---

## 📂 Estrutura do Projeto

```
BOOKS-SERVER/
├── 📁 controladores/       # Lógica de controle das requisições
│   └── livro.js
├── 📁 rotas/               # Definição das rotas da API
│   └── livro.js
├── 📁 servicos/            # Lógica de negócio (acesso a dados)
│   └── livro.js
├── 📄 app.js               # Arquivo principal do servidor
├── 📄 livros.json         # Banco de dados simulado (JSON)
├── 📄 package.json         # Configurações e dependências do projeto
└── 📄 readme.md            # Documentação do projeto
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Node.js instalado (versão 14 ou superior)
- npm (gerenciador de pacotes do Node)

### Instalação

```bash
# Clone o repositório ou baixe os arquivos
cd BOOKS-SERVER

# Instale as dependências
npm install
```

### Executando o Servidor

```bash
# Inicia o servidor com nodemon (modo desenvolvimento)
npm run dev

# Ou diretamente com node
node app.js
```

O servidor estará disponível em: `http://localhost:8000`

---

## 📡 Endpoints da API

A API oferece os seguintes endpoints para gerenciamento de livros:

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/livros` | Retorna todos os livros |
| `GET` | `/livros/:id` | Retorna um livro específico pelo ID |
| `POST` | `/livros` | Cria um novo livro |
| `PATCH` | `/livros/:id` | Atualiza parcialmente um livro |
| `DELETE` | `/livros/:id` | Remove um livro |

---

## 📌 Exemplos de Uso

### 🔵 Obter todos os livros

```bash
curl -X GET http://localhost:8000/livros
```

### 🔵 Obter um livro específico

```bash
curl -X GET http://localhost:8000/livros/1
```

### 🟢 Criar um novo livro

```bash
curl -X POST http://localhost:8000/livros \
  -H "Content-Type: application/json" \
  -d '{
    "id": "3",
    "titulo": "O Projeto",
    "autor": "Enio Muliterno Neto"
  }'
```

### 🟡 Atualizar um livro

```bash
curl -X PATCH http://localhost:8000/livros/1 \
  -H "Content-Type: application/json" \
  -d '{
    "titulo": "Novo Título"
  }'
```

### 🔴 Deletar um livro

```bash
curl -X DELETE http://localhost:8000/livros/1
```

---

## 🏗️ Arquitetura MVC

O projeto segue o padrão arquitetural **MVC (Model-View-Controller)**:

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Rotas     │────▶│ Controlador │────▶│  Serviços   │
│  (Routes)   │     │ (Controller)│     │ (Services)  │
└─────────────┘     └─────────────┘     └─────────────┘
       │                   │                   │
       ▼                   ▼                   ▼
  Define URLs        Lógica de negócio    Acesso a dados
  e métodos          e validações         (livros.json)
```

### Camadas:

1. **Rotas (`rotas/livro.js`)** — Define os endpoints e mapeia para os controladores
2. **Controladores (`controladores/livro.js`)** — Processa as requisições e chama os serviços
3. **Serviços (`servicos/livro.js`)** — Contém a lógica de acesso e manipulação dos dados

---

## 📝 Banco de Dados

O projeto utiliza um arquivo JSON (`livros.json`) como banco de dados simulado. Esta abordagem é ideal para:

- Aprendizado sem necessidade de configurar um banco de dados real
- Testes rápidos de API
- Prototipagem

Estrutura esperada do arquivo `livros.json`:

```json
[
  {
    "id": "1",
    "titulo": "Nome do Livro",
    "autor": "Nome do Autor"
  }
]
```

---

## 🎓 Objetivos de Aprendizado

Este projeto foi desenvolvido para praticar os seguintes conceitos:

- ✅ Criação de servidores HTTP com Node.js
- ✅ Definição de rotas RESTful
- ✅ Manipulação de métodos HTTP (GET, POST, PUT, PATCH, DELETE)
- ✅ Leitura e escrita de arquivos JSON
- ✅ Estruturação de projetos em camadas (MVC)
- ✅ Tratamento de erros em APIs
- ✅ Utilização do framework Express

---

## 📄 Licença

Este projeto está sob a licença **ISC**.

---

## 👤 Autor

**Enio Muliterno Neto**

---

<div align="center">

⭐️ *Projeto desenvolvido para fins de estudos* ⭐️

</div>


