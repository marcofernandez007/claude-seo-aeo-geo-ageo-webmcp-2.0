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
