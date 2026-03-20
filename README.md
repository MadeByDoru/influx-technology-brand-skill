<div align="center">

```
██  ██  ██
██  ██  ██
██  ██  ██
```

# Influx Technology — AI Brand Guidelines

**A Claude skill that enforces the Influx Technology design system across every AI-generated output.**

`v0.2` · `Design System v0.2` · `2026-03-20`

---

</div>

## What this does

Upload this skill to Claude and it automatically applies Influx Technology brand standards whenever it produces styled output. No more correcting colours, swapping fonts or fixing spacing after the fact.

Covers **HTML artifacts · Word documents · Presentations · Mockups · Reports · Emails** — anything branded.

## What's inside

```
influx-technology-ai-brand-guidelines/
├── SKILL.md                              # Core brand rules and trigger logic
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
        └── grid-pattern.svg              # Decorative 3×3 grid element
```

### Design system

Full colour ramps (10 stops per colour), type scale, spacing tokens, responsive breakpoints and grid specifications. Covers Outfit, Inter and IBM Plex Mono with exact weights, sizes and line heights.

### Logo SVGs

Seven variants bundled — dark, light, small, logomark. Claude reads and embeds the real SVG directly rather than generating a placeholder.

### Icon guidance

IBM Carbon pictograms (productive style) for consistent iconography across all outputs.

## Install

1. Download `influx-technology-ai-brand-guidelines.skill` from [Releases](../../releases)
2. In Claude, go to **Settings → Customize → Skills**
3. Upload the `.skill` file
4. Done — the skill activates automatically when producing Influx-branded output

## Build from source

```bash
cd influx-technology-ai-brand-guidelines
zip -r ../influx-technology-ai-brand-guidelines.skill SKILL.md references/ assets/
```

## Licence

Internal use — Influx Technology Ltd.
