# Influx Technology Design System — Full Reference
# v0.2 — Last updated 2026-03-20

---

## CSS Custom Properties (complete block)

```css
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;700&family=Inter:wght@400;600&family=IBM+Plex+Mono:wght@400;500&display=swap');

:root {
  /* Type Scale */
  --text-4xl: 4.75rem;    /* 76px */
  --text-3xl: 3.5625rem;  /* 57px */
  --text-2xl: 2.6875rem;  /* 43px */
  --text-xl:  2rem;       /* 32px */
  --text-lg:  1.5rem;     /* 24px */
  --text-base: 1.125rem;  /* 18px */
  --text-sm:  1rem;       /* 16px */
  --text-xs:  0.875rem;   /* 14px */

  /* Fonts */
  --font-heading: 'Outfit', system-ui, sans-serif;
  --font-body:    'Inter', system-ui, sans-serif;
  --font-mono:    'IBM Plex Mono', 'Courier New', monospace;

  /* Weights */
  --font-regular:  400;
  --font-semibold: 600;
  --font-bold:     700;

  /* Line Heights */
  --leading-tightest: 1.05;
  --leading-tight:    1.1;
  --leading-snug:     1.15;
  --leading-heading:  1.2;
  --leading-kicker:   1.4;
  --leading-normal:   1.5;
  --leading-relaxed:  1.6;

  /* Spacing (8px base grid) */
  --space-0-5: 0.25rem;   /* 4px */
  --space-1:   0.5rem;    /* 8px */
  --space-2:   1rem;      /* 16px */
  --space-3:   1.5rem;    /* 24px */
  --space-4:   2rem;      /* 32px */
  --space-5:   2.5rem;    /* 40px */
  --space-6:   3rem;      /* 48px */
  --space-8:   4rem;      /* 64px */
  --space-10:  5rem;      /* 80px */
  --space-12:  6rem;      /* 96px */
  --space-16:  8rem;      /* 128px */

  /* Brand Colours */
  --color-primary:      #4FA31A;  /* Brand green — CTAs, kickers, active states */
  --color-bg-primary:   #050F02;  /* Dark background */
  --color-text-primary: #E9E9E9;  /* Text on dark */

  /* Product Colours (400 UI stops) */
  --color-rexgen:          #CCA800;  /* Mikado Yellow — REXGEN, REBEL, REXDESK */
  --color-k-series:        #CE4C12;  /* Giants Orange — K-TC, K-Box, K-AN8, K-Volt, K-CAL */
  --color-rexgen-pro:      #1498BA;  /* Blue Curacao — REXGEN Pro, Module Analyser */
  --color-rexgen-air:      #CCA800;  /* Mikado Yellow — REXGEN Air, REXBRIDGE */
  --color-dialog:          #1AA082;  /* Light Sea Green — DIALOG, Streamlog */
  --color-rebel-dash:      #CC1E1E;  /* Chilli Red — REBEL Dash (legacy) */
  --color-h-box:           #C4108C;  /* Brilliant Rose — H-Box (legacy) */
}
```

---

## Influx Green Ramp

| Stop | Hex | Usage |
|---|---|---|
| 50  | #F2FAE8 | Light backgrounds, subtle fills |
| 100 | #DAEFC0 | Hover on light bg, tag backgrounds |
| 200 | #A8D96B | Decorative, illustrations |
| 300 | #78C220 | Logo variant (higher vibrancy) |
| **400** | **#4FA31A** | **Brand primary — CTAs, kickers, active states, links** |
| 500 | #2E7D14 | Button hover/pressed |
| 600 | #1E5C0D | Borders, card outlines on dark bg |
| 700 | #123D08 | Dark borders, subtle separators |
| 800 | #0A2504 | Very dark accents |
| 900 | #050F02 | Near-black with green tint |

---

## Neutral Ramp

| Stop | Hex |
|---|---|
| 0   | #FFFFFF |
| 50  | #F7F8F7 |
| 100 | #EAECE9 |
| 200 | #D0D4CF |
| 300 | #AEB4AD |
| 400 | #878F86 |
| 500 | #636B62 |
| 600 | #454D44 |
| 700 | #2D332C |
| 800 | #181C18 |
| 900 | #0C0E0C |

Dark bg: `#050F02` (green 900 stop — used on the website).

---

## Product Colour Ramps

Logo (300 stop) vs UI (400 stop) — the split is intentional; use the right one.

### Mikado Yellow (REXGEN, REXGEN 2, REXGEN 2 IMU, REBEL, REXDESK)
| Stop | Hex |
|---|---|
| 300 (logo) | #F5CC00 |
| **400 (UI)** | **#CCA800** |
| 500 | #A38700 |

### Giants Orange (K-TC, K-Box, K-AN8, K-Volt, K-IEPE, K-CAL)
| Stop | Hex |
|---|---|
| 300 (logo) | #EA6E2E |
| **400 (UI)** | **#CE4C12** |
| 500 | #A83A0E |

### Blue Curacao (REXGEN Pro, Module Analyser)
| Stop | Hex |
|---|---|
| 300 (logo) | #28BCDE |
| **400 (UI)** | **#1498BA** |
| 500 | #107A96 |

### Cornflower Blue (unassigned — formerly REXGEN Air, REXBRIDGE)
> ⚠️ REXGEN Air and REXBRIDGE have moved to Mikado Yellow (`#CCA800`). Cornflower Blue is retained here for historical reference only — do not use for any current product range.

| Stop | Hex |
|---|---|
| 300 (logo) | #5B7AEF |
| **400 (UI)** | **#3555D4** |
| 500 | #2A44AB |

### Light Sea Green (DIALOG, Streamlog)
| Stop | Hex |
|---|---|
| 300 (logo) | #2CC4A0 |
| **400 (UI)** | **#1AA082** |
| 500 | #148066 |

---

## Type Scale Reference

Ratio: 1.333 (Perfect Fourth). Base: 18px.

| Token | px | rem |
|---|---|---|
| --text-4xl | 76  | 4.75   |
| --text-3xl | 57  | 3.5625 |
| --text-2xl | 43  | 2.6875 |
| --text-xl  | 32  | 2      |
| --text-lg  | 24  | 1.5    |
| --text-base| 18  | 1.125  |
| --text-sm  | 16  | 1      |
| --text-xs  | 14  | 0.875  |

### Text Style Details

**Headlines — Outfit Regular 400**
| Style | Size | Line Height | Letter Spacing |
|---|---|---|---|
| H1 | 76px | 1.05 | -0.025em |
| H2 | 57px | 1.1  | -0.02em  |
| H3 | 43px | 1.15 | -0.015em |
| H4 | 32px | 1.2  | -0.01em  |

**Kicker — Outfit Bold 700, uppercase**
| Style | Size | Line Height | Letter Spacing | Colour |
|---|---|---|---|---|
| Kicker | 14px | 1.4 | 0.1em | #4FA31A |
| Kicker Large | 16px | 1.4 | 0.08em | #4FA31A |

**Body — Inter Regular 400**
| Style | Size | Line Height | Max Width |
|---|---|---|---|
| Body | 18px | 1.6 | 70ch |
| Body Small | 16px | 1.6 | 70ch |
| Body XS | 14px | 1.5 | none |

**Lead — Inter Regular 400** — 24px, line-height 1.5, max-width 60ch. One per section.

**Mono — IBM Plex Mono**
| Style | Size | Weight | Line Height | Letter Spacing |
|---|---|---|---|---|
| Mono | 18px | 400 | 1.5 | 0 |
| Mono Small | 16px | 400 | 1.5 | 0 |
| Mono Tag | 14px | 500 | 1.4 | 0.02em |

Mono Tag for: INF-XXXXX codes, SKUs, protocol labels in badges.

---

## Responsive Headlines

| Style | Desktop (1024+) | Tablet (640–1023) | Mobile (<640) |
|---|---|---|---|
| H1 | 76px | 57px | 38px |
| H2 | 57px | 43px | 32px |
| H3 | 43px | 36px | 28px |
| H4 | 32px | 28px | 24px |
| Lead | 24px | 22px | 20px |

```css
h1 { font-size: clamp(2.375rem, 1.5rem + 3.5vw, 4.75rem); }
h2 { font-size: clamp(2rem, 1.25rem + 2.8vw, 3.5625rem); }
h3 { font-size: clamp(1.75rem, 1.25rem + 2vw, 2.6875rem); }
h4 { font-size: clamp(1.5rem, 1.15rem + 1.5vw, 2rem); }
```

---

## Spacing Reference

All multiples of 8px. Card grid gap is 12px (deliberate exception).

| Token | px | rem |
|---|---|---|
| --space-0-5 | 4   | 0.25 |
| --space-1   | 8   | 0.5  |
| --space-2   | 16  | 1    |
| --space-3   | 24  | 1.5  |
| --space-4   | 32  | 2    |
| --space-5   | 40  | 2.5  |
| --space-6   | 48  | 3    |
| --space-8   | 64  | 4    |
| --space-10  | 80  | 5    |
| --space-12  | 96  | 6    |
| --space-16  | 128 | 8    |

**Common patterns:**
- Section header stack: Kicker → 8px → Headline → 16px → Lead → 48px → content
- Section padding: 80px vertical desktop, 48px mobile
- Card padding: 24px desktop, 16px mobile
- Card grid gap: 12px
- Button padding: 12px 24px standard, 10px 20px small
- CTA group gap: 12px

---

## Layout

| Property | Value |
|---|---|
| Container max-width | 1200px |
| Page padding desktop | 48px |
| Page padding mobile | 16px |

**Grid:**
| Viewport | Columns | Gap | Margin |
|---|---|---|---|
| Desktop (1024+) | 12 | 32px | 48px |
| Tablet (640–1023) | 6 | 24px | 32px |
| Mobile (<640) | 4 | 16px | 16px |

**Breakpoints:** sm 640px, md 768px, lg 1024px, xl 1280px

---

## Logo Assets Reference

| File | Size | Use |
|---|---|---|
| `assets/logos/logo-full-light.svg` | 91×26 | Full logo, light text (`#F7F8F7`) — dark backgrounds |
| `assets/logos/logo-full-dark.svg` | 91×26 | Full logo, dark text (`#0C0E0C`) — light backgrounds |
| `assets/logos/logo-sm-light.svg` | 50×14 | Small logo, light text (`#F7F8F7`) — dark backgrounds, tight spaces |
| `assets/logos/logo-sm-dark.svg` | 50×14 | Small logo, dark text (`#0C0E0C`) — light backgrounds, tight spaces |
| `assets/logos/logomark.svg` | 26×26 | 3×3 grid symbol, green — standard contexts |
| `assets/logos/logomark-sm.svg` | 14×14 | 3×3 grid symbol, green — very small contexts |
| `assets/decorative/grid-pattern.svg` | 260×260 | Decorative 3×3 grid, `#0A2504` fill / `#78C220` stroke |

Logomark colour is always `#4FA31A` — text colour changes, mark does not.
Minimum clear space = width of one square in the 3×3 grid.
Never rotate, stretch, recolour or add effects.

---

## Do / Don't

**Do:**
- Outfit for headlines and kickers only
- Inter Semi Bold 600 for buttons and navigation
- IBM Plex Mono for product codes, protocol labels, data values
- `text-transform: uppercase` for kickers (never type them in caps manually)
- Zero border radius everywhere
- 8px grid for all spacing
- Green sparingly for maximum impact
- Product colours only for their assigned product ranges
- `clamp()` for responsive headlines

**Don't:**
- Outfit for buttons or body text
- Bold 700 on headlines (Regular 400 only; Bold is kickers only)
- All-caps headlines
- Mono for body text
- Font sizes outside the scale
- Arbitrary spacing values
- Rounded corners on buttons, cards, inputs or tags
- Product colours for generic UI elements
- `#2DB24A` anywhere (deprecated legacy green)
- Pure white (`#FFFFFF`) for body text on dark backgrounds — use `#E9E9E9`
