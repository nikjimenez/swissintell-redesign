# Design System v1.0

The foundational design language for Swissintell. Two CSS files power the entire homepage — and will power every future page.

## Files

```
design-system/
├── css/
│   ├── tokens.css          Foundation variables (import first)
│   └── components.css      Reusable components (import second)
│
├── docs/
│   ├── design-system.html  Navigable visual reference (open in browser)
│   └── Swissintell_Design_System_v1.pdf
│
└── examples/
    └── usage.html          Minimal working example
```

## Install

```html
<link rel="stylesheet" href="path/to/design-system/css/tokens.css">
<link rel="stylesheet" href="path/to/design-system/css/components.css">
```

**Import order matters.** `tokens.css` must load first — `components.css` consumes its variables.

## Use

Every value in `components.css` references a token. Never hardcode values in your pages; always reference tokens:

```css
/* ✓ Correct */
.my-card {
  padding: var(--space-6);
  background: var(--color-surface-card);
  border-radius: var(--radius-base);
  box-shadow: var(--shadow-sm);
}

/* ✗ Wrong */
.my-card {
  padding: 24px;
  background: #FFFFFF;
  border-radius: 6px;
  box-shadow: 0 2px 8px rgba(13, 27, 53, 0.08);
}
```

## What's covered

### Tokens (`tokens.css`)

| Category | What's in it |
|---|---|
| **Color** | Brand red + hovers, navy surfaces, light surfaces, text, 4 tag colors |
| **Typography** | Calibri + 8-size modular scale, weights, line-heights, letter-spacing |
| **Spacing** | 4px-based scale (1, 2, 3, 4, 6, 8, 12, 16, 20, 24) |
| **Layout** | Container max-width, padding |
| **Radius** | sm, base, lg, pill |
| **Elevation** | 5 shadow levels + 2 red-glow variants |
| **Motion** | 3 durations + 2 easing curves |
| **Z-index** | nav, modal, toast |

### Components (`components.css`)

- **Buttons** — `.btn-primary`, `.btn-ghost`, `.btn-ghost-light`
- **Labels & tags** — `.label`, `.press-tag` (+ `.tag-geo`, `.tag-econ`, `.tag-tech`), `.price-badge`
- **Cards** — `.card-event`, `.card-vertical`, `.card-resource`, `.panel-elevated`
- **Forms** — `.form-newsletter`
- **Icons** — `.icon-tile`
- **Stats** — `.stat`, `.stat-number`, `.stat-label`
- **Section headers** — `.section-header`, `.section-row`
- **Surfaces** — `.surface-light`, `.surface-white`, `.surface-dark`, `.surface-gradient-dark`
- **Utilities** — `.container`, `.section-padding`

## Documentation

For the full visual reference with color swatches, type samples, do's/don'ts, and principles:

- **Interactive (navigable):** `docs/design-system.html`
- **PDF (printable):** `docs/Swissintell_Design_System_v1.pdf`

## Principles (short version)

1. **Institutional, not corporate.** Confident and serious. Strong typography. Generous whitespace.
2. **Red earns its weight.** Used sparingly — CTAs, brand marks, key emphasis. Never decorative.
3. **Dark for authority, light for content.** Navy sections project institutional weight; light sections carry editorial content. Alternation creates rhythm.
4. **Motion is a whisper.** Fast (150–250ms), one easing curve. No bouncing, no parallax, no carousels.

## Versioning

This is **version 1.0**, scoped to what the homepage needs. As more pages are built (Events listing, Members Area interior, About, etc.), new components will be added here — not duplicated elsewhere.

When the system extends:
- Add new tokens to `tokens.css` — never override existing ones
- Add new components to `components.css` following the same pattern (every value references a token)
- Update this README and the docs

## Quick reference card

```css
/* Spacing */
--space-1   4px    --space-2   8px
--space-3  12px    --space-4  16px
--space-6  24px    --space-8  32px
--space-12 48px    --space-16 64px
--space-20 80px    (section vertical rhythm)

/* Type sizes */
--font-size-xs    12px    --font-size-sm   14px
--font-size-base  16px    --font-size-lg   18px
--font-size-xl    22px    --font-size-2xl  28px
--font-size-3xl   40px    --font-size-4xl  56px

/* Brand colors */
--color-brand-red       #E01A27
--color-surface-navy    #0D1B35
--color-surface-bg      #F8F9FB
--color-text-primary    #111827

/* Motion */
--duration-fast  150ms    (button hover)
--duration-base  200ms    (most transitions)
--duration-slow  250ms    (card elevations)
```
