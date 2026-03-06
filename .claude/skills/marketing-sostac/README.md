# marketing-sostac

SOSTAC Marketing Plan Builder — a guided interview skill that takes a brand through all 6 phases of the SOSTAC framework and produces a complete, structured marketing plan.

## What it does

Runs a deep guided interview through each SOSTAC phase, then saves structured documents to `brands/{brand-slug}/sostac/`. Designed to work across multiple sessions — it resumes from where it left off.

**Phases:**

| # | Phase | Question answered | Output file |
|---|-------|-------------------|-------------|
| 0 | Auto-Discovery | Automated web research before the interview starts | `00-auto-discovery.md` |
| 1 | Situation | Where are we now? | `01-situation.md` |
| 2 | Objectives | Where do we want to be? | `02-objectives.md` |
| 3 | Strategy | How do we get there? | `03-strategy.md` |
| 4 | Tactics | Details of strategy | `04-tactics.md` |
| 5 | Action | Who does what, when? | `05-action.md` |
| 6 | Control | How do we monitor and improve? | `06-control.md` |

## Frameworks applied

- **Situation:** SWOT+TOWS, PESTLE, Porter's Five Forces, TAM/SAM/SOM, Jobs-to-be-Done, 5S digital baseline
- **Objectives:** OKR structure, RACE framework, 5S cross-check, benchmark pressure-testing
- **Strategy:** STP, Moore's positioning formula, Ansoff Matrix, Porter's Generic Strategies, OVP, Value Proposition Canvas, customer journey mapping
- **Tactics:** Situational Playbook Router (brand maturity × AARRR), ICE scoring, Hub-Hero-Help content model, 7P marketing mix, 70/20/10 budget rule
- **Action:** RACI matrix, agile sprint planning, objective-and-task budgeting, risk register
- **Control:** North Star Metric, attribution model selection, PDCA, Balanced Scorecard, OKR review cadence, optimization triggers

## How to use

Invoke via Claude Code:

```
/marketing-sostac
```

Then tell it which brand to work on. It will:
1. Run automated web research on the brand and competitors
2. Present findings
3. Begin the Phase 1 interview, skipping anything already confirmed by research
4. Save each phase document after confirmation
5. Resume from the last completed phase in future sessions

## Brand workspace structure

```
brands/{brand-slug}/sostac/
├── README.md                # Phase completion tracker
├── 00-auto-discovery.md     # Research findings
├── 01-situation.md
├── 02-objectives.md
├── 03-strategy.md
├── 04-tactics.md
├── 05-action.md
├── 06-control.md
└── plan-summary.md          # Executive summary (generated after all 6 phases)
```

## Reference files

- `references/frameworks.md` — Full methodology detail for every framework used
- `references/auto-discovery.md` — Automated research command sequences
- `references/best-practices.md` — Interview and synthesis best practices
