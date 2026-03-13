# Brand Directory Structure

This reference defines the standard directory layout for brand workspaces. Create this structure during new brand onboarding.

---

## Full Structure

```
./brands/{brand-slug}/
  brand-context.md                    # Core brand identity and context
  product-marketing-context.md        # Deep positioning reference (when created)
  sostac/                             # SOSTAC strategic planning phases
    README.md                         # SOSTAC overview and status tracker

  campaigns/                          # Named campaigns (Campaign → Channel → Content)
    {type}-{campaign-slug}/           # e.g. launch-spring-release, promotion-black-friday
      strategy.md                     # Campaign strategy doc
      channels/
        email/content/                # Email content for this campaign
        social/content/               # Social content for this campaign
        paid-ads/content/             # Ad creatives for this campaign
        seo/content/                  # SEO deliverables for this campaign
        pr/content/                   # PR deliverables for this campaign
        blog/content/                 # Blog posts for this campaign
        video/content/                # Video scripts for this campaign
        influencer/content/           # Influencer briefs for this campaign
      cro/                            # CRO work for this campaign
      retention/                      # Retention work for this campaign
      sales/                          # Sales enablement for this campaign
      pricing/                        # Pricing work for this campaign
      community/                      # Community work for this campaign
      guerrilla/                      # Growth hacks for this campaign
      referral/                       # Referral work for this campaign
      launch/                         # Launch coordination for this campaign
      performance/                    # Campaign performance reports

  channels/                           # Standalone/evergreen (no campaign)
    email/content/
    social/content/
    blog/content/                     # Evergreen blog, case studies, whitepapers
    seo/content/
    video/content/
    paid-ads/content/
    pr/content/
    influencer/content/
    content/content/                  # Meta: content strategy, calendars, briefs

  operations/                         # Standalone operational disciplines
    cro/
    retention/
    sales/
    pricing/
    community/
    guerrilla/
    referral/

  analytics/                          # Brand-level analytics
  assets/                             # Brand assets (logos, style guides, templates)
```

## Campaign Type Prefixes

`launch`, `evergreen`, `seasonal`, `promotion`, `awareness`, `growth`, `retention`, `event`

## Quick Reference: All File Paths

All paths are relative to the project root.

```
./brands/                                                    # All brands
./brands/{slug}/brand-context.md                             # Brand identity and context
./brands/{slug}/product-marketing-context.md                 # Deep positioning reference
./brands/{slug}/sostac/README.md                             # SOSTAC status tracker
./brands/{slug}/sostac/01-situation.md                       # Situation Analysis
./brands/{slug}/sostac/02-objectives.md                      # Objectives
./brands/{slug}/sostac/03-strategy.md                        # Strategy
./brands/{slug}/sostac/04-tactics.md                         # Tactics
./brands/{slug}/sostac/05-action.md                          # Action Plan
./brands/{slug}/sostac/06-control.md                         # Control & Measurement
./brands/{slug}/campaigns/{type}-{campaign-slug}/            # Named campaigns
./brands/{slug}/campaigns/{type}-{slug}/strategy.md          # Campaign strategy
./brands/{slug}/campaigns/{type}-{slug}/channels/{ch}/content/  # Campaign channel content
./brands/{slug}/campaigns/{type}-{slug}/{discipline}/        # Campaign operational work
./brands/{slug}/campaigns/{type}-{slug}/performance/         # Campaign performance
./brands/{slug}/channels/{channel}/content/                  # Standalone channel content
./brands/{slug}/operations/{discipline}/                     # Standalone operational work
./brands/{slug}/analytics/                                   # Reports and metrics
./brands/{slug}/assets/                                      # Brand assets and templates
```
