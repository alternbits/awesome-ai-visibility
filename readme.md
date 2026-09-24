# Awesome AI Visibility [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources for **AI Visibility** — measuring, monitoring, and benchmarking how a brand is mentioned, cited, and represented across AI answer engines like ChatGPT, Perplexity, Google AI Overviews, Gemini, Copilot, and Claude.

AI Visibility is the measurement layer that sits alongside AEO/GEO optimization work: before you can improve how a brand shows up in AI-generated answers, you need a reliable way to see how it shows up today. This list collects the research, tools, and communities that define that measurement discipline as it stands in mid-2026. Contributions welcome — see [Contributing](#contributing).

## Contents

- [What Is AI Visibility?](#what-is-ai-visibility)
- [Foundational Research](#foundational-research)
- [Official Platform Documentation](#official-platform-documentation)
- [Guides & Explainers](#guides--explainers)
- [Tools & Platforms](#tools--platforms)
  - [AI Visibility Platforms](#ai-visibility-platforms)
  - [Open-Source Tools](#open-source-tools)
- [Measurement Methodology](#measurement-methodology)
- [Books](#books)
- [Courses & Training](#courses--training)
- [Newsletters, Blogs & People](#newsletters-blogs--people)
- [Communities](#communities)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
- [License](#license)

## What Is AI Visibility?

AI Visibility is the practice of tracking how often, how accurately, and how favorably a brand appears when people ask AI systems questions — as distinct from *optimizing* that content (the job AEO/GEO cover). In practice the two are inseparable: visibility tracking is the diagnostic step that tells a team whether their AEO/GEO work is actually landing, and most commercial tools now bundle both.

The category sits under several overlapping labels:

- **AI Visibility** / **AI Search Visibility** — the term used by most monitoring platforms and communications/PR teams.
- **Share of Model** / **Share of Voice (in AI)** — competitive-benchmarking framing, borrowed from traditional media measurement.
- **GEO / AEO tracking** — the same category, described from the content-optimization side rather than the measurement side.

Whatever the label, the underlying question is the same: when a real buyer asks ChatGPT, Perplexity, or Gemini about your category, does your brand show up, what does the AI say about it, and who else shows up alongside it?

## Foundational Research

- [**GEO: Generative Engine Optimization**](https://arxiv.org/abs/2311.09735) — The Princeton/Georgia Tech/Allen Institute/IIT Delhi paper (KDD 2024) that introduced the "impression score" — the first formal metric for a source's visibility inside a generated answer — along with the **GEO-BENCH** benchmark used to evaluate it.
- **Word-Count Attribution & Subjective Impression metrics** *(built on the 2024 GEO paper)* — Later work refined visibility measurement into two complementary metrics: a positional, word-count-weighted attribution score (citations earlier in an answer count for more), and a seven-dimension qualitative score — relevance, influence, uniqueness, positional prominence, volume, click likelihood, and information diversity — evaluated via G-Eval.
- **Source Composition of AI Answers** *(Rankfor.AI, 2026)* — Large-scale analysis of citation patterns across 167,000+ AI-generated citations, breaking down which sources generative engines draw on and how consistently.
- [**AgentGEO — Diagnosing and Repairing Citation Failures**](https://arxiv.org/abs/2603.09296) — Introduces a taxonomy of citation-failure modes, useful as a diagnostic framework for interpreting *why* a visibility report shows what it shows, not just what it shows.
- [**Awesome-GEO** by DavidHuji](https://github.com/DavidHuji/Awesome-GEO) — A deeper, research-paper-focused companion list if you want the academic grounding behind these metrics.

## Official Platform Documentation

- [Google Search Central — AI features & Search](https://developers.google.com/search) — Background on how AI Overviews are generated, relevant to interpreting any visibility report that includes Google's surfaces.
- [OpenAI — Crawlers documentation](https://platform.openai.com/docs/bots) — Explains `GPTBot`, `OAI-SearchBot`, and `ChatGPT-User`; relevant to understanding *why* a domain may or may not be visible in ChatGPT search results.
- [Perplexity — Bots & crawling](https://docs.perplexity.ai/) — Documents `PerplexityBot` vs. `Perplexity-User`, useful context for interpreting Perplexity citation data.
- [Google Analytics 4 — Traffic acquisition reports](https://support.google.com/analytics) — The standard (free) way to see AI referral traffic by filtering source/medium for domains like `chat.openai.com`, `perplexity.ai`, and `gemini.google.com`.

## Guides & Explainers

- [Search Engine Land — AI search & visibility coverage](https://searchengineland.com/) — Ongoing trade-press coverage of how visibility is measured and reported as the category evolves.
- [Frase — Answer Engine Optimization: Complete Guide](https://www.frase.io/blog/what-is-answer-engine-optimization-the-complete-guide-to-getting-cited-by-ai) — Lays out concrete AI-visibility metrics (citation count, share of voice, referral traffic, appearance rate) and how to track each with free tools.
- [CXL — Answer Engine Optimization guide](https://cxl.com/blog/answer-engine-optimization-aeo-the-comprehensive-guide/) — Covers measurement alongside optimization tactics.
- [emarketer — coverage of AI visibility indices](https://www.emarketer.com/) — Trade coverage of new visibility-measurement products as they launch (e.g., agency-built brand indices).

## Tools & Platforms

### AI Visibility Platforms

This is the core commercial category — dashboards that run prompts against multiple AI engines, then report on brand mentions, citation frequency, competitive share, and sentiment. Evaluate on: engine coverage, how the score is calculated (and whether that's disclosed), and whether it connects to an actual content or PR workflow rather than just reporting a number.

- [Profound](https://www.tryprofound.com/) — Enterprise-focused AI-visibility analytics with detailed publisher-partnership research.
- [Scrunch](https://scrunch.com/) — Monitoring, auditing, and content-delivery in one platform.
- [Otterly.AI](https://otterly.ai/) — Straightforward visibility tracking aimed at small and mid-size teams.
- [Peec AI](https://peec.ai/) — European-market AI-visibility monitoring platform.
- [AthenaHQ](https://www.athenahq.ai/) — Large-scale AI-response analysis with free visibility reports.
- [AirOps](https://www.airops.com/) — Connects visibility data directly to content briefing and production.
- [Brandi AI](https://mybrandi.ai/) — Combines AI-visibility intelligence with competitive benchmarking and sentiment analysis, aimed at marketing and PR teams.
- [Highwire AI Index](https://www.teamhighwire.com/insights/highwire-launches-ai-index-to-measure-brand-presence-in-generative-ai-platforms) — A communications-first visibility index built for corporate-reputation and comms teams rather than pure SEO/content teams.
- [Conductor](https://www.conductor.com/) / [Nightwatch](https://nightwatch.io/) / [SE Ranking](https://seranking.com/) — Established SEO platforms that have added AI-citation tracking modules.
- [Screpy](https://screpy.com/feature/ai-visibility/) — Tracks selected prompts across supported AI platforms, with brand mentions, citations, sentiment, sources, and competitor share of voice.

### Open-Source Tools

- [**Elmo**](https://github.com/elmohq/elmo) — Self-hosted, MIT-licensed AI-visibility tracker. Runs prompts against ChatGPT, Claude, Perplexity, Gemini, Copilot, and Google AI Overviews via your own API keys, so your prompt history and results stay on your own infrastructure — a transparent, auditable alternative to closed dashboards.
- [**geo-aeo-tracker**](https://github.com/danishashko/geo-aeo-tracker) — Local-first, Next.js-based AI-visibility dashboard tracking six AI models via scraping APIs, with a built-in site-audit crawler.
- [**AI Visibility topic page on GitHub**](https://github.com/topics/ai-visibility) — Browse the `ai-visibility` topic directly for the newest self-hosted trackers and citation-testing CLIs — this is a young, fast-moving corner of open source.

## Measurement Methodology

The metrics that recur across most credible visibility reports:

- **Citation frequency** — how often a source is cited across a set of tracked prompts.
- **Share of voice / share of model** — citation frequency relative to named competitors on the same prompts.
- **Appearance rate** — the percentage of relevant queries where a brand appears at all (many brands score surprisingly close to zero here even with strong SEO).
- **Answer/citation consistency** — whether a brand shows up reliably across repeated, near-identical queries, rather than in one lucky run.
- **Brand mention sentiment** — how favorably (or accurately) a brand is characterized when it is mentioned, separate from whether it's mentioned at all.
- **AI referral traffic** — actual site visits attributable to AI platforms, trackable for free via GA4 referral filtering, alongside manual periodic prompt testing as a sanity check on any paid tool's numbers.

## Books

- [**Answer Engine Optimization: A Field Guide for Navigating AI-Driven Search**](https://www.oreilly.com/library/view/answer-engine-optimization/0642572275549/) by Rodrigo Stockebrand (O'Reilly) — Covers how LLMs retrieve and select sources, which is the mechanism any visibility metric is ultimately trying to measure.

## Courses & Training

- [NoGood — AI Search & Answer Engine Optimization Course](https://nogood.io/aeo-course/) — Includes a measurement/tracking module alongside optimization tactics.
- [Class Central — Answer Engine Optimization courses](https://www.classcentral.com/subject/answer-engine-optimization) — Aggregates free and paid courses that include AI-visibility tracking fundamentals.

## Newsletters, Blogs & People

- [**The Marketing Newsletter**](https://themarketingnewsletter.org/) — Weekly marketing-growth newsletter covering AI, SEO, and content strategy for marketers and creators.
- [**Lead Generators**](https://leadgenerators.substack.com/) — Newsletter focused on lead-generation tactics and demand-gen strategy for growth teams.
- [**Aleyda Solis — SEOFOMO**](https://seofomo.co/) — Weekly SEO/AI-search newsletter with 45,000+ subscribers; regularly covers new AI-visibility tools and studies.
- [**Marie Haynes**](https://mariehaynes.com/newsletter) — Research-first newsletter with a strong quality/E-E-A-T lens applied to how AI systems select and represent sources.
- [**Mike King — Rank Report (iPullRank)**](https://ipullrank.com/blog) — Technical research on how LLMs select and cite sources, foundational reading for interpreting any visibility metric.
- [**The GTM Index — AI Search & GEO resource hub**](https://thegtmindex.com/geo/) — Curated, quarterly-updated round-up of visibility tools, newsletters, and communities.

## Communities

- [The AEO Community](https://theaeocommunity.com/) — Free Slack community where practitioners share real visibility-tracking experiments and results.
- [Gen Engine Optimizers](https://genengineoptimizers.com/) — GEO-focused Slack community with a dedicated `#llm-visibility` channel.
- [The SEO Community](https://theseocommunity.com/) — Large general SEO Slack (5,000+ members) with active AI-visibility discussion.

## Related Awesome Lists

If you're building out a full AI-search toolkit, these companion lists cover the adjacent ground:

- **Awesome AEO** — Answer Engine Optimization: the content and technical work that drives the numbers this list tracks.
- **Awesome GEO** — Generative Engine Optimization: the research-grounded framing of the same optimization work.
- [DavidHuji/Awesome-GEO](https://github.com/DavidHuji/Awesome-GEO) — Deeper academic research collection.
- [amplifying-ai/awesome-generative-engine-optimization](https://github.com/amplifying-ai/awesome-generative-engine-optimization) — Guides, tools, and research with an agency/practitioner lean.

## Contributing

Contributions are welcome — this category is consolidating fast and tool claims go stale quickly. Please:

1. Check the resource isn't already listed.
2. Add it to the most relevant section, keeping descriptions to one concise, original sentence.
3. Prefer tools that disclose their measurement methodology over ones that only report a proprietary score.
4. Open a pull request with a short note on why it belongs.

## License

[CC0](https://creativecommons.org/publicdomain/zero/1.0/) — To the extent possible under law, this list is released into the public domain.
