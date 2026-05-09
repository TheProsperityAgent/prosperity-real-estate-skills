---
name: canva-open-house
description: Generates the full Open House promotional package — flyer, sign rider, IG/FB/TikTok posts, email blast, and door-knocking script. Highest FH-risk skill in the repo because OH flyers historically violate (school refs, "family-friendly" language). This skill blocks those by default.
author: Al Pinder, Victoria Pinder
version: 1.0.0
---

# Canva Open House

The highest-Fair-Housing-risk skill in the repo. Open house flyers and signs are where most agents accidentally cross a line — "family-friendly", "great schools nearby", "safe quiet neighborhood" all show up routinely. This skill produces the full OH package with those phrases hard-blocked.

## When to use this skill

You scheduled an open house. You have 5-7 days to promote it. You need:
- Printed flyer (door-knocking + listing)
- Yard-sign rider (the strip below the For Sale sign)
- 2 Instagram posts (one announce + one day-of teaser)
- 1 Facebook post
- 1 TikTok video caption + script outline
- Email to your owned list (NOT cold)
- Door-knocking 30-second script

This skill produces all 7 in one pass with FH compliance baked in.

## Prerequisite

Run [`canva-foundation`](../foundation/) first. Assumes folder `02-Open-House/` exists with templates:
- `OH-Flyer-Letter` (8.5×11)
- `OH-Sign-Rider-Strip` (24×6)
- `OH-IG-Square-Announce` (1080×1080)
- `OH-IG-Story-Day-Of` (1080×1920)
- `OH-FB-Landscape` (1200×630)

## Prompt

```
I'm a real estate agent. Build the full Open House package.

LISTING DATA:
- Address: [ADDRESS]
- City: [CITY] [STATE]
- Price: $[PRICE]
- Beds/Baths/SqFt: [B] / [B] / [SQFT]
- 3 standout features: [F1, F2, F3]
- Cover photo URL: [URL]

OPEN HOUSE DETAILS:
- Date: [DATE]
- Time: [START - END]
- My phone for RSVP: [PHONE]
- Refreshments? [yes/no]
- Lender on-site? [yes/no — name and license if yes]

REQUIRED COMPLIANCE — STRICT MODE (load fair-housing-overlay):
- NEVER reference schools by name, district, ranking, or "great schools nearby"
- NEVER use "family-friendly", "great for families", "perfect for [demographic]"
- NEVER use "safe", "quiet" (use objective: "low-traffic street", "X mph speed limit")
- NEVER use "tight-knit community", "exclusive", "private", "up-and-coming"
- NEVER use scarcity ("won't last", "rare opportunity", "act now")
- ALWAYS positive about every nearby town/neighborhood
- License + brokerage line on every printed asset
- Equal Housing Opportunity logo on flyer + sign rider

OUTPUT — seven pieces:

1. PRINTED FLYER (Canva brief for OH-Flyer-Letter)
   - HEADLINE
   - SUBHEAD (price, beds/baths/sqft)
   - 3 BULLET features (objective, FH-clean)
   - DAY/TIME block
   - RSVP block (your phone, your branded URL)
   - Photo selection (which MLS photo, framing)
   - License + brokerage footer (auto from Brand Kit)
   - EHO logo placement

2. YARD SIGN RIDER (Canva brief for OH-Sign-Rider-Strip)
   - 5-word headline max ("OPEN HOUSE THIS SUNDAY 1-3")
   - Date + time only

3. INSTAGRAM ANNOUNCE POST (Canva brief + caption)
   - 100-150 word caption
   - 5 hashtags (1 city, 1 OH, 2 listing, 1 brand)
   - No "won't last" / "rare opportunity"

4. INSTAGRAM DAY-OF STORY (Canva brief)
   - "OPEN NOW" overlay
   - Address + countdown to close time

5. FACEBOOK POST
   - 200-word conversational
   - Ends with question to drive engagement

6. TIKTOK SCRIPT OUTLINE
   - Hook (3 sec)
   - 3 features walkthrough (15 sec each)
   - CTA (5 sec)
   - Caption ≤300 chars + 5 hashtags

7. DOOR-KNOCKING 30-SEC SCRIPT
   - Opener (10 sec — friendly, neighborhood-context)
   - Pitch (10 sec — invite, no pressure)
   - Close (10 sec — flyer hand-off, walk away)

8. EMAIL TO MY OWNED LIST
   - Subject: ≤50 chars
   - Body: 100 words, includes opt-out language

Write all eight.
```

## What good output looks like

See [`examples/`](examples/) for an anonymized real-world output:
- $385K Greenville open house, Sunday 1-3
- All 8 assets, FH-compliance verified
- Flyer brief + IG square + IG story + FB post + TikTok script + door-knock + email

## Variants

**Twilight open house:**
Add: `Reframe to evening hours, emphasize lighting/landscape, photo selection prefers exterior dusk shots.`

**Brokers-only OH:**
Replace public-facing assets with broker-network email + LinkedIn post. Compliance same.

**Multi-listing same-day OH:**
Add: `I'm running [N] open houses on the same day in the same area. Build a single combined flyer with route map (Canva template OH-Tour-Map-Letter), individual property captions, and a unified email.`

## Companion content

YouTube Episode 13: [Open House Flyer — Compliant by Default](https://youtube.com/@theprosperityagents)

## Compliance notes — read this carefully

Open house marketing is the #1 source of Fair Housing complaints in real estate. The skill enforces these specific patterns:

- **School refs blocked:** any phrase containing "school", "district", "elementary", "middle school", "high school", "education" is rewritten or removed. If the agent's input includes a school name, the skill returns a warning and produces output without it.
- **Demographic implications blocked:** "great for families", "young professionals will love", "perfect starter home" — all blocked.
- **Safety language blocked:** "safe", "quiet", "secure" — replaced with objective alternatives.
- **Scarcity blocked:** "won't last", "rare", "act now" — banned.
- **Always positive:** if the agent's input describes a competing nearby town/neighborhood negatively, the skill reframes positively.

If the agent disagrees with a block, the skill explains WHY (cites the specific FHA section) and offers a compliant alternative.

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
