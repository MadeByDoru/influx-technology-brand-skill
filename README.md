# Influx Technology AI Brand Guidelines — Claude Skill

A [Claude skill](https://support.claude.com/en/articles/12512180-use-skills-in-claude) that enforces Influx Technology's design system across all AI-generated outputs — HTML, documents, presentations, mockups and more.

## What it does

When installed, Claude will automatically apply Influx Technology brand standards whenever producing styled output. This includes:

- Correct colours, typography (Outfit, Inter, IBM Plex Mono) and spacing on the 8px grid
- Product colour assignments for REXGEN, K-Series, DIALOG and all other ranges
- Zero border-radius, brand voice rules and section header stacking
- **Bundled logo SVGs** — Claude embeds the real logo rather than generating a placeholder
- **IBM Carbon pictogram guidance** for consistent iconography

## Install

### Individual (Pro / Free plans)

1. Download `influx-technology-ai-brand-guidelines.skill` from [Releases](../../releases)
2. In Claude, go to **Settings → Customize → Skills**
3. Upload the `.skill` file
4. The skill activates automatically when producing Influx-branded output

### Organisation (Team / Enterprise plans)

1. Download the `.skill` file from [Releases](../../releases)
2. An **Owner** goes to **Organisation Settings → Skills**
3. Upload the skill to provision it for all users
4. Individual users can toggle it on/off in their own **Customize → Skills**

> **Note:** Peer-to-peer sharing between individuals isn't currently supported.
> Everyone on individual plans needs to upload the skill to their own account.

## What's inside

```
influx-technology-ai-brand-guidelines/
├── SKILL.md                              # Core rules and trigger logic
├── references/
│   └── design-system.md                  # Full token reference
└── assets/
    ├── logos/
    │   ├── logo-full-light.svg           # Full logo — dark backgrounds
    │   ├── logo-full-dark.svg            # Full logo — light backgrounds
    │   ├── logo-sm-light.svg             # Small logo — dark backgrounds
    │   ├── logo-sm-dark.svg              # Small logo — light backgrounds
    │   ├── logomark.svg                  # 3×3 grid mark (26×26)
    │   └── logomark-sm.svg               # 3×3 grid mark (14×14)
    └── decorative/
        └── grid-pattern.svg              # Decorative 3×3 grid background element
```

## Build from source

```bash
cd influx-technology-ai-brand-guidelines
zip -r ../influx-technology-ai-brand-guidelines.skill SKILL.md references/ assets/
```

## Version

- **Skill**: v0.2
- **Design System**: v0.2 (2026-03-20)

## Licence

Internal use — Influx Technology Ltd.
