---
name: onr_mapa_registro_imoveis-mcp
description: Skill da REST API do ONR: Mapa do Registro de Imóveis na MCP.AI: 1 endpoint em /api/onr_mapa_registro_imoveis. ONR: Mapa do Registro de Imóveis, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ONR: Mapa do Registro de Imóveis — REST API skill

Você tem acesso à **ONR: Mapa do Registro de Imóveis** REST API na MCP.AI.

> ONR: Mapa do Registro de Imóveis, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/onr_mapa_registro_imoveis
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
curl -X POST https://api.mcp.ai/api/onr_mapa_registro_imoveis/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"camada":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/onr_mapa_registro_imoveis/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `onr_mapa_registro_imoveis_consultar`

ONR: Mapa do Registro de Imóveis, consulta em fonte oficial. _(POST /api/onr_mapa_registro_imoveis/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `camada` | string | Sim | Parâmetro de consulta "camada". |
| `hash_endereco` | string | Não | Parâmetro de consulta "hash_endereco". |
| `car` | string | Não | Parâmetro de consulta "car". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_onr_mapa_registro_imoveis` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
