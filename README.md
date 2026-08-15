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

<!-- CROSS_LINKS_START -->

## Related projects

Explore these closely related implementation paths:

- [amazon-mcp-server](https://github.com/data-scrape/amazon-mcp-server) — Amazon MCP Server - AI agent access to product data, prices, and reviews via MCP
- [best-google-maps-scraper](https://github.com/data-scrape/best-google-maps-scraper) — Best Google Maps Scraper - Extract business data, reviews, ratings & contact info via API
- [google-maps-data-api](https://github.com/data-scrape/google-maps-data-api) — Google Maps Data API - Structured local business data for AI agents and automation
- [google-maps-scraper-api](https://github.com/data-scrape/google-maps-scraper-api) — Google Maps Scraper API - Production-ready REST API for local business data extraction
- [linkedin-mcp-server](https://github.com/data-scrape/linkedin-mcp-server) — LinkedIn MCP Server - Give AI agents access to profiles, companies, and jobs via Model Context Protocol
- [awesome-google-maps](https://github.com/data-scrape/awesome-google-maps) — Awesome Google Maps - Curated tools for Google Maps data extraction and local SEO

<!-- CROSS_LINKS_END -->