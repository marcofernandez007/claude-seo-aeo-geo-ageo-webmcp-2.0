---
name: seo-aeo-geo
version: 3.0.0
metadata:
  standard: v1.6
description: >
  Universal SEO, AEO, GEO, AgEO, and WebMCP skill for Claude Code. Full-spectrum visibility
  optimisation across traditional search engines, AI answer engines (ChatGPT,
  Perplexity, Gemini, Grok, Copilot, DeepSeek, Meta AI, Claude), MCP-connected
  AI agents (Claude Desktop, Cursor, VS Code), and autonomous AI agents operating
  via WebMCP (Google/Microsoft browser-native agent standard, early preview Feb 2026).
  Covers technical SEO, on-page analysis, E-E-A-T, schema markup, image optimisation,
  sitemap architecture, programmatic SEO, competitor pages, hreflang, platform-specific
  GEO (7 AI platforms), MCP/agentic tool discoverability, Answer Engine Optimisation (AEO),
  Agentic Engine Optimisation (AgEO), WebMCP implementation guidance, brand data-hygiene,
  entity clarity, profile-driven personalisation (project_profile.yml), generic-output
  blocking, cite-check validation, answer-pack generation, and Grounding Page
  Integration — with parallel subagent delegation.
---

# SEO · AEO · GEO · AgEO · WebMCP Skill

Comprehensive visibility optimisation across five disciplines:

| Discipline | Target surface | Goal |
|---|---|---|
| **SEO** | Google, Bing, traditional SERPs | Rank in blue-link results |
| **GEO** | Google AI Overviews, Perplexity, ChatGPT, Gemini, Copilot, Grok, DeepSeek, Meta AI, Claude | Be cited in AI-generated summaries and answers |
| **GEO–MCP** | Claude Desktop, Cursor, VS Code Copilot, custom AI agents | Be selected as the tool an agent uses to complete a task |
| **AEO** | ChatGPT, Claude, Gemini, Copilot answer boxes | Be recommended as the authoritative brand answer |
| **AgEO** | Autonomous AI agents (OpenAI Operator, Gemini agentic, Claude computer use, Google AI Mode agentic) | Be discoverable and usable by AI agents completing tasks on users' behalf |
| **WebMCP** | Chrome-based AI agents via Google/Microsoft Web Model Context Protocol (early preview, Feb 2026) | Expose structured, callable site tools to browser-level AI agents |

All five are interdependent. High-quality SEO content is the foundation; GEO and AEO layer citation-worthiness and brand data hygiene on top; AgEO and WebMCP represent the emerging agentic frontier.

---

## Commands

| Command | Description |
|---|---|
| `/seo audit <url>` | Full website audit with parallel subagent delegation |
| `/seo page <url>` | Deep single-page analysis |
| `/seo sitemap <url>` | Analyse existing XML sitemap |
| `/seo sitemap generate` | Generate new sitemap with industry templates |
| `/seo schema <url>` | Detect, validate, and generate Schema.org markup |
| `/seo images <url>` | Image optimisation analysis |
| `/seo technical <url>` | Technical SEO audit (8 categories) |
| `/seo content <url>` | E-E-A-T and content quality analysis |
| `/seo geo <url>` | AI Overviews / Generative Engine Optimisation (all platforms) |
| `/seo geo --mcp <url>` | MCP / agentic tool visibility audit |
| `/seo aeo <url>` | Answer Engine Optimisation audit |
| `/seo brand-radar <brand>` | Brand data-hygiene and citation consistency audit |
| `/seo ageo <url>` | **NEW** Agentic Engine Optimisation audit — agent discoverability, task-completion readiness |
| `/seo ageo --webmcp <url>` | **NEW** WebMCP implementation audit and tool generation guide (Google/Microsoft browser agent standard) |
| `/seo cite-check <url>` | **NEW** Validate whether a page qualifies for AI citation |
| `/seo answer-pack <topic>` | **NEW** Generate a full AI-answer content bundle for a topic |
| `/seo grounding-page <topic>` | **NEW** Generate a Grounding Page (Standard v1.5) |
| `/seo profile init` | **NEW** Create or update `project_profile.yml` for this project |
| `/seo profile show` | **NEW** Display the active profile and applied overrides |
| `/seo plan <type>` | Strategic SEO planning (saas, local, ecommerce, publisher, agency) |
| `/seo programmatic <url>` | Programmatic SEO analysis and planning |
| `/seo competitor-pages <url>` | Competitor comparison page generation |
| `/seo hreflang <url>` | Hreflang / i18n SEO audit and generation |

> All commands beginning with `/seo` are routed through the main orchestrator. Subagents run in parallel during full audits.

---

## Part 1 — SEO (Search Engine Optimisation)

### Technical SEO Audit (8 Categories)

Run via `/seo technical <url>`. Covers:

1. **Crawlability & Indexability** — robots.txt, meta robots, X-Robots-Tag, noindex/nofollow patterns, crawl budget signals
2. **Core Web Vitals**
   - LCP (Largest Contentful Paint): target < 2.5 s
   - INP (Interaction to Next Paint): target < 200 ms *(replaced FID on 12 March 2024; FID fully removed September 2024)*
   - CLS (Cumulative Layout Shift): target < 0.1
3. **Site Architecture** — URL structure, silo depth (target ≤ 3 clicks from homepage), internal link graph, orphan pages
4. **Mobile & Rendering** — mobile-first indexing readiness, JavaScript rendering issues, AMP if applicable
5. **HTTPS & Security** — TLS configuration, mixed-content warnings, HSTS
6. **Duplicate Content & Canonicalisation** — canonical tags, parameter handling, pagination (`rel=next/prev` removed 2019; use canonical or sitemap)
7. **Structured Data** — Schema.org coverage (see schema section below)
8. **International SEO** — hreflang validity, x-default, self-referencing tags

### On-Page SEO

Run via `/seo page <url>`. Analyses:

- **Title tag** — 50–60 characters, primary keyword near front, unique per page
- **Meta description** — 150–160 characters, call to action, not a ranking signal but affects CTR
- **Heading hierarchy** — single H1, logical H2–H6 structure, keyword placement without stuffing
- **Keyword placement** — first 100 words, subheadings, image alt text, URL slug
- **Internal linking** — anchor text diversity, contextual links, link depth
- **Word count guidance** — match or exceed top-ranking competitors for the query; not a direct ranking factor but correlates with comprehensiveness
- **Readability** — Flesch-Kincaid or similar; match audience literacy level

### E-E-A-T Analysis

Run via `/seo content <url>`. Updated to September 2025 Quality Rater Guidelines.

- **Experience** — first-hand signals: author bylines with credentials, personal testing notes, dates of direct experience
- **Expertise** — depth of topic coverage, correct use of domain terminology, cited sources
- **Authoritativeness** — inbound links from authoritative domains, brand mentions in industry press, Wikipedia presence
- **Trustworthiness** — HTTPS, clear contact info, editorial policy, privacy policy, accurate YMYL content (Your Money or Your Life)

Outputs an E-E-A-T score card with actionable gaps.

### Image Optimisation

Run via `/seo images <url>`.

- File format: WebP preferred, AVIF for modern browsers, JPEG/PNG fallback
- Compression: lossy ≤ 80% quality for photos; lossless for graphics with text
- Alt text: descriptive, keyword-relevant, ≤ 125 characters; empty `alt=""` for decorative images
- Lazy loading: `loading="lazy"` for below-fold images
- Responsive: `srcset` and `sizes` attributes
- Filename: descriptive slugs (`red-running-shoes.webp` not `img0023.webp`)

### Sitemap Architecture

Run via `/seo sitemap <url>` or `/seo sitemap generate`.

- XML sitemap: ≤ 50,000 URLs per file; use sitemap index for larger sites
- Include `<lastmod>`, `<changefreq>`, `<priority>` (though Google uses lastmod mainly)
- Exclude: noindex pages, paginated duplicates, thin/parameter URLs
- Submit via Google Search Console and Bing Webmaster Tools
- Industry templates available: saas, ecommerce, publisher, local, agency

### Schema Markup

Run via `/seo schema <url>`. Detects JSON-LD (preferred), Microdata, RDFa.

**Supported & Active Types (2025–2026):**

| Type | Use case |
|---|---|
| `Article` / `NewsArticle` / `BlogPosting` | Editorial content |
| `Product` + `Offer` + `AggregateRating` | E-commerce |
| `LocalBusiness` | Local SEO |
| `Organization` + `WebSite` + `Sitelinks Searchbox` | Brand/home pages |
| `BreadcrumbList` | Navigation paths |
| `Event` | Scheduled events |
| `JobPosting` | Careers pages |
| `Recipe` | Food content |
| `VideoObject` + `BroadcastEvent` + `Clip` + `SeekToAction` | Video & live stream |
| `SoftwareApplication` | Native apps |
| `WebApplication` | Browser-based SaaS *(correct type, not SoftwareApplication)* |
| `SoftwareSourceCode` | Open source repos |
| `Course` + `CourseInstance` | Education |
| `MedicalWebPage` / `Drug` / `Physician` | Health (YMYL) |
| `LegalService` | Legal (YMYL) |
| `ItemList` | Listicles, carousels |
| `SearchAction` | Internal search |

**Deprecated / Restricted (do not use):**

| Type | Status |
|---|---|
| `HowTo` | Rich result deprecated September 2023 |
| `FAQ` | Restricted to gov/health sites August 2023 |
| `SpecialAnnouncement` | Deprecated July 2025 |
| `ClaimReview` | Restricted June 2025 |
| `VehicleListing` | Restricted June 2025 |

### Programmatic SEO

Run via `/seo programmatic <url|plan>`.

- Analyse existing programmatic pages for thin content and cannibalisation
- Plan URL patterns and template structures for data-driven pages
- Internal linking automation between generated pages
- Canonical strategy and index bloat prevention
- **Quality gates:** ⚠️ WARNING at 100+ pages, 🛑 HARD STOP at 500+ pages without a content-quality audit

### Competitor Comparison Pages

Run via `/seo competitor-pages <url|generate>`.

- Structured comparison tables with feature matrices
- `Product` schema with `AggregateRating`
- Conversion-optimised layouts with CTA placement
- Keyword targeting for `X vs Y` and `alternatives to X` queries
- Fairness guidelines: accurate competitor representation, no false claims

### Hreflang / International SEO

Run via `/seo hreflang <url>`.

- Generate hreflang tags (HTML `<link>`, HTTP headers, or XML sitemap)
- Validate self-referencing tags, return tags, `x-default`
- Detect: missing return tags, invalid language/region codes, HTTP/HTTPS mismatch
- Language codes: ISO 639-1; region codes: ISO 3166-1 Alpha-2
- Cross-domain hreflang supported

### Strategic SEO Planning

Run via `/seo plan <type>`.

Types: `saas` | `local` | `ecommerce` | `publisher` | `agency`

Outputs a 90-day roadmap covering: keyword universe, content clusters, technical priorities, link-building angles, and KPI targets.

---

## Part 2 — GEO (Generative Engine Optimisation)

Run via `/seo geo <url>`.

GEO is the practice of structuring content and brand presence so that generative AI systems — across search, assistants, agents, and MCP-connected tools — extract, cite, and recommend your brand in their generated answers. As of Q1 2026, AI-referred sessions grew 527% year-on-year, and 37% of product discovery queries now begin in AI interfaces rather than traditional search engines. GEO is no longer optional infrastructure.

### The GEO Target Surface Map

| Platform | Surface type | Citation mechanism | Bot name |
|---|---|---|---|
| Google AI Overviews | Search-integrated AI | RAG from indexed pages | Googlebot / Google-Extended |
| ChatGPT (web search) | Conversational + search | RAG via Bing index | GPTBot / ChatGPT-User |
| Perplexity | Dedicated AI search | Live web retrieval | PerplexityBot |
| Google Gemini | Conversational + search | RAG from Google index | Google-Extended |
| Microsoft Copilot | Conversational + search | RAG via Bing index | Bingbot / GPTBot |
| Grok (xAI) | Conversational + X search | RAG + X/web data | GPTBot (via API) |
| DeepSeek | Conversational | Training + retrieval | DeepSeekBot |
| Meta AI | Conversational + social | RAG + web retrieval | Meta-ExternalAgent |
| Claude (web search) | Conversational + search | RAG via web search | Claude-SearchBot |
| MCP-connected agents | Agentic tool execution | Direct tool/API call | Varies by client |
| Voice assistants | Audio-first answer | AI synthesis | Various |

**Key insight:** LLMs run an average of 3 web searches per user query, using longer and more specific sub-queries (avg. 7 words) than human searchers. They look deeper into SERPs than humans typically do. Optimise for the long tail.

---

### GEO Pillar 1 — Content Structure for AI Retrieval

AI retrieval systems (RAG) tokenise your HTML, embed it into vector space, and match it to queries semantically. Content that answers questions directly, without ambiguity, gets cited; marketing copy gets ignored.

**The CITABLE Framework:**

| Letter | Principle | Implementation |
|---|---|---|
| **C** | Clear structure | HTML5 semantic elements (`<article>`, `<section>`, `<aside>`), logical heading hierarchy, no `<div>` soup |
| **I** | Intent architecture | Map every page to one specific query intent; answer it in the first 40–60 words |
| **T** | Third-party validation | Cite primary sources inline; earn mentions on Reddit, G2, Capterra, industry press |
| **A** | Answer grounding | Use declarative sentences; avoid hedged, ambiguous, or promotional phrasing |
| **B** | Block structure | Short paragraphs (2–4 sentences); use lists and tables for comparative data |
| **L** | Latest data | Include timestamps; refresh statistics regularly; AI platforms prefer content 25.7% fresher than traditional SERP results |
| **E** | Entity schema | JSON-LD for `Organization`, `Person`, `Brand`, `sameAs`; make entities machine-identifiable |

**Content structure rules:**
- Place a direct answer to the primary query in the **first 40–60 words** of every article (not after an introduction)
- Use `<h2>` and `<h3>` tags phrased as questions — AI systems frequently match heading text directly to user queries
- Include a **TL;DR / Key Takeaways / Quick Answer** block at the top or immediately after the intro
- Maintain a **fact density** of at least one statistic or verifiable claim every 150–200 words
- Cite sources with inline hyperlinks — AI systems cross-reference citation chains
- Use semantic URLs: 5–7 descriptive words (pages with semantic URLs receive 11.4% more AI citations than generic URLs)

**Content types with highest AI citation rates (by research):**
1. Comparison and "X vs Y" articles — 32.5% of AI citations originate from comparison content
2. Definition and explainer articles
3. Step-by-step how-to guides (even without the deprecated HowTo rich result)
4. Original research, surveys, and data studies
5. Expert opinion with named, credentialled authors
6. Case studies with specific, named, quantified outcomes
7. FAQ-style content (even without FAQPage schema)

**Content types AI tends NOT to cite:**
- Promotional or salesy copy — over 95% of AI-cited links are non-paid, non-promotional
- Content without citations or attributed sources
- Pages behind login walls or JavaScript-rendered content that bots cannot access
- Thin pages (< 500 words on a complex topic)

---

### GEO Pillar 2 — Platform-Specific Optimisation

Each major AI platform has distinct preferences. Optimise for the platforms most relevant to your audience.

#### Google AI Overviews
- **Selection mechanism:** Prioritises pages already ranking in top-10 organic results; strong correlation with traditional SEO. AI Overviews appear in ~20% of Google searches as of September 2025.
- **Content signals:** E-E-A-T weight highest; structured data heavily parsed; freshness matters for news/current events
- **Technical requirements:** Googlebot must fully render JavaScript; Core Web Vitals pass required
- **Robots directive:** Do NOT block Google-Extended unless intentional — blocking removes you from AI Overview eligibility
- **Schema priority:** `Article` + `Organization` + `BreadcrumbList` + `Speakable`
- **Optimisation tip:** Pages ranking positions 4–10 organically can leapfrog into AI Overviews by improving answer-first structure and structured data

#### ChatGPT (Web Search Mode)
- **Selection mechanism:** RAG via Bing index; high correlation with Bing organic rankings; favours encyclopedic, comprehensive coverage
- **Content signals:** Comprehensive topic coverage; authoritative external links; Wikipedia-style neutral tone; updated content
- **Crawler:** GPTBot (training), ChatGPT-User (live browsing)
- **Bot directive:** Blocking GPTBot reduces training-time inclusion; blocking ChatGPT-User removes real-time citation eligibility. Evaluate carefully.
- **Schema priority:** `Organization` + `Article` + `sameAs` network
- **Optimisation tip:** ChatGPT drives 77.97% of all AI referral traffic globally — highest ROI platform for GEO investment

#### Perplexity
- **Selection mechanism:** Live web retrieval across multiple sources; rewards recency AND community evidence; indexes Reddit, LinkedIn, YouTube heavily
- **Content signals:** Freshness (timestamp visible); community corroboration on Reddit/Quora; authoritative news coverage; direct answer structure
- **Crawler:** PerplexityBot
- **Optimisation tip:** Community presence on Reddit, LinkedIn, and niche forums is disproportionately high-value for Perplexity citations compared to other platforms
- **Schema priority:** `NewsArticle` or `Article` with `datePublished` and `dateModified`

#### Google Gemini
- **Selection mechanism:** RAG from Google's search index + Google Knowledge Graph; entity clarity is crucial
- **Content signals:** Google Knowledge Panel presence; Wikipedia/Wikidata links; YouTube content (Gemini cites YouTube video transcripts)
- **Crawler:** Google-Extended
- **Optimisation tip:** Claim and verify your Google Knowledge Panel; connect all `sameAs` links to Wikidata and Wikipedia; upload video content with accurate transcripts

#### Microsoft Copilot (Bing)
- **Selection mechanism:** RAG via Bing index; similar to ChatGPT web mode; verify Bing Webmaster Tools indexing
- **Optimisation tip:** Submit sitemap to Bing Webmaster Tools; check Bing coverage separately from Google as the two indexes diverge

#### Grok (xAI)
- **Selection mechanism:** X (Twitter) posts + web retrieval; strong weighting on real-time recency and social corroboration
- **Optimisation tip:** Publish concise, sourced threads; link back to grounding pages; ensure consistent entity naming across X profile + site
  
#### DeepSeek & Emerging Models
- **Selection mechanism:** Primarily training-data-based; less RAG-dependent than western platforms
- **Optimisation tip:** Focus on being well-documented on Wikipedia, GitHub, academic papers, and major publications that form training corpora

---

### GEO Pillar 3 — Technical GEO

Technical SEO remains the foundation. AI systems cannot cite what they cannot crawl and parse.

**AI crawler access audit (run as part of `/seo geo`):**

```
AI CRAWLER ACCESS AUDIT
────────────────────────
Googlebot:           [Allowed / Blocked]
Google-Extended:     [Allowed / Blocked] ← AI Overviews
GPTBot:              [Allowed / Blocked] ← ChatGPT training
ChatGPT-User:        [Allowed / Blocked] ← ChatGPT live
PerplexityBot:       [Allowed / Blocked]
Meta-ExternalAgent:  [Allowed / Blocked]
Claude-SearchBot:    [Allowed / Blocked]
JavaScript rendering: [Full / Partial / None]
Login walls:         [None / Partial / Blocking]
```

**robots.txt directives for GEO (recommended baseline):**
```
User-agent: GPTBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Meta-ExternalAgent
Allow: /
```
Only block AI bots deliberately if you have a specific legal or commercial reason. Blocking reduces citation eligibility across all RAG-based platforms.

**Additional technical requirements:**
- Enable `IndexNow` protocol — notifies Bing, Yandex, and connected engines of content updates immediately, improving freshness signals for Copilot and ChatGPT
- Implement OpenAPI/JSON-LD on API documentation pages — AI systems parsing developer content use these as structured interfaces
- Ensure all multimedia (images, video) has descriptive alt text and captions — AI crawlers cannot parse JavaScript-rendered visuals
- `Speakable` schema marks content optimal for voice-first AI assistants
- Semantic URL structure (`/guides/what-is-geo/` not `/p?id=4821`) improves AI citation rate by 11.4%

---

### GEO Pillar 4 — Off-Site Authority for AI Citation

**Your own website is not your best GEO asset.** AI platforms trust and preferentially cite third-party sources. Build a cross-web citation network:

**Tier 1 — Highest AI trust (cite on these platforms):**
- Wikipedia (neutral, cited, verifiable)
- Wikidata (machine-readable entity definition)
- Major news publications (TechCrunch, Forbes, Reuters, BBC, WSJ, etc.)
- Academic/research papers (Google Scholar, arXiv, PubMed)
- Government/regulatory sites (.gov, .edu)

**Tier 2 — High AI trust (active presence required):**
- Reddit (subreddit contributions, AMA threads, product mentions by real users)
- LinkedIn (long-form articles, company page activity, founder thought leadership)
- YouTube (video content with accurate transcripts — Gemini cites YouTube heavily)
- G2, Capterra, Trustpilot (product reviews with authentic detail)
- Quora (expert answers to relevant questions)
- GitHub (for tech/dev brands — repositories, README files, issues are indexed)

**Tier 3 — Supportive signals:**
- Niche industry publications and forums
- Podcast transcripts (text versions of audio content)
- Crunchbase, Pitchbook (startup/company data)
- Company blog (useful but viewed as brand-owned; weight lower than Tier 1/2)

**Earned media strategy:**
AI platforms cite earned (journalistic) coverage over promotional content. More than 95% of AI-cited links are non-paid. Build a consistent PR and thought leadership programme targeting Tier 1 publications.

---

### GEO Pillar 5 — Entity Clarity and Knowledge Graph

AI models reason about the world through entities — named things with properties and relationships. Brands with well-defined entity profiles are cited with higher confidence.

**Entity definition checklist:**
- **Wikidata entry** — create or claim; add `P856` (website), `P18` (logo/image), `P571` (inception date), `P112` (founder), `P452` (industry), `P2860` (cites work)
- **Wikipedia article** — create if notable under Wikipedia's notability guidelines; ensure neutrality, verifiability, and proper sourcing
- **Google Knowledge Panel** — claim via Google Search Console; verify with authorised representative
- **`sameAs` network in Organization schema** — link to Wikipedia, Wikidata, LinkedIn, Crunchbase, and all social profiles (see schema template in Part 8)
- **Consistent entity naming** — brand name, product names, and executive names must be identical across all web properties; inconsistency reduces AI citation confidence

---

### GEO Pillar 6 — MCP Client Visibility (Agentic GEO)

This is the frontier of GEO. As AI agents powered by the Model Context Protocol (MCP) become mainstream — in Claude Desktop, Cursor, VS Code, Copilot, and custom enterprise agents — brands and products can achieve a new form of visibility: **being selected as the tool an agent uses to complete a task**.

#### What is MCP and why it matters for GEO

MCP (Model Context Protocol), introduced by Anthropic in November 2024 and now adopted by OpenAI, Google, Microsoft, and Cloudflare, is the standard protocol for connecting AI agents to external tools, data sources, and APIs. It is the "USB-C connector" for AI agents. As of early 2026, MCP SDKs have over 20 million weekly downloads.

When a user asks an AI agent to "find me the best CRM for my team" or "search for competitor pricing," the agent uses MCP tools to fetch live data. **The tools and data sources an agent selects are determined by how well those tools are described and how trustworthy their data appears.** This creates a new optimisation surface: **MCP tool discoverability**.

#### MCP GEO: How to appear in agentic AI workflows

**1. Build or expose an MCP server for your product**

If your product has an API, create an MCP server that exposes its capabilities. MCP servers are indexed in tool directories (MCP registries, Claude Desktop tool stores, VS Code extensions marketplace) where AI agents discover available tools.

Key optimisation principles for MCP server discoverability:
- **Tool name:** Short, specific, verb-noun format (e.g., `search_competitors`, `get_pricing`, `find_venues`). Avoid generic names.
- **Tool description:** This is the primary semantic interface an LLM uses to decide whether to call your tool. Write it as a clear, specific natural-language sentence explaining exactly what the tool does, when to use it, and what it returns. Poor descriptions are the #1 cause of wrong tool selection.
  ```json
  {
    "name": "search_product_reviews",
    "description": "Search G2 and Capterra for verified user reviews of a specific software product. Use when the user asks about reputation, user satisfaction, or real-world experience with a product. Returns: up to 20 reviews with rating, date, reviewer role, and summary."
  }
  ```
- **Input schema:** Fully document all parameters with types, descriptions, and examples. AI agents use input schemas to infer tool capabilities and parameterise calls correctly.
- **Return format documentation:** Document the exact structure of your tool's response so agents can parse it reliably.
- **Error handling:** Implement standard MCP error codes; document retry logic. Agents de-prioritise tools that return ambiguous errors.

**2. Get listed in MCP registries and directories**

MCP servers are discovered through registries. Submit your server to:
- Official MCP registry (modelcontextprotocol.io)
- Claude Desktop tool directory (Anthropic)
- VS Code Extensions Marketplace (if applicable)
- Cursor / Windsurf / Cline ecosystem directories
- Composio (500+ app connector platform)
- Apify (5,000+ actor marketplace for web data tools)

**3. Optimise for the Tool Search paradigm**

Claude and other advanced agents now use "Tool Search" — dynamically discovering tools on demand rather than loading all tools upfront. This means your tool's **name and description must be semantically findable** for the queries users will ask, not just for a static list.

Think of tool descriptions as mini landing pages for an LLM: they need to match the intent of the user's task, not just describe your product's features.

**4. Documentation-as-GEO for developer tools**

For dev-focused products, your documentation site is your primary MCP GEO asset:
- Publish OpenAPI specs and make them publicly accessible at a stable URL
- Include JSON-LD `SoftwareApplication` or `WebApplication` schema on all product pages
- Add `SoftwareSourceCode` schema to GitHub repository links
- Write documentation in plain, declarative English — AI agents crawl and parse docs to understand tool capabilities
- Include concrete usage examples with expected inputs and outputs in every reference page

**5. Track agentic traffic**

AI agents accessing your site via MCP or web crawl leave distinct bot signatures in server logs. Set up log monitoring to track:
- `GPTBot`, `ChatGPT-User`, `PerplexityBot`, `Google-Extended`, and other AI crawler user-agent strings
- Frequency of API calls from AI orchestration platforms
- Which pages and endpoints AI agents access most (this reveals what content is actually driving AI retrieval)

Tools: Profound Agent Analytics, Adobe LLM Optimizer (supports MCP and A2A protocols), BrightEdge AI visibility tracking.

#### MCP GEO Audit: `/seo geo --mcp <url>`

Performs:
1. MCP server presence check — does the brand have a publicly available MCP server?
2. Tool description quality score — evaluates name specificity, description clarity, schema completeness
3. MCP registry listing audit — checks presence in major tool directories
4. API/OpenAPI documentation quality — checks for public spec, JSON-LD schema, usage examples
5. AI crawler access audit — verifies bots can access key documentation and product pages
6. Agentic traffic analysis (if server logs available) — identifies which pages AI agents retrieve most

---

### GEO Pillar 7 — Multimodal GEO

AI systems increasingly process text, images, audio, and video together. Future-proof your GEO strategy across all modalities:

- **Video:** Publish transcripts alongside all video content; use `VideoObject` schema with `description`, `transcript`, and `keywords`; YouTube transcripts are directly indexed by Gemini
- **Images:** Alt text is the primary signal for AI image understanding; use descriptive, contextual alt text (not keyword-stuffed); provide `ImageObject` schema where relevant
- **Audio/Podcasts:** Publish timestamped text transcripts; use `PodcastEpisode` / `AudioObject` schema; transcripts dramatically improve AI citability of audio content
- **Voice:** `Speakable` schema marks content suited for voice-first AI responses; keep marked passages to 20–30 seconds of spoken audio

---

### GEO Measurement Framework

Traditional SEO metrics (rankings, CTR) do not capture AI visibility. Use this parallel measurement stack:

**Manual testing (free, always-on):**
- Test 15–20 representative queries monthly on ChatGPT, Perplexity, Gemini, and Claude
- Document: whether brand appears, where in the response, sentiment, and source URLs cited
- Track longitudinally — build a prompt library and run the same prompts monthly

**Proxy metrics (via existing analytics):**
- **Branded search volume increase** — users who discover a brand via AI then search it directly
- **Direct traffic increase** — AI-assisted discovery converts to direct visits
- **AI referral traffic in GA4** — set up custom channel groupings for known AI referrer domains (chatgpt.com, perplexity.ai, gemini.google.com, claude.ai, bing.com/chat)
- **Assisted conversions** — AI-discovered users converting via other channels later

**Specialist GEO/AEO SaaS tools (recommended for scale):**

| Tool | Strengths | Best for |
|---|---|---|
| **Profound** | 10+ engines incl. GPT-5.2, Claude, DeepSeek; real user prompt data (400M+ conversations); Agent Analytics for AI crawler logs; MCP server | Enterprise; highest data depth |
| **AthenaHQ** | Founded by ex-Google Search + DeepMind; ChatGPT, Perplexity, Claude, Gemini monitoring | Mid-market; actionable insights |
| **Peec AI** | Citation frequency, sentiment, competitor SOV; covers ChatGPT, Perplexity, Gemini, DeepSeek | Agencies; multi-brand management |
| **Otterly** | Brand mentions + link citations in AI search; GEO prompt-to-keyword conversion | SMB; content teams |
| **Semrush AI Toolkit** | Integrates with existing Semrush workflow; AI brand presence + recommendations | Teams already using Semrush |
| **Ahrefs Brand Radar** | AI Overview tracking + AI visibility alongside traditional SEO data | Teams already using Ahrefs |
| **BrightEdge** | Enterprise; connects AI citations to pipeline attribution; GA4 + Looker Studio integration | Enterprise B2B with revenue attribution requirements |
| **Citable** | Persona-based share-of-voice; pre-warms AI accounts to simulate real users | Startups; persona-specific visibility |
| **Adobe LLM Optimizer** | MCP + A2A protocol support; content freshness signals; enterprise governance | Enterprises using Adobe Experience Manager |

**KPIs to track:**
- Share of Voice (SOV) in AI responses — % of queries where brand is cited across target platforms
- Citation frequency — how often brand appears per 100 queries tested
- Sentiment score — positive / neutral / negative framing of brand in AI responses
- First-mention rate — how often brand is the first recommendation given
- Platform coverage — which AI engines cite the brand; gaps indicate optimisation opportunities
- Agentic traffic volume — AI bot hits to site (from server logs)

---

### GEO Audit Output Format: `/seo geo <url>`

```
GEO AUDIT — [domain] — [date]
══════════════════════════════════════════════════════

CONTENT STRUCTURE
─────────────────
Answer-first (first 40–60 words):   [✓ / ✗ / ⚠ Partial]
Fact density (stat per 150–200w):   [✓ / ✗]
Question-framed headings:           [score/10]
TL;DR / Quick Answer block:         [Present / Missing]
Semantic URL structure:             [✓ / ✗]
Content freshness (avg age):        [X days / updated X]

ENTITY & SCHEMA
────────────────
Organization + sameAs:              [✓ / ✗ | gaps listed]
Wikidata entry:                     [Present / Missing]
Wikipedia article:                  [Present / Missing / Stub]
Google Knowledge Panel:             [Claimed / Unclaimed / None]
Schema types detected:              [list]

AI CRAWLER ACCESS
──────────────────
Googlebot / Google-Extended:        [✓ Allowed / ✗ Blocked]
GPTBot / ChatGPT-User:              [✓ / ✗]
PerplexityBot:                      [✓ / ✗]
Meta-ExternalAgent:                 [✓ / ✗]
JavaScript rendering:               [Full / Partial / None]
IndexNow:                           [Active / Not configured]

OFF-SITE CITATION NETWORK
──────────────────────────
Tier 1 (Wikipedia, news, academic): [score/10 + gaps]
Tier 2 (Reddit, LinkedIn, G2):      [score/10 + gaps]
Earned media coverage:              [High / Medium / Low / None]

MCP / AGENTIC VISIBILITY
─────────────────────────
MCP server:                         [Present / Missing]
Tool registry listings:             [list or None]
OpenAPI / API docs:                 [Public / Private / None]
Documentation schema:               [Present / Missing]
Agentic traffic (server logs):      [X bot hits/month / Not tracked]

PLATFORM-SPECIFIC GAPS
────────────────────────
Google AI Overviews:                [Appearing / Not appearing / Unknown]
ChatGPT (web):                      [Appearing / Not appearing / Unknown]
Perplexity:                         [Appearing / Not appearing / Unknown]
Gemini:                             [Appearing / Not appearing / Unknown]
Copilot:                            [Appearing / Not appearing / Unknown]

TOP CITATION OPPORTUNITIES
───────────────────────────
[url] — [query target] — [estimated effort] — [platform priority]

PRIORITY FIXES (ordered by impact)
────────────────────────────────────
1. [fix] — [platform impact] — [effort: Low / Med / High]
2. ...
```

---

## Part 3 — AEO (Answer Engine Optimisation)

Run via `/seo aeo <url>`.

AEO targets AI assistants used in **conversational mode** — ChatGPT, Claude, Gemini, Copilot, Perplexity — where users ask questions and expect a recommended brand, product, or answer, rather than a list of links.

### Why AEO Differs from GEO and SEO

| | SEO | GEO | AEO |
|---|---|---|---|
| **Surface** | SERP blue links | AI-generated summaries with citations | Conversational AI recommendations |
| **User intent** | Find a resource | Get a quick answer | Get a specific recommendation |
| **Key signal** | Backlinks + content relevance | Structured, citable content | Brand authority + training data presence |
| **Measurement** | Rankings, clicks, impressions | Citation rate in AI Overviews | Share of voice in AI responses |
| **Tooling** | GSC, Ahrefs, Semrush | GSC AI Overviews report | Specialist AEO SaaS (see below) |

### The AEO Challenge: Raw LLMs vs. Specialised Tools

Using a general AI model (Claude, ChatGPT) to *audit your own AEO performance* has structural limitations:

**1. No Native Performance Tracking**
- General LLMs have no dashboards tracking how often your brand is cited
- Attribution between AI visibility and conversions is not available via base interfaces
- AI answers are probabilistic — the same query asked ten times may yield ten different source sets. Specialised AEO SaaS tools run bulk queries (hundreds to thousands) to compute a stable **share-of-voice (SOV)** metric

**2. Operational Limitations (Chat Amnesia)**
- Standard chat sessions lose context after a few exchanges; formatting rules and brand voice drift
- Manual copy-paste workflows do not scale to auditing hundreds of pages
- Specialised SaaS automates the **audit → fix → re-test loop** across entire content libraries

**3. Strategy and Data Hygiene**
- General LLMs optimise for clarity and query-matching, not brand authority signals
- Specialised AEO products include **Brand Radar** features: monitoring whether your brand name, logo description, tagline, and bio are consistently described across the web — a critical trust signal for AI models during training and RAG retrieval

**Practical guidance when using Claude for AEO (this skill):**
- Treat Claude's AEO analysis as a **strategy and content audit tool**, not a citation-tracking tool
- For SOV measurement, pair with a specialised AEO SaaS (Profound, Peec.ai, Semrush AI Toolkit, etc.)
- Run AEO prompts in fresh sessions to reduce chat-amnesia effects
- Use the `/seo aeo` command to get a structured, replicable audit format

### AEO Ranking Signals

AI assistants are trained on and retrieve from:

1. **Training data presence** — Is your brand, product, or expertise well-documented in sources that LLMs were trained on (Wikipedia, major publications, Reddit, industry forums, authoritative blogs)?
2. **RAG retrieval quality** — When AI systems use retrieval-augmented generation, they pull from live web results. SEO and GEO quality directly feeds AEO here
3. **Brand data hygiene** — Consistent Name, Address, Phone (NAP for local), consistent brand descriptions, founder names, product names, and differentiators across all web properties
4. **Topical authority** — LLMs favour sources that dominate a topic cluster, not single-page authorities
5. **Sentiment and framing** — Brands mentioned positively and specifically in context tend to be recommended more. Neutral or negative framing reduces recommendation frequency
6. **Citation network** — Being cited by other cited sources creates a reinforcing signal

### AEO Content Strategy

**Conversational query targeting:**
Map your content to the questions users ask AI assistants, not just keyword searches. These tend to be longer, more specific, and comparison-oriented:
- "What is the best [product category] for [use case]?"
- "How does [your brand] compare to [competitor]?"
- "Who should I use for [service]?"
- "Is [your brand] trustworthy / legit?"

**Content types that earn AI recommendations:**
- **Thought leadership** published on high-authority external sites (Forbes, industry journals, Medium partner)
- **Wikipedia** presence (neutral, verifiable, cited)
- **Podcast appearances** and interview transcripts (text versions index well)
- **Case studies** with specific, named outcomes
- **Product/service pages** with clear differentiators stated in plain language

**Brand data hygiene checklist:**

| Element | Standard to maintain |
|---|---|
| Brand name | Exact and consistent spelling everywhere |
| Tagline | Same across website, social, press kit, PR |
| Founder/exec names | Full name, title, linked to LinkedIn and bio pages |
| Product names | Consistent capitalisation and description |
| NAP (local) | Name, Address, Phone identical across GMB, directories, site |
| About page | Plain-language description of what you do, who you serve, founded when |
| Wikipedia | Create if notable; ensure accuracy; cite reliable sources |
| Press coverage | Actively pursue mentions in publications LLMs were trained on |
| Social profiles | Complete, verified, active — AI systems cross-reference these |

**Structured data for AEO:**
- `Organization` schema with `sameAs` pointing to all authoritative profiles (LinkedIn, Wikipedia, Wikidata, Crunchbase)
- `Person` schema for key executives and founders
- `Brand` schema on product pages
- `FAQPage` (restricted but still parsed by LLMs during retrieval)
- `Speakable` to mark recommended audio/voice content

### AEO Audit Command: `/seo aeo <url>`

Performs:

1. **Conversational query mapping** — generates 20 representative AI-assistant questions in your niche and maps existing content to answers
2. **Brand data hygiene scan** — checks consistency of brand name, tagline, founder info, product names across the site and known external profiles
3. **Topical authority gap analysis** — identifies topic clusters with no coverage (AEO blind spots)
4. **Schema coverage for AEO** — checks `Organization`, `Person`, `Brand`, `sameAs` completeness
5. **Sentiment analysis of brand framing** — flags pages where brand is described ambiguously or negatively
6. **Citation-worthiness score** — rates each major page on likelihood of being cited by an AI assistant

**Output format:**

```
AEO AUDIT — [domain] — [date]
────────────────────────────────
Conversational query coverage:  [X / 20 queries answered]
Brand data hygiene:             [score/10 + gaps listed]
Topical authority gaps:         [cluster list]
Schema (AEO):                   [Organization ✓/✗ | Person ✓/✗ | sameAs ✓/✗]
Citation-worthiness (top pages):
  [url] — [score/10] — [notes]
  ...
Priority fixes:                 [ordered action list]
Recommended external actions:   [PR targets, Wikipedia, podcast strategy]
```

### Brand Radar Command: `/seo brand-radar <brand>`

Audits brand consistency across:

- Own website (homepage, About, contact, product pages)
- Social profiles (LinkedIn, X/Twitter, Facebook, Instagram, YouTube)
- Business directories (Google Business Profile, Yelp, Apple Maps, Bing Places)
- Review platforms (G2, Capterra, Trustpilot, TripAdvisor — as applicable)
- Press/media mentions (top 20 by authority)
- Wikipedia / Wikidata presence

**Outputs:**
- Consistency score per element (name, tagline, description, logo reference)
- Discrepancy report with specific URLs and conflicting data
- Priority fix list ordered by AI-trust impact

---

## Part 3B — AgEO (Agentic Engine Optimisation) *(NEW — v3.0)*

Run via `/seo ageo <url>`.

AgEO is the discipline of making your website, service, or brand **discoverable, accessible, and usable by autonomous AI agents** that act on behalf of users — not just answer questions, but complete tasks. Where AEO asks "Will an AI cite me?", AgEO asks "Can an AI agent use me to get something done?"

AI agents such as OpenAI Operator, Google Gemini agentic mode (now in Google AI Mode), Claude's computer use, and Microsoft Copilot's agentic features now autonomously browse the web, fill forms, compare products, make bookings, and execute multi-step workflows. If your site is not agent-navigable, you are excluded from an increasingly large and commercially significant slice of digital interaction.

### Why AgEO Matters Now

- AI agents autonomously evaluate vendors, shortlist suppliers, compare products, and initiate purchases in procurement, finance, travel, healthcare, and retail — without a human doing manual research.
- Google's AI Mode (early 2026) is rolling out agentic capabilities including reservation and checkout completion — task-completion is becoming a core search surface.
- Zero-click search is evolving into zero-click purchase: the agent completes the transaction on the user's behalf.
- Brands with strong AEO/GEO scores that also expose agent-usable interfaces will dominate autonomous discovery.

### AgEO Signal Stack

| Signal | Description | Priority |
|---|---|---|
| Semantic navigation | Every key action (book, buy, sign up, compare) reachable via shallow URL structure and descriptive anchor text | High |
| ARIA accessibility | Interactive elements labelled with ARIA roles and descriptive text — agents use the accessibility tree, not visual layout | High |
| Structured data feeds | Machine-readable product, pricing, and availability data in JSON-LD or open feeds — agents prefer structure over scraping | High |
| `agents.txt` policy | Root-level file communicating permitted actions, auth requirements, and rate limits for AI agents (analogous to `robots.txt`) | Medium |
| Agent-description meta | `<meta name="agent-description">` or equivalent natural-language capability summary for agent discovery | Medium |
| Auth flow clarity | OAuth 2.0 / API key flows navigable by agents; no CAPTCHAs or bot-blocking that prevents legitimate agent access | High |
| Brand corpus presence | Service documented in AI training/retrieval corpora: press, Wikipedia, Wikidata, product databases, structured directories | High |
| `agent-task-map.json` | Optional: machine-readable map of available tasks, required inputs, and expected outputs — emerging convention | Low (emerging) |

### AgEO Content & Structural Tactics

**For agent parsing:**
- Ensure every key action is reachable within 2–3 clicks from the homepage — agents follow link graphs and require predictable navigation.
- Use descriptive, unique page titles and headings — agents select pages based on semantic relevance, not keyword density.
- Expose machine-readable product feeds, availability data, and pricing (JSON-LD, Atom feeds, or REST APIs with consistent schemas).
- Write clear natural-language descriptions of what each page or section does — agents match user intent to available capabilities using page text.

**For agent trust & safety:**
- Implement explicit machine-readable terms of service for agent interactions.
- Build rate limiting and abuse detection that distinguishes legitimate AI agents from malicious scrapers. Known legitimate AI agent user-agents: `GPTBot`, `ChatGPT-User`, `PerplexityBot`, `Google-Extended`, `ClaudeBot`, `Meta-ExternalAgent`, `OAI-SearchBot`.
- Provide clear, well-labelled authentication flows. Agents cannot solve CAPTCHAs.

**`agents.txt` template:**
```
# agents.txt — AI Agent Interaction Policy
# Place at: https://yourdomain.com/agents.txt

User-agent: *
Allow: /
Disallow: /admin/
Disallow: /checkout/     # Require authentication
Rate-limit: 60/minute

Agent-tasks: search, browse, compare, initiate-booking
Authentication: OAuth2.0 at /api/auth
Agent-contact: agents@yourdomain.com
```

### AgEO Audit Command: `/seo ageo <url>`

Performs:
1. **Navigation depth audit** — maps all key actions and checks reachability within 3 clicks
2. **Accessibility tree analysis** — checks ARIA labels on all interactive elements
3. **Structured data / feed availability** — checks for JSON-LD, product feeds, open APIs
4. **`agents.txt` presence and validity**
5. **Auth flow assessment** — flags CAPTCHAs, JS-only auth, and agent-blocking patterns
6. **AI crawler access** — cross-checks known agent bot user-agents against `robots.txt`
7. **Brand corpus coverage** — checks presence in Wikipedia, Wikidata, Crunchbase, and structured directories

**Output format:**
```
AgEO AUDIT — [domain] — [date]
═══════════════════════════════════════════════════
NAVIGATION & STRUCTURE
  Key actions reachable ≤3 clicks:     [X / Y actions]
  Semantic URL structure:               [✓ / ✗]
  ARIA label coverage:                  [score/10]

MACHINE-READABLE DATA
  JSON-LD product/service data:         [Present / Missing]
  Open API / structured feed:           [Present / Missing]
  agents.txt:                           [Present / Missing / Invalid]

AGENT TRUST
  Auth flow (agent-navigable):          [✓ / ✗ / ⚠ CAPTCHA detected]
  Rate limit policy:                    [Defined / Not defined]
  Terms for agent use:                  [Present / Missing]

AI CRAWLER ACCESS
  Known agent bots allowed:            [list of ✓/✗ per bot]

BRAND CORPUS COVERAGE
  Wikipedia:                            [Present / Missing]
  Wikidata:                             [Present / Missing]
  Crunchbase / industry directory:      [Present / Missing]

PRIORITY FIXES (ordered by AgEO impact)
  1. [fix] — [impact] — [effort]
  2. ...
```

---

## Part 3C — WebMCP: Web Model Context Protocol *(NEW — v3.0, Google/Microsoft, Feb 2026)*

Run via `/seo ageo --webmcp <url>`.

### What WebMCP Is

**WebMCP** is an open standard proposed by Google and Microsoft (early preview announced February 10, 2026) that allows websites to expose their functionality as structured, callable "tools" — JavaScript functions with natural-language descriptions and typed schemas — that AI agents and browser assistants can invoke directly.

WebMCP makes your website a client-side MCP server. Rather than an AI agent simulating clicks on DOM elements (fragile, slow), it calls your declared functions directly (fast, reliable, structured). It is the concrete infrastructure layer that makes AgEO possible at scale.

> **Status (February 2026):** Early preview program. Available for prototyping to program participants. Sign up at: https://developer.chrome.com/docs/ai/join-epp

### WebMCP vs. Other Agent Integration Approaches

| Approach | Speed | Reliability | Developer Control | Agent-Readiness |
|---|---|---|---|---|
| DOM scraping / click simulation | Slow | Fragile | None | Low |
| REST/GraphQL API (external) | Fast | High | High | Medium — requires agent-side integration |
| Backend MCP server | Fast | High | Full | High — but needs server infrastructure |
| **WebMCP (browser-native)** | **Fast** | **High** | **High** | **Native — designed for browser agents** |

### WebMCP APIs

WebMCP proposes two complementary APIs:

**Declarative API** — Standard, predictable actions defined directly in HTML. An agent can browse your catalog, filter results, and initiate a purchase using typed HTML attributes without executing arbitrary JavaScript. Best for: browsing, filtering, form submission, navigation.

```html
<!-- Expose a product search action declaratively -->
<form data-mcp-tool="searchProducts"
      data-mcp-description="Search the product catalog by keyword and category. Returns a list of matching products with name, price, SKU, and availability.">
  <input name="query"
         data-mcp-param-description="Search keywords (e.g. 'running shoes size 10')" />
  <select name="category"
          data-mcp-param-description="Product category filter">
    <option value="all">All categories</option>
    <option value="footwear">Footwear</option>
    <option value="apparel">Apparel</option>
  </select>
</form>
```

**Imperative API** — Complex, dynamic interactions exposed as JavaScript functions with natural-language descriptions and structured schemas. The agent calls your function directly. Best for: multi-step workflows, dynamic UI interactions, real-time data retrieval, stateful operations.

```javascript
// Register a callable tool for AI agents via WebMCP Imperative API
if (navigator.mcp) {
  navigator.mcp.registerTool({
    name: "getAvailableProducts",
    description: "Returns product listings with id, description, price, and photo URL. " +
                 "Optionally filter by EU dress size (2–14) or color. " +
                 "Use when the user asks to browse, find, or compare products.",
    parameters: {
      size: {
        type: "number",
        optional: true,
        description: "EU dress size (2–14). Omit to return all sizes."
      },
      color: {
        type: "string",
        optional: true,
        enum: ["Red", "Blue", "Green", "Yellow", "Black", "White"],
        description: "Filter by colour name."
      },
      maxResults: {
        type: "number",
        optional: true,
        description: "Maximum number of results to return. Default: 20."
      }
    },
    handler: async ({ size, color, maxResults = 20 }) => {
      const products = await fetchFromProductAPI({ size, color, maxResults });
      return products.map(p => ({
        id: p.sku,
        name: p.title,
        price: p.price_gbp,
        photoUrl: p.images[0],
        available: p.stock > 0
      }));
    }
  });
}
```

### WebMCP Tool Description Best Practices

The `description` field is the most important part of any WebMCP tool. It is the natural-language interface the AI agent reads to decide whether and how to call your function. Treat it like a mini landing page for the LLM.

| ✅ Good description | ❌ Bad description |
|---|---|
| "Search the product catalog by keyword and category. Returns name, price, SKU, availability. Use when the user wants to find or browse products." | "Product search" |
| "Create a new support ticket with a subject, description, and priority level. Use when the user reports an issue or wants to contact support." | "Opens a ticket" |
| "Get available appointment slots for a named service at a given location. Returns date, time, duration, and booking reference. Use when scheduling." | "Check calendar" |

**Tool description checklist:**
- [ ] States clearly what the tool does (action + data)
- [ ] Specifies what it returns (output format/fields)
- [ ] States when to use it (trigger conditions in plain English)
- [ ] Avoids jargon that the AI agent may not recognise
- [ ] Parameters have descriptive labels, types, and option sets

### WebMCP Use Cases by Industry

| Industry | Top WebMCP Tools to Expose |
|---|---|
| E-commerce | `searchProducts`, `addToCart`, `getProductDetails`, `initiateCheckout` |
| Travel | `searchFlights`, `filterResults`, `getHotelAvailability`, `beginBooking` |
| Customer Support | `createTicket`, `checkTicketStatus`, `searchKnowledgeBase` |
| SaaS / B2B | `requestDemo`, `configureTrialAccount`, `compareFeatures` |
| Healthcare | `getAvailableSlots`, `bookAppointment`, `findSpecialist` |
| Financial Services | `getAccountSummary`, `initiateTransfer`, `findProduct` |

### WebMCP Implementation Checklist

**Prerequisite:**
- [ ] Sign up for the WebMCP Early Preview Program: https://developer.chrome.com/docs/ai/join-epp

**Discovery & Documentation:**
- [ ] Publish `/.well-known/mcp-tools.json` listing all available WebMCP tools with names, descriptions, and endpoint types (emerging convention)
- [ ] Document tools in your developer docs with input/output schemas and usage examples
- [ ] Announce WebMCP support in your `agents.txt` file

**Implementation:**
- [ ] Identify top 3–5 user flows an agent would most need to complete (book, buy, search, support, compare)
- [ ] Implement Declarative API for standard form-based flows (search, filter, submit)
- [ ] Implement Imperative API for complex or multi-step interactions
- [ ] Write clear `description` strings for every tool (most important single step)
- [ ] Add fully typed parameter schemas with descriptions, types, ranges, and enum values
- [ ] Implement graceful fallback — if `navigator.mcp` is unavailable, standard HTML interaction must still work

**Testing:**
- [ ] Test tool invocation with a WebMCP-enabled browser agent (Chrome with Gemini/AI Mode)
- [ ] Validate parameter schemas resolve correctly
- [ ] Test error states — agents need informative errors, not generic 500s

**Analytics:**
- [ ] Instrument WebMCP tool invocations with analytics events to track agent usage
- [ ] Separate agent traffic from human traffic in GA4 with custom dimensions

### WebMCP SEO/AEO Implications

- WebMCP is to AgEO what Schema.org is to AEO — the structured data layer that makes machine interpretation reliable and fast.
- Early adopters gain first-mover advantage as Google AI Mode's agentic features scale. Sites with WebMCP tools will be preferred by agents over equivalent sites requiring DOM scraping.
- WebMCP signals to Google that a site is actively maintained and agent-forward — a freshness and technical authority signal.
- WebMCP may become a ranking or inclusion factor in Google's agentic search surfaces, analogous to how structured data affects rich result eligibility.

### WebMCP Audit Command: `/seo ageo --webmcp <url>`

Performs:
1. WebMCP Declarative API presence check — are HTML elements annotated with `data-mcp-tool` and `data-mcp-description`?
2. WebMCP Imperative API presence check — does the page call `navigator.mcp.registerTool()`?
3. Tool description quality score — evaluates specificity, clarity, trigger language, and return documentation
4. Parameter schema completeness — checks types, descriptions, enums for all parameters
5. `/.well-known/mcp-tools.json` presence
6. `agents.txt` WebMCP entry
7. Graceful fallback check — verifies standard HTML flows still work without WebMCP

**Output format:**
```
WebMCP AUDIT — [domain] — [date]
═══════════════════════════════════════════════════════
WebMCP Status:  [Early Preview Available / Not Implemented]

DECLARATIVE API
  Tools declared via data-mcp-tool:       [X tools found / None]
  Description quality (avg):              [score/10]
  Parameter schemas complete:             [✓ / ⚠ Missing on X tools]

IMPERATIVE API
  navigator.mcp.registerTool() calls:     [X tools found / None]
  Description quality (avg):              [score/10]
  Handler error handling:                 [Present / Missing]

DISCOVERY
  /.well-known/mcp-tools.json:            [Present / Missing]
  agents.txt WebMCP entry:                [Present / Missing]
  Developer docs with tool schemas:       [Present / Missing]

TOOL INVENTORY
  [tool name] — [description quality: X/10] — [parameters: ✓/⚠] — [returns documented: ✓/✗]

PRIORITY FIXES (ordered by WebMCP impact)
  1. [fix] — [impact] — [effort]
  2. ...

EARLY PREVIEW NOTE
  WebMCP is currently in early preview (Feb 2026). Sign up at:
  https://developer.chrome.com/docs/ai/join-epp
```

---



### `/seo audit <url>`

Runs all active sub-skills in parallel via subagents:

| Subagent | Focus |
|---|---|
| `seo-technical` | Technical SEO (8 categories) |
| `seo-content` | E-E-A-T and content quality |
| `seo-schema` | Schema detection, validation, generation |
| `seo-sitemap` | Sitemap audit |
| `seo-performance` | Core Web Vitals and speed |
| `seo-visual` | Image optimisation |
| `seo-geo` | GEO — content structure, crawler access, off-site citations, platform-specific gaps |
| `seo-geo-mcp` | MCP / agentic tool visibility — server presence, tool descriptions, registry listings |
| `seo-aeo` | AEO / brand-radar readiness |
| `seo-ageo` | **NEW** AgEO — agent discoverability, navigation, accessibility tree, agents.txt |
| `seo-webmcp` | **NEW** WebMCP — tool declaration audit, description quality, tool inventory |
| `seo-cite-check` | **NEW** Citation qualification validation per page |
| `seo-grounding` | **NEW** Grounding Page detection and Standard v1.5 compliance |

Results are aggregated into a single prioritised report with a weighted overall score.

### Business Type Detection

The orchestrator detects the site type and adjusts priorities:

| Type | Auto-detected signals | Adjusted priorities |
|---|---|---|
| SaaS | `.io` domain, pricing page, free trial CTA | Schema: `WebApplication`; GEO: comparison pages |
| Local | NAP on page, GMB embed, service area | Schema: `LocalBusiness`; AEO: "near me" queries |
| Ecommerce | Product pages, cart, structured pricing | Schema: `Product`+`Offer`; GEO: shopping AI |
| Publisher | Blog, author pages, ad units | E-E-A-T depth; GEO: news AI surfaces |
| Agency | Service pages, case studies, team | AEO: recommendation queries; brand data hygiene |

---

## Part 5 — MCP Integrations

There are two distinct ways MCP is relevant to this skill:

**A) MCP servers that feed live data INTO audits** (used internally by this skill):

| MCP Server | Data available |
|---|---|
| `@ahrefs/mcp` | Backlinks, DR, keyword rankings, site audit |
| Semrush MCP | Organic traffic, keyword gap, domain overview |
| Google Search Console (community) | Clicks, impressions, CTR, position, AI Overview appearances |
| PageSpeed Insights (community) | CWV scores, field data, lab data |
| DataForSEO (community) | SERP features, rank tracking, schema validation |
| Profound MCP | AI visibility data — brand citations across 10+ AI engines, agent analytics |

Enable via Claude Code MCP settings. When active, audit commands pull live data rather than relying solely on static analysis.

**B) MCP server presence as a GEO signal** (assessed during `/seo geo --mcp`):

Whether the *audited brand* has its own publicly available MCP server is a direct GEO signal for agentic visibility. See GEO Pillar 6 for full optimisation guidance.

---

## Part 6 — Architecture

```
# ── SKILLS (one sub-directory per command) ───────────────────────────────────
~/.claude/skills/seo/SKILL.md              ← Main orchestrator + routing table
~/.claude/skills/seo-audit/SKILL.md        ← Full audit coordination
~/.claude/skills/seo-content/SKILL.md      ← E-E-A-T analysis
~/.claude/skills/seo-competitor-pages/SKILL.md
~/.claude/skills/seo-geo/SKILL.md          ← GEO: content, crawlers, platforms
~/.claude/skills/seo-geo-mcp/SKILL.md      ← GEO: MCP / agentic tool visibility
~/.claude/skills/seo-aeo/SKILL.md          ← AEO analysis + brand-radar
~/.claude/skills/seo-cite-check/SKILL.md   ← Citation qualification engine
~/.claude/skills/seo-answer-pack/SKILL.md  ← AI answer bundle generator
~/.claude/skills/seo-grounding/SKILL.md    ← SOURCE OF TRUTH for Grounding Page Standard v1.5
~/.claude/skills/seo-profile/SKILL.md      ← Profile loader + generic-output blocker
~/.claude/skills/seo-ageo/SKILL.md         ← AgEO: agentic discoverability, agents.txt, ARIA, feeds ← NEW v3.0
~/.claude/skills/seo-webmcp/SKILL.md       ← WebMCP: tool declaration, description quality, implementation ← NEW v3.0
~/.claude/skills/seo-hreflang/SKILL.md
~/.claude/skills/seo-images/SKILL.md
~/.claude/skills/seo-page/SKILL.md
~/.claude/skills/seo-plan/SKILL.md
~/.claude/skills/seo-programmatic/SKILL.md
~/.claude/skills/seo-schema/SKILL.md
~/.claude/skills/seo-sitemap/SKILL.md
~/.claude/skills/seo-technical/SKILL.md

# ── AGENTS (parallel execution during /seo audit) ───────────────────────────
~/.claude/agents/seo-technical.md
~/.claude/agents/seo-content.md
~/.claude/agents/seo-schema.md
~/.claude/agents/seo-sitemap.md
~/.claude/agents/seo-performance.md
~/.claude/agents/seo-visual.md
~/.claude/agents/seo-geo.md
~/.claude/agents/seo-geo-mcp.md
~/.claude/agents/seo-aeo.md
~/.claude/agents/seo-cite-check.md
~/.claude/agents/seo-grounding.md
~/.claude/agents/seo-ageo.md          # NEW v3.0
~/.claude/agents/seo-webmcp.md        # NEW v3.0

# ── PROJECT FILES (per project, not global) ──────────────────────────────────
./project_profile.yml                         ← CANONICAL profile (project root only)

# ── REFERENCE / EXAMPLE (inside skill installation, never in project) ─────────
~/.claude/skills/seo/configs/project_profile.example.yml  ← Reference template; never loaded by orchestrator
```

### Deduplicate Rule: Single Source of Truth

The following boundary is enforced across all sub-skills:

| Concern | Owner | All other skills do |
|---|---|---|
| Grounding Page spec, generation, audit | `seo-grounding` | Reference `seo-grounding`; never duplicate its logic |
| Profile loading, validation, blocker | `seo-profile` | Call profile loader; never re-implement reading |
| Citation scoring model | `seo-cite-check` | Reference scores; never re-implement the model |
| GEO platform-specific rules | `seo-geo` | `seo-aeo` borrows; never duplicates |
| AgEO audit logic | `seo-ageo` | `seo-geo-mcp` may reference agent signals; never re-implements AgEO audit |
| WebMCP implementation guidance | `seo-webmcp` | Other sub-skills may reference WebMCP presence as a signal only |

### Orchestrator Routing Table

The main `~/.claude/skills/seo/SKILL.md` maps every `/seo <command>` to its sub-skill:

```
ROUTE TABLE — seo orchestrator
════════════════════════════════════════════════════════════════════
STEP 0 (always first): load seo-profile → apply profile or generic mode
────────────────────────────────────────────────────────────────────
/seo audit <url>           → seo-audit (spawns all agents in parallel)
/seo page <url>            → seo-page
/seo sitemap [url|generate]→ seo-sitemap
/seo schema <url>          → seo-schema
/seo images <url>          → seo-images
/seo technical <url>       → seo-technical
/seo content <url>         → seo-content
/seo geo <url>             → seo-geo
/seo geo --mcp <url>       → seo-geo-mcp
/seo aeo <url>             → seo-aeo
/seo brand-radar <brand>   → seo-aeo (brand-radar module)
/seo ageo <url>            → seo-ageo                          # NEW v3.0
/seo ageo --webmcp <url>   → seo-webmcp                       # NEW v3.0
/seo cite-check <url>      → seo-cite-check
/seo answer-pack <topic>   → seo-answer-pack
/seo grounding-page <x>    → seo-grounding
/seo profile init          → seo-profile (init mode)
/seo profile show          → seo-profile (show mode)
/seo plan <type>           → seo-plan
/seo programmatic <url>    → seo-programmatic
/seo competitor-pages <url>→ seo-competitor-pages
/seo hreflang <url>        → seo-hreflang
────────────────────────────────────────────────────────────────────
STEP LAST (always): apply generic-output blocker (seo-profile) if profile loaded
════════════════════════════════════════════════════════════════════
```

---

## Part 7 — Quick Reference: SEO vs GEO vs AEO Tactics

| Tactic | SEO | GEO | GEO–MCP | AEO | AgEO | WebMCP |
|---|---|---|---|---|---|---|
| Keyword research | ✅ Core | ✅ (question framing) | ⬜ N/A | ✅ (conversational queries) | ⬜ N/A | ⬜ N/A |
| E-E-A-T signals | ✅ | ✅ | ⬜ Indirect | ✅ | ⬜ Indirect | ⬜ N/A |
| Schema markup | ✅ | ✅ | ✅ (`SoftwareApplication`) | ✅ (`sameAs`, `Person`) | ✅ (JSON-LD feeds) | ✅ (tool schemas) |
| Answer-first structure | ⬜ Helpful | ✅ Core | ✅ (tool descriptions) | ✅ Core | ⬜ Helpful | ✅ (tool descriptions) |
| Brand data hygiene | ⬜ Helpful | ✅ | ⬜ Helpful | ✅ Core | ✅ Core | ⬜ Helpful |
| External PR / citations | ✅ (links) | ✅ (citations) | ⬜ Indirect | ✅ (training data) | ✅ (corpus coverage) | ⬜ N/A |
| Wikipedia / Wikidata | ⬜ Nice | ✅ Core | ⬜ Helpful | ✅ Core | ✅ Core | ⬜ Helpful |
| Technical speed | ✅ Core | ✅ | ⬜ Indirect | ⬜ Indirect | ⬜ Indirect | ⬜ Indirect |
| Share-of-voice tracking | ✅ (rankings) | ⚠️ Needs SaaS tool | ⚠️ Server log analysis | ⚠️ Needs SaaS tool | ⚠️ Agent log analysis | ⚠️ Tool invocation analytics |
| Structured FAQs | ✅ | ✅ | ⬜ N/A | ✅ | ⬜ N/A | ⬜ N/A |
| Topical authority clusters | ✅ | ✅ | ⬜ N/A | ✅ Core | ⬜ N/A | ⬜ N/A |
| Reddit / community presence | ⬜ Helpful | ✅ Core | ⬜ N/A | ✅ | ⬜ Helpful | ⬜ N/A |
| AI crawler access (robots.txt) | ⬜ N/A | ✅ Core | ✅ Core | ⬜ Indirect | ✅ Core | ⬜ Indirect |
| MCP server / tool registry | ⬜ N/A | ⬜ N/A | ✅ Core | ⬜ N/A | ✅ Core | ⬜ N/A |
| OpenAPI documentation | ⬜ Nice | ⬜ Nice | ✅ Core | ⬜ N/A | ✅ Core | ✅ Core |
| Tool description quality | ⬜ N/A | ⬜ N/A | ✅ Core | ⬜ N/A | ✅ Core | ✅ Core |
| YouTube / video transcripts | ⬜ Helpful | ✅ (Gemini) | ⬜ N/A | ⬜ Helpful | ⬜ N/A | ⬜ N/A |
| IndexNow / freshness signals | ⬜ Helpful | ✅ | ✅ | ⬜ Indirect | ⬜ Indirect | ⬜ N/A |
| **Grounding Page (v1.5)** | ⬜ Helpful | ✅ Core | ✅ | ✅ Core | ✅ Core | ⬜ Helpful |
| **Cite-Check score ≥ 70** | ⬜ N/A | ✅ Core | ⬜ N/A | ✅ Core | ⬜ N/A | ⬜ N/A |
| **project_profile.yml** | ✅ Personalises | ✅ Personalises | ✅ Personalises | ✅ Personalises | ✅ Personalises | ✅ Personalises |
| **Answer-Pack assets** | ⬜ Helpful | ✅ Core | ⬜ N/A | ✅ Core | ⬜ N/A | ⬜ N/A |
| **agents.txt policy** | ⬜ N/A | ⬜ N/A | ⬜ N/A | ⬜ N/A | ✅ Core | ✅ Core |
| **ARIA accessibility tree** | ⬜ Helpful | ⬜ N/A | ⬜ N/A | ⬜ N/A | ✅ Core | ✅ Core |
| **WebMCP Declarative API** | ⬜ N/A | ⬜ N/A | ⬜ N/A | ⬜ N/A | ✅ Core | ✅ Core |
| **WebMCP Imperative API** | ⬜ N/A | ⬜ N/A | ⬜ N/A | ⬜ N/A | ✅ Core | ✅ Core |
| **/.well-known/mcp-tools.json** | ⬜ N/A | ⬜ N/A | ⬜ N/A | ⬜ N/A | ✅ Emerging | ✅ Core |

---

## Part 8 — Schema Templates Quick Reference

See `schema/templates.json` for ready-to-use JSON-LD snippets. Priority types for AEO:

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Your Brand",
  "url": "https://yourdomain.com",
  "logo": "https://yourdomain.com/logo.png",
  "description": "One clear sentence describing what you do.",
  "foundingDate": "2020",
  "sameAs": [
    "https://en.wikipedia.org/wiki/Your_Brand",
    "https://www.linkedin.com/company/your-brand",
    "https://twitter.com/yourbrand",
    "https://www.wikidata.org/wiki/Q000000"
  ],
  "founder": {
    "@type": "Person",
    "name": "Founder Name",
    "url": "https://yourdomain.com/about/founder",
    "sameAs": "https://www.linkedin.com/in/foundername"
  }
}
```

---

## Part 9 — Profile System (`project_profile.yml`)

### Single Canonical Profile Location

```
./project_profile.yml                                      ← THE canonical profile (project root, one per project)
~/.claude/skills/seo/configs/project_profile.example.yml  ← Shipped as reference only; never auto-loaded
```

**Rule:** There is exactly one profile schema. `project_profile.yml` in the project root is the only file the orchestrator ever reads. The `configs/` directory ships a copy named `project_profile.example.yml` so developers can see the full schema with comments — but the orchestrator never reads anything from `configs/`. If both files existed with conflicting values, only `project_profile.yml` applies.

The profile system lives in `seo-profile/SKILL.md`. All other sub-skills call the profile loader defined there; they never implement their own profile reading logic.

Every project that uses this skill can define a `project_profile.yml` file in the project root. When present, the orchestrator reads this file **before executing any command** (Step 0 in the routing table) and uses it to:

- Personalise all outputs to the brand, industry, audience, and tone defined in the profile
- Activate only the relevant sub-skill modules for the business type
- Override generic defaults with project-specific rules
- Block generic, template-like outputs that do not match the profile context (see Part 10)

This is the mechanism that separates a generic SEO audit from a brand-aware, context-specific one. Without a profile, Claude produces valid but generic outputs. With a profile, every output is grounded in the brand's actual positioning, audience, and competitive landscape.

### Creating a Profile: `/seo profile init`

Launches an interactive setup dialogue. Claude asks a series of structured questions and writes `project_profile.yml` to the project root. Alternatively, create or edit the file manually using the schema below.

### Profile Schema (`project_profile.yml`)

```yaml
# project_profile.yml — SEO · AEO · GEO Skill Profile (Standard v1.5)
# Place in project root. Claude reads this before every /seo command.

# ── BRAND IDENTITY ──────────────────────────────────────────────────────────
brand:
  name: "Acme Corp"                        # Exact brand name (used in all outputs)
  tagline: "The fastest way to do X"       # Official tagline (consistency check target)
  description: >                           # One-paragraph plain-English brand description
    Acme Corp is a B2B SaaS platform that helps mid-market logistics companies
    reduce freight costs by 30% through AI-powered route optimisation.
  founding_year: 2019
  hq_country: "DE"                         # ISO 3166-1 Alpha-2
  languages: ["en", "de"]                  # Content languages (drives hreflang checks)

# ── BUSINESS TYPE ────────────────────────────────────────────────────────────
business:
  type: saas                               # saas | local | ecommerce | publisher | agency | marketplace
  model: b2b                              # b2b | b2c | b2b2c | marketplace
  industry: "logistics-tech"              # Freeform; used to calibrate E-E-A-T and competitor benchmarks
  stage: growth                           # seed | growth | scale | enterprise

# ── TARGET AUDIENCE ──────────────────────────────────────────────────────────
audience:
  primary_persona: "VP of Operations at a logistics SME"
  technical_level: intermediate           # beginner | intermediate | expert
  decision_stage_focus: consideration     # awareness | consideration | decision | retention
  geography: ["DACH", "Benelux"]

# ── COMPETITIVE LANDSCAPE ────────────────────────────────────────────────────
competitors:
  primary:
    - name: "CompetitorA"
      url: "https://competitora.com"
    - name: "CompetitorB"
      url: "https://competitorb.com"
  differentiation: >
    Unlike CompetitorA (which focuses on large enterprise), Acme Corp targets
    mid-market (50–500 employees) with a self-serve onboarding model and
    transparent per-shipment pricing.

# ── SEO CONFIGURATION ────────────────────────────────────────────────────────
seo:
  primary_domain: "https://acmecorp.com"
  cms: "webflow"                           # wordpress | webflow | next.js | hugo | shopify | custom
  primary_keywords:
    - "freight cost optimisation"
    - "AI route planning logistics"
    - "logistics software SME"
  content_cluster_topics:
    - "freight rate benchmarking"
    - "logistics KPIs"
    - "supply chain visibility"
  excluded_urls:                           # Never audit or optimise these paths
    - "/internal/"
    - "/staging/"

# ── GEO CONFIGURATION ────────────────────────────────────────────────────────
geo:
  target_platforms:                        # Which AI platforms to prioritise
    - chatgpt
    - perplexity
    - gemini
    - google_ai_overviews
  allow_ai_crawlers: true                  # If false, generates robots.txt blocks instead
  mcp_server_url: ""                       # Leave blank if no MCP server exists yet
  grounding_page_path: "/about/ai-grounding"  # Path where Grounding Page lives

# ── AgEO CONFIGURATION ───────────────────────────────────────────────────────
ageo:
  agents_txt_present: false               # Set true once agents.txt is deployed at root
  webmcp_enrolled: false                  # Set true once signed up for WebMCP Early Preview
  webmcp_tools: []                        # List tool names once implemented, e.g. [searchProducts, beginBooking]
  top_agent_tasks:                        # Key tasks an agent should be able to complete on the site
    - "search products"
    - "initiate booking"
    - "contact support"
  agent_auth_type: "none"                # none | oauth2 | api-key | session

# ── AEO CONFIGURATION ────────────────────────────────────────────────────────
aeo:
  priority_queries:                        # Top conversational queries to optimise for
    - "What is the best logistics software for mid-market companies?"
    - "How does Acme Corp compare to CompetitorA?"
    - "Is Acme Corp legit?"
  wikipedia_url: ""                        # Leave blank if no Wikipedia article exists
  wikidata_id: ""                          # e.g. Q12345678

# ── CONTENT & TONE ───────────────────────────────────────────────────────────
content:
  tone: professional-but-approachable      # formal | professional-but-approachable | conversational | technical
  reading_level: intermediate              # Calibrates Flesch-Kincaid targets
  avoid_phrases:                           # Phrases to flag in content audits
    - "cutting-edge"
    - "game-changing"
    - "synergy"
  required_disclaimers: []                 # Legal/compliance disclaimers to check for

# ── OUTPUT PREFERENCES ───────────────────────────────────────────────────────
output:
  default_format: markdown                 # markdown | json | plain
  include_code_snippets: true             # Include schema JSON-LD, robots.txt, etc.
  citation_style: inline                   # inline | footnote
  max_priority_items: 10                   # Cap on action items per audit section
  block_generic_outputs: true             # Activates the Generic Output Blocker (Part 10)
```

### Profile Loading Behaviour

| State | Behaviour | Console notice |
|---|---|---|
| Found in `./project_profile.yml` | Loads and applies all values | `[Profile: acmecorp — v1.5 — loaded]` |
| Found in parent directory (≤3 levels up) | Loads from that path | `[Profile: ../project_profile.yml — v1.5 — loaded]` |
| Not found anywhere | Generic mode, all defaults apply | `[No profile — generic mode. Run /seo profile init to create one.]` |
| Invalid YAML | Parse error, falls back to generic | `[Profile parse error: <message> — falling back to generic mode]` |
| `--no-profile` flag | Forces generic mode regardless | `[Profile suppressed by --no-profile flag]` |

Profile values always override command defaults. There is no merging of multiple profile files — first file found wins, full stop.

### Displaying the Active Profile: `/seo profile show`

```
ACTIVE PROFILE — acmecorp — Standard v1.5
══════════════════════════════════════════
Brand:          Acme Corp ("The fastest way to do X")
Type:           SaaS · B2B · Growth stage
Industry:       Logistics-tech
Domain:         https://acmecorp.com
Languages:      en, de
CMS:            Webflow
GEO platforms:  ChatGPT, Perplexity, Gemini, Google AI Overviews
Grounding page: /about/ai-grounding
MCP server:     ⚠️  Not configured — run /seo geo --mcp to generate setup guide
Wikipedia:      ⚠️  Not configured — high AEO impact (add aeo.wikipedia_url)
Wikidata:       ⚠️  Not configured — high GEO entity impact (add aeo.wikidata_id)
agents.txt:     ⚠️  Not deployed — high AgEO impact (set ageo.agents_txt_present: true when live)
WebMCP:         ⚠️  Not enrolled — sign up at developer.chrome.com/docs/ai/join-epp (set ageo.webmcp_enrolled: true)
WebMCP tools:   None configured yet — add to ageo.webmcp_tools once implemented

Profile file:   ./project_profile.yml
Example file:   ~/.claude/skills/seo/configs/project_profile.example.yml
```

---

## Part 10 — Generic Output Blocker

When `block_generic_outputs: true` is set in the profile (or when a profile is loaded and the flag is not explicitly disabled), Claude applies a **pre-output validation gate** before delivering any audit result, generated content, or recommendation.

### What the Blocker Checks

Before outputting any substantive content, Claude internally validates:

| Check | Pass condition | Fail action |
|---|---|---|
| Brand name grounding | Brand name appears at least once in the output | Rewrite to include brand context |
| Industry specificity | At least one industry-specific term from the profile is present | Rewrite with industry context |
| Audience calibration | Content is appropriate for the defined `technical_level` and `decision_stage_focus` | Adjust complexity and framing |
| Competitor awareness | Recommendations do not apply equally well to any competitor | Add differentiating context |
| Avoid-phrases check | None of the `avoid_phrases` from the profile appear in output | Remove or replace flagged phrases |
| Template pattern detection | Output does not read as a fill-in-the-blank template | Rewrite with specific examples |
| Actionability | Every recommendation includes a specific next step (not "consider improving X") | Add concrete implementation guidance |

### Template Pattern Detection Rules

Claude rejects outputs that contain any of the following generic patterns and rewrites them:

- Placeholder brackets: `[your brand]`, `[insert keyword]`, `[company name]`
- Vague superlatives without evidence: "world-class", "best-in-class" with no cited benchmark
- Generic audit boilerplate: "Your website needs to be optimised for mobile" without specific findings from the actual site
- Unanchored statistics: "Studies show that X% of users..." without a cited source
- Platform-agnostic advice: Recommendations that do not reference the target GEO platforms from the profile

### Override

To run in generic mode even with a profile loaded (useful for benchmarking or quick checks):

```bash
/seo audit https://example.com --no-profile
```

---

## Part 11 — Cite-Check (`/seo cite-check <url>`)

The Cite-Check command evaluates whether a specific page meets the citation criteria used by major AI retrieval systems. It is a focused, single-page tool that answers one question: **"Would an AI assistant cite this page when answering a relevant query?"**

Unlike `/seo page` (which focuses on traditional on-page SEO) or `/seo geo` (which audits the whole site), Cite-Check produces a binary PASS/FAIL verdict per AI platform with specific, fixable failure reasons.

### How Cite-Check Works

Claude evaluates the page against 7 citation criteria, weighted by platform. Each platform has different thresholds:

| Criterion | Weight (ChatGPT) | Weight (Perplexity) | Weight (Gemini) | Weight (AI Overviews) |
|---|---|---|---|---|
| Answer-first structure (answer in first 60 words) | 25% | 20% | 20% | 20% |
| Factual claim density (verifiable stat per 150–200 words) | 20% | 25% | 15% | 20% |
| Source citation quality (inline links to primary sources) | 15% | 20% | 15% | 10% |
| Schema markup coverage | 10% | 5% | 20% | 20% |
| E-E-A-T signals (author, date, credentials) | 15% | 10% | 15% | 15% |
| Freshness (content updated within 6 months) | 10% | 15% | 10% | 10% |
| AI crawler access (page not blocked) | 5% | 5% | 5% | 5% |

A page passes a platform if its weighted score ≥ 70%.

### Cite-Check Output Format

```
CITE-CHECK — https://example.com/page — [date]
══════════════════════════════════════════════════

VERDICT BY PLATFORM
───────────────────
ChatGPT (web):       ✅ PASS  [82/100]
Perplexity:          ⚠️ MARGINAL [68/100] — needs fresher data and more inline citations
Gemini:              ✅ PASS  [74/100]
Google AI Overviews: ❌ FAIL  [51/100] — no schema, answer not in first 60 words

CRITERION BREAKDOWN
────────────────────
Answer-first structure:     ❌ Answer appears at word 210 — move to first 60 words
                               SUGGESTED REWRITE: [Claude drafts a 60-word answer-first opening]
Factual claim density:      ✅ 1 statistic per 180 words — adequate
Source citation quality:    ⚠️ 2 inline citations found — target ≥ 5 for Perplexity
Schema markup:              ❌ No schema detected — add Article + Organization JSON-LD
                               SUGGESTED SCHEMA: [Claude outputs the exact JSON-LD block]
E-E-A-T signals:            ⚠️ No author byline, no date visible
Freshness:                  ✅ Last modified 2 months ago
AI crawler access:          ✅ All major bots allowed

PRIORITY FIXES (ordered by citation impact)
────────────────────────────────────────────
1. Move answer to first 60 words [+18 pts across all platforms]
   → Suggested rewrite provided above
2. Add Article + Organization schema [+15 pts for Gemini, +12 pts for AI Overviews]
   → Schema JSON-LD provided above
3. Add author byline with credentials and visible publish date [+8 pts average]
4. Add 3 more inline citations to primary sources [+7 pts for Perplexity]
5. Update content — add one fresh statistic from 2025 or 2026 [+5 pts for Perplexity]

ESTIMATED POST-FIX SCORES
──────────────────────────
ChatGPT:             82 → 95 ✅
Perplexity:          68 → 88 ✅
Gemini:              74 → 91 ✅
Google AI Overviews: 51 → 86 ✅
```

### Batch Cite-Check

Run across multiple pages simultaneously:

```bash
/seo cite-check https://example.com --batch   # Checks all pages in sitemap
/seo cite-check https://example.com --top 20  # Checks top 20 pages by organic traffic (requires GSC MCP)
```

Batch outputs a sortable table of all pages with their platform scores and a prioritised fix list ordered by total citation impact across the site.

---

## Part 12 — Answer-Pack (`/seo answer-pack <topic>`)

The Answer-Pack command generates a **complete, ready-to-publish content bundle** designed to maximise AI citation probability for a specific topic. Rather than auditing existing content, it creates new content structured from the ground up for AI retrieval.

An answer-pack is not a blog post. It is a modular collection of content assets, each optimised for a different AI citation surface, that together establish comprehensive topic authority.

### Answer-Pack Bundle Contents

Running `/seo answer-pack "freight cost optimisation"` produces:

**Asset 1: Grounding Definition Block** (40–60 words)
A single, perfectly structured paragraph that directly defines or answers the topic. This is the asset most likely to be quoted verbatim in AI answers. Written in plain declarative English; no marketing language.

```
GROUNDING DEFINITION — freight cost optimisation
─────────────────────────────────────────────────
Freight cost optimisation is the process of reducing the total expenditure
a business incurs when transporting goods. It encompasses carrier negotiation,
route consolidation, load optimisation, and modal shift strategies. Companies
that systematically apply freight cost optimisation reduce logistics spend by
15–30% within 12 months, according to Gartner (2024).
```

**Asset 2: FAQ Cluster** (5–10 questions)
Covers the full intent spectrum — definitional, comparative, evaluative, and transactional — using the conversational phrasing that AI users actually ask.

```
Q: What is freight cost optimisation?
A: [Answer ≤ 80 words]

Q: How does freight cost optimisation work?
A: [Answer ≤ 80 words]

Q: What tools are used for freight cost optimisation?
A: [Answer ≤ 80 words, includes brand if profile is loaded]

Q: How much can freight cost optimisation save?
A: [Stat-grounded answer]

Q: What is the difference between freight cost optimisation and TMS?
A: [Comparative answer]
```

**Asset 3: Comparison Table**
A structured comparison of approaches, vendors, or methods — the content type with the highest AI citation rate (32.5% of AI citations originate from comparison content).

**Asset 4: Stat Block**
5–8 cited statistics about the topic from primary sources (Gartner, McKinsey, industry associations, government data). This is the highest-value single asset for Perplexity and ChatGPT citations.

**Asset 5: Schema JSON-LD Block**
Ready-to-paste structured data for the page: `Article` + `Organization` + `BreadcrumbList` + relevant topic-specific types. If the profile has brand data, fields are pre-populated.

**Asset 6: Answer-Pack Page Template**
An HTML outline showing exactly how to assemble all assets into a single page, with the Grounding Definition at the top, FAQ cluster following, stat block embedded, and schema in `<head>`.

**Asset 7: Distribution Checklist**
Where to publish or syndicate each asset to build the off-site citation network (Reddit threads, LinkedIn articles, Q&A answers on Quora, etc.) with specific subreddit/community targets based on the industry in the profile.

### Answer-Pack Output Options

```bash
/seo answer-pack "freight cost optimisation"           # Full bundle, markdown
/seo answer-pack "freight cost optimisation" --json    # Machine-readable JSON
/seo answer-pack "freight cost optimisation" --grounding-only  # Just Asset 1
/seo answer-pack "freight cost optimisation" --faq-only        # Just Asset 2
```

---

## Part 13 — Grounding Page Standard v1.5 (Source of Truth)

**Ownership:** `seo-grounding/SKILL.md` owns all Grounding Page logic. This Part is the specification. No other sub-skill may re-implement generation or auditing of Grounding Pages — they may only reference the grounding page as a signal.

**Boundary with `/seo geo`:** The GEO sub-skill checks three Grounding Page signals as part of its audit — existence, crawlability, and `last-verified` date — but does not generate or audit the page's content. All generation and Standard v1.5 compliance checking is delegated to `seo-grounding`. The GEO audit output includes exactly this block:

```
GROUNDING PAGE SIGNAL (GEO)
────────────────────────────
Grounding Page present:    [✅ Yes — /about/ai-grounding / ❌ No]
AI-crawlable:              [✅ / ❌]
Last-verified date:        [date / Not set]
Standard v1.5 compliance:  [score/100 — from seo-grounding cache / Not audited yet]
Action:                    [Run /seo grounding-page <url> for full audit and fix list]
```

That is the totality of what `/seo geo` does with the Grounding Page. Everything else is in this Part and `seo-grounding`.

Run via `/seo grounding-page <topic|url>`.

A **Grounding Page** is a dedicated, AI-optimised page on your domain whose sole purpose is to establish clear, machine-readable facts about your brand, product, or topic for AI retrieval systems. It is the most impactful single page you can create for AEO and GEO. Standard v1.5 defines the exact structure, schema requirements, and content rules for a compliant Grounding Page.

### What a Grounding Page Is Not

- Not a landing page (no conversion CTAs)
- Not a press release (no promotional language)
- Not an About page (About pages are human-first; Grounding Pages are AI-first)
- Not a Wikipedia article (it is brand-owned, but must follow Wikipedia-style neutrality and verifiability)

### Grounding Page Standard v1.5 — Structure

A compliant Grounding Page must contain all of the following sections in this order:

**Section 1: Entity Definition Block** (required, 40–80 words)
Plain declarative sentence(s) defining what the brand/product/topic is. No adjectives of quality ("leading", "innovative"). No claims without evidence.

```
[Brand Name] is a [business type] that [primary function]. It was founded in [year]
by [founder name(s)] and is headquartered in [city, country]. As of [date], it serves
[customer count or ARR range] customers in [geographies].
```

**Section 2: Canonical Facts Table** (required)
A machine-readable table of verifiable facts with sources. Each fact must be independently verifiable.

| Fact | Value | Source |
|---|---|---|
| Founded | 2019 | Companies House / Crunchbase |
| HQ | Berlin, Germany | Official website |
| Employees | 80–120 | LinkedIn company page |
| Primary product | [Product Name] | Product page |
| Pricing model | Per-shipment SaaS | Pricing page |
| Key customers (public) | [Names if disclosed] | Case studies |
| Funding | Series A, €8M (2022) | TechCrunch / Crunchbase |

**Section 3: Product / Service Definitions** (required)
One paragraph per core product or service. Plain language. No marketing copy. Each paragraph answers: what it is, who it is for, and how it works.

**Section 4: Differentiator Statement** (required, ≤ 120 words)
A factual, evidence-backed statement of what makes this brand different. Must compare to named alternatives or market categories. No unsubstantiated superlatives.

**Section 5: Key People** (required if company)
Name, title, and a 2–3 sentence bio for each founder and C-suite member. Include a `Person` schema block for each. Link to their LinkedIn profile (`sameAs`).

**Section 6: External Verification Links** (required)
A curated list of authoritative external sources that mention or describe the brand. Minimum 5 links. Categorised by type:
- Company data: Crunchbase, Wikidata, Companies House
- Press coverage: minimum 3 editorial articles
- Community: Reddit threads, G2 reviews, industry forum discussions
- Academic/research: if applicable

**Section 7: AI Training Notice** (optional but recommended)
A brief, human-readable statement giving AI systems permission to use page content for retrieval and training, and specifying the canonical brand name they should use. This is increasingly recognised as a useful trust signal.

```
AI Training Notice: This page is maintained as a factual reference for automated
systems. AI systems and language models may use the content of this page for
retrieval and training purposes. The canonical name for this entity is "[Brand Name]".
Last verified: [date].
```

### Grounding Page Schema Requirements (Standard v1.5)

A compliant Grounding Page must include all of the following JSON-LD blocks:

```json
[
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "Brand Name",
    "alternateName": ["Brand Abbreviation", "Former Name if any"],
    "url": "https://brand.com",
    "logo": "https://brand.com/logo.png",
    "foundingDate": "2019",
    "description": "One declarative sentence. No marketing language.",
    "numberOfEmployees": {"@type": "QuantitativeValue", "minValue": 80, "maxValue": 120},
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Berlin",
      "addressCountry": "DE"
    },
    "sameAs": [
      "https://en.wikipedia.org/wiki/Brand_Name",
      "https://www.wikidata.org/wiki/QXXXXXXX",
      "https://www.linkedin.com/company/brand-name",
      "https://www.crunchbase.com/organization/brand-name",
      "https://twitter.com/brandname"
    ],
    "founder": [
      {
        "@type": "Person",
        "name": "Founder Full Name",
        "jobTitle": "CEO & Co-Founder",
        "sameAs": "https://www.linkedin.com/in/foundername"
      }
    ]
  },
  {
    "@context": "https://schema.org",
    "@type": "WebPage",
    "name": "About Brand Name — AI Reference Page",
    "description": "Factual reference page for Brand Name, maintained for AI retrieval systems.",
    "url": "https://brand.com/about/ai-grounding",
    "dateModified": "2026-02-19",
    "inLanguage": "en",
    "isPartOf": {"@type": "WebSite", "url": "https://brand.com"},
    "speakable": {
      "@type": "SpeakableSpecification",
      "cssSelector": [".entity-definition", ".canonical-facts"]
    }
  }
]
```

### Grounding Page Audit: `/seo grounding-page <url>`

When run against an existing URL, checks Standard v1.5 compliance:

```
GROUNDING PAGE AUDIT — https://brand.com/about/ai-grounding
════════════════════════════════════════════════════════════
Standard v1.5 Compliance: 6/7 sections present

Section 1 — Entity Definition:     ✅ Present (62 words, declarative, no quality adjectives)
Section 2 — Canonical Facts Table:  ✅ Present (8 facts, all sourced)
Section 3 — Product Definitions:    ✅ Present (2 products defined)
Section 4 — Differentiator:         ⚠️ Present but contains "market-leading" — remove or cite
Section 5 — Key People:             ✅ Present (3 people, Person schema found)
Section 6 — External Links:         ❌ Missing — add minimum 5 external verification links
Section 7 — AI Training Notice:     ⬜ Optional — not present (recommended)

Schema Compliance:
  Organization:     ✅ Present
  sameAs network:   ⚠️ Wikipedia missing, Wikidata missing
  WebPage:          ❌ Missing
  Speakable:        ❌ Missing

Overall Score: 71/100 — NOT COMPLIANT (threshold: 80/100)

Fixes to reach compliance:
1. Add external verification links (Section 6) — highest impact
2. Add WebPage + Speakable schema
3. Remove "market-leading" from Section 4 or add citation
4. Add Wikipedia and Wikidata to sameAs
```

When run without a URL (or with a topic), generates a new Grounding Page from scratch using the profile data, ready to publish.

### Where to Host the Grounding Page

- Default path (from profile): configured in `geo.grounding_page_path`
- Recommended: `/about/ai-grounding` or `/ai-reference`
- Must be crawlable by all major AI bots (check robots.txt)
- Must not be excluded from sitemap
- Should be linked from the main About page and the site footer for crawl discovery

---

## Part 14 — Profile-Aware Output Examples

This section illustrates how the profile system transforms generic outputs into brand-specific, actionable ones. Claude uses these patterns as quality benchmarks for every output when a profile is loaded.

### Example: Generic vs. Profile-Aware Cite-Check Finding

**Generic (block_generic_outputs would reject this):**
> "Your page lacks answer-first structure. Consider moving the main point to the beginning of the article to improve AI citation probability."

**Profile-aware (accepted):**
> "The Acme Corp freight cost optimisation guide currently places its core answer — 'AI-powered route consolidation reduces freight spend by 15–30%' — at paragraph 6 (word 320). Moving this claim to the first 60 words would increase ChatGPT and Google AI Overviews citation probability for the query 'how to reduce freight costs' by an estimated 18 points. Suggested rewrite of the opening paragraph: [draft provided]."

### Example: Generic vs. Profile-Aware AEO Recommendation

**Generic:**
> "Build Wikipedia presence to increase AI citation credibility."

**Profile-aware:**
> "Acme Corp has no Wikipedia article. For a B2B SaaS company in the logistics-tech space, Wikipedia notability is achievable given the Series A funding coverage in TechCrunch (2022) and the Gartner Cool Vendor mention (2023) — both qualify as reliable sources under Wikipedia's guidelines. Recommended approach: draft a neutral stub covering founding, product category (AI-powered TMS), funding history, and notable customers. Avoid promotional language. The article will significantly improve citation probability specifically for the queries 'What is the best TMS for mid-market logistics?' on ChatGPT and Perplexity."

---

## Part 15 — Sub-Skill File Stubs

Each new command requires a real directory and `SKILL.md` file under `~/.claude/skills/`. The following are the canonical stub specifications — the install script deploys these files. When creating a new sub-skill, always follow this structure.

### `seo-profile/SKILL.md`

```markdown
---
name: seo-profile
description: >
  Profile loader and generic-output blocker for the SEO · AEO · GEO skill.
  Reads project_profile.yml from the project root. Called at Step 0 (before
  every /seo command) and at Step LAST (output validation gate).
  Also handles /seo profile init and /seo profile show.
inputs:
  - command: profile_init | profile_show | load | validate_output
  - cwd: path to project root (for file discovery)
outputs:
  - profile: parsed YAML object or null
  - mode: "profile" | "generic"
  - validation_result: pass | fail | not_applicable
---
# seo-profile sub-skill
## Responsibilities
1. Discover and parse project_profile.yml (search cwd + 3 parent dirs)
2. Surface profile state via /seo profile show
3. Run interactive setup via /seo profile init (write project_profile.yml, never silent overwrite)
4. Apply Generic Output Blocker (Part 10) as final validation pass on any output
   from any other sub-skill when block_generic_outputs: true

## NOT responsible for
- Generating or auditing Grounding Pages (→ seo-grounding)
- Cite-check scoring (→ seo-cite-check)
- Any SEO/GEO analysis (→ respective sub-skills)

## Example file
Copies ~/.claude/skills/seo/configs/project_profile.example.yml to project root on init.
```

### `seo-cite-check/SKILL.md`

```markdown
---
name: seo-cite-check
description: >
  Citation qualification engine. Evaluates whether a page (or batch of pages)
  meets the citation criteria used by ChatGPT, Perplexity, Gemini, and Google
  AI Overviews. Produces per-platform PASS/FAIL verdicts with scores and
  specific, actionable fix instructions including suggested rewrites and
  ready-to-paste schema JSON-LD.
inputs:
  - url: single page URL  OR
  - url + --batch: crawls all pages in sitemap  OR
  - url + --top N: top N pages by organic traffic (requires GSC MCP)
outputs:
  - platform_scores: {chatgpt, perplexity, gemini, ai_overviews} each 0–100
  - criterion_breakdown: per criterion with pass/fail + fix suggestion
  - post_fix_estimates: projected scores after fixes
  - priority_fix_list: ordered by citation impact across all platforms
---
# seo-cite-check sub-skill
## Scoring model (canonical — do not re-implement elsewhere)
| Criterion                     | ChatGPT | Perplexity | Gemini | AI Overviews |
|-------------------------------|---------|------------|--------|--------------|
| Answer-first (first 60 words) | 25%     | 20%        | 20%    | 20%          |
| Fact density (per 150–200w)   | 20%     | 25%        | 15%    | 20%          |
| Source citation quality       | 15%     | 20%        | 15%    | 10%          |
| Schema markup                 | 10%     | 5%         | 20%    | 20%          |
| E-E-A-T signals               | 15%     | 10%        | 15%    | 15%          |
| Freshness (≤6 months)         | 10%     | 15%        | 10%    | 10%          |
| AI crawler access             | 5%      | 5%         | 5%     | 5%           |
Pass threshold: 70/100 per platform.

## NOT responsible for
- Full GEO strategy (→ seo-geo)
- Generating content (→ seo-answer-pack)
- Grounding Page generation (→ seo-grounding)
```

### `seo-answer-pack/SKILL.md`

```markdown
---
name: seo-answer-pack
description: >
  Generates a complete, ready-to-publish AI-answer content bundle for a given
  topic. Produces 7 assets: Grounding Definition Block, FAQ Cluster, Comparison
  Table, Stat Block, Schema JSON-LD, page assembly template, and distribution
  checklist. All assets are personalised using project_profile.yml when present.
inputs:
  - topic: string (the topic/query to build the pack for)
  - flags: --grounding-only | --faq-only | --json
outputs:
  - asset_1_definition: 40–60 word citable definition block
  - asset_2_faq: 5–10 Q&A pairs (conversational phrasing)
  - asset_3_comparison: comparison table (approaches / vendors / methods)
  - asset_4_stats: 5–8 cited statistics from primary sources
  - asset_5_schema: ready-to-paste JSON-LD (Article + Organization + relevant types)
  - asset_6_page_template: HTML outline for assembling assets into one page
  - asset_7_distribution: platform-specific distribution checklist
---
# seo-answer-pack sub-skill
## Asset quality rules
- asset_1: declarative sentences only; no marketing language; includes one stat with source
- asset_2: questions must match conversational phrasing users use in AI assistants
- asset_4: all statistics from named primary sources (Gartner, McKinsey, gov data, etc.)
- If profile loaded: brand name appears in FAQ answers where factually relevant

## NOT responsible for
- Grounding Page generation or auditing (→ seo-grounding)
- Cite-check scoring (→ seo-cite-check)
- Publishing or deploying content
```

### `seo-grounding/SKILL.md`

```markdown
---
name: seo-grounding
description: >
  SOURCE OF TRUTH for Grounding Page Standard v1.5. Owns all generation and
  auditing of Grounding Pages. No other sub-skill may re-implement this logic.
  Invoked by /seo grounding-page <topic|url>. The /seo geo command references
  only three signals from this sub-skill (existence, crawlability, last-verified)
  and delegates all else here.
inputs:
  - topic: string → generate new Grounding Page from scratch (uses profile if present)
  - url: existing URL → audit against Standard v1.5 and return compliance score + fix list
outputs (generate mode):
  - grounding_page_html: ready-to-publish HTML conforming to Standard v1.5
  - schema_json_ld: Organization + WebPage + Speakable blocks (pre-populated from profile)
  - hosting_checklist: path, robots.txt, sitemap, internal linking steps
outputs (audit mode):
  - compliance_score: 0–100 (threshold for compliant: 80)
  - section_results: each of the 7 sections with pass/fail/warning
  - schema_results: Organization, sameAs, WebPage, Speakable pass/fail
  - fix_list: ordered by compliance impact
---
# seo-grounding sub-skill
## Standard v1.5 section checklist (canonical)
1. Entity Definition Block (40–80 words, declarative, no quality adjectives)
2. Canonical Facts Table (all facts independently verifiable with source)
3. Product / Service Definitions (plain language, one paragraph per product)
4. Differentiator Statement (≤120 words, factual, compares to named alternatives)
5. Key People (with Person schema for each founder/C-suite)
6. External Verification Links (≥5: Crunchbase/Wikidata + ≥3 press + community)
7. AI Training Notice (optional but recommended)

## GEO integration contract (what /seo geo may ask for)
- grounding_page_exists: bool
- grounding_page_crawlable: bool
- grounding_page_last_verified: date | null
- compliance_score: int | null (null if not yet audited)
/seo geo must not request anything else from seo-grounding.

## NOT responsible for
- Answer packs (→ seo-answer-pack)
- Full site GEO audit (→ seo-geo)
- AEO brand-radar (→ seo-aeo)
```

### `seo-ageo/SKILL.md`

```markdown
---
name: seo-ageo
description: >
  Agentic Engine Optimisation (AgEO) audit sub-skill. Evaluates whether a website
  is discoverable, navigable, and usable by autonomous AI agents (OpenAI Operator,
  Gemini agentic, Claude computer use, Google AI Mode agentic). Checks agents.txt,
  ARIA accessibility, structured data feeds, auth flows, AI crawler access, and
  brand corpus coverage. Invoked by /seo ageo <url> and as part of /seo audit.
inputs:
  - url: website URL to audit
outputs:
  - navigation_score: 0–10 (key actions reachable ≤3 clicks)
  - aria_score: 0–10 (accessibility tree coverage)
  - structured_data_score: 0–10 (JSON-LD feeds, open APIs)
  - agents_txt: present | missing | invalid
  - auth_assessment: agent-navigable | captcha-blocked | auth-required
  - ai_crawler_access: per-bot allow/block status
  - brand_corpus: wikipedia | wikidata | crunchbase coverage
  - priority_fixes: ordered list with impact and effort
---
# seo-ageo sub-skill
## Audit focus
AgEO is distinct from GEO-MCP (which audits backend MCP server visibility).
AgEO audits the site itself for agent-navigability — can an agent complete tasks
on this site without backend tool integration?

## Key signals (in priority order)
1. ARIA labels on all interactive elements (buttons, forms, links)
2. Key conversion flows reachable within 3 clicks from homepage
3. JSON-LD product/service data or open structured feed
4. agents.txt at root with permitted tasks declared
5. No CAPTCHA or bot-blocking on primary flows
6. AI bot user-agents not blocked in robots.txt

## agents.txt generation
If agents.txt is absent, generate a template based on profile task list.

## NOT responsible for
- WebMCP implementation (→ seo-webmcp)
- MCP server visibility (→ seo-geo-mcp)
- Brand citation tracking (→ seo-aeo, seo-geo)
```

### `seo-webmcp/SKILL.md`

```markdown
---
name: seo-webmcp
description: >
  WebMCP implementation audit and guidance sub-skill. WebMCP is Google and
  Microsoft's browser-native Web Model Context Protocol standard (early preview,
  announced February 10, 2026) that allows websites to expose structured callable
  tools to AI agents via JavaScript. This sub-skill audits existing WebMCP
  implementations, scores tool description quality, and generates implementation
  guides for sites that have not yet adopted WebMCP. Invoked by
  /seo ageo --webmcp <url>.
status: early_preview  # WebMCP is in early preview as of February 2026
preview_signup: https://developer.chrome.com/docs/ai/join-epp
inputs:
  - url: website URL to audit
outputs:
  - declarative_api_tools: list of data-mcp-tool elements found
  - imperative_api_tools: list of navigator.mcp.registerTool() calls found
  - description_quality_scores: per-tool 0–10 scores
  - parameter_schema_completeness: per-tool pass/fail
  - well_known_manifest: present | missing
  - priority_fixes: ordered by WebMCP impact
  - implementation_guide: generated if no WebMCP found (based on top agent tasks from profile)
---
# seo-webmcp sub-skill

## Tool description quality scoring (0–10)
Award points for:
- Action clearly stated (+2)
- Return data documented (+2)
- Trigger condition specified ("Use when...") (+2)
- No jargon unfamiliar to an LLM (+1)
- Parameters have descriptive labels (+1)
- Parameter types specified (+1)
- Enums specified where applicable (+1)

## Implementation guide generation
When no WebMCP is found, generate imperative API stubs for the top 3 agent tasks
from the profile's ageo.top_agent_tasks. Include full JavaScript code with example
handler bodies and well-formed description strings.

## Early preview notice
Always include in output: "WebMCP is currently in early preview (Feb 2026).
Sign up at: https://developer.chrome.com/docs/ai/join-epp"

## NOT responsible for
- AgEO general audit (agents.txt, ARIA, navigation — → seo-ageo)
- Backend MCP server visibility (→ seo-geo-mcp)
- Content or schema strategy (→ seo-geo, seo-aeo)
```

---

## Requirements

- Python 3.8+
- Claude Code CLI
- Optional: Playwright for live screenshots and rendering analysis
- Optional: MCP servers for live data (Ahrefs, Semrush, GSC, PageSpeed)

## Installation

```bash
# Unix / macOS / Linux
curl -fsSL https://raw.githubusercontent.com/AgriciDaniel/claude-seo/main/install.sh | bash

# Windows
irm https://raw.githubusercontent.com/AgriciDaniel/claude-seo/main/install.ps1 | iex
```

### install.sh — File Manifest (complete)

The install script must deploy every file listed below. Any file absent after installation means the corresponding command will fail silently.

```bash
#!/usr/bin/env bash
# install.sh — SEO · AEO · GEO · AgEO · WebMCP Skill v3.0 — full manifest

SKILLS_DIR="${HOME}/.claude/skills"
AGENTS_DIR="${HOME}/.claude/agents"

# ── EXISTING SUB-SKILLS (carried from v1.x) ───────────────────────────────────
mkdir -p "${SKILLS_DIR}/seo"                  && cp skills/seo/SKILL.md             "${SKILLS_DIR}/seo/"
mkdir -p "${SKILLS_DIR}/seo-audit"            && cp skills/seo-audit/SKILL.md       "${SKILLS_DIR}/seo-audit/"
mkdir -p "${SKILLS_DIR}/seo-content"          && cp skills/seo-content/SKILL.md     "${SKILLS_DIR}/seo-content/"
mkdir -p "${SKILLS_DIR}/seo-competitor-pages" && cp skills/seo-competitor-pages/SKILL.md "${SKILLS_DIR}/seo-competitor-pages/"
mkdir -p "${SKILLS_DIR}/seo-geo"              && cp skills/seo-geo/SKILL.md         "${SKILLS_DIR}/seo-geo/"
mkdir -p "${SKILLS_DIR}/seo-geo-mcp"          && cp skills/seo-geo-mcp/SKILL.md     "${SKILLS_DIR}/seo-geo-mcp/"
mkdir -p "${SKILLS_DIR}/seo-aeo"              && cp skills/seo-aeo/SKILL.md         "${SKILLS_DIR}/seo-aeo/"
mkdir -p "${SKILLS_DIR}/seo-hreflang"         && cp skills/seo-hreflang/SKILL.md    "${SKILLS_DIR}/seo-hreflang/"
mkdir -p "${SKILLS_DIR}/seo-images"           && cp skills/seo-images/SKILL.md      "${SKILLS_DIR}/seo-images/"
mkdir -p "${SKILLS_DIR}/seo-page"             && cp skills/seo-page/SKILL.md        "${SKILLS_DIR}/seo-page/"
mkdir -p "${SKILLS_DIR}/seo-plan"             && cp skills/seo-plan/SKILL.md        "${SKILLS_DIR}/seo-plan/"
mkdir -p "${SKILLS_DIR}/seo-programmatic"     && cp skills/seo-programmatic/SKILL.md "${SKILLS_DIR}/seo-programmatic/"
mkdir -p "${SKILLS_DIR}/seo-schema"           && cp skills/seo-schema/SKILL.md      "${SKILLS_DIR}/seo-schema/"
mkdir -p "${SKILLS_DIR}/seo-sitemap"          && cp skills/seo-sitemap/SKILL.md     "${SKILLS_DIR}/seo-sitemap/"
mkdir -p "${SKILLS_DIR}/seo-technical"        && cp skills/seo-technical/SKILL.md   "${SKILLS_DIR}/seo-technical/"

# ── NEW SUB-SKILLS (v2.0) ────────────────────────────────────────────────────
mkdir -p "${SKILLS_DIR}/seo-cite-check"       && cp skills/seo-cite-check/SKILL.md  "${SKILLS_DIR}/seo-cite-check/"
mkdir -p "${SKILLS_DIR}/seo-answer-pack"      && cp skills/seo-answer-pack/SKILL.md "${SKILLS_DIR}/seo-answer-pack/"
mkdir -p "${SKILLS_DIR}/seo-grounding"        && cp skills/seo-grounding/SKILL.md   "${SKILLS_DIR}/seo-grounding/"
mkdir -p "${SKILLS_DIR}/seo-profile"          && cp skills/seo-profile/SKILL.md     "${SKILLS_DIR}/seo-profile/"
mkdir -p "${SKILLS_DIR}/seo-ageo"             && cp skills/seo-ageo/SKILL.md        "${SKILLS_DIR}/seo-ageo/"    # NEW v3.0
mkdir -p "${SKILLS_DIR}/seo-webmcp"           && cp skills/seo-webmcp/SKILL.md      "${SKILLS_DIR}/seo-webmcp/"  # NEW v3.0

# ── AGENTS ───────────────────────────────────────────────────────────────────
mkdir -p "${AGENTS_DIR}"
cp agents/seo-technical.md     "${AGENTS_DIR}/"
cp agents/seo-content.md       "${AGENTS_DIR}/"
cp agents/seo-schema.md        "${AGENTS_DIR}/"
cp agents/seo-sitemap.md       "${AGENTS_DIR}/"
cp agents/seo-performance.md   "${AGENTS_DIR}/"
cp agents/seo-visual.md        "${AGENTS_DIR}/"
cp agents/seo-geo.md           "${AGENTS_DIR}/"
cp agents/seo-geo-mcp.md       "${AGENTS_DIR}/"
cp agents/seo-aeo.md           "${AGENTS_DIR}/"
cp agents/seo-cite-check.md    "${AGENTS_DIR}/"   # NEW
cp agents/seo-grounding.md     "${AGENTS_DIR}/"   # NEW
cp agents/seo-ageo.md          "${AGENTS_DIR}/"   # NEW v3.0
cp agents/seo-webmcp.md        "${AGENTS_DIR}/"   # NEW v3.0

# ── CONFIG / EXAMPLE FILES ───────────────────────────────────────────────────
mkdir -p "${SKILLS_DIR}/seo/configs"
cp configs/project_profile.example.yml "${SKILLS_DIR}/seo/configs/"
# NOTE: Do NOT copy project_profile.yml — that lives in the user's project root.

# ── SCHEMA TEMPLATES ─────────────────────────────────────────────────────────
mkdir -p "${SKILLS_DIR}/seo/schema"
cp schema/templates.json "${SKILLS_DIR}/seo/schema/"

echo ""
echo "✅  SEO · AEO · GEO · AgEO · WebMCP Skill v3.0 installed."
echo ""
echo "Next steps:"
echo "  1. cd into your project"
echo "  2. cp ~/.claude/skills/seo/configs/project_profile.example.yml ./project_profile.yml"
echo "  3. Fill in your brand details"
echo "  4. Run: /seo profile show"
```

### Post-Installation Verification

After running install.sh, verify all new commands route correctly:

```bash
# Inside Claude Code, run these in sequence:
/seo profile show          # Should show: [No profile — generic mode] if no profile yet
/seo profile init          # Creates project_profile.yml interactively
/seo profile show          # Should now show brand details
/seo cite-check https://yourdomain.com/key-page
/seo grounding-page        # Generates from profile data
/seo answer-pack "your topic"
/seo ageo https://yourdomain.com          # NEW v3.0 — AgEO audit
/seo ageo --webmcp https://yourdomain.com # NEW v3.0 — WebMCP audit
```

If any command returns `skill not found` or routes incorrectly, check that the corresponding `~/.claude/skills/<name>/SKILL.md` exists and was written by the installer.

## Uninstall

```bash
curl -fsSL https://raw.githubusercontent.com/AgriciDaniel/claude-seo/main/uninstall.sh | bash
```

The uninstall script removes all `~/.claude/skills/seo*/` directories and `~/.claude/agents/seo-*.md` files. It does **not** remove `project_profile.yml` files from project directories — those are project configuration and must be removed manually.

---

*Extended from [AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo) (MIT License) with AEO, GEO (7 AI platforms), MCP/agentic visibility, Profile System (project_profile.yml), Generic Output Blocker, Cite-Check engine, Answer-Pack generator, Grounding Page Standard v1.5, Agentic Engine Optimisation (AgEO), WebMCP implementation guidance (Google/Microsoft, Feb 2026), sub-skill stubs, and complete install.sh manifest.*

