<p align="center">
  <img src=".github/logo.svg" alt="awesome-geo" width="128">
</p>

# Awesome GEO [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**English** | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md) | [Español](README.es.md) | [Français](README.fr.md)

> A curated, source-first map of **Generative Engine Optimization (GEO)**, Answer Engine Optimization (AEO), and AI search — built on official engine documentation, not vendor hype.

**The uncomfortable thesis of this list:** by the search engines' *own* official docs, GEO/AEO is not a secret new optimization discipline. For Google Search it is foundational SEO applied to new answer surfaces (AI Overviews, AI Mode). Most other AI search engines (ChatGPT, Perplexity, Claude) officially share the same base — crawlable, indexable, trustworthy, fresh — and publish **no** separate "rewrite your content for AI" guidance. The one engine that *does* take a visibly different official stance is Microsoft Bing/Copilot. The real difference between engines is not *how you write* but the **retrieval backend** each one reads from.

Every claim here links to a primary source. Marketing blog posts are kept in a clearly-labeled secondary section and are never promoted to fact.

## Contents

- [The Core Argument](#the-core-argument)
- [Terminology Map](#terminology-map)
- [Google — Official Docs](#google--official-docs)
- [Measuring AI Search Performance](#measuring-ai-search-performance)
- [Per-Engine Official Stances](#per-engine-official-stances-beyond-google)
- [llms.txt — What It Actually Is](#llmstxt--what-it-actually-is)
- [Social / SNS Surfaces](#social--sns-surfaces)
- [Industry & Academic References](#industry--academic-references-secondary)
- [What to Ignore](#what-to-ignore-overhyped-claims)
- [Contributing](#contributing)

## The Core Argument

**AEO** (Answer Engine Optimization) and **GEO** (Generative Engine Optimization) are real, widely-used industry terms for getting a brand or content cited in AI answers — AI Overviews, AI Mode, ChatGPT, Perplexity, voice search. **GEO** was formalized academically by the 2023 paper [*GEO: Generative Engine Optimization*](https://arxiv.org/abs/2311.09735) (KDD 2024).

The disputed part is not whether the terms exist — it is whether they describe a **separate optimization system**. Google's own [generative-AI optimization guide](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide) acknowledges these terms are "common online," then states plainly: for Google Search, you keep applying foundational SEO. **No special schema, no `llms.txt`, no AI-only markdown, no content chunking, no AI-only rewrites are required** for AI Overviews / AI Mode.

So this list treats GEO as **SEO basics applied to new answer surfaces** — with engine-specific caveats documented from primary sources, not invented.

## Terminology Map

| Term | Full name | Nature | Google's official position |
|---|---|---|---|
| **SEO** | Search Engine Optimization | The base system: help engines understand content and users find it | Official. Core of Google Search Central docs |
| **AEO** | Answer Engine Optimization | Industry term for being cited in AI/direct/voice answers | Mentioned as a "common online" term. Not a separate Google system |
| **GEO** | Generative Engine Optimization | Industry/academic term for visibility & attribution in generative answers | Mentioned as "common online." Treated as SEO-based for Google Search |
| **LLMO / AI SEO / AIO** | LLM Optimization, etc. | Marketing neologisms | Not an official Google framework — verify each claim per source |

## Google — Official Docs

The foundation. If you read nothing else, read the first row.

| Doc | Link | Why it matters |
|---|---|---|
| Optimizing for generative AI features on Google Search | https://developers.google.com/search/docs/fundamentals/ai-optimization-guide | The primary official answer to the GEO/AEO question. For Google Search, optimizing for generative AI is still SEO. No `llms.txt`, chunking, or special AI markup needed |
| AI features and your website | https://developers.google.com/search/docs/appearance/ai-features | How AI Overviews / AI Mode work from a site owner's view. No extra technical requirements — being indexable + snippet-eligible is the point |
| SEO Starter Guide | https://developers.google.com/search/docs/fundamentals/seo-starter-guide | The fundamentals: structure, content, links, titles, snippets, images/video, promotion |
| Google Search Essentials | https://developers.google.com/search/docs/essentials | Minimum bar to appear in Google Search: technical requirements, spam policies, key best practices |
| Technical requirements | https://developers.google.com/search/docs/crawling-indexing/technical-requirements | Minimum conditions for Google to fetch, render, and index a page |
| Structured data intro | https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data | The official role of structured data: rich-results eligibility — not a special "AI search" schema |
| Snippets / meta description | https://developers.google.com/search/docs/appearance/snippet | Snippet eligibility feeds AI-feature eligibility; understand preview control + meta description |
| Robots meta / nosnippet / max-snippet | https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag | Control what's shown in Search and AI features: `nosnippet`, `data-nosnippet`, `max-snippet`, `noindex` |
| Google-Extended | https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers#google-extended | Product token to control Gemini/Vertex AI training & grounding. Does **not** affect Google Search inclusion/ranking |

## Measuring AI Search Performance

| Doc | Link | Why it matters |
|---|---|---|
| Search Console generative-AI performance reports | https://developers.google.com/search/blog/2026/06/gen-ai-performance-reports | Official blog on reporting generative-AI performance in Search Console (announced 2026-06-03) |
| Clicks / impressions / position in Search Console | https://support.google.com/webmasters/answer/7042828 | How clicks, impressions, and position are counted in AI Mode / AI Overviews |
| AI Overviews (user help) | https://support.google.com/websearch/answer/14901683 | User-facing explanation. A core feature — not fully disableable; the Web filter shows text links only |
| AI Mode (user help) | https://support.google.com/websearch/answer/16296315 | AI Mode / Search Labs / follow-ups / agentic capabilities |

## Per-Engine Official Stances (Beyond Google)

Core question: *Google says GEO/AEO = SEO — do other major AI engines officially claim their engine is different?*

Short answer: **most share Google's base** (crawlable · indexable · trustworthy · fresh) and require no official "secret optimization." The one clearly different official stance is **Microsoft Bing/Copilot** — Bing states that schema markup helps its LLM understand content, and recommends IndexNow for freshness. And the real cross-engine difference is the **retrieval backend** (own index vs. third-party search provider), not the writing.

| Engine / product | Retrieval backend (official) | Official publisher approach | vs. Google "SEO is enough" |
|---|---|---|---|
| Google AI Overviews / AI Mode | Google index | Search Essentials + SEO basics. No special schema / `llms.txt` | Baseline |
| ChatGPT search (OpenAI) | OAI-SearchBot crawl + third-party search providers | Allow `OAI-SearchBot` in robots.txt; opt out via `noindex`. **No separate content-optimization guide** | Effectively the same |
| Perplexity | PerplexityBot index + Perplexity-User live fetch | Allow PerplexityBot + IP ranges. **Technical access only, no content strategy** | Effectively the same |
| Claude web search (Anthropic) | Third-party search provider (reported: Brave) + ClaudeBot | No publisher-optimization doc. Inline citations; prefers primary/verifiable sources | Effectively the same |
| Microsoft Bing / Copilot | Bing index | **Officially says schema helps its LLM** + IndexNow freshness + clear headings/tables/FAQ. AI Performance report in Bing Webmaster Tools | **Different** — publishes generative-specific guidance |

Per-platform primary sources:

- **OpenAI / ChatGPT** — [Publishers & developers FAQ](https://help.openai.com/en/articles/12627856-publishers-and-developers-faq), [ChatGPT search](https://help.openai.com/en/articles/9237897-chatgpt-search), [bots / crawlers](https://developers.openai.com/api/docs/bots). `OAI-SearchBot` (search/product) is separate from `GPTBot` (training). The official guidance is "don't block it, or use `noindex` to opt out" — not "rewrite your content for AI."
- **Perplexity** — [crawlers](https://docs.perplexity.ai/docs/resources/perplexity-crawlers), [robots.txt policy](https://www.perplexity.ai/help-center/en/articles/10354969-how-does-perplexity-follow-robots-txt). PerplexityBot = search visibility (not training); Perplexity-User = user-triggered fetch. Docs cover technical access only. (Entity-clarity / front-loading / Reddit-citation tips are third-party reverse-engineering, **not** official — not promoted here.)
- **Anthropic / Claude** — [web search tool](https://platform.claude.com/docs/en/agents-and-tools/tool-use/web-search-tool), [enabling web search](https://support.claude.com/en/articles/10684626-enabling-and-using-web-search). Underlying search relies on a third-party provider (reported: Brave Search); responses carry inline citations and conservatively prefer verifiable primary sources. "Getting picked up by Claude" ≈ "being in the search provider's index as a trustworthy primary source."
- **Microsoft Bing / Copilot** — [AI Performance in Bing Webmaster Tools](https://blogs.bing.com/webmaster/February-2026/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview), [Bing/Copilot uses schema for its LLMs](https://searchengineland.com/microsoft-bing-copilot-use-schema-for-its-llms-453455). The most opinionated of the set — but Microsoft's Fabrice Canel still stresses "less is more: precision, not volume."

## llms.txt — What It Actually Is

**Origin:** proposed 2024-09-03 by **Jeremy Howard** (fast.ai / Answer.AI co-founder) via an answer.ai post and the [`llmstxt.org`](https://llmstxt.org) spec. A curated markdown index at site root `/llms.txt` meant to help an LLM use the site at inference time. It is a **one-person community proposal**, not a search-consortium standard like schema.org — which is the root cause of the support gap below.

**Support status (as of 2026 Q1):**

- **Google** — officially unsupported. John Mueller (2025) and Gary Illyes (Search Central Live 2025-07) stated no AI system currently uses `llms.txt` and Google has no plans to.
- **OpenAI / others** — no official announcement that GPTBot/ChatGPT parses `llms.txt`.
- **"Anthropic/Perplexity confirmed support"** — some SEO blogs claim this; other reporting says major platforms ignore it and adoption has stalled. **No primary confirmation → not promoted to fact here.** (Anthropic *publishing* an `llms.txt` on its own docs is publisher behavior — it does not mean Claude *consumes* yours.)

`llms.txt` remains a community convention, not an official standard.

## Social / SNS Surfaces

SNS is less a separate "AEO/GEO play" and more a **public web surface indexed by Google Search** + brand/profile connection signals.

| Doc | Link | Relation to SNS |
|---|---|---|
| Organization structured data | https://developers.google.com/search/docs/appearance/structured-data/organization | Link SNS/review profiles from your homepage via `sameAs` |
| ProfilePage structured data | https://developers.google.com/search/docs/appearance/structured-data/profile-page | For user/author/about profile pages on forum & social sites |
| DiscussionForumPosting / SocialMediaPosting | https://developers.google.com/search/docs/appearance/structured-data/discussion-forum | UGC post markup for community/forum/social platforms. Not for publisher-authored articles |
| Google Business Profile social links | https://support.google.com/business/answer/3039617 | Add one link per platform (Facebook, Instagram, LinkedIn, Pinterest, TikTok, X, YouTube) on some accounts |
| Social channels in Search Console | https://developers.google.com/search/blog/2025/12/social-channels-search-console | Experiment unifying site + some social-channel search performance in Search Console Insights (limited rollout) |

## Industry & Academic References (Secondary)

These corroborate that the terms exist; they are **not** promoted to Google policy or ranking fact.

| Source | Link | Use |
|---|---|---|
| arXiv — GEO: Generative Engine Optimization | https://arxiv.org/abs/2311.09735 | The paper that formalized "GEO." KDD 2024 accepted |
| Semrush — Answer Engine Optimization | https://www.semrush.com/blog/answer-engine-optimization/ | Frames AEO as marketing practices for brand visibility in AI answers |
| Ahrefs — Answer Engine Optimization | https://ahrefs.com/blog/answer-engine-optimization/ | Frames AEO as an SEO complement for direct-answer surfaces |
| Search Engine Journal — Google's guide calls AEO/GEO still SEO | https://www.searchenginejournal.com/googles-new-ai-search-guide-calls-aeo-and-geo-still-seo/575026/ | Industry read of Google's official guide. Keep the Google doc as the primary source |
| AEO Footnotes Lab: robots.txt and llms.txt across 118 AEO vendor sites | https://aeofootnotes.com/lab/robotstxt-and-llmstxt-across-118-aeo-tools-and-agency-sites-what-we-found | Measured data, not policy: 64 of 118 AEO vendor sites serve llms.txt and almost none block AI crawlers. Raw JSON linked |

## What to Ignore (Overhyped Claims)

Per Google's official position, treat these as red flags:

- "You need an `llms.txt` for Google Search"
- "AI search needs a special/secret schema"
- "You must chop content into tiny chunks for AI"
- Awkward rewrites written only for AI systems
- Artificial mention farming
- "Guaranteed #1 AI Overview ranking" sales pitches

Safe common denominator across ChatGPT / Perplexity / Claude / others:

- Publicly accessible source text
- Clear author / org / date / evidence
- Canonical, non-duplicate URLs
- Trustworthy external citations
- Up-to-date product / price / policy / FAQ info
- Consistent naming of your brand and key entities

## Contributing

Contributions welcome — but this list has one hard rule: **primary source or it doesn't go in.**

- Official engine/standards docs → main sections.
- Vendor blogs / analyses → the *Industry & Academic References* section, clearly labeled, never stated as fact.
- Reverse-engineered "ranking factor" claims without official confirmation are rejected.

See [contributing.md](contributing.md). Open a PR or an issue.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related rights to this work.
