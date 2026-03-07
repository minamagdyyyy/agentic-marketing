# Workflow: SOSTAC Planning

Use this workflow when you want a full strategy before running channel execution.

## Best starting command

```text
/marketing-sostac
```

You can also start with `/marketing-agency`, which will route you here when planning is missing.

## What SOSTAC creates

The planning workflow builds a complete strategy in six phases:

1. Situation
2. Objectives
3. Strategy
4. Tactics
5. Action
6. Control

Before Phase 1, it also runs **Auto-Discovery** research.

## Output files

```text
brands/{brand-slug}/sostac/
├── README.md
├── 00-auto-discovery.md
├── 01-situation.md
├── 02-objectives.md
├── 03-strategy.md
├── 04-tactics.md
├── 05-action.md
├── 06-control.md
└── plan-summary.md
```

## How the interaction works

- The skill reads existing brand files first
- It resumes from the first incomplete phase
- It asks questions in batches, not all at once
- It drafts each phase for confirmation before saving
- It uses earlier phases to shape later ones

## When to use it

Use SOSTAC when:
- you are starting serious marketing from scratch
- tactics feel disconnected
- multiple specialists will need a shared strategy
- you want a plan that can survive across sessions

## Mermaid overview

```mermaid
flowchart LR
    A[00 Auto-Discovery] --> B[01 Situation]
    B --> C[02 Objectives]
    C --> D[03 Strategy]
    D --> E[04 Tactics]
    E --> F[05 Action]
    F --> G[06 Control]
    G --> H[plan-summary.md]
```

## What to prepare

Bring as much of this as you can:
- website and pricing page
- product description
- audience and segments
- current results or baselines
- competitors
- known channel history
- budget and team constraints

## After planning

A complete plan usually leads into:
- `/product-marketing-context`
- `/marketing-content`
- `/marketing-seo`
- `/marketing-email`
- `/marketing-social`
- `/marketing-paid-ads`
- `/marketing-analytics`

## Sample prompts

### Basic
```text
/marketing-sostac
Let's build a marketing plan for our brand.
```

### Resume an in-progress plan
```text
/marketing-sostac
Continue the SOSTAC plan for BrightLedger from the next incomplete phase.
```

### Strategy-first prompt
```text
/marketing-sostac
We're scaling a B2B workflow tool and need a full 6-phase marketing plan before we invest further in content, paid ads, and lifecycle email.
```

## Related pages

- [Implementation after SOSTAC](implementation-after-sostac.md)
- [Product marketing context](../skills/product-marketing-context.md)
- [Deliverables and file locations](../reference/deliverables-and-file-locations.md)
