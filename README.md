<div align="center">

# Google Maps Mcp Server

**MCP server for Google Maps public-data workflows** — expose focused tools to compatible AI clients.

![MCP](https://img.shields.io/badge/MCP-Compatible-7C3AED?style=flat)
![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=flat)

</div>

## Agent job: local-market research and lead-list enrichment

This server gives an MCP-compatible client a narrow tool surface for Google Maps tasks. The design principle is: request a specific question, return structured records with source context, then let the agent explain or act with those records.

## Quick configuration

```json
{
  "mcpServers": {
    "google_maps": {
      "command": "uvx",
      "args": ["google-maps-mcp-server"]
    }
  }
}
```

## Example tool call

```text
google_maps_search(query="restaurants in Seattle", limit=10)
```

Use a small result limit first. In a production agent, validate arguments, preserve source metadata, restrict sensitive actions, and log tool outcomes.


## License

MIT License.
