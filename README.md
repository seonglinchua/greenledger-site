# GreenLedger

A professional, content-led informational website explaining sustainable finance for investors, institutions, and businesses.

## What it is

GreenLedger is a static single-page site — no framework, no build step, no backend. It covers:

- **Why sustainable finance matters** — the case for ESG integration
- **Core pillars** — Environmental, Social, Governance, and Impact Measurement
- **Use cases** — Institutional investors, corporates, development finance, wealth advisors
- **Insights** — Reports, analysis, and guides
- **Methodology** — TCFD, GRI, SFDR, and SBTi alignment
- **Contact / CTA** — Form to capture inbound interest

## Stack

| Layer | Choice |
|-------|--------|
| Markup | HTML5 (semantic, accessible) |
| Styles | Vanilla CSS with custom properties |
| Interactivity | Vanilla JavaScript (no dependencies) |
| Deployment | Any static host (Netlify, Vercel, shared hosting, VPS) |

## File structure

```
greenledger-site/
├── index.html          — all page markup
├── styles.css          — all styles
├── script.js           — mobile nav, scroll behaviour, form handling
├── docs/
│   └── content-outline.md   — editorial content plan
├── AGENTS.md           — guidelines for AI agents working in this repo
└── README.md           — this file
```

## Getting started

No install required. Open `index.html` directly in a browser, or serve with any static file server:

```bash
# Python
python3 -m http.server 8080

# Node (npx)
npx serve .
```

## Design system

All design tokens live in `styles.css` under `:root`:

| Token group | Purpose |
|-------------|---------|
| `--green-*` | Brand accent colours |
| `--ink-*` | Neutral text and surface colours |
| `--radius`, `--radius-lg` | Border radii |
| `--shadow-*` | Box shadow levels |
| `--section-y` | Vertical section padding |
| `--max-w` | Maximum content width (1120 px) |
| `--transition` | Default transition duration/easing |

## Responsive breakpoints

| Breakpoint | Behaviour |
|------------|-----------|
| ≤ 1024 px | Two-column grids collapse to two columns |
| ≤ 768 px | Mobile nav, single-column stacking |
| ≤ 480 px | Full single-column, stacked hero actions |

## Deployment

Copy the repo contents to any web root. No build step required.

For a VPS with nginx, point the server root at the repo directory and ensure `index.html` is served for `/`.

## Goals

- Clean finance-style design with restrained green accents
- Clear content hierarchy readable without JavaScript
- No external dependencies at runtime
- Easy handoff to a CMS or backend in a future version
