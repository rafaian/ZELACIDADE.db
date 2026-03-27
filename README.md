Seu README já está muito bom — só fiz pequenos ajustes de ortografia, padronização e organização 👇

# 📝 API ZelaCidade 🏙️

## 📌 Sobre o Projeto

A API **ZelaCidade** é uma API para registrar e gerenciar problemas urbanos como:

* Falta de iluminação
* Buraco na rua
* Queda de árvore
* Lixo acumulado
* Vazamento de água
* Esgoto a céu aberto
* Semáforo quebrado
* Calçada danificada
* Poste danificado
* Alagamento
* Falta de sinalização
* Terreno abandonado

Ela permite criar, visualizar, atualizar e deletar ocorrências.

---

## 🛠️ Tecnologias utilizadas:

* Node.js
* Express
* SQLite
* SQLite3
* JavaScript
* Postman

---

## 🔽 Instalação

```bash
npm install
```

---

## ▶️ Como Executar

```bash
npm run dev
```

*Servidor disponível em*: [http://localhost:3000](http://localhost:3000)

---

## 🗄️ Banco de dados

O banco de dados é criado automaticamente ao iniciar o projeto.

**database.db**

---

### 📈 Tabela

| Campo            | Descrição                 |
| ---------------- | ------------------------- |
| Id               | Identificador único       |
| tipo_problema    | Tipo do problema          |
| localizacao      | Onde ocorreu              |
| descricao        | Detalhe do incidente      |
| prioridade       | Baixa, média ou alta      |
| nome_solicitante | Contato                   |
| data_registro    | Data do registro          |
| hora_registro    | Hora do registro          |
| status_resolucao | Status (padrão: pendente) |
| imagem_problema  | URL da imagem             |

---

## 🔗 Endpoints

### Rota Inicial

```http
GET /
```

Retorna uma página HTML simples com informações da API

---

### Listar todos os incidentes

```http
GET /incidentes
```

Retorna todos os registros do banco de dados

---

### Buscar incidente por ID

```http
GET /incidentes/:id
```

Retorna um incidente específico com base no ID

---

### Criar novo incidente

```http
POST /incidentes
```

Cria um novo registro no banco de dados

**Body (JSON):**

```json
{
  "tipo_problema": "Buraco na rua",
  "localizacao": "Rua Exemplo, 123",
  "descricao": "Buraco grande causando risco",
  "prioridade": "Alta",
  "nome_solicitante": "João",
  "imagem_problema": "http://imagem.com/foto.jpg"
}
```

---

### Atualizar incidente

```http
PUT /incidentes/:id
```

Atualiza um incidente existente pelo ID

**Body (JSON):**

```json
{
  "tipo_problema": "Buraco na rua",
  "localizacao": "Rua Exemplo, 123",
  "descricao": "Buraco já foi parcialmente resolvido",
  "prioridade": "Média",
  "nome_solicitante": "João",
  "status_resolucao": "Em andamento",
  "imagem_problema": "http://imagem.com/foto.jpg"
}
```

---

### Deletar incidente

```http
DELETE /incidentes/:id
```

Remove um incidente do banco de dados

---

## 🔒 Segurança

A API utiliza `?` nas queries SQL para evitar SQL Injection:

```sql
WHERE id = ?
```

---

## 📚 Conceitos

* CRUD
* Rotas com Express
* Métodos HTTP (GET, POST, PUT, DELETE)
* Banco de dados SQLite
* SQL básico
* Uso de `req.params` e `req.body`

---

## 💡 Observações

* O banco é criado automaticamente
* Dados iniciais são inseridos apenas se estiverem vazios
* A API pode ser testada com Postman

---

## 🧠 Licença

Este projeto foi desenvolvido para fins de aprendizado em backend com Node.js

---

## 🤝 Contribuição

 Escola Vai na Web

