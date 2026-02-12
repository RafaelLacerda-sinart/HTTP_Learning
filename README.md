# 📘 Conceitos Básicos de Métodos HTTP e Erros de Servidor

Este documento explica de forma simples os principais métodos HTTP utilizados em APIs REST e os erros de servidor mais comuns.

---

## 🌐 Métodos HTTP

Os métodos HTTP são utilizados para indicar a ação que deve ser realizada sobre um recurso em um servidor.

### 🔹 GET
- **Função:** Buscar dados do servidor.
- **Uso comum:** Listar ou obter informações.
- **Exemplo:** Buscar lista de usuários.
- **Observação:** Não deve alterar dados.

---

### 🔹 POST
- **Função:** Enviar dados para o servidor.
- **Uso comum:** Criar um novo recurso.
- **Exemplo:** Criar um novo usuário.
- **Observação:** Pode alterar o estado do servidor.

---

### 🔹 PUT
- **Função:** Atualizar um recurso existente.
- **Uso comum:** Atualizar todos os dados de um registro.
- **Exemplo:** Atualizar informações completas de um usuário.
- **Observação:** Normalmente substitui o recurso inteiro.

---

### 🔹 PATCH
- **Função:** Atualizar parcialmente um recurso.
- **Uso comum:** Alterar apenas alguns campos.
- **Exemplo:** Atualizar apenas o e-mail do usuário.

---

### 🔹 DELETE
- **Função:** Remover um recurso.
- **Uso comum:** Excluir um registro do sistema.
- **Exemplo:** Deletar um usuário.

---

## ⚠️ Erros HTTP Mais Comuns

Os códigos de status HTTP indicam o resultado da requisição.

### ✅ 2xx — Sucesso
- **200 OK** → Requisição bem-sucedida.
- **201 Created** → Recurso criado com sucesso.
- **204 No Content** → Sucesso sem conteúdo de resposta.

---

### ❌ 4xx — Erro do Cliente
- **400 Bad Request** → Requisição inválida.
- **401 Unauthorized** → Autenticação necessária ou inválida.
- **403 Forbidden** → Acesso proibido.
- **404 Not Found** → Recurso não encontrado.
- **405 Method Not Allowed** → Método não permitido para o endpoint.

---

### 🚨 5xx — Erro do Servidor
- **500 Internal Server Error** → Erro interno no servidor.
- **502 Bad Gateway** → Resposta inválida de outro servidor.
- **503 Service Unavailable** → Serviço temporariamente indisponível.
- **504 Gateway Timeout** → Tempo de resposta excedido.

---

## 📌 Resumo Rápido

| Método | Ação |
|--------|------|
| GET    | Buscar dados |
| POST   | Criar dados |
| PUT    | Atualizar totalmente |
| PATCH  | Atualizar parcialmente |
| DELETE | Remover dados |

---

## 🧠 Dica

Sempre verifique:
- O método correto para a operação.
- O código de status retornado.
- A mensagem de erro no corpo da resposta.

---

📖 Referência oficial: https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods
