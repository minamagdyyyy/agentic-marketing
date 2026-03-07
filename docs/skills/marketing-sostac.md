# `marketing-sostac`

## Overview

Builds a full SOSTAC marketing plan that can guide all later execution.

## When to use it

Use `/marketing-sostac` when:
- you need a full marketing plan
- your current tactics feel disconnected
- you want strategy saved to files for future sessions
- a coordinator routed you here

## Inputs to prepare

- brand context
- website and product overview
- target audience
- goals and KPIs
- competitors
- budget and team constraints

## What the interaction looks like

The skill runs:
1. Auto-Discovery research
2. Situation
3. Objectives
4. Strategy
5. Tactics
6. Action
7. Control

It resumes from the first incomplete phase and confirms each phase before saving.

## Deliverables

- six SOSTAC phase files
- auto-discovery brief
- executive plan summary

## Output locations

```text
brands/{brand-slug}/sostac/
```

Including:
- `00-auto-discovery.md`
- `01-situation.md`
- `02-objectives.md`
- `03-strategy.md`
- `04-tactics.md`
- `05-action.md`
- `06-control.md`
- `plan-summary.md`

## Related skills

- `marketing-agency`
- `product-marketing-context`
- all execution specialists

## Sample prompts

```text
/marketing-sostac
Build a complete marketing plan for our brand.
```

```text
/marketing-sostac
Continue the existing SOSTAC plan for Acorn Legal from the next incomplete phase.
```

```text
/marketing-sostac
We sell a workflow tool for recruiting teams. We need a strategy before investing more in SEO, paid ads, and email.
```
