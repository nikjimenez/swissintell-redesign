# Mockup · Homepage

A complete, working HTML prototype of the Swissintell homepage redesign.

## Open it

```bash
open index.html            # macOS
start index.html           # Windows
xdg-open index.html        # Linux
```

Or simply double-click `index.html`. No server, no build, no dependencies.

## What's inside

A single self-contained HTML file that implements the full homepage:

| Section | Purpose |
|---------|---------|
| Top bar | Address + language switcher (EN / FR / DE) |
| Navbar | Logo, navigation, CTAs (Members Login · Become a Member) |
| Hero | Positioning statement + decorative radar visual |
| Stats | 20+ years · 350+ members · 50+ events · 3 languages |
| Upcoming Events | 1 featured + 3 regular event cards |
| Intelligence Verticals | 8 curated content areas |
| Members Area | Premium access preview (simulates the gating) |
| Press Review | Latest briefings + topic sidebar |
| Newsletter | Weekly digest signup |
| Partners | Institutional sponsors |
| Footer | Full site map |

## Technical notes

- **Typography:** Calibri is loaded from `fonts.cdnfonts.com`. System fallbacks (Segoe UI, Helvetica Neue, Arial) render cleanly if the CDN fails.
- **Icons:** All icons are inlined SVGs in a `<symbol>` sprite at the top of `<body>`. No external dependencies.
- **Logo:** Embedded inline as a `<symbol>` for portability. The source file lives in `assets/logo.svg`.
- **Responsive:** Breakpoint at 960px collapses the grid to single-column on mobile.
- **No JavaScript:** the mockup is fully static. Interactions (hovers, transitions) are CSS-only.

## Assets

- `assets/logo.svg` — Original brand logo (red on transparent). Use this file for any place that needs the logo as a separate asset (e.g., favicon source, marketing materials, WordPress media library).

## Relationship to the design system

The mockup was built first; the design system was then extracted from it. Every color, spacing value, typography choice and component in this mockup corresponds to a token documented in `/design-system`.

When implementing in WordPress, the recommended workflow is:
1. Import `design-system/css/tokens.css` and `design-system/css/components.css`
2. Replicate the section structure from this mockup using the documented components
3. Replace static content with dynamic WordPress blocks / fields

## Screenshots

See `/mockup-preview-hero.png` and `/mockup-preview-full.png` at the root of the repo.
