---
name: claude-boldtrail-bridge
description: Connects Claude to BoldTrail (formerly kvCore) so contact data, notes, opt-in status, and nurture state flow between the two systems. The "moat" episode of Season 1 — built after Victoria fought upper management for the integration path.
author: Al Pinder, Victoria Pinder
version: 0.1.0-stub
status: stub — drops with Episode 7
---

# Claude → BoldTrail / kvCore Bridge

**Coming with Episode 7 — [Claude → BoldTrail/kvCore Integration](https://youtube.com/@theprosperityagents)**

The moat episode of Season 1. The full SKILL.md drops the day this episode airs. What it'll do:

- Read BoldTrail contact data into Claude (structured)
- Push Claude-generated notes back to BoldTrail's contact note timeline
- Read consent state (`gave_consent`, `email_optin`, `text_on`) so downstream skills respect it automatically
- Flag stale leads + suggest re-engagement timing
- API auth setup (Basic Auth: `api_key:user_id`, IP-whitelisting handling)

References [`fair-housing-overlay`](../fair-housing-overlay/) and [`lead-nurture-cadence`](../lead-nurture-cadence/). The bridge is what makes nurture-cadence outputs actionable — Claude writes the touch, the bridge logs it back to BoldTrail and sets the next-touch date.

This episode covers the negotiation that unlocked the integration path with BoldTrail's API team. The story IS the differentiator — nobody else in the realtor-AI space has this connection.

Subscribe to [@theprosperityagents](https://youtube.com/@theprosperityagents) for the drop.

## Built by

Al & Victoria Pinder · ICON Agents · eXp Realty · Greenville, NC
