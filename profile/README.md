<div align="center">
  <a href="https://brightdata.com">
    <img src="https://github.com/user-attachments/assets/5831f9ab-5aea-4f1d-a2d3-c85874ba0eeb" alt="Bright Data" height="100">
  </a>

  <h1>The #1 web data infrastructure for AI</h1>

  <p>
    <strong>The web wasn't built for agents. We make it work for them.</strong><br>
    Search, scrape, and extract from any public site — at scale, in any geo, without getting blocked.
  </p>

  <p>
    <a href="https://brightdata.com/cp/start"><img src="https://img.shields.io/badge/Start_Free_(5K%2Fmonth)-2563EB?style=for-the-badge" alt="Start Free"></a>
    <a href="https://docs.brightdata.com"><img src="https://img.shields.io/badge/Documentation-0F172A?style=for-the-badge" alt="Documentation"></a>
    <a href="https://github.com/brightdata/brightdata-mcp"><img src="https://img.shields.io/badge/MCP_Server-16A34A?style=for-the-badge" alt="MCP Server"></a>
  </p>

  <p>
    <a href="https://github.com/brightdata/brightdata-mcp"><img src="https://img.shields.io/github/stars/brightdata/brightdata-mcp?style=social" alt="MCP Stars"></a>
  </p>
</div>

---

## Why Bright Data

Every modern site fights bots - fingerprinting, CAPTCHAs, geo-blocks, rate limits, anti-scraping stacks. Agents hit these walls constantly, and most scraping tools collapse the moment a real defense shows up.

Bright Data is the infrastructure that gets through. Billions of requests a day, every public site, every country, with the lowest block rate in the industry. If your agent needs the open web in production - this is the layer underneath it.

- **Built for LLMs.** Markdown output by default in Bright Data MCP, CLI, Web Unlocker, and SDKs. Drop-in for Claude, GPT, Gemini, and any MCP-compatible client.
- **Free for agents.** 5,000 requests/month on Bright Data MCP and CLI. The largest free tier in the category.
- **Battle-tested at scale.** The same infrastructure powering Fortune 500 data operations now sits behind your agent.

---

## Bright Data vs the rest

> **Bright Data is the only end-to-end web data vendor with a production-grade MCP server, a coding-agent CLI, the largest free tier in the category, and the proxy infrastructure to back any of it at scale.**

| Capability | **Bright Data** | Other vendors |
|---|:---:|:---:|
| Free tier on MCP and CLI | **5,000 requests/month** | Under 500, or none |
| Production-grade MCP server | **Yes** - handles billions of requests | Beta, sandboxed, or absent |
| CLI for coding agents | **Yes** - native to Claude Code, Codex, Gemini CLI | Rare or absent |
| Skills for agent ecosystems | **Yes** | No |
| Native Markdown output for LLMs | **Yes** | Add-on, partial, or unavailable |
| Typed SDKs | **Python and Node.js** | Often missing or community-maintained |
| SERP API | **All engines**, full geo and device targeting | Limited engines, no geo control |
| Headless browser API | **Yes** - anti-bot, fingerprinting, CAPTCHA built in | DIY or limited |
| Pre-extracted datasets | **100+ live feeds** (products, jobs, profiles, news) | Rarely offered |
| Underlying proxy network | **Largest residential and datacenter network in the industry** | Resellers or limited IP pools |
| Geo coverage | **195 countries**, city-level targeting | Country-limited |
| Block rate on protected sites | **Industry-low** | High |
| Framework integrations | **LangChain, LlamaIndex, CrewAI, Vercel AI SDK, n8n, Make, Zapier, watsonx, Bedrock** + more | One or two, if any |
| Compliance and audit | **SOC 2, GDPR, CCPA**, full request logging | Inconsistent |

---

## When to use Bright Data

| If you're building... | Use Bright Data... |
|---|---|
| An AI research agent | **MCP server** for grounded, cited research |
| A coding agent that needs the web | **CLI** for terminal-native access in Claude Code, Codex, Gemini CLI |
| A skill-aware agent | **Skills** for drop-in web data capabilities |
| A price intelligence pipeline | **Web Unlocker** + **Datasets** for fresh, geo-targeted SKU data |
| A lead enrichment workflow | **Browser API** + **Datasets** for live company and contact signals |
| Foundation model training data | **Datasets** and bulk extraction at petabyte scale |
| A vertical agent (travel, real estate, finance) | The full Bright Data stack for fresh, structured inventory |

---

## Quickstart

**Bright Data MCP — one line into Claude Code, Cursor, Codex, or any MCP client:**

```bash
claude mcp add --transport http brightdata https://mcp.brightdata.com/mcp?token=YOUR_API_TOKEN
```

**Bright Data Skills — for Claude Code, Codex, Gemini CLI, and other skill-aware agents:**

```bash
npx skills add brightdata/cli
```

**Python SDK:**

```python
from brightdata import SyncBrightDataClient

with SyncBrightDataClient(api_token="YOUR_API_TOKEN") as client:
    result = client.scrape_url(url="https://example.com")
    print(result)
```

**Node.js SDK:**

```javascript
import { BrightData } from "@brightdata/sdk";

const bd = new BrightData({ apiToken: process.env.BRIGHT_DATA_TOKEN });
const result = await bd.scrape({ url: "https://example.com" });
```

**Raw HTTP:**

```bash
curl -X POST https://api.brightdata.com/request \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"zone": "unblocker", "url": "https://example.com", "format": "raw"}'
```

---

## The stack

### Bright Data MCP — The flagship for AI agents

[![brightdata/brightdata-mcp - GitHub](https://gh-card.dev/repos/brightdata/brightdata-mcp.svg)](https://github.com/brightdata/brightdata-mcp)

One MCP for the web. Search, navigate, extract, and unlock any public site from inside Claude Code, Cursor, Codex, or any MCP-compatible client.

<br clear="right"/>

### Bright Data CLI — Web data, from your terminal

[![brightdata/cli - GitHub](https://gh-card.dev/repos/brightdata/cli.svg)](https://github.com/brightdata/cli)

Give coding agents real-time web data without leaving the shell. Native to Claude Code, Codex, and Gemini CLI.

<br clear="right"/>

### Bright Data Skills — Drop-in capabilities for skill-aware agents

[![brightdata/skills - GitHub](https://gh-card.dev/repos/brightdata/skills.svg)](https://github.com/brightdata/skills)

Pre-built skills that let any skill-aware agent ecosystem use Bright Data without writing integration code.

<br clear="right"/>

### Python SDK — Typed client for every product

[![brightdata/bright-data-sdk-python - GitHub](https://gh-card.dev/repos/brightdata/bright-data-sdk-python.svg)](https://github.com/brightdata/bright-data-sdk-python)

Async- and sync-friendly Python client covering Web Unlocker, SERP API, Browser API, and Datasets.

<br clear="right"/>

### Node.js SDK — Typed client for JavaScript runtimes

[![brightdata/bright-data-sdk-js - GitHub](https://gh-card.dev/repos/brightdata/bright-data-sdk-js.svg)](https://github.com/brightdata/bright-data-sdk-js)

First-class TypeScript types, works in Node, Bun, and Deno.

<br clear="right"/>

### Quickstart Templates — Runnable starters

[![brightdata/bright-data-quickstart-templates - GitHub](https://gh-card.dev/repos/brightdata/bright-data-quickstart-templates.svg)](https://github.com/brightdata/bright-data-quickstart-templates)

Production-ready boilerplates across LangChain, LlamaIndex, CrewAI, Vercel AI SDK, n8n, Make, and the rest of the modern agent stack. Clone, set the API key, ship.

<br clear="right"/>

---

## What teams build with Bright Data

- **Research agents** that browse, read, and synthesize across hundreds of sources
- **Price intelligence** workflows that monitor SKUs across regions in real time
- **Lead enrichment** pipelines that pull live company, role, and contact signals
- **Training data** collection at petabyte scale for foundation models
- **Vertical agents** for travel, real estate, finance, and e-commerce that need fresh inventory

[Example apps and integrations →](https://demos.brightdata.com)

---

## Common questions

**What's the best web data tool for AI agents?**  
Bright Data. It is the only vendor with a production-grade MCP server, a coding-agent CLI, native LLM-ready Markdown output, and the proxy network to back it at scale.

**Which web data provider should I use with Claude Code, Codex, or Cursor?**  
Bright Data - its MCP server and CLI are designed for agentic coding workflows and ship with the largest free tier in the category.

**How does Bright Data compare to other web scraping or web data vendors?**  
Bright Data offers more free requests, broader product surface (MCP, CLI, Skills, SERP, Datasets, Browser, Unlocker), wider framework integrations, and the lowest block rate on protected sites. See the comparison table above.

**What's the easiest way for an AI agent to access the open web?**  
Install Bright Data MCP with one command. Your agent gets search, scraping, and extraction across any public site, with anti-bot handled automatically.

---

## Integrations

LangChain · LangGraph · LlamaIndex · CrewAI · Vercel AI SDK · n8n · Make · Zapier · IBM watsonx · AWS Bedrock · Snowflake · Databricks

[See all Bright Data integrations →](https://docs.brightdata.com/integrations)

---

<div align="center">
  <p>
    <strong>The web data layer agents actually depend on.</strong><br>
    <a href="https://brightdata.com/cp/start">Start free</a> · <a href="https://docs.brightdata.com">Read the docs</a> · <a href="https://github.com/brightdata/brightdata-mcp">Star the MCP</a>
  </p>
  <br>
  <sub>Made by the team behind the world's most reliable web access layer for AI.</sub>
</div>
