---
name: offer-counter
description: Generates a counter-offer reply email that holds price firm but signals flexibility on close date, inspections, and appliances. Tone: collegial, never pressure-y. Designed for small markets where you'll see the same listing agents every week.
author: Al Pinder, Victoria Pinder
version: 1.0.0
---

# Offer Counter

Drafts the email reply to a counter-offer. Most agents under-write this email — it's half the negotiation, but they treat it as a formality. This skill writes it like a 20-year agent would.

## When to use this skill

Your buyer made an offer. The seller countered. You need to reply in a way that:
- Holds your buyer's position on price
- Signals flexibility on terms you don't actually care about (close date, appliances, minor inspection items)
- Stays collegial — the listing agent will be on the other side of your next deal too
- Includes no clichés or pressure language
- Looks like a real lawyer-broker professional, not an AI

This skill writes that reply in 40 seconds.

## Prompt

```
I'm a real estate agent. My buyer offered $[X] on a list price of $[Y].
The seller countered at $[Z] with [TERMS].

Write a reply email to the listing agent [NAME if known] that:
- Holds my position on price (we are NOT raising)
- Signals flexibility on these terms (pick the ones that don't matter to my buyer):
  [ ] Close date
  [ ] Appliances (which appliances we'll let go)
  [ ] Minor inspection items (under $[THRESHOLD])
  [ ] Earnest money increase
  [ ] Settlement attorney choice
- Tone: collegial, no pressure, respect the listing agent's professionalism
- Length: short — 4 to 6 sentences max
- Sign-off: warm but professional

CONTEXT:
- This is a small market where I work with [NAME] regularly
- I don't want to bluff or make threats
- I want to leave room for one more counter

Write the email.
```

## What good output looks like

See [`examples/`](examples/) for an anonymized real-world output:
- Buyer offered $385K, seller countered $405K
- Reply held at $385K, flexed on close date + appliances
- 6 sentences, collegial tone, no clichés

## Variants

**Hard-no counter (we're walking):**
Add: `My buyer is firm at the original offer. Write a reply that politely declines the counter, leaves the door open if seller reconsiders, and includes our deadline for a response.`

**Multiple-offer scenario:**
Add: `There are [N] other offers. The listing agent has hinted at highest-and-best. Write a reply that raises by [AMOUNT] but flags the maximum and signals we will not chase past it.`

**Seller-side (you're representing the listing):**
Add: `Reverse the prompt — I'm the listing agent receiving a counter to my counter. Write the reply from the seller's side: hold price, identify which seller-side flex points to offer.`

## Companion content

YouTube Episode 4: [Counter Every Offer Like a 20-Year Pro](https://youtube.com/@theprosperityagents)

## Compliance notes

References [`fair-housing-overlay`](../fair-housing-overlay/) — never describe the buyer's intent in protected-class terms ("they're a young family looking for a starter home" is a violation; "they're a buyer with an approved-financing letter at this price band" is fine).

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
