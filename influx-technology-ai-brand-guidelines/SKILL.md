---
name: influx-technology-ai-brand-guidelines
description: >
  Apply Influx Technology brand standards whenever creating or styling any output for Influx Technology —
  documents (.docx), HTML artifacts, mockups, slide decks, reports, emails, or any other deliverable.
  Trigger this skill whenever the user mentions "Influx", "REXGEN", "K-CAL", "REXDESK", "DIALOG",
  "REBEL", "REXBRIDGE", references Influx branding, asks for something to "look on-brand", or is
  producing any professional output for Influx Technology. Also trigger when producing any internal
  report, evaluation, customer communication, or product document in an Influx context.
  Read references/design-system.md for full token values before writing any styled output.
---

# Influx Technology AI Brand Guidelines v0.1

This skill ensures all outputs match the Influx Technology design system (v0.2, updated 2026-03-20).

**Before writing any styled code or document, read `references/design-system.md`** for the complete token reference. The summary below covers the most critical rules — the reference file has all hex values, ramps, and spacing tokens.

---

## Critical Rules (memorise these)

### Brand Voice
- Company name: always **"Influx Technology"** in full, never abbreviated
- Product names always **ALL CAPS**: REXGEN, REXDESK, K-CAL, DIALOG, REBEL, REXBRIDGE
- No em dashes. No Oxford commas.
- Technical but accessible — engineers, not marketers

### Colours
| Token | Hex | Use |
|---|---|---|
| Brand primary | `#4FA31A` | CTAs, kickers, active states, links, focus rings |
| Background dark | `#050F02` | Primary dark background |
| Text on dark | `#E9E9E9` | Body text on dark backgrounds |
| **DEPRECATED** | `#2DB24A` | **Never use this** |
| **DEPRECATED** | `#091512` | **Never use this — old dark bg** |

- Green (`#4FA31A`) is an accent only — never a background
- Body text on dark is `#E9E9E9`, never pure white
- Product colours (see reference) identify product ranges only — never repurpose them

### Typography
| Role | Font | Weight |
|---|---|---|
| Headlines (H1–H4) | Outfit | Regular 400 only |
| Kickers / Labels | Outfit | Bold 700, uppercase, `#4FA31A` |
| Body / Nav / Buttons | Inter | Regular 400 / Semi Bold 600 |
| Code / Data / SKUs | IBM Plex Mono | Regular 400 / Medium 500 |

- **Buttons**: Inter Semi Bold 600, never Outfit, never all caps
- **Kickers**: always `text-transform: uppercase`, max 3–4 words, 8px gap before headline
- **Headlines**: Regular 400 only — no Bold on headlines (Bold 700 is kicker-only)

### Spacing & Layout
- 8px base grid — all spacing is multiples of 8 (exception: 12px card gap)
- Section padding: 80px top/bottom desktop, 48px mobile
- Card padding: 24px desktop, 16px mobile
- Button padding: 12px 24px standard, 10px 20px small
- Container max-width: 1200px

### Border Radius
**Zero everywhere.** No rounded corners on buttons, cards, inputs, tags, badges.
(Exceptions only for avatar circles or explicit pill indicators.)

### Section Header Stack
```
Kicker → 8px gap → Headline → 16px gap → Lead → 48px gap → content
```

---

## Product Colour Quick Reference

Use the **400 stop** for UI. Use the **300 stop** for logos only.

| Product / Range | UI colour (400) |
|---|---|
| REXGEN, REXGEN 2, REBEL, REXDESK | `#CCA800` (Mikado Yellow) |
| K-TC, K-Box, K-AN8, K-Volt, K-CAL | `#CE4C12` (Giants Orange) |
| REXGEN Pro, Module Analyser | `#1498BA` (Blue Curacao) |
| REXGEN Air, REXBRIDGE | `#CCA800` (Mikado Yellow) |
| DIALOG, Streamlog | `#1AA082` (Light Sea Green) |

---

## For HTML / CSS Artifacts

Load Google Fonts: Outfit (400, 700), Inter (400, 600), IBM Plex Mono (400, 500).

Use the CSS custom properties defined in `references/design-system.md` (`--color-primary`, `--font-heading`, etc.). Dark-theme backgrounds use `#050F02`.

Use `clamp()` for responsive headlines:
```css
h1 { font-size: clamp(2.375rem, 1.5rem + 3.5vw, 4.75rem); }
h2 { font-size: clamp(2rem, 1.25rem + 2.8vw, 3.5625rem); }
h3 { font-size: clamp(1.75rem, 1.25rem + 2vw, 2.6875rem); }
h4 { font-size: clamp(1.5rem, 1.15rem + 1.5vw, 2rem); }
```

---

## For Word Documents (.docx)

Also read the `docx` skill (`/mnt/skills/public/docx/SKILL.md`) for the technical docx-js implementation.

Apply Influx brand within docx constraints:
- **Heading font**: Outfit (embed or substitute Arial if embedding unavailable — note the substitution)
- **Body font**: Inter (embed or substitute Calibri if unavailable)
- **Heading colour**: neutral dark (`#181C18`) — test for readability at each level
- **Accent colour**: `#4FA31A` for kicker-style labels, horizontal rules, table header fills
- **Table header shading**: `#050F02` fill, `#E9E9E9` text — use `ShadingType.CLEAR`
- **Zero border radius**: no rounded corners anywhere
- **Spacing**: use the 8px grid in DXA (1 DXA = 1/1440 inch; 8px ≈ 114 DXA at 96dpi)

---

## For Presentations (.pptx)

Also read the `pptx` skill before building slides.

- Background: `#050F02` (dark) or `#F7F8F7` (light) — choose one per deck, stay consistent
- Accent bar / rule colour: `#4FA31A`
- Headline font: Outfit Regular 400
- Body font: Inter Regular 400
- Data / code callouts: IBM Plex Mono
- Zero border radius on all shapes and cards

---

## Logo Assets

**Always use the bundled SVG files** — never generate, approximate or describe the Influx logo. Read the SVG source from the `assets/logos/` directory and embed it directly.

### Selection guide

| File | Size | Text colour | Use on |
|---|---|---|---|
| `assets/logos/logo-full-light.svg` | 91×26 | `#F7F8F7` | Dark backgrounds |
| `assets/logos/logo-full-dark.svg` | 91×26 | `#0C0E0C` | Light backgrounds |
| `assets/logos/logo-sm-light.svg` | 50×14 | `#F7F8F7` | Dark backgrounds, tight spaces |
| `assets/logos/logo-sm-dark.svg` | 50×14 | `#0C0E0C` | Light backgrounds, tight spaces |
| `assets/logos/logomark.svg` | 26×26 | green only | Favicons, avatars, compact UI |
| `assets/logos/logomark-sm.svg` | 14×14 | green only | Very small contexts, badges |

### Decorative

| File | Description |
|---|---|
| `assets/decorative/grid-pattern.svg` | 260×260 3×3 grid, `#0A2504` fill / `#78C220` stroke — background texture or hero element |

### Rules
- Logomark colour is always `#4FA31A` — never recolour
- Text colour changes per variant (dark/light) — the mark does not
- Minimum clear space = width of one square in the 3×3 grid
- Never rotate, stretch, add effects or place on low-contrast backgrounds
- For HTML: read the file and embed as inline SVG (not `<img>`)
- For .docx / .pptx: read the file, convert to base64, and embed as an image

---

## Icons (Carbon Pictograms)

When icons or pictograms are needed, use IBM Carbon Design pictograms (productive style, not expressive). These are line-art pictograms that pair well with the Influx visual language.

- Standard size: 48px minimum, scale in accepted increments
- Colour: `#4FA31A` on dark backgrounds, `#0C0E0C` on light backgrounds
- Style: productive (single colour, no gradients)
- Source: `@carbon/pictograms` npm package or [Carbon pictogram library](https://carbondesignsystem.com/elements/pictograms/library/)

If bundled pictogram SVGs are available in `assets/pictograms/`, use those first. Otherwise, describe the intended pictogram by its Carbon name so the user can source it.

---

## Reference File

For full hex ramps (all 10 stops per colour), complete CSS custom properties, type scale tokens, spacing tokens, and logo file names, read:

```
references/design-system.md
```

Read it when you need a specific stop beyond the 400 UI value, or when building a complete CSS variables block.
