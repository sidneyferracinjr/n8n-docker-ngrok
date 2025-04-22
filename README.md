# Projeto Local: n8n + Docker + Ngrok

Este projeto configura uma instância do [n8n](https://n8n.io/) em um ambiente local utilizando Docker e expõe o serviço com Ngrok.

## ✅ Pré-requisitos

- [Docker](https://www.docker.com/)
- [Ngrok](https://ngrok.com/) instalado e configurado no PATH

## 📁 Estrutura

```
n8n-local/
├── docker-compose.yml
├── .env
├── start-ngrok.sh
├── README.md
```

## 🚀 Como rodar

1. **Suba o n8n:**

```bash
docker-compose up -d
```

2. **Em outro terminal, inicie o Ngrok:**

```bash
./start-ngrok.sh
```

3. **Atualize a URL gerada no terminal do ngrok** no arquivo `.env` em `WEBHOOK_TUNNEL_URL`.

4. **Reinicie o n8n** para ele usar a URL correta:

```bash
docker-compose down
docker-compose up -d
```

5. **Acesse o n8n no navegador:**  
   - Local: `http://localhost:5678`
   - Público (via ngrok): `https://<sua-url-ngrok>.ngrok.io`

## 🔐 Autenticação

Login: `admin`  
Senha: `admin123`  

Esses dados estão no `.env` e você pode alterá-los.

---
Feito com 💻 e café ☕
