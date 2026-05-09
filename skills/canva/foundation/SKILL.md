---
name: canva-foundation
description: One-time Canva brand kit setup for realtors. Generates the brand-asset checklist, font + color palette spec, and template-naming convention so every other Canva skill in this repo produces consistent, on-brand designs.
author: Al Pinder, Victoria Pinder
version: 1.0.0
---

# Canva Foundation — Brand Kit Setup

The one-time setup every other Canva skill assumes is in place. Run this once when you start using the Canva stack, then never again. Loads your Canva Brand Kit with the assets each downstream skill references by name.

## When to use this skill

You're an eXp agent (or any agent with Canva Pro). You've installed `quick-start-3-wins`. You're about to use `canva/just-listed`, `canva/open-house`, etc. This skill produces the spec for what your Canva account needs to have set up FIRST.

Run once. Save to your Canva. Move on.

## What it produces

A 10-item Canva Brand Kit checklist + a generation prompt that writes the spec for your specific brand:

### The 10 Brand Kit assets

1. **Logo (primary)** — square, transparent PNG, 1080×1080
2. **Logo (horizontal)** — for footers and stationery
3. **Logo (mono dark)** — single-color for over-photo overlays
4. **Logo (mono light)** — single-color for over-dark overlays
5. **Headshot — solo + paired** — Al alone, Victoria alone, Al+Victoria together
6. **Color palette** — primary, secondary, accent, dark, light (5 hex codes)
7. **Font pair** — display font (headers) + body font (everything else)
8. **License + brokerage line** — exact text for footer compliance ("Al Pinder, NC #334543 · eXp Realty LLC")
9. **NAP block** — name + address + phone + email (uniform across all designs)
10. **Disclaimers** — Fair Housing logo + Equal Housing Opportunity tagline (required on most printed real estate marketing)

### Prompt to generate YOUR spec

```
I'm a real estate agent. Generate my Canva Brand Kit spec.

INPUTS:
- Agent name(s): [NAME(S)]
- Brokerage: [BROKERAGE]
- License number(s): [LICENSE NUMBERS]
- Phone: [PHONE]
- Email: [EMAIL]
- Website: [WEBSITE]
- City/State served: [CITY], [STATE]
- Brand vibe (3 words): [e.g., "warm, specific, calm" or "bold, modern,
  confident" or "rural, honest, neighborly"]
- Existing brand colors (if any): [HEX codes or "I don't have any yet"]

REQUIRED COMPLIANCE:
- License + brokerage line MUST appear on every design (NAR + state rules)
- Equal Housing Opportunity logo placement specified for every printed asset
- NO school refs in any sample copy generated

OUTPUT (Canva-ready):
1. Color palette (5 hex codes with use-case for each)
2. Font pair (display + body, with Google Fonts equivalent if Canva-Pro
   font isn't free)
3. Logo asset list (4 variants needed, with dimensions)
4. NAP footer block (exact text, copy-paste ready)
5. Compliance footer block (exact text, copy-paste ready)
6. Template-naming convention for the rest of the Canva stack
   (e.g., "JL-{address}-{date}" for Just Listed)
```

## Canva template structure (recommended)

After the Brand Kit is set up, organize Canva templates into folders that match this repo's skill names:

```
Your Canva account/
├── 01-Just-Listed/         (canva/just-listed templates)
├── 02-Open-House/          (canva/open-house templates)
├── 03-Just-Sold/           (canva/just-sold templates)
├── 04-Coming-Soon/         (canva/coming-soon templates)
├── 05-Listing-Presentation/(canva/listing-presentation templates)
├── 06-CMA-Covers/          (canva/cma-cover templates)
├── 07-Quarterly-Postcards/ (canva/quarterly-postcard templates)
├── 08-Closing-Day/         (canva/closing-day templates)
├── 09-Price-Reduced/       (canva/price-reduced templates)
└── 99-Brand-Kit/           (logos, footers, headshots)
```

Each downstream skill assumes templates with the corresponding folder names exist.

## How a downstream skill uses this

When you run `canva/just-listed`, it produces output like:

> Open Canva → folder `01-Just-Listed` → template `JL-Square-Photo-Forward`
> Replace placeholder text:
> - HEADLINE: "Just Listed in Greenville"
> - SUBHEAD: "$385,000 · 4 Bed · 3 Bath · 0.6 acre"
> - BUTTON: "See Photos"
> Replace placeholder image with cover photo from MLS.

Without the Brand Kit + folder structure in place, the downstream skill output references templates that don't exist. Run THIS skill first.

## Companion content

YouTube Episode 11: [Canva + Claude — Replace Your Designer](https://youtube.com/@theprosperityagents)

## Compliance notes

Loads [`fair-housing-overlay`](../../fair-housing-overlay/). Specific Canva-relevant rules enforced:
- Brand Kit must include the Equal Housing Opportunity logo (FHA compliance for printed marketing)
- License + brokerage line is non-optional in any design output
- Fonts and colors are visual-only — no demographic targeting through "young / old / family" stylistic choices

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
