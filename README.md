<!-- Updated: 2026-02-25 -->

![Claude SEO](screenshots/cover-image.jpeg)

# SEO · AEO · GEO · AgEO · WebMCP (Claude Code Skill)

Universal visibility optimisation skill for Claude Code across:
- **SEO** (traditional search: Google/Bing)
- **AEO** (answer engines)
- **GEO** (generative engines: AI Overviews + AI search)
- **AgEO** (agentic engines: autonomous agents)
- **WebMCP** (browser-native agent tool surfaces; early preview Feb 2026)

This repo provides a full-spectrum analysis framework covering technical SEO, on-page analysis, E-E-A-T, schema markup, image optimisation, sitemap architecture, programmatic SEO, competitor pages, hreflang, platform-specific GEO (major AI platforms), MCP/agentic tool discoverability, brand data-hygiene, cite-check validation, answer-pack generation, and grounding page generation.

![SEO Command Demo](screenshots/seo-command-demo.gif)

[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-blue)](https://claude.ai/claude-code)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Installation

### One-Command Install (Unix/macOS/Linux)

```bash
curl -fsSL https://raw.githubusercontent.com/AgriciDaniel/claude-seo/main/install.sh | bash
```

### Manual Install

```bash
git clone https://github.com/AgriciDaniel/claude-seo.git
cd claude-seo
./install.sh
```

### Windows

```powershell
irm https://raw.githubusercontent.com/AgriciDaniel/claude-seo/main/install.ps1 | iex
```

## Quick Start

```bash
# Start Claude Code
claude

# Run a full site audit
/seo audit https://example.com

# Analyze a single page
/seo page https://example.com/about

# Technical audit
/seo technical https://example.com

# Check schema markup
/seo schema https://example.com

# Generate a sitemap
/seo sitemap generate

# GEO (Generative Engine Optimisation)
/seo geo https://example.com

# AEO (Answer Engine Optimisation)
/seo aeo https://example.com

# AgEO (Agentic Engine Optimisation)
/seo ageo https://example.com

# Validate if a page is citation-ready
/seo cite-check https://example.com
```

### Demo
[Watch the full demo on YouTube](https://www.youtube.com/watch?v=COMnNlUakQk)

**`/seo audit` — full site audit with parallel subagents:**

![SEO Audit Demo](screenshots/seo-audit-demo.gif)

## Commands

| Command | Description |
|---|---|
| `/seo audit <url>` | Full website audit with parallel subagent delegation |
| `/seo page <url>` | Deep single-page analysis |
| `/seo technical <url>` | Technical SEO audit (8 categories) |
| `/seo content <url>` | E-E-A-T and content quality analysis |
| `/seo schema <url>` | Detect, validate, and generate Schema.org markup |
| `/seo images <url>` | Image optimisation analysis |
| `/seo sitemap <url>` | Analyse existing XML sitemap |
| `/seo sitemap generate` | Generate new sitemap with industry templates |
| `/seo geo <url>` | Generative Engine Optimisation audit (multi-platform) |
| `/seo geo --mcp <url>` | MCP / agentic tool visibility audit |
| `/seo aeo <url>` | Answer Engine Optimisation audit |
| `/seo brand-radar <brand>` | Brand data-hygiene and citation consistency audit |
| `/seo ageo <url>` | Agentic Engine Optimisation audit |
| `/seo ageo --webmcp <url>` | WebMCP implementation audit + tool generation guidance |
| `/seo cite-check <url>` | Validate whether a page qualifies for AI citation |
| `/seo answer-pack <topic>` | Generate a full AI-answer content bundle for a topic |
| `/seo grounding-page <topic>` | Generate a Grounding Page (Standard v1.5) |
| `/seo profile init` | Create/update `project_profile.yml` (personalisation + overrides) |
| `/seo profile show` | Show active profile and applied overrides |
| `/seo plan <type>` | Strategic planning (saas, local, ecommerce, publisher, agency) |
| `/seo programmatic <url>` | Programmatic SEO analysis and planning |
| `/seo competitor-pages <url>` | Competitor comparison page generation |
| `/seo hreflang <url>` | Hreflang / i18n SEO audit and generation |

## Features

### Core Web Vitals (Current Metrics)
- **LCP** (Largest Contentful Paint): target < 2.5s
- **INP** (Interaction to Next Paint): target < 200ms
- **CLS** (Cumulative Layout Shift): target < 0.1

> Note: INP replaced FID on March 12, 2024. FID was fully removed from all Chrome tools on September 9, 2024.

### E-E-A-T Analysis
Updated to September 2025 Quality Rater Guidelines:
- **Experience**: first-hand knowledge signals
- **Expertise**: author credentials and depth
- **Authoritativeness**: industry recognition
- **Trustworthiness**: contact info, security, transparency

### Schema Markup
- Detection: JSON-LD (preferred), Microdata, RDFa
- Validation against supported types
- Generation with templates
- Deprecation awareness (e.g., HowTo deprecated Sept 2023; FAQ restricted Aug 2023)

### GEO / AEO / AgEO / WebMCP
- Platform-specific optimisation guidance across major AI answer and agent surfaces
- Citability validation (`/seo cite-check`)
- Answer bundle generation (`/seo answer-pack`)
- Grounding Page generation (`/seo grounding-page`)
- MCP discoverability (`/seo geo --mcp`)
- WebMCP implementation guidance (`/seo ageo --webmcp`)

## Architecture

```
~/.claude/skills/seo/         # Main skill
~/.claude/skills/seo-*/       # Sub-skills
~/.claude/agents/seo-*.md     # Subagents
```

## Requirements

- Python 3.8+
- Claude Code CLI
- Optional: Playwright (for screenshots)

## Uninstall

```bash
curl -fsSL https://raw.githubusercontent.com/AgriciDaniel/claude-seo/main/uninstall.sh | bash
```

### MCP Integrations

Integrates with MCP servers for live SEO data — including official servers from **Ahrefs** (`@ahrefs/mcp`) and **Semrush**, plus community servers for Google Search Console, PageSpeed Insights, and DataForSEO. See [MCP Integration Guide](docs/MCP-INTEGRATION.md) for setup.

## Documentation

- [Installation Guide](docs/INSTALLATION.md)
- [Commands Reference](docs/COMMANDS.md)
- [Architecture](docs/ARCHITECTURE.md)
- [MCP Integration](docs/MCP-INTEGRATION.md)
- [Troubleshooting](docs/TROUBLESHOOTING.md)

## License

MIT License - see [LICENSE](LICENSE) for details.

## Contributing

Contributions welcome! Please read the guidelines in `docs/` before submitting PRs.

---

Built for Claude Code.