---
name: canva-just-listed
description: Generates a complete Just Listed package for any new MLS listing — Instagram caption, Facebook post, TikTok caption, plus a Canva design brief specifying which Brand Kit template to use, what text replaces what placeholder, and which photo to feature.
author: Al Pinder, Victoria Pinder
version: 1.0.0
---

# Canva Just Listed

The single highest-frequency Canva skill in this repo. Every new listing needs a Just Listed post. This skill writes the captions for three platforms PLUS the Canva brief, all in one shot.

## When to use this skill

You just took a listing. The MLS data is fresh. You need to post on Instagram, Facebook, and TikTok within the first 24 hours (the highest-engagement window). You also need a flyer for door-knocking the surrounding neighborhood.

This skill produces all four assets in one pass.

## Prerequisite

Run [`canva-foundation`](../foundation/) first. This skill assumes:
- Canva Brand Kit is set up (logo, fonts, colors, license footer)
- Folder `01-Just-Listed/` exists with these template names:
  - `JL-Square-Photo-Forward` (1080×1080 — IG feed + FB)
  - `JL-Story-Photo-Forward` (1080×1920 — IG/FB story, TikTok cover)
  - `JL-Flyer-Letter` (8.5×11 — door-knocking handout)

## Prompt

```
I'm a real estate agent. New listing just hit MLS. Build the full
Just Listed package.

LISTING DATA:
- Address: [ADDRESS]
- City/Town: [CITY] [STATE]
- Price: $[PRICE]
- Beds/Baths: [B] / [B]
- Square footage: [SQFT]
- Lot: [LOT] acres
- Year built: [YEAR]
- 3 standout features:
  - [FEATURE 1]
  - [FEATURE 2]
  - [FEATURE 3]
- Cover photo URL (from MLS): [URL]
- Listing URL on my website: [URL]
- Open house date (if any): [DATE / TIME]

REQUIRED COMPLIANCE (load fair-housing-overlay):
- NO school references
- NO demographic targeting ("perfect for young families" etc.)
- NO scarcity language ("won't last", "act now")
- ALWAYS positive about the neighborhood
- NO "safe" or "quiet" — use objective alternatives

OUTPUT — four pieces:

1. INSTAGRAM CAPTION (≤2200 chars, 5 hashtags, no link)
2. FACEBOOK POST (≤700 chars, conversational, ends with a question)
3. TIKTOK CAPTION (≤300 chars, 5 hashtags, punchy)
4. CANVA DESIGN BRIEF — for each of 3 templates:
   - Template name (from foundation skill)
   - Each placeholder text replaced (HEADLINE, SUBHEAD, PRICE, BEDS_BATHS, etc.)
   - Photo selection guidance (which MLS photo to feature; framing/crop notes)
   - 1-line "skip this" guidance if a template doesn't fit (e.g., flyer
     might not be needed for high-rise condo)

Hashtag rules: 5 max, mix of 1 city, 1 state, 2 listing-attribute, 1 brand.
NEVER use #DreamHome, #YourNextHome, #MustSee — banned clichés.
```

## What good output looks like

See [`examples/`](examples/) for an anonymized real-world output:
- $385K Greenville 4-bed
- IG caption (98 words, 5 hashtags)
- FB post (110 words, ends with "What's the most underrated feature in a Greenville home for you?")
- TikTok caption (47 chars + 5 hashtags)
- Canva brief for 3 templates with exact text replacements

## Variants

**Open house first weekend:**
Add: `Lead with the open house date. The post should drive traffic to the OH, not just show the listing.`

**Coming soon (pre-MLS):**
Use [`canva/coming-soon`](../coming-soon/) instead — different compliance rules apply pre-MLS (you can't claim it's "available" until it hits the feed).

**Luxury ($700K+):**
Add: `Tone shifts to specific-detail-rich. Replace TikTok output with Reels-friendly long-form (B-roll list + voiceover script).`

**New construction:**
Add: `Lead with builder name + warranty + delivery date. Photos focus on materials + finish quality, not yard.`

## Companion content

YouTube Episode 12: [Just Listed in 60 Seconds](https://youtube.com/@theprosperityagents)

## Compliance notes

Loads [`fair-housing-overlay`](../../fair-housing-overlay/). Specific Just-Listed rules enforced:
- License + brokerage line auto-included on every Canva template via Brand Kit
- Equal Housing Opportunity logo on the printed flyer (template embeds it)
- Caption never uses school refs even if the listing is in a sought-after district
- All three captions positively frame the neighborhood without ranking it

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
