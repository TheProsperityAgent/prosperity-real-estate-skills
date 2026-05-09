---
name: lead-nurture-cadence
description: Generates multi-touch lead-nurture sequences (email + text + social DM) for buyers and sellers at every funnel stage. TCPA-aware — assumes prior express written consent and produces only consent-respecting cadences.
author: Al Pinder, Victoria Pinder
version: 1.0.0
---

# Lead Nurture Cadence

The follow-up plan most realtors don't have time to write. Generates a complete multi-touch nurture sequence for any lead-source + funnel-stage combination. TCPA-aware — never produces cold-blast or unsolicited content.

## When to use this skill

A new lead came in. You know they came from a specific source (your website, an open house, a referral, a Facebook ad, a Zillow inquiry). You know what they were looking at (a buyer in a price band, a seller in a town). You need a cadence — when to follow up, on what channel, with what content.

This skill writes the cadence, the content for each touch, and the spacing.

## Prompt

```
I'm a real estate agent. A new lead just came in. Build me a nurture
cadence.

LEAD CONTEXT:
- Source: [website form / open house / FB lead ad / Zillow / referral / other]
- Consent on file: [opted-in via form ✓ / opted-in via signed visitor sheet ✓ /
  unknown — DO NOT INCLUDE THIS LEAD if unknown]
- Funnel stage: [just-curious / actively browsing / pre-approved / under contract / past client]
- Side: [buyer / seller / both]
- Price band / area: [BAND], [TOWN]
- Pulse on urgency: [hot — talking to other agents] [warm — researching] [cool — 6+ months out]

OUTPUT FORMAT — multi-touch cadence over 30 days:

Day 0 (immediate response, within 5 minutes):
  Channel: [text or email — pick based on what they used]
  Content: [4-6 sentence personal reply that ANSWERS what they asked, not "let me help you"]

Day 1 (next morning):
  Channel: [...]
  Content: [...]

Day 3, Day 7, Day 14, Day 21, Day 30: [same format]

REQUIRED COMPLIANCE (load fair-housing-overlay):
- NO unsolicited cold-call or cold-text scripts (TCPA)
- NO mass-blast SMS without opt-in path
- NO school-quality references
- NO scarcity language ("won't last", "act now")
- ALWAYS-positive about every neighborhood / town / builder
- Each touch must add VALUE (a real listing, a real comp, a real market datum)
  — never "just checking in"

Write the full 30-day cadence.
```

## What good output looks like

See [`examples/`](examples/) for an anonymized real-world output:
- New buyer lead from a Facebook ad targeting Greenville $300-400K homes
- 7-touch cadence over 30 days
- Each touch includes a real listing, a real datum, or a real next-step

## Variants

**Past-client win-back (year-after-closing):**
Add: `Build a 4-touch annual cadence for a past client who closed [N] months ago. Touches: closing anniversary card, neighborhood-value-update at year 1, refer-a-friend ask at year 2, full-CMA-offer at year 3. All consent-respecting.`

**Past open-house attendees:**
Add: `Build a 5-touch cadence for an open-house attendee. Touches: thank-you within 24 hours, market-update on the same town in 7 days, similar-listings in 14 days, financing-options email in 21 days, next-open-house invite in 30 days.`

**Cold-list re-engagement (RE-CONSENT REQUIRED):**
Reject the prompt. The skill refuses to generate cold-list re-engagement content because re-engagement of a cold list without re-consent violates TCPA. Direct the agent to a re-consent path (a one-time opt-in form, a re-subscribe link, a permission-based ad) instead.

## Companion content

YouTube Episode 5: [Your Lead Nurture Just Wrote Itself](https://youtube.com/@theprosperityagents)

## Compliance notes

Loads [`fair-housing-overlay`](../fair-housing-overlay/). Critical TCPA rules:
- The skill REFUSES to produce content for leads where consent status is "unknown"
- The skill REFUSES to produce auto-dialer-compatible mass templates
- All output is owned-channel + opt-in-respected
- For SMS specifically: the skill includes a STOP-to-opt-out line in every text touch (TCPA requirement)

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
