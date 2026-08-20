# Instalação detalhada

ONR: Mapa do Registro de Imóveis é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_onr_mapa_registro_imoveis`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_onr_mapa_registro_imoveis` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_onr_mapa_registro_imoveis` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_onr_mapa_registro_imoveis` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.onr_mapa_registro_imoveis` (ou `servers.onr_mapa_registro_imoveis` no VS Code) do config do cliente e reinicie.
