---
name: tribunal_tjsp_pedido_criminal-mcp
description: Skill da REST API do Tribunal TJSP: Certidão Criminal de 1º Grau na MCP.AI: 1 endpoint em /api/tribunal_tjsp_pedido_criminal. Tribunal TJSP: Certidão Criminal de 1º Grau, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TJSP: Certidão Criminal de 1º Grau — REST API skill

Você tem acesso à **Tribunal TJSP: Certidão Criminal de 1º Grau** REST API na MCP.AI.

> Tribunal TJSP: Certidão Criminal de 1º Grau, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tjsp_pedido_criminal
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/tribunal_tjsp_pedido_criminal/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"email":"...","finalidade":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tjsp_pedido_criminal/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tjsp_pedido_criminal_consultar`

Tribunal TJSP: Certidão Criminal de 1º Grau, consulta em fonte oficial. _(POST /api/tribunal_tjsp_pedido_criminal/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `nome` | string | Não | Parâmetro de consulta "nome". |
| `razao_social` | string | Não | Parâmetro de consulta "razao_social". |
| `email` | string | Sim | Parâmetro de consulta "email". |
| `finalidade` | string | Sim | Parâmetro de consulta "finalidade". |
| `pais` | string | Não | Parâmetro de consulta "pais". |
| `uf` | string | Não | Parâmetro de consulta "uf". |
| `municipio` | string | Não | Parâmetro de consulta "municipio". |
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tjsp_pedido_criminal` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
