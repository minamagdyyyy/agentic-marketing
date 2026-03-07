# Agentic Marketing Suite

A modular suite of Claude Code skills for full-stack marketing — from strategic planning through channel execution, measurement, and automation. Each skill is a specialist that can be invoked independently or routed to by the agency coordinator.

## Installation

Install all skills into your project with one command:

```bash
npx skills add gnoviawan/agentic-marketing
```

Or install globally (available in every project):

```bash
npx skills add gnoviawan/agentic-marketing --global
```

Install a specific skill only:

```bash
npx skills add gnoviawan/agentic-marketing --skill marketing-sostac
npx skills add gnoviawan/agentic-marketing --skill marketing-seo
```

> Skills are installed to `.claude/skills/` in your project, or `~/.claude/skills/` globally. Requires [Claude Code](https://claude.ai/code).

## Quick Start

Once installed, invoke skills from Claude Code:

```
/marketing-agency    — Start here for any marketing task (routes to specialists)
/marketing-sostac    — Build a full SOSTAC marketing plan
/marketing-seo       — SEO audit, keyword research, content optimization
/marketing-email     — Email sequences, drip campaigns, newsletters, cold outbound
/marketing-paid-ads  — Google Ads, Meta Ads, campaign setup
/marketing-cro       — Landing pages, signup flows, conversion optimization
/marketing-launch    — Product launch strategy and go-to-market
/marketing-retention — Churn reduction, cancel flows, win-back campaigns
```

## Documentation

Use the docs for workflow guidance, brand workspace conventions, and a page for every skill:

- [`docs/README.md`](docs/README.md) — docs home
- [`docs/getting-started.md`](docs/getting-started.md) — where to start and what to prepare
- [`docs/workflows/new-brand-onboarding.md`](docs/workflows/new-brand-onboarding.md)
- [`docs/workflows/sostac-planning.md`](docs/workflows/sostac-planning.md)
- [`docs/workflows/implementation-after-sostac.md`](docs/workflows/implementation-after-sostac.md)
- [`docs/workflows/quick-task-without-full-plan.md`](docs/workflows/quick-task-without-full-plan.md)
- [`docs/reference/brand-workspace.md`](docs/reference/brand-workspace.md)
- [`docs/reference/deliverables-and-file-locations.md`](docs/reference/deliverables-and-file-locations.md)
- [`docs/skills/`](docs/skills/) — one page per skill

If you're new to the suite, the recommended path is:
1. Start with [`docs/getting-started.md`](docs/getting-started.md)
2. Use `/marketing-agency` to select or create a brand
3. Run `/marketing-sostac` if strategy is missing
4. Create `/product-marketing-context` before scaling content and campaigns
5. Move into the specialist skills for execution

---

## Project Structure

```
.
├── skills/                      # All skills (canonical source)
│   ├── marketing-agency/        # Entry point — coordinator
│   ├── marketing-sostac/        # Strategy — SOSTAC plan builder
│   ├── marketing-analytics/     # Measurement & tracking
│   ├── marketing-community/     # Community building
│   ├── marketing-content/       # Content marketing
│   ├── marketing-cro/           # Conversion rate optimization
│   ├── marketing-email/         # Email marketing
│   ├── marketing-guerrilla/     # Growth hacking
│   ├── marketing-influencer/    # Influencer & creator
│   ├── marketing-launch/        # Product launch & GTM
│   ├── marketing-paid-ads/      # Paid advertising
│   ├── marketing-pr/            # Digital PR & earned media
│   ├── marketing-pricing/       # Pricing strategy & packaging
│   ├── marketing-psychology/    # Behavioral science & persuasion
│   ├── marketing-referral/      # Referral & affiliate
│   ├── marketing-retention/     # Churn reduction & win-back
│   ├── marketing-sales/         # Sales enablement
│   ├── marketing-seo/           # SEO & organic search
│   ├── marketing-social/        # Social media
│   ├── marketing-video/         # Video marketing
│   └── product-marketing-context/ # Product marketing context builder
├── brands/                      # Brand workspaces (gitignored — client data)
└── skills-lock.json             # Installed skill versions
```

> `.agents/`, `.claude/`, and `brands/` are gitignored.

---

## Skills Reference

### Entry Point

#### `marketing-agency`
Digital marketing agency coordinator. The recommended starting point for any marketing task. Routes to the right specialist based on what you need — planning, channel execution, measurement, or creative. Use when working on any marketing task for a brand, even if you know which channel you want; the coordinator provides context and continuity across skills.

---

### Strategy

#### `marketing-sostac`
Full SOSTAC marketing plan builder. Runs a deep guided interview through all 6 phases and produces a structured, cross-validated plan saved to `brands/{brand-slug}/sostac/`. Starts with automated web research before the first question is asked.

| Phase | Question | Output |
|-------|----------|--------|
| 0 — Auto-Discovery | Automated research | `00-auto-discovery.md` |
| 1 — Situation | Where are we now? | `01-situation.md` |
| 2 — Objectives | Where do we want to be? | `02-objectives.md` |
| 3 — Strategy | How do we get there? | `03-strategy.md` |
| 4 — Tactics | Details of strategy | `04-tactics.md` |
| 5 — Action | Who does what, when? | `05-action.md` |
| 6 — Control | How do we monitor? | `06-control.md` |

Frameworks: SWOT+TOWS, PESTLE, Porter's Five Forces, TAM/SAM/SOM, JTBD, OKR, RACE, STP, Ansoff, Moore's positioning, AARRR, ICE scoring, 7P, RACI, PDCA, Balanced Scorecard.

See [`skills/marketing-sostac/README.md`](skills/marketing-sostac/README.md) for full documentation.

---

### Channel Execution

#### `marketing-content`
Content marketing strategist. Plans content strategy, creates editorial calendars, writes blog posts, whitepapers, case studies, ebooks, and lead magnets. Covers content pillars, Hub-Hero-Help structure, conversion copywriting for landing and pricing pages, content repurposing, distribution, and ROI measurement.

#### `marketing-email`
Email marketing specialist. Writes email sequences, drip campaigns, welcome flows, newsletters, and cold/outbound B2B email. Covers deliverability, list segmentation, automation workflows, subject line optimization, ESP selection, and outbound sequence strategy.

#### `marketing-social`
Social media specialist. Covers all platforms: Instagram, TikTok, LinkedIn, X/Twitter, Facebook, YouTube, Pinterest, Threads, Bluesky, Reddit. Creates content calendars, grows organic presence, manages community, sets up social commerce (TikTok Shop, Instagram Shopping), and designs UGC campaigns.

#### `marketing-paid-ads`
Paid advertising specialist. Google Ads, Meta Ads, LinkedIn Ads, TikTok Ads, X Ads, Pinterest Ads, and programmatic. Covers campaign setup, angle-based creative generation, platform-specific ad specs, creative iteration logging, audience targeting, ROAS optimization, retargeting, and conversion tracking.

#### `marketing-seo`
SEO specialist. Technical SEO audits, content SEO, keyword research, link building, local SEO, schema markup, site speed, and AI search optimization (GEO / Google AI Overviews). Includes evidence-based citation boost statistics for maximizing AI Overview visibility. Covers full organic search strategy from crawl to rank.

#### `marketing-video`
Video marketing strategist. Short-form (TikTok, Reels, YouTube Shorts) and long-form (YouTube). Covers channel strategy, video scripting, hooks, thumbnail optimization, video SEO, live streaming, video ad scripts, and production workflow.

#### `marketing-pr`
Digital PR and earned media specialist. Media outreach, press releases, journalist pitching, HARO/Connectively, digital PR for link building, crisis communications, brand reputation management, media kits, and thought leadership placement.

#### `marketing-influencer`
Influencer and creator partnership specialist. Influencer identification, outreach, campaign management, UGC programs, brand ambassador programs, creator affiliate programs, and creator economy strategy. Covers micro, nano, and macro influencer tiers.

#### `marketing-referral`
Referral and affiliate specialist. Designs referral programs, affiliate networks, incentive structures, partner marketing, co-marketing campaigns, and viral word-of-mouth loops. Covers commission structures, referral mechanics, and affiliate platform selection.

---

### Conversion & Revenue

#### `marketing-cro`
Conversion rate optimization specialist. Landing pages, signup flows, onboarding activation, paywalls, popups, forms, and checkout optimization. Covers hypothesis formation, test design, page structure, and CRO frameworks.

#### `marketing-retention`
Retention and churn reduction specialist. Cancel flows, dunning sequences, win-back campaigns, churn prediction, health scoring, and engagement re-activation. Keeps revenue already won.

#### `marketing-pricing`
Pricing strategy and packaging specialist. Tier design, value metric selection, pricing page optimization, willingness-to-pay research, annual/monthly discount strategy, and price increase communication.

#### `marketing-launch`
Product launch and go-to-market specialist. Launch strategy, Product Hunt campaigns, announcement cadence, press coordination, launch content, waitlist cultivation, and launch retrospectives.

#### `marketing-sales`
Sales enablement specialist. Sales decks, one-pagers, battle cards, objection handling, demo scripts, ROI calculators, champion kits, and competitive positioning for sales conversations.

#### `product-marketing-context`
Product marketing context builder. Creates and maintains the `product-marketing-context.md` file — deep positioning, customer language, jobs-to-be-done, objections, and competitive differentiation. Feeds every specialist skill for on-brand output.

---

### Growth & Measurement

#### `marketing-analytics`
Marketing analytics specialist. GA4 setup, Google Tag Manager, UTM standards, event naming conventions, tool selection (Mixpanel, Amplitude, PostHog, Segment), conversion tracking, attribution modeling, dashboards, A/B test design, funnel analysis, cohort analysis, and marketing ROI reporting.

#### `marketing-community`
Community building and management specialist. Discord, Slack, Circle, Skool, Facebook Groups, Reddit, and forums. Covers community-led growth strategy, engagement programs, community events, moderation, member retention, and turning customers into advocates.

#### `marketing-guerrilla`
Guerrilla marketing and growth hacking specialist. Unconventional tactics, viral campaign design, competitive disruption, growth experiments, product-led growth loops, and low-budget high-impact strategies. Use when budget is constrained or conventional channels are saturated.

#### `marketing-psychology`
Behavioral science and persuasion specialist. Cognitive biases, social proof patterns, urgency and scarcity mechanics, framing effects, anchoring, commitment and consistency, and loss aversion. Annotates and improves copy and UX across all channels using evidence-based psychological principles.

---

## Brand Workspaces

All brand-specific work lives in `brands/{brand-slug}/` and is **gitignored** — client data never enters version control.

```
brands/{brand-slug}/
├── brand-context.md             # Core brand info, tone, positioning
├── research-*.md                # Research files
└── sostac/                      # SOSTAC plan (created by marketing-sostac)
    ├── README.md                # Phase completion tracker
    ├── 00-auto-discovery.md     # Pre-interview research
    ├── 01-situation.md
    ├── 02-objectives.md
    ├── 03-strategy.md
    ├── 04-tactics.md
    ├── 05-action.md
    ├── 06-control.md
    └── plan-summary.md          # Executive summary (after all 6 phases)
```

---

## Skill Architecture

Each skill follows a consistent layout:

```
skill-name/
├── SKILL.md              # Instructions loaded into Claude's context
└── references/
    ├── frameworks.md     # Methodology detail for frameworks used
    ├── best-practices.md # Execution best practices
    └── *.md              # Additional domain-specific references
```

Skills use progressive context loading — only `SKILL.md` is in context when the skill is active; reference files are read on demand. This keeps each invocation lean while giving deep methodology access when needed.

---

## Adding a New Brand

1. Create `brands/{brand-slug}/brand-context.md` with the brand's core information
2. Run `/marketing-sostac` and tell it the brand slug — it will handle the rest
3. Brand files are local only (gitignored); back them up separately if needed

---

## Contributing

Skills are plain Markdown — edit any `skills/{skill-name}/SKILL.md` or its `references/` files directly. The format follows the [Agent Skills open standard](https://agentskills.io/specification).
