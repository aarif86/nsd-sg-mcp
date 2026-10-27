# NSD.SG connector (MCP)

Put the page your AI made online at your own name, like `kopi-stall.nsd.sg`. Say "put this online as kopi-stall" and your AI publishes it and replies with the link.

Works with Claude (web, desktop, Claude Code), ChatGPT, Codex, Cursor, Gemini CLI and any app that supports MCP connectors.

- Website: https://nsd.sg
- Set-up guide: https://nsd.sg/guides/connect
- Live example, published through the connector: https://kopi-catcher.nsd.sg

## Connect

1. Sign up free at https://nsd.sg/signup, open **Connect your AI**, press one button. You get a personal connector address.
2. Add it to your AI.
   - Claude: Settings, Connectors, Add custom connector. Paste the address. Authentication: No sign-in.
   - ChatGPT: Settings, Connectors, switch on Developer mode under Advanced, then Create. Paste the address. Authentication: None.
   - Claude Code: `claude mcp add --transport http nsd https://nsd.sg/mcp/YOUR_KEY`
   - Codex: `codex mcp add nsd --url https://nsd.sg/mcp/YOUR_KEY`
   - Gemini CLI: `gemini mcp add --transport http nsd https://nsd.sg/mcp/YOUR_KEY`
   - Cursor (`.cursor/mcp.json`): `{ "mcpServers": { "nsd": { "url": "https://nsd.sg/mcp/YOUR_KEY" } } }`
3. Ask: "Put this page online as kopi-stall."

Endpoint: `https://nsd.sg/mcp` (Streamable HTTP). The key goes in the address, or as `Authorization: Bearer <key>`.

## Tools

| Tool | What it does |
| --- | --- |
| `nsd_publish` | Put a new page or site online at a name you pick |
| `nsd_update` | Replace the page, the address stays the same, older copies are kept |
| `nsd_list_sites` | Show your sites |
| `nsd_get_site` | Details of one site |
| `nsd_delete_site` | Remove a site |

Up to 100 files or 8 MB per call. Files with JavaScript go up base64. The connector tells the AI this itself.

## What works

Anything that runs in the browser: pages, menus, invites, quizzes, calculators, games, Astro, Vite or Next exports. `404.html` and `_redirects` work. No server code, no database, no logins.

## Plans

Free for 30 days, then one tap to keep it. Plus is S$9 a month or S$90 a year for five sites and no badge. Details at https://nsd.sg/pricing.

## Help

Made in Singapore by NasarDigital. A real person answers on WhatsApp, usually within the hour: https://nsd.sg/contact
