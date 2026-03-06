# Agentic Marketing

A collection of Claude Code skills for full-stack marketing operations — from strategy through execution.

## Structure

```
.
├── .agents/skills/          # Agent-level skills (agent-browser, etc.)
├── .claude/skills/          # Claude Code skills (marketing-*)
├── brands/                  # Brand workspaces (gitignored — client data)
└── skills-lock.json         # Skill version lockfile
```

## Skills

### Strategy
| Skill | Description |
|-------|-------------|
| `marketing-sostac` | SOSTAC plan builder — full 6-phase guided interview (Situation → Objectives → Strategy → Tactics → Action → Control) |
| `marketing-agency` | Digital marketing agency coordinator and brand manager |

### Channel Execution
| Skill | Description |
|-------|-------------|
| `marketing-content` | Content marketing — blog, articles, long-form |
| `marketing-email` | Email sequences, newsletters, automation |
| `marketing-social` | Organic social strategy and content |
| `marketing-paid-ads` | Google Ads, Meta Ads, paid acquisition |
| `marketing-seo` | Technical SEO, content SEO, link building |
| `marketing-video` | Short-form and long-form video marketing |
| `marketing-pr` | Digital PR, media relations, outreach |
| `marketing-influencer` | Influencer and creator partnerships |
| `marketing-referral` | Referral programs and affiliate marketing |

### Growth & Measurement
| Skill | Description |
|-------|-------------|
| `marketing-analytics` | Tracking setup, dashboards, attribution |
| `marketing-community` | Discord, Slack, Circle community building |
| `marketing-guerrilla` | Growth hacking and unconventional tactics |

### Automation
| Skill | Description |
|-------|-------------|
| `agent-browser` | Browser automation for AI agents |

## Brand Workspaces

Brand-specific work lives in `brands/{brand-slug}/`. This directory is gitignored to keep client data out of version control. Each brand workspace contains:

```
brands/{brand-slug}/
├── brand-context.md         # Core brand information
├── research-*.md            # Research files
└── sostac/                  # SOSTAC plan phases
    ├── README.md
    ├── 00-auto-discovery.md
    ├── 01-situation.md
    └── ...
```

## Usage

Skills are invoked via Claude Code. Example:

```
/marketing-sostac   — Start or resume a SOSTAC marketing plan
/marketing-agency   — Route a marketing task to the right specialist
```
