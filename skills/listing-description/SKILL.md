---
name: listing-description
description: Generates compliant, cliché-free listing descriptions for any market. References fair-housing-overlay for compliance. Output is 145 words, MLS-feed-ready, with a localized closing line that doesn't mention schools.
author: Al Pinder, Victoria Pinder
version: 1.0.0
---

# Listing Description

Writes a 145-word listing description in under two minutes. Compliant by default. References [`fair-housing-overlay`](../fair-housing-overlay/) for the underlying rule set.

## When to use this skill

You just took a new listing. You have the address, beds/baths, square footage, lot, year built, and three standout features. You need a description that:
- Hits the MLS field cap exactly
- Avoids the dead-cliché filter (won't get downranked by Realtor.com / Zillow)
- Stays inside Fair Housing
- Localizes the close without referencing schools

This skill replaces 20 minutes of writing-and-rewriting with 90 seconds.

## Prompt

```
You're writing a [CITY] [STATE] listing description for me, an agent.

REQUIRED COMPLIANCE (load fair-housing-overlay if available):
- NO clichés: never use "must-see", "won't last", "rare opportunity",
  "hidden gem", "priced to sell", "act now"
- NO school references
- NO demographic targeting or steering language
- NO "safe", "quiet" (replace with "low-traffic street")
- ALWAYS positive

REQUIRED OUTPUT:
- 145 words exactly (MLS field cap)
- Tone: warm, specific, factual
- Open with the strongest objective feature
- Middle: floor plan, indoor flow, key spaces
- End: ONE line about [CITY] life that doesn't mention schools
  (use commute time to a major employer, or a public park, or a downtown
  amenity, or a commute-to-coast time — all objective, all FH-clean)

PROPERTY DATA:
- Address: [ADDRESS]
- Beds/Baths: [BEDS] / [BATHS]
- Square footage: [SQFT]
- Lot size: [LOT] acres
- Year built: [YEAR]
- Standout features (pick 3):
  - [FEATURE 1]
  - [FEATURE 2]
  - [FEATURE 3]
- Major nearby employer / park / amenity for the close: [ANCHOR]

Write the description.
```

## What good output looks like

See [`examples/`](examples/) for two anonymized real-world outputs:
- A $300-400K Greenville home (suburban, screened porch)
- A $200K-under Pitt-County rural home (acreage, workshop)

Both are 145 words exactly. Both pass MLS feed filters. Both have FH-compliant local-life closing lines.

## Variants

**For luxury ($700K+):**
Add this line to the prompt: `Tone shifts to specific-detail-rich, longer sentences, restraint over hype.`

**For new construction:**
Add: `Lead with build year, builder name (if requested), and warranty terms. End with delivery timeline (move-in date) instead of city-life line.`

**For investor-targeted:**
Add: `Replace city-life close with cap rate (if known), monthly rent (if known), or 1-mile rental comp range.`

## Companion content

YouTube Episode 3: [Write 10 Listing Descriptions in 10 Minutes](https://youtube.com/@theprosperityagents)

## Compliance notes

Loads the `fair-housing-overlay` skill rules. If you don't have that skill loaded, the prompt above includes the same compliance lines inline. Either way: school refs, scarcity clichés, and demographic targeting are blocked.

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
