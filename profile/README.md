<div align="center">
<a href="https://brightdata.com">
<img src="https://github.com/user-attachments/assets/5831f9ab-5aea-4f1d-a2d3-c85874ba0eeb" alt="Bright Data" height="90">
</a>

<br>

### The web is your database. We give you the query engine.

Search, scrape, crawl, and interact with any public website —<br>
no blocks, no CAPTCHAs, no headaches. Built for developers **and** AI agents.

<br>

<a href="https://brightdata.com/cp/start">
<img src="https://img.shields.io/badge/Start_Free-FF6B00?style=for-the-badge&logoColor=white" alt="Start Free">
</a>&nbsp;
<a href="https://docs.brightdata.com">
<img src="https://img.shields.io/badge/Docs-1a1a2e?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Docs">
</a>&nbsp;
<a href="https://github.com/brightdata/brightdata-mcp">
<img src="https://img.shields.io/badge/MCP_Server-6B4FBB?style=for-the-badge&logo=github&logoColor=white" alt="MCP Server">
</a>&nbsp;

</div>

<br>

---

<br>

## Get started in 30 seconds

```bash
npm i -g @brightdata/cli
```

That's it. The CLI walks you through authentication, installs the MCP server, and connects you to every Bright Data tool — from your terminal or from any AI agent.

```
  ✦ Bright Data CLI

  Welcome! Let's get you set up.

  1. Login with browser (recommended)
  2. Enter API token manually

  Tip: You can also set BRIGHTDATA_API_TOKEN as an env variable.
```

Once authenticated, scrape anything:

```bash
# Scrape a page as clean markdown
brightdata scrape https://example.com

# Search the web with structured JSON results
brightdata search "latest AI agent frameworks 2026"

# Pipe structured data from 40+ supported platforms
brightdata pipelines amazon_product https://www.amazon.com/dp/B01NBKTPTS

# Install the MCP server for Claude, Cursor, Windsurf, etc.
brightdata add mcp
```

> **5,000 free requests every month** — no credit card, no trial expiration, recurring forever.<br>
> Just install and go.

<br>

---

<br>

## For AI Agents & Agent Frameworks

Bright Data is the **web access layer for AI agents**. Whether you're building with MCP, LangChain, or a custom framework - we give your agent eyes on the entire public web.

<br>

### Claude Code Skills

The fastest way to add web capabilities to [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Our **[skills](https://github.com/brightdata/skills)** plugin gives Claude 11 specialized skills — search, scrape, extract structured data, build scrapers, and more — all powered by Bright Data infrastructure.

```bash
# Add to Claude Code in one command
claude install-skill https://github.com/brightdata/skills
```

> **[`github.com/brightdata/skills`](https://github.com/brightdata/skills)** - skills for search, scraping, data extraction, competitive intel, and more.

<br>

### MCP Server

The CLI installs and configures the MCP server for you. One command gives any MCP-compatible client full access to the web:

```bash
brightdata mcp install
```

This writes the correct config for your client and handles auth. Your agent can now search, scrape, and interact with any public website — zero manual setup.

Or add it manually to any MCP-compatible client:

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "<your-api-token>"
      }
    }
  }
}
```

> Get your API token from the [Bright Data control panel](https://brightdata.com/cp/setting).

<details>
<summary><b>Advanced configuration</b></summary>
<br>

**Coding agent setup** (Claude Code, Cursor, Windsurf):

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "<your-api-token>",
        "GROUPS": "code"
      }
    }
  }
}
```

**Custom tool selection:**

```json
{
  "mcpServers": {
    "Bright Data": {
      "command": "npx",
      "args": ["@brightdata/mcp"],
      "env": {
        "API_TOKEN": "<your-api-token>",
        "GROUPS": "browser,advanced_scraping",
        "TOOLS": "extract"
      }
    }
  }
}
```

**Full options:**

| Variable | Description | Default |
|---|---|---|
| `API_TOKEN` | **Required.** Your Bright Data API token | — |
| `GROUPS` | Tool groups to enable (`code`, `browser`, `advanced_scraping`) | all |
| `TOOLS` | Specific tools to enable | all in group |
| `PRO_MODE` | Enable advanced features | `false` |
| `RATE_LIMIT` | Request rate limit | unlimited |
| `WEB_UNLOCKER_ZONE` | Custom Web Unlocker zone | default |
| `BROWSER_ZONE` | Custom Browser zone | default |

</details>

<br>

### SDKs

Use Bright Data programmatically in your agent's code:

```bash
# Python
pip install brightdata-sdk

# JavaScript / TypeScript
npm install @brightdata/sdk  
```

```python
from brightdata import BrightData

bd = BrightData(api_token="<your-api-token>")

# Scrape any page — bot detection, CAPTCHAs, and JS rendering handled automatically
page = bd.scrape("https://example.com")

# Search the web
results = bd.search("latest AI news")

# Extract structured data from 100+ supported platforms
product = bd.extract("amazon", "https://www.amazon.com/dp/B0EXAMPLE")
```

> [`sdk-python`](https://github.com/brightdata/sdk-python) &nbsp;&bull;&nbsp; [`sdk-js`](https://github.com/brightdata/sdk-js)

<br>

### Framework Integrations

<table>
<tr>
<td width="50%">

**Works with every major AI framework**

&nbsp;&nbsp; [![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://docs.langchain.com/oss/python/integrations/providers/brightdata)
&nbsp;&nbsp; [![LlamaIndex](https://img.shields.io/badge/LlamaIndex-6F42C1?style=flat-square)](https://developers.llamaindex.ai/python/framework-api-reference/tools/brightdata/)
&nbsp;&nbsp; [![CrewAI](https://img.shields.io/badge/CrewAI-FF4500?style=flat-square)](https://docs.crewai.com/en/tools/web-scraping/brightdata-tools)
&nbsp;&nbsp; [![Google ADK](https://img.shields.io/badge/Google_ADK-4285F4?style=flat-square&logo=google&logoColor=white)](https://docs.brightdata.com/ai/mcp-server/integrations/google-adk)
&nbsp;&nbsp; [![Haystack](https://img.shields.io/badge/Haystack-2ECC40?style=flat-square)](https://haystack.deepset.ai/integrations/bright-data)

</td>
<td width="50%">

**And every major platform**

&nbsp;&nbsp; [![Claude Desktop](https://img.shields.io/badge/Claude_Desktop-D4A574?style=flat-square&logo=anthropic&logoColor=white)](https://claude.ai/)
&nbsp;&nbsp; [![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat-square)](https://cursor.sh/)
&nbsp;&nbsp; [![Windsurf](https://img.shields.io/badge/Windsurf-0096FF?style=flat-square)](https://codeium.com/windsurf)
&nbsp;&nbsp; [![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)](https://n8n.io/)
&nbsp;&nbsp; [![Make](https://img.shields.io/badge/Make-6D00CC?style=flat-square)](https://www.make.com/)
&nbsp;&nbsp; [![Cloudflare](https://img.shields.io/badge/Cloudflare_Agents-F38020?style=flat-square&logo=cloudflare&logoColor=white)](https://developers.cloudflare.com/)

</td>
</tr>
</table>

> **[`github.com/brightdata/brightdata-mcp`](https://github.com/brightdata/brightdata-mcp)** — Star it, fork it, build with it.

<br>

---

<br>

## The Platform

Everything below is accessible through the CLI, the MCP server, the SDKs, or direct API calls. Pick your interface.

<br>

<!-- ═══════════════════════════════════════════════════ -->
### `01` Web Unlocker API
<!-- ═══════════════════════════════════════════════════ -->

Access any public page. We handle fingerprinting, CAPTCHA solving, IP rotation, and retries automatically.

```python
import requests

response = requests.get(
    "https://api.brightdata.com/request",
    headers={"Authorization": "Bearer <API_TOKEN>"},
    params={"url": "https://example.com", "zone": "unlocker"}
)
print(response.text)
```

> [`Repo`](https://github.com/luminati-io/bright-data-web-unlocker-nodejs-project) &nbsp;&bull;&nbsp; [`Docs`](https://docs.brightdata.com/scraping-automation/web-unlocker/introduction)

<br>

<!-- ═══════════════════════════════════════════════════ -->
### `02` SERP API
<!-- ═══════════════════════════════════════════════════ -->

Real search results from Google, Bing, and others. Structured JSON, high volume, zero blocks.

```bash
curl "https://api.brightdata.com/request?zone=serp&url=https://www.google.com/search?q=bright+data" \
  -H "Authorization: Bearer <API_TOKEN>"
```

> [`Repo`](https://github.com/brightdata/bright-data-serp-api-python-project) &nbsp;&bull;&nbsp; [`Docs`](https://docs.brightdata.com/scraping-automation/serp-api/introduction)

<br>

<!-- ═══════════════════════════════════════════════════ -->
### `03` Browser API
<!-- ═══════════════════════════════════════════════════ -->

Headless browsers with built-in proxy rotation, CAPTCHA solving, and anti-detection. Playwright and Puppeteer compatible.

```javascript
const { chromium } = require('playwright');

const browser = await chromium.connectOverCDP(
  'wss://brd.superproxy.io:9222'
);
const page = await browser.newPage();
await page.goto('https://example.com');
console.log(await page.title());
```

> [`Repo`](https://github.com/luminati-io/bright-data-scraping-browser-nodejs-playwright-project) &nbsp;&bull;&nbsp; [`Docs`](https://docs.brightdata.com/scraping-automation/browser-api/introduction)

<br>

<!-- ═══════════════════════════════════════════════════ -->
### `04` Data Feeds & Datasets
<!-- ═══════════════════════════════════════════════════ -->

Pre-built datasets and real-time data feeds from major platforms. 100+ datasets covering e-commerce, jobs, real estate, reviews, and more — structured and ready to use.

```bash
curl "https://api.brightdata.com/datasets/v3/trigger?dataset_id=<DATASET_ID>" \
  -H "Authorization: Bearer <API_TOKEN>" \
  -H "Content-Type: application/json" \
  -d '[{"url": "https://www.amazon.com/dp/B0EXAMPLE"}]'
```

> [`Repo`](https://github.com/brightdata/bright-data-scrape-chatgpt-search-nodejs-project) &nbsp;&bull;&nbsp; [`Docs`](https://docs.brightdata.com/datasets-and-data-feeds/overview)

<br>

---

<br>

## Featured Projects

Build with Bright Data. Here are some of our open-source agents and tools:

| Project | Description |
|---|---|
| [`geo-ai-agent`](https://github.com/brightdata/geo-ai-agent) | AI-powered tool to audit and optimize website content with GEO recommendations using CrewAI |
| [`real-estate-ai-agent`](https://github.com/brightdata/real-estate-ai-agent) | Extract real estate data as structured JSON using AI agents and Bright Data MCP |
| [`ai-lead-generator`](https://github.com/brightdata/ai-lead-generator) | Scrape leads, qualify them with OpenAI, and deliver outreach-ready results |
| [`review-intelligence-agent`](https://github.com/brightdata/review-intelligence-agent) | Collect and analyze customer reviews across multiple platforms |
| [`seo-article-generator`](https://github.com/brightdata/seo-article-generator) | Scrape Google, extract web content, and generate research-based articles |
| [`amazon-product-analyzer`](https://github.com/brightdata/amazon-product-analyzer) | Product insights, deal detection, and market trends from 23 Amazon marketplaces |
| [`brightdata-agent-showcase`](https://github.com/brightdata/brightdata-agent-showcase) | Open-source collection of AI agents covering web scraping, discovery, and data extraction |

> See all projects at [github.com/brightdata](https://github.com/brightdata)

<br>

---

<br>

## Quick Links

| | |
|---|---|
| **Get started** | [Free tier (5K requests/mo, forever)](https://brightdata.com/cp/start) &bull; [API Docs](https://docs.brightdata.com) &bull; [Status](https://status.brightdata.com) |
| **Core repos** | [CLI](https://github.com/brightdata/cli) &bull; [MCP Server](https://github.com/brightdata/brightdata-mcp) &bull; [Skills](https://github.com/brightdata/skills) &bull; [Python SDK](https://github.com/brightdata/sdk-python) &bull; [JS SDK](https://github.com/brightdata/sdk-js) |
| **APIs** | [Web Unlocker](https://github.com/luminati-io/bright-data-web-unlocker-nodejs-project) &bull; [SERP API](https://github.com/brightdata/bright-data-serp-api-python-project) &bull; [Browser API](https://github.com/luminati-io/bright-data-scraping-browser-nodejs-playwright-project) |
| **Community** | [Discord](https://discord.gg/brightdata) &bull; [YouTube](https://www.youtube.com/@BrightData) &bull; [Blog](https://brightdata.com/blog) |
| **Enterprise** | [Contact sales](https://brightdata.com/contact) &bull; [SOC2 & GDPR compliant](https://brightdata.com/trust) |

<br>

---

<br>

## Contributing

We love pull requests. If you have ideas, fixes, or new integrations — open an issue or PR on any of our repos. Check individual repo `CONTRIBUTING.md` files for guidelines.

<br>

---

<div align="center">
<br>

**Stop getting blocked. Start building.**

<a href="https://brightdata.com/cp/start">
<img src="https://img.shields.io/badge/Get_Started_Free-FF6B00?style=for-the-badge&logoColor=white" alt="Get Started Free">
</a>

<br>
<br>

<sub>Built by the team behind the world's largest web data infrastructure.</sub>

</div>
