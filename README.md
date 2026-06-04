# viral.app MCP Server (Deprecated)

> [!WARNING]
> The viral.app TikTok MCP is deprecated. Do not start new integrations with this MCP server or the legacy `https://viral.app/api/mcp` endpoint.

viral.app now recommends using the [viral.app API](https://viral.app/api/v1/docs) for new integrations. For agent workflows, use the [viral.app agent skill](https://viral.app/app/org/api/agents) instead of MCP-style client configuration.

For the full migration context, read: [TikTok MCP Deprecated: Use the viral.app API](https://viral.app/free-tools/tiktok-mcp).

## What changed

This repository originally documented a hosted MCP endpoint for TikTok-only lookups. That endpoint answered a narrow set of questions: fetch a TikTok profile, inspect a TikTok video, list recent profile videos, and run simple analysis around those results.

The replacement is the broader viral.app API surface, which supports live lookups, tracked analytics, projects, Creator Hub workflows, payouts, exports, and multiple short-form platforms through the API `platform` parameter.

## Recommended path

1. Create a viral.app API key in [API Keys](https://viral.app/app/org/api/keys).
2. Use the [interactive API docs](https://viral.app/api/v1/docs) to build against the supported endpoints.
3. For AI agent workflows, install the viral.app skill and expose `VIRAL_API_KEY` in the agent environment.
4. Start with read-only analytics workflows before enabling any write actions.

## Legacy MCP context

The historical MCP endpoint was:

```text
https://viral.app/api/mcp
```

Existing Cursor, Raycast, Claude Desktop, Windsurf, Cline, or `mcp-remote` configurations that point to this endpoint should be treated as legacy configuration and migrated to API-key based workflows.

## Useful links

- [Deprecation and migration article](https://viral.app/free-tools/tiktok-mcp)
- [viral.app API docs](https://viral.app/api/v1/docs)
- [viral.app agent skill](https://viral.app/app/org/api/agents)
- [API keys](https://viral.app/app/org/api/keys)
