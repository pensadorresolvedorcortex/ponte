
# LogPoste Clone - Backend + Docker

Este projeto é um clone funcional da plataforma LogPoste (painel do seller), com integração completa de frontend, backend e banco de dados.

---

## 🚀 Como executar localmente

### Pré-requisitos

- Docker e Docker Compose instalados

### Passos

```bash
# 1. Clone o projeto
git clone <seu-repositorio>.git
cd logposte-backend

# 2. Inicie os containers
docker-compose up --build
```

Acesse a API em: [http://localhost:4000/api/envios](http://localhost:4000/api/envios)

---

## 📦 Estrutura do Projeto

- **/models** – Esquema Mongoose do envio
- **/routes** – Rotas REST de envios
- **server.js** – Inicialização do servidor Express
- **.env** – Variáveis de ambiente (porta e URI Mongo)
- **Dockerfile** – Build da aplicação Node.js
- **docker-compose.yml** – Orquestra MongoDB + backend

---

## 🌐 Deploy na Railway

1. Suba o backend para o GitHub
2. Acesse [https://railway.app](https://railway.app)
3. Crie novo projeto → Deploy via GitHub
4. Adicione variáveis no painel:
   - `PORT=4000`
   - `MONGO_URI=<sua string do MongoDB Atlas ou Railway>`

---

## 🔗 Frontend

Você pode usar o `index.html` gerado no frontend como página estática e conectar à API em:

```js
fetch("https://logposte-backend.up.railway.app/api/envios", {...})
```

---

## ✨ Tecnologias

- Node.js
- Express
- MongoDB
- Leaflet.js + OpenStreetMap
- Docker / Docker Compose
