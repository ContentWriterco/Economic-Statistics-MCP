# Economic Statistics MCP Server

GDP and national accounts, inflation and prices, interest and exchange rates, trade and public finance from Eurostat, OECD, the World Bank, the IMF and national statistics offices.

Remote MCP server (Streamable HTTP), read-only, hosted by [Monitly](https://monit.ly).

```
https://monit.ly/api/mcp/economy
```

## Tools

| Tool | What it does |
|---|---|
| `search_catalog` | Find economic datasets by topic, country and source. |
| `inspect_dataset` | Check country coverage, dimensions and the latest values. |
| `get_dataset` | Dataset metadata and period range. |
| `get_series` | Time series for one country. |

## Example prompts

- What is the latest inflation rate in Germany?
- Compare GDP growth in Poland, Czechia and Hungary since 2015.
- Show government debt as % of GDP for Italy.

## Authentication

No account or key is needed. A fair-use daily limit applies; for higher volumes use the keyed Monitly MCP at https://monit.ly/mcp-docs.

## Setup

**Claude (claude.ai, Desktop):** Settings → Connectors → Add custom connector → paste the URL above.

**Cursor / VS Code / Windsurf** (`mcp.json`):

```json
{
  "mcpServers": {
    "economic-statistics": {
      "url": "https://monit.ly/api/mcp/economy"
    }
  }
}
```

**ChatGPT:** Settings → Apps → Developer mode → Create → paste the URL.

## About

Part of the [Monitly](https://monit.ly/mcp-docs) MCP family. Full Monitly catalog (100,000+ datasets, all topics): https://monit.ly/api/mcp/public.

Questions: info@monit.ly
