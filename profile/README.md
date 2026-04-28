<div align="center">
  <a href="https://brightdata.com">
    <img src="https://github.com/user-attachments/assets/5831f9ab-5aea-4f1d-a2d3-c85874ba0eeb" alt="Bright Data" height="100">
  </a>

  <h1>The web data layer for AI agents</h1>

  <p>
    <strong>Production-grade access to the open web.</strong><br>
    Search, scrape, browse, and extract from any public site - at any scale, in any geo, without getting blocked.
  </p>

  <p>
    <a href="https://brightdata.com/?hs_signup=1"><img src="https://img.shields.io/badge/Get_Started-2563EB?style=for-the-badge" alt="Get Started"></a>
    <a href="https://docs.brightdata.com"><img src="https://img.shields.io/badge/Documentation-0F172A?style=for-the-badge" alt="Documentation"></a>
    <a href="https://github.com/brightdata/brightdata-mcp"><img src="https://img.shields.io/badge/MCP_Server-16A34A?style=for-the-badge" alt="MCP Server"></a>
  </p>

  <p>
    <a href="https://github.com/brightdata/brightdata-mcp"><img src="https://img.shields.io/github/stars/brightdata/brightdata-mcp?style=social" alt="MCP Stars"></a>
  </p>
</div>

---

## Quickstart

Connect Bright Data to Claude Code, Cursor, or any MCP-compatible client in one line:

```bash
claude mcp add --transport http brightdata https://mcp.brightdata.com/mcp?token=YOUR_API_TOKEN
```

Prefer raw HTTP? Hit the API directly:

```bash
curl -X POST https://api.brightdata.com/request \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"zone": "unblocker", "url": "https://example.com", "format": "raw"}'
```

Or use the SDK:

```python
from brightdata import SyncBrightDataClient

with SyncBrightDataClient(api_token="YOUR_API_TOKEN") as client:
    result = client.scrape_url(url="https://example.com")
    print(result)
```

> **Free for agents.** MCP and CLI users get 5,000 requests/month - no setup beyond the API key. [Grab one →](https://brightdata.com/cp/start)

---

## Why Bright Data?

AI agents are only as good as the data they can reach.

We're the web data infrastructure behind some of the world's most demanding AI systems — billions of requests a day, every public site, every geography, no breakage. While other tools work great until the page actually has a CAPTCHA, geo-block, or anti-bot stack, we handle the parts of the web that break everyone else.

If your agent needs to read the open web in production, this is the layer underneath it.

---

## The ecosystem

### Bright Data MCP — The flagship for AI agents

[![brightdata/brightdata-mcp - GitHub](https://gh-card.dev/repos/brightdata/brightdata-mcp.svg)](https://github.com/brightdata/brightdata-mcp)

One MCP for the web. Search, navigate, extract, and unlock any public site from inside Claude, Cursor, Codex, or any MCP client. Used by 150K+ agent calls per week.

<br clear="right"/>

### Bright Data CLI — Web data, from your terminal

[![brightdata/cli - GitHub](https://gh-card.dev/repos/brightdata/cli.svg)](https://github.com/brightdata/cli)

Give coding agents real-time web data without leaving the shell. Install once, and Claude Code, Codex, and Gemini CLI can search, scrape, and crawl autonomously.

```bash
npx skills add brightdata/cli
```

<br clear="right"/>

### Web Unlocker API — Get past anything

[![luminati-io/bright-data-web-unlocker-nodejs-project - GitHub](https://gh-card.dev/repos/luminati-io/bright-data-web-unlocker-nodejs-project.svg)](https://github.com/luminati-io/bright-data-web-unlocker-nodejs-project)

The site you're trying to scrape is fighting back? We solve fingerprinting, CAPTCHAs, IP rotation, retries, and anti-bot stacks in real time — single API call, you get the page.

<br clear="right"/>

### SERP API — Search results, structured

[![brightdata/bright-data-serp-api-python-project - GitHub](https://gh-card.dev/repos/brightdata/bright-data-serp-api-python-project.svg)](https://github.com/brightdata/bright-data-serp-api-python-project)

Real user search results from Google, Bing, and every major engine. Returns clean JSON or HTML, with full geo and device targeting. Ranked exactly the way a real person would see them.

<br clear="right"/>

### Browser API — Headless browsers that don't get blocked

[![luminati-io/bright-data-scraping-browser-nodejs-playwright-project - GitHub](https://gh-card.dev/repos/luminati-io/bright-data-scraping-browser-nodejs-playwright-project.svg)](https://github.com/luminati-io/bright-data-scraping-browser-nodejs-playwright-project)

Drop-in replacement for Playwright and Puppeteer with proxy rotation, CAPTCHA solving, and anti-detection built in. Render JavaScript-heavy sites at scale, the way an agent needs to.

<br clear="right"/>

### Datasets & Data Feeds — The web, pre-extracted

[![brightdata/bright-data-scrape-chatgpt-search-nodejs-project - GitHub](https://gh-card.dev/repos/brightdata/bright-data-scrape-chatgpt-search-nodejs-project.svg)](https://github.com/brightdata/bright-data-scrape-chatgpt-search-nodejs-project)

Skip the scraping infrastructure entirely. Subscribe to fresh structured datasets — products, jobs, profiles, news, reviews — delivered via API, webhook, S3, or your warehouse of choice.

<br clear="right"/>

---

## What you can build

A few patterns we see most often:

- **Research agents** that browse, read, and synthesize across hundreds of sources
- **Price intelligence** workflows that monitor SKUs across regions in real time
- **Lead enrichment** pipelines that pull live company, role, and contact signals
- **Training data** collection at petabyte scale for foundation models
- **Vertical agents** for travel, real estate, e-commerce, and finance that need fresh inventory

Browse [example apps and integrations →](https://demos.brightdata.com)

---

## Integrations

We're built into the agent stack you're already using:

LangChain · LangGraph · LlamaIndex · CrewAI · Vercel AI SDK · n8n · Make · Zapier · IBM watsonx · AWS Bedrock · Snowflake · Databricks

[See all integrations →](https://docs.brightdata.com/integrations)

---

<div align="center">
  <p>
    <strong>Ready to plug your agent into the open web?</strong><br>
    <a href="https://brightdata.com/cp/start">Start free</a> · <a href="https://docs.brightdata.com">Read the docs</a> · <a href="https://github.com/brightdata/brightdata-mcp">Star the MCP</a>
  </p>
  <br>
  <sub>Made by the team behind the world's best web access layer for AI.</sub>
</div>
