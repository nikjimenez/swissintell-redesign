# Swissintell · Redesign 2026

<div align="center">

**Web redesign project for [Swissintell](https://swissintell.ch)** — the reference association for the Swiss intelligence community.

Homepage mockup · Design system · Client deliverables

![Status](https://img.shields.io/badge/status-in%20progress-E01A27)
![Version](https://img.shields.io/badge/version-1.0-0D1B35)
![License](https://img.shields.io/badge/license-proprietary-333)

</div>

---

## About this project

This repository contains the design and frontend foundation for the redesign of **swissintell.ch**, a Swiss nonprofit association connecting 350+ intelligence professionals. The project is structured as a monorepo with two main deliverables:

- **`/mockup`** — A working HTML homepage redesign, based on the audit diagnosis.
- **`/design-system`** — Design tokens and components distilled from the mockup, ready to power the full WordPress implementation.

Additionally, `/docs` holds the client-facing reports that framed the project.

---

## Repository structure

```
swissintell-redesign/
│
├── mockup/                          Homepage redesign mockup
│   ├── index.html                   Single-file HTML mockup (open in browser)
│   ├── assets/
│   │   └── logo.svg                 Original brand logo
│   └── README.md
│
├── design-system/                   Reusable design foundation
│   ├── css/
│   │   ├── tokens.css               Foundation variables (color, type, space…)
│   │   └── components.css           Reusable components (buttons, cards…)
│   ├── docs/
│   │   ├── design-system.html       Navigable visual reference
│   │   └── Swissintell_Design_System_v1.pdf
│   ├── examples/
│   │   └── usage.html               Minimal example using the CSS files
│   └── README.md
│
├── docs/                            Client-facing project deliverables
│   ├── audit-report-EN.pdf          Executive audit (English)
│   ├── audit-report-FR.pdf          Executive audit (French)
│   ├── audit-report-ES.pdf          Executive audit (Spanish)
│   └── call-script-EN.docx          Client call script
│
├── README.md                        This file
├── LICENSE                          All rights reserved
└── .gitignore
```

---

## Quick start

### View the mockup

Open `mockup/index.html` in any modern browser. No build, no dependencies — the file is fully self-contained (fonts are loaded from a public CDN, icons are inlined as SVG).

### Use the design system

```html
<link rel="stylesheet" href="design-system/css/tokens.css">
<link rel="stylesheet" href="design-system/css/components.css">
```

A minimal working example lives in `design-system/examples/usage.html`.

### Read the design system documentation

- **Visual (navigable):** open `design-system/docs/design-system.html` in a browser
- **Print-ready PDF:** `design-system/docs/Swissintell_Design_System_v1.pdf`

---

## Project phases

| Phase | Status | Deliverables |
|-------|--------|-----|
| 01 · Audit diagnosis | ✓ Done | Executive audit reports (EN / FR / ES), call script |
| 02 · Homepage mockup | ✓ Done | `/mockup/index.html` |
| 03 · Design system v1 | ✓ Done | `/design-system/` |
| 04 · Additional pages | ▫ Pending | Events, Members Area, About, Press Review |
| 05 · WordPress implementation | ▫ Pending | Custom theme integration |

---

## Design decisions

The redesign addresses six priorities identified in the audit:

1. **Real private Members Area** — replacing the current public page with links
2. **Distinctive institutional visual identity** — replacing the generic WordPress theme
3. **Radical simplification** — consolidating 60+ categories into 8 clear verticals
4. **Native multilingual experience** (EN / FR / DE) — replacing inconsistent translations
5. **On-domain payment flow** — ending the external Infomaniak redirect
6. **Mobile-first performance** — removing heavy legacy widgets

See `docs/audit-report-EN.pdf` for the full reasoning.

---

## Stack & constraints

- **CMS:** WordPress (keep existing)
- **Frontend:** Vanilla HTML / CSS, no build step required for the mockup
- **Typography:** Calibri (brand typeface) with system fallbacks
- **Hosting:** Infomaniak (keep existing)
- **Payments backend:** Infomaniak Tickets (integrate, don't replace)

---

## Credits

Designed and developed by **Nico** for the Swissintell Association.

For questions, contact via the Swissintell team.

---

<div align="center">
<sub>© 2026 Swissintell Association · All rights reserved</sub>
</div>
