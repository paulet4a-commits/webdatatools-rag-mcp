# WebDataTools Web content for AI & RAG MCP server
`webdatatools-rag-mcp`

An MCP server with 6 web content for ai & rag tools for AI agents — Claude Desktop, Cursor, Cline or any MCP client. Web search with page text, website-to-Markdown crawling, clean article extraction, JSON-LD/structured data, Google News and press-release monitoring — ready for LLM context and RAG pipelines.

**This server uses *your own* Apify API token.** Every tool call runs a [WebDataTools](https://apify.com/webdatatools) Actor under your Apify account and is billed to your Apify credit — pay per result, the price is in each tool description. Your token is only sent to Apify's API.

## Quick start

Requires Node.js 18+.

```bash
APIFY_TOKEN=apify_api_... npx -y github:paulet4a-commits/webdatatools-rag-mcp
```

Get a free token (the free plan includes monthly credit): https://console.apify.com/settings/integrations

## Claude Desktop / Cursor

Add this to `claude_desktop_config.json` (Claude Desktop) or `.cursor/mcp.json` (Cursor):

```json
{
  "mcpServers": {
    "webdatatools-rag": {
      "command": "npx",
      "args": [
        "-y",
        "github:paulet4a-commits/webdatatools-rag-mcp"
      ],
      "env": {
        "APIFY_TOKEN": "apify_api_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
      }
    }
  }
}
```

## Tools (6)

| Tool | What it does | Price (free plan) | Backing Actor |
|---|---|---|---|
| `ai_web_search` | AI Web Search & Read: Google results as clean Markdown | $0.005 / result | [Actor](https://apify.com/webdatatools/ai-web-search) |
| `website_to_markdown` | Website to Markdown — Content Crawler for LLM & RAG | $0.001 / result | [Actor](https://apify.com/webdatatools/website-to-markdown) |
| `article_extractor` | Article & News Extractor (clean text, author, date, markdown) | $0.002 / result | [Actor](https://apify.com/webdatatools/article-extractor) |
| `structured_data_extractor` | Structured Data & JSON-LD Extractor (Schema.org, Open Graph) | $0.002 / result | [Actor](https://apify.com/webdatatools/structured-data-extractor) |
| `google_news_scraper` | Google News Scraper (RSS search by keyword, topic, site) | $0.0005 / article | [Actor](https://apify.com/webdatatools/google-news-scraper) |
| `press_release_monitor` | Press Release Monitor: PR Newswire, BusinessWire, GlobeNewswire | $0.001 / result | [Actor](https://apify.com/webdatatools/press-release-monitor) |

## More WebDataTools MCP servers

- [webdatatools-mcp-server](https://github.com/paulet4a-commits/webdatatools-mcp-server) — the 10 most popular tools in one server
- [webdatatools-domain-mcp](https://github.com/paulet4a-commits/webdatatools-domain-mcp) — Domain & website intelligence
- [webdatatools-social-mcp](https://github.com/paulet4a-commits/webdatatools-social-mcp) — Search, video & social data
- [webdatatools-leads-mcp](https://github.com/paulet4a-commits/webdatatools-leads-mcp) — Leads, jobs & company data
- [webdatatools-dev-mcp](https://github.com/paulet4a-commits/webdatatools-dev-mcp) — Developer, app & research data

## License

MIT
