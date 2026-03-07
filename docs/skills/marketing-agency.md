# `marketing-agency`

## Overview

The coordinator skill. Start here when you want help choosing the right workflow or specialist.

## When to use it

Use `/marketing-agency` when:
- you are starting marketing work for a brand
- you are not sure which specialist to use
- you want the suite to check brand context and SOSTAC status first
- you want coordinated implementation after planning

## Inputs to prepare

- brand name or slug
- business goal
- timeline and constraints
- any existing strategy or campaign context

## What the interaction looks like

This skill usually:
1. selects the brand
2. reads `brand-context.md`
3. checks `product-marketing-context.md` and `sostac/`
4. routes to planning or execution

## Deliverables

- routing decision
- recommended workflow
- specialist handoff guidance
- implementation team recommendation when strategy is complete

## Output locations

This skill mainly routes work into:
- `brands/{brand-slug}/campaigns/`
- `brands/{brand-slug}/content/`
- `brands/{brand-slug}/analytics/`

## Related skills

- `marketing-sostac`
- `product-marketing-context`
- all specialist skills

## Sample prompts

```text
/marketing-agency
Help me figure out what marketing work we should do next.
```

```text
/marketing-agency
Work on Northstar AI. We have some brand context already, but I need to know whether to do SOSTAC planning first or go straight into execution.
```

```text
/marketing-agency
Our SOSTAC plan is complete. Assemble the right specialist workflow for implementation.
```
