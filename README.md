# Homesage.ai MCP

Homesage.ai MCP connects Claude, ChatGPT, Cursor and any other MCP client to real estate data on 160M+ US properties and 200B+ data points. Its 30+ tools price a property, pull sold comps, estimate rent and budget a rehab from listing photos.

It is a hosted, remote MCP server. There is nothing to install. Add the URL below to your client and sign in with your Homesage.ai account.

```
https://api.homesage.ai/mcp
```

- **Transport:** Streamable HTTP
- **Auth:** OAuth sign-in with a Homesage.ai account
- **Billing:** the same credits as the Homesage.ai Real Estate APIs. See [pricing](https://homesage.ai/pricing/).

## What it does

- Estimated value, value history and comparable sales for any US address
- Condition score and line-item estimated renovation cost from listing photos
- Estimated long-term and short-term rent, flip return and investment potential
- Seller Motivation Score on listed properties
- Area search in a city, county or ZIP, filtered by price, condition, cap rate and rent
- Owner of record, mortgage and lien records for property research
- A Full Property Report that combines value, comps, condition, returns and location red flags in one call

Free catalog tools list every endpoint and return its docs, so an agent can find the right tool before it spends a credit.

## Connect

### Claude

Settings → Connectors → Add custom connector. Paste `https://api.homesage.ai/mcp`, then sign in.

### Claude Code

```bash
claude mcp add --transport http homesage https://api.homesage.ai/mcp
```

### Cursor

Add this to `.cursor/mcp.json` (also in this repo):

```json
{
  "mcpServers": {
    "homesage": {
      "url": "https://api.homesage.ai/mcp"
    }
  }
}
```

### VS Code

Add this to `.vscode/mcp.json` (also in this repo):

```json
{
  "servers": {
    "homesage": {
      "type": "http",
      "url": "https://api.homesage.ai/mcp"
    }
  }
}
```

### Cline

In Cline, open MCP Servers, then Remote Servers. Enter the name `homesage`, the URL `https://api.homesage.ai/mcp` and the transport Streamable HTTP. Or add this to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "homesage": {
      "type": "streamableHttp",
      "url": "https://api.homesage.ai/mcp"
    }
  }
}
```

Then press **Authorize OAuth** and sign in with your Homesage.ai account.

### ChatGPT and other MCP clients

Add a remote MCP server with the URL `https://api.homesage.ai/mcp` and sign in when asked.

## About this repository

This repository holds the public listing files for Homesage.ai MCP: this README, `server.json` for the [Official MCP Registry](https://registry.modelcontextprotocol.io), the Cursor Directory plugin files (`.cursor-plugin/plugin.json`, `mcp.json`, `assets/logo.png`) and client config examples. The server itself is hosted by Homesage.ai.

## Links

- Product page: https://homesage.ai/products/real-estate-mcps/
- Real Estate APIs: https://homesage.ai/products/real-estate-apis/
- Contact: contact@homesage.ai

## Listed on

[![Homesage.ai MCP on AI Agents Listing](https://aiagentslisting.com/homesage-ai-mcp/badge.svg)](https://aiagentslisting.com/mcp/homesage-ai-mcp)
