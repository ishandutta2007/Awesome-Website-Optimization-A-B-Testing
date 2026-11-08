# Awesome-Website-Optimization-A-B-Testing

# Awesome Website Optimization & A/B Testing

> A curated list of top Website Optimization and A/B Testing platforms — both SaaS/Hosted commercial solutions and open-source alternatives for experimentation, personalization, and conversion rate optimization.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Zoho PageSense](#zoho-pagesense)
  - [Optimizely](#optimizely)
  - [VWO](#vwo)
  - [AB Tasty](#ab-tasty)
  - [Kameleoon](#kameleoon)
  - [Unbounce](#unbounce)
  - [Instapage](#instapage)
  - [Crazy Egg](#crazy-egg)
  - [Dynamic Yield](#dynamic-yield)
- [Open-Source Software](#-open-source-software)
  - [Controlvar](#controlvar)
  - [Bucketeer](#bucketeer)
  - [GrowthBook](#growthbook)
  - [OpenReplay](#openreplay)
  - [oss-clarity](#oss-clarity)
  - [Localess](#localess)
  - [modelab](#modelab)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Website Optimization and A/B Testing platforms. These are not open-source but are included as reference points for feature comparison.

### Zoho PageSense
**Type:** Conversion optimization suite with A/B testing  
Zoho PageSense provides a free forever plan covering web analytics, heatmaps, session recording, and form analytics for up to 5,000 monthly tracked users. A/B testing, split URL testing, and personalization are locked to the Enterprise tier [citation:15][citation:20]. This tiered structure means teams can start with behavior analytics at zero cost but must upgrade to run actual experiments. Integrated within the broader Zoho ecosystem.

### Optimizely
**Type:** Enterprise experimentation platform  
Optimizely is the long-standing enterprise standard for A/B testing and feature experimentation, with deep statistical rigor and a mature governance layer. It offers both client-side web experimentation and server-side feature flags. Pricing is enterprise-quoted and typically targets larger organizations with dedicated optimization teams.

### VWO
**Type:** All-in-one experimentation and optimization  
VWO combines A/B testing, personalization, and behavioral analytics (heatmaps, recordings) in a single platform. G2's Fall 2025 report shows VWO Testing with 55% user adoption and an estimated 9-month payback period [citation:21]. Positioned as a more accessible alternative to Optimizely for mid-market teams.

### AB Tasty
**Type:** Experimentation and personalization  
AB Tasty offers A/B testing, multivariate testing, and personalization with a modular pricing structure. G2 data shows 63% user adoption with a 10-month payback period [citation:21]. The platform has been consolidating its roadmap post-merger, though it remains a strong mid-market option with published entry pricing.

### Kameleoon
**Type:** Privacy-first experimentation  
Kameleoon differentiates on compliance, with published GDPR, HIPAA, and CCPA tooling built for regulated industries rather than bolted on [citation:25]. Supports client-side and server-side experimentation alongside feature management. Published entry pricing starts at $495/month for up to 10 experiments and 50,000 tested visitors. G2 shows 62% adoption with a notably fast 5-month payback [citation:21].

### Unbounce
**Type:** Landing page builder with testing  
Unbounce specializes in landing page creation with built-in A/B testing, smart traffic routing, and conversion intelligence. Popular for marketing teams running paid acquisition campaigns. Pricing is based on traffic volume and features.

### Instapage
**Type:** Enterprise landing page platform  
Instapage provides landing page creation, personalization, and A/B testing at enterprise scale. Features include AMP pages, server-side rendering, and ad-to-page personalization. Positioned for marketing teams with significant paid media spend.

### Crazy Egg
**Type:** Behavioral analytics and testing  
Crazy Egg provides heatmaps, scrollmaps, session recordings, and A/B testing (via integration or its own testing tools). Focused on understanding visitor behavior and identifying optimization opportunities. A more accessible price point than enterprise experimentation platforms.

### Dynamic Yield
**Type:** Personalization and experimentation  
Dynamic Yield (now part of Mastercard) specializes in personalization across web, app, email, and physical channels, with A/B testing capabilities. G2 data shows 64% adoption with a 7-month payback period [citation:21]. Suited for organizations wanting cross-channel personalization rather than web-only testing.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Website Optimization and A/B Testing tools. All listed projects offer source code you can deploy on your own infrastructure.

### Controlvar
**Stack:** FastAPI / PostgreSQL / Redis | **License:** Apache-2.0  
An open-source A/B testing and feature flag platform built for self-hosting with enterprise-grade statistics. The core profile includes frequentist and Bayesian analysis, sequential testing, CUPED variance reduction, multi-armed bandits, mutual exclusion groups, and global holdouts . Targeting supports 20+ operators, gradual rollouts, and per-flag safety monitoring with automatic rollback. Ships with 16 SDKs (JavaScript, Python, Go, and others) and deployment options via Docker Compose, Helm/Kubernetes, or AWS CDK. The project explicitly states it holds no SOC 2, ISO 27001, or HIPAA attestations and claims none .  
**Best for:** Teams wanting a genuinely self-hosted experimentation platform with sophisticated statistics and no vendor lock-in.

### Bucketeer
**Stack:** Go / MySQL / Redis | **License:** Apache-2.0  
An enterprise-grade feature flag management and A/B testing platform open-sourced by CyberAgent, battle-tested in production at scale (100M+ users, billions of evaluations) [citation:2][citation:11]. Features include role-based access control, complete audit logging, environment isolation, code references (detecting flag usage in source), stale flag detection, and an interactive debugger for testing flag evaluations without deploying. Deploys via Docker Compose for lightweight setups or Helm/Kubernetes for production. OpenFeature compatible with official SDKs for Android, iOS, JavaScript, Flutter, React, Go, and Node.js [citation:11].  
**Best for:** Engineering teams wanting a production-proven, self-hosted feature flag platform with strong developer tooling and Kubernetes-native scaling.

### GrowthBook
**Stack:** TypeScript / MongoDB | **License:** MIT (core)  
A warehouse-native experimentation platform that connects to your data warehouse (BigQuery, Snowflake, Databricks) for analysis rather than ingesting events. Features include feature flags, Bayesian and frequentist statistics, CUPED, sequential testing, and multi-armed bandits. The open-source core is MIT-licensed and self-hostable; advanced features like SSO and visual editor are gated to the commercial Enterprise edition. Often paired with frontend scaffolds like Astropress for project-level flag and experiment setup [citation:7].  
**Best for:** Data teams whose primary need is rigorous experimentation tied to warehouse data, accepting that some conveniences require the paid tier.

### OpenReplay
**Stack:** Go / Python / React | **License:** Open Source (self-hosted)  
An open-source session replay and product analytics platform that pairs with experimentation workflows. Features include session replay with DevTools (network, console, state, performance), heatmaps, funnels, and journeys [citation:28]. Privacy controls include capture-time sanitization, private mode (mask all text/inputs by default), and GDPR/CCPA tooling. While not a dedicated A/B testing engine, OpenReplay provides the behavioral data (recordings, funnels, heatmaps) that teams need to validate experiment hypotheses and understand why a variant won or lost. Self-hosted so session data never leaves your infrastructure .  
**Best for:** Teams wanting self-hosted session replay and product analytics to complement their experimentation program without sending user data to a third party.

### oss-clarity
**Stack:** Python / Django | **License:** Open Source (per PyPI)  
A self-hosted session replay, heatmap, and behavioral signal tool for Django sites. Adds one script tag to capture page views, clicks, scroll depth, and sampled session recordings (via rrweb) [citation:4]. Surfaces struggle signals including rage clicks, dead clicks, hesitations, and form abandons — exactly the behavioral indicators that inform A/B test hypotheses. Privacy-focused: form fields are always masked, no IP addresses stored, Global Privacy Control honored, and recordings deleted after 30 days by default. Early release (0.1.2) with notes that APIs may change [citation:4].  
**Best for:** Django-based teams wanting lightweight, privacy-respecting behavioral analytics to inform optimization decisions.

### Localess
**Stack:** TypeScript / PostgreSQL/MySQL/SQLite | **License:** AGPL-3.0  
A free, open-source website builder and CMS with a visual drag-and-drop editor, multilingual support, and **built-in A/B testing and analytics** [citation:22]. Combines page design, content management, and experimentation in a single self-hosted platform. Deploys on your own server or via Docker, with data stored in your choice of database. No paid tiers or feature restrictions — the entire platform is AGPL-3.0 with no open-core gating. The project is relatively new but actively growing.  
**Best for:** Freelancers, small agencies, and site owners wanting an all-in-one self-hosted website builder with native A/B testing and no per-experiment costs.

### modelab
**Stack:** Python / FastAPI / PostgreSQL | **License:** Open Source (per PyPI)  
A specialized A/B testing SDK and self-hosted dashboard for **LLM systems** rather than websites. Provides deterministic variant assignment (MD5 hashing into 10,000 buckets), rollout percentages, and per-variant evaluation of success rate, latency, cost, and token usage [citation:1]. Records execution metrics automatically for OpenAI and Anthropic response formats. Deploys with Docker Compose (PostgreSQL + FastAPI + React dashboard). Zero-dependency Python SDK.  
**Best for:** Teams running A/B tests on LLM prompts, models, or configurations who want the same experimentation rigor applied to AI features.

---

## 📊 Comparison at a Glance

| Software | License | Type | Experiment Engine | Behavioral Data | Self-Hosted | Best For |
|----------|---------|------|-------------------|-----------------|-------------|----------|
| **Zoho PageSense** | Proprietary | CRO suite | ✅ (Enterprise tier) | ✅ Heatmaps/replay | ❌ | Zoho ecosystem + analytics |
| **Optimizely** | Proprietary | Enterprise experimentation | ✅ | Limited | ❌ | Large-scale enterprise testing |
| **VWO** | Proprietary | All-in-one | ✅ | ✅ Heatmaps/replay | ❌ | Mid-market full suite |
| **AB Tasty** | Proprietary | Experimentation | ✅ | Limited | ❌ | Modular mid-market |
| **Kameleoon** | Proprietary | Privacy-first testing | ✅ | Limited | ❌ | Regulated industries |
| **Unbounce** | Proprietary | Landing page testing | ✅ | Limited | ❌ | Paid acquisition campaigns |
| **Crazy Egg** | Proprietary | Behavioral analytics | Limited | ✅ Heatmaps/replay | ❌ | Behavior-first optimization |
| **Controlvar** | Apache-2.0 | Experimentation + flags | ✅ Full stats | ❌ | ✅ | Self-hosted rigorous testing |
| **Bucketeer** | Apache-2.0 | Feature flags + A/B | ✅ | ❌ | ✅ | Production-proven flags at scale |
| **GrowthBook** | MIT (core) | Warehouse-native | ✅ | ❌ | ✅ | Warehouse-tied experiments |
| **OpenReplay** | Open Source | Session replay + analytics | ❌ (companion) | ✅ Replay/heatmaps | ✅ | Self-hosted behavioral data |
| **oss-clarity** | Open Source | Session replay (Django) | ❌ (companion) | ✅ Replay/heatmaps | ✅ | Django privacy-first signals |
| **Localess** | AGPL-3.0 | Website builder + testing | ✅ Built-in | ❌ | ✅ | All-in-one site + experiments |
| **modelab** | Open Source | LLM A/B testing | ✅ LLM-focused | ❌ | ✅ | Testing AI prompts/models |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Website Optimization or A/B Testing tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for dedicated A/B testing engines is smaller than for feature flags; many tools focus on behavioral analytics (session replay, heatmaps) that complement rather than replace experimentation platforms.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
