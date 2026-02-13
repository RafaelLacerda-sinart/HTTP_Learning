# Conceitos Básicos de Métodos HTTP e Erros de Servidor

Este documento explica de forma simples os principais métodos HTTP utilizados em APIs REST e os erros de servidor mais comuns.

---

## Métodos HTTP

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

-------------------------------

# Outros Conceitos Fundamentais de HTTP

Este documento resume **os conceitos mais importantes do HTTP**, além de métodos (GET, POST, PUT, etc.) e códigos de status (200, 404, 500...).

---

## 1. Modelo Cliente-Servidor

O HTTP segue o modelo **cliente-servidor**:

- **Cliente** → normalmente o navegador
- **Servidor** → aplicação que responde às requisições

A comunicação é feita por meio de **requisições (requests)** e **respostas (responses)**.

---

## 2. Stateless (Sem Estado)

O HTTP é **stateless**, ou seja:

- Cada requisição é independente
- O servidor não guarda automaticamente o estado entre requisições

Para manter estado são usados:
- Cookies
- Sessões
- Tokens (ex: JWT)

---

## 3. Estrutura de Requisição e Resposta

### Requisição HTTP

É composta por:

- Linha inicial (método + URL + versão)
- Headers (cabeçalhos)
- Corpo (opcional)

### Resposta HTTP

Contém:

- Linha de status
- Headers
- Corpo da resposta

---

## 4. Headers (Cabeçalhos)

Headers transportam metadados da requisição/resposta.

Exemplos importantes:

- `Content-Type` → tipo do conteúdo (JSON, HTML, etc.)
- `Authorization` → credenciais de autenticação
- `Cache-Control` → regras de cache
- `Accept` → formatos aceitos pelo cliente
- `User-Agent` → identificação do cliente

---

## 5. URL e URI

- **URI** → Identificador de recurso
- **URL** → Tipo específico de URI que indica localização
Partes:
- Protocolo
- Domínio
- Porta
- Caminho (path)
- Query string

---

## 6. Protocolo de Aplicação

HTTP é um **protocolo de camada de aplicação** (modelo TCP/IP).

Ele normalmente roda sobre:

- TCP
- TLS (quando é HTTPS)

---

## 7. HTTPS (HTTP Secure)

HTTPS é HTTP com **criptografia TLS**.

Garante:

- Confidencialidade
- Integridade
- Autenticidade

---

## 8. Cache

HTTP permite cache para melhorar performance.

Pode ocorrer em:

- Navegador
- Proxy
- CDN

Headers importantes:

- `Cache-Control`
- `ETag`
- `Expires`
- `Last-Modified`

---

## 9. Content Negotiation

Mecanismo onde cliente e servidor negociam o formato da resposta.

Permite que o mesmo endpoint retorne:
- JSON
- XML
- HTML

---

## 10. Idempotência e Segurança

### Métodos Seguros
Não alteram o estado do servidor.
Ex: GET

### Métodos Idempotentes
Podem ser repetidos sem alterar o resultado final.
Ex: PUT, DELETE

---

## 11. Conexões e Persistência

- HTTP/1.0 → conexão fechada após cada requisição
- HTTP/1.1 → conexões persistentes (keep-alive)
- HTTP/2 → multiplexação (várias requisições na mesma conexão)
- HTTP/3 → baseado em QUIC (UDP)

---

## 12. Versionamento

Principais versões:

- HTTP/1.0
- HTTP/1.1
- HTTP/2
- HTTP/3

Cada versão trouxe melhorias de performance e eficiência.

---

# Resumo Final

Os conceitos mais importantes do HTTP são:

- Modelo cliente-servidor
- Stateless
- Estrutura de request/response
- Headers
- HTTPS e segurança
- Cache
- Content negotiation
- Idempotência
- Conexões persistentes
- Versionamento

Esses fundamentos são essenciais para entender APIs REST, aplicações web e arquiteturas modernas.




