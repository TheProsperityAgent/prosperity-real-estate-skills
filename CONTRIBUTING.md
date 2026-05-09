# Contributing

Want to add a skill? Yes please. Here's the format.

## Skill structure

Each skill is a folder under `/skills/` containing:

```
skills/your-skill-name/
├── SKILL.md          # Required — the prompt + when-to-use
└── examples/         # Optional — anonymized real-world examples
    └── example.txt
```

## SKILL.md format

```markdown
---
name: your-skill-name
description: One sentence about what this skill does. Used by Claude to decide when to invoke.
author: Your Name
version: 1.0.0
---

# Skill title

## When to use this skill
One paragraph: the exact situation a realtor is in when this skill helps.

## What it does
Outputs you can expect. Constraints. Tone. Format.

## Prompt
\`\`\`
The exact prompt, with [PLACEHOLDERS] for the agent to fill in.
\`\`\`

## Compliance notes
- Fair Housing rules this prompt enforces
- TCPA rules this prompt enforces
- Any state-specific rules

## Companion content
Link to any associated YouTube episode, blog post, etc.
```

## Compliance gates

Every PR must:
- [ ] Pass Fair Housing review (no school refs, no demographic targeting)
- [ ] Avoid scarcity language ("won't last", "act now")
- [ ] Stay positive (no knocking towns, builders, neighborhoods, or platforms)
- [ ] Not embed real client data (anonymize examples)

## How to submit

1. Fork this repo
2. Create your skill folder under `/skills/`
3. Open a pull request with the skill + at least one anonymized example
4. We'll review within a week

## Code of conduct

Be kind. We're all just realtors trying to ship better work in less time.
