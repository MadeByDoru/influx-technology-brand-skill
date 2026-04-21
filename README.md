<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="influx-technology-ai-brand-guidelines/assets/logos/logo-full-light.svg">
  <img src="influx-technology-ai-brand-guidelines/assets/logos/logo-full-dark.svg" alt="Influx Technology" width="360">
</picture>

# AI Brand Guidelines

**A Claude skill that enforces the Influx Technology design system across every AI-generated output.**

`v0.3` · `Design System v0.3` · `2026-04-21`

[**Download latest release →**](../../releases/latest)

---

</div>

## What this does

Upload this skill to Claude and it automatically applies Influx Technology brand standards whenever it produces styled output. No more correcting colours, swapping fonts or fixing spacing after the fact.

Covers **HTML artifacts · Word documents · Presentations · Data sheets · Social posts · Mockups · Reports · Emails**. Anything branded.

## What's inside

```
influx-technology-ai-brand-guidelines/
├── SKILL.md                              # Core brand rules and trigger logic
├── colors_and_type.css                   # Paste-ready stylesheet (tokens + components)
├── references/
│   └── design-system.md                  # Full token reference
└── assets/
    ├── fonts/                            # Brand fonts bundled as TTF
    │   ├── Outfit-Regular.ttf
    │   ├── Outfit-Bold.ttf
    │   ├── Inter-Regular.ttf
    │   ├── Inter-SemiBold.ttf
    │   ├── Inter-Bold.ttf
    │   ├── IBMPlexMono-Regular.ttf
    │   └── IBMPlexMono-Medium.ttf
    ├── logos/
    │   ├── logo-full-light.svg           # Full logo, dark backgrounds
    │   ├── logo-full-dark.svg            # Full logo, light backgrounds
    │   ├── logo-sm-light.svg             # Small logo, dark backgrounds
    │   ├── logo-sm-dark.svg              # Small logo, light backgrounds
    │   ├── logomark.svg                  # 3×3 grid mark (26×26)
    │   └── logomark-sm.svg               # 3×3 grid mark (14×14)
    └── decorative/
        └── grid-pattern.svg              # Decorative 3×3 grid element
```

### Design system

Full colour ramps (10 stops per colour), type scale, spacing tokens, responsive breakpoints and grid specifications. Covers Outfit, Inter and IBM Plex Mono with exact weights, sizes and line heights.

### Fonts

All seven TTF files bundled so outputs render consistently on any machine, not only those with Google Fonts installed locally.

### Logo SVGs

Six variants bundled. Claude reads and embeds the real SVG directly rather than generating a placeholder.

### Icon guidance

IBM Carbon pictograms (productive style) for consistent iconography across all outputs. Lucide is an acceptable substitute where a lightweight UI glyph is needed.

## What's new in v0.3

- **Three greens separated.** `#2DB24A` is now logo-only (no longer deprecated). Interactive primary moves to `#78C220`. A new lime `#92EA00` is reserved for one "loud" moment per page.
- **Product-colour-per-product rule.** Single-product deliverables (a REXGEN 2 one-pager, a K-CAL deck, a DIALOG section) lead with that product range's 300 stop as the primary accent, not brand green. Green only returns for brand-wide or cross-product content.
- **Pure neutral ramp.** Neutrals are Tailwind/Radix style with no green tint. The canonical dark surface moves from `#091512` to `#09090B`.
- **Fonts bundled.** Outfit, Inter and IBM Plex Mono ship as TTF inside the skill so anything Claude generates renders correctly end-to-end.
- **New file.** `colors_and_type.css` at the skill root. Complete token block, semantic type rules and button variants, paste-ready.
- **Legacy ramps preserved.** Cornflower Blue, Chilli Red and Brilliant Rose remain in `references/design-system.md` for reference.

## Install

1. Download `influx-technology-ai-brand-guidelines.skill` from [Releases](../../releases/latest)
2. In Claude, go to **Settings → Capabilities → Skills**
3. Upload the `.skill` file
4. Done. The skill activates automatically when producing Influx-branded output.

## Build from source

```bash
cd influx-technology-ai-brand-guidelines
zip -r ../influx-technology-ai-brand-guidelines.skill \
  SKILL.md colors_and_type.css references/ assets/
```

## Licence

Internal use. Influx Technology Ltd.
