# GreenLedger

GreenLedger is a static, single-page sustainable finance website for investors, institutions, and businesses. It explains ESG integration, sustainable finance use cases, reporting frameworks, and ways to align capital with long-term environmental and social value.

## Current status

This repository contains a complete static site implementation. There is no application framework, build step, package manager, backend service, or runtime dependency to install.

## What the site includes

- **Hero section** introducing GreenLedger and its sustainable finance positioning
- **Why It Matters** section explaining ESG as long-term risk management
- **Core Pillars** covering Environmental, Social, Governance, and Impact Measurement topics
- **Use Cases** for institutional investors, corporations, development finance, and wealth advisors
- **Insights** cards for reports, analysis, and guides
- **Methodology** section referencing TCFD, GRI, SFDR, and SBTi-aligned standards
- **Contact / CTA** form with client-side validation and a simulated success state

## Technology

| Area | Implementation |
|------|----------------|
| Markup | Semantic HTML5 in `index.html` |
| Styling | Vanilla CSS in `styles.css` |
| Interactivity | Dependency-free JavaScript in `script.js` |
| Documentation | Markdown files in the repository root and `docs/` |
| Deployment | Static hosting or GitHub Pages via GitHub Actions |
## Programming languages

The codebase aligns with the stack above. It is made up of:

| Language | Files | Purpose |
|----------|-------|---------|
| HTML | `index.html` | Single-page site markup and content structure |
| CSS | `styles.css` | Visual design, layout, responsive styles, and design tokens |
| JavaScript | `script.js` | Small progressive enhancements for navigation, scrolling, and form handling |
| Markdown | `README.md`, `AGENTS.md`, `docs/content-outline.md` | Project documentation and editorial planning |

There are no framework files, package manifests, compiled assets, or backend language files in the repository.

- **Hero section** introducing GreenLedger and its sustainable finance positioning
- **Why It Matters** section explaining ESG as long-term risk management
- **Core Pillars** covering Environmental, Social, Governance, and Impact Measurement topics
- **Use Cases** for institutional investors, corporations, development finance, and wealth advisors
- **Insights** cards for reports, analysis, and guides
- **Methodology** section referencing TCFD, GRI, SFDR, and SBTi-aligned standards
- **Contact / CTA** form with client-side validation and a simulated success state

## Languages and file types

| Type | Files | Purpose |
|------|-------|---------|
| HTML | `index.html` | Page content, landmarks, navigation, sections, and form markup |
| CSS | `styles.css` | Design tokens, layout, components, responsive behavior, and visual polish |
| JavaScript | `script.js` | Sticky header state, mobile navigation, smooth UI behavior, and form handling |
| Markdown | `README.md`, `AGENTS.md`, `docs/content-outline.md` | Project documentation, agent instructions, and editorial planning |
| YAML | `.github/workflows/static.yml` | GitHub Pages deployment workflow |

## Project structure

```text
greenledger-site/
├── index.html                 # Single-page site markup
├── styles.css                 # Design system, layout, components, and responsive styles
├── script.js                  # Small progressive enhancements, no dependencies
├── docs/
│   └── content-outline.md     # Editorial outline for the page content
├── .github/
│   └── workflows/
│       └── static.yml         # GitHub Pages deployment workflow
├── .gitkeep                   # Repository placeholder file
├── AGENTS.md                  # Instructions for AI agents working in this repo
└── README.md                  # Project overview and development notes
```

## Getting started

Because the site is static, you can open `index.html` directly in a browser, or serve the repository with any static file server:

```bash
python3 -m http.server 8080
```

Then visit:

```text
http://localhost:8080
```

If you prefer Node-based tooling, you can also use a temporary static server without adding project dependencies:

```bash
npx serve .
```

## Development notes

- Keep the site dependency-free unless the project direction changes.
- Keep markup in `index.html`, styles in `styles.css`, and behavior in `script.js`.
- Preserve the CSS custom property system in `:root`, including `--green-*`, `--ink-*`, spacing, radius, shadow, and transition tokens.
- Maintain accessible labels, semantic sections, and keyboard-friendly navigation.
- The contact form currently simulates submission on the client; replace that behavior with a real endpoint when backend integration is introduced.

## Responsive behavior

| Viewport | Expected behavior |
|----------|-------------------|
| `≤ 1024px` | Large grids reduce column count where needed |
| `≤ 768px` | Mobile navigation is used and content stacks into single-column layouts |
| `≤ 480px` | Compact mobile spacing and stacked hero actions |

Recommended manual checks:

- Open the page at `320px`, `768px`, and `1280px` widths.
- Confirm the mobile navigation opens, closes, and resets after link clicks.
- Confirm the contact form validates required fields and shows the success state after submission.
- Confirm the page remains readable and navigable without relying on external assets.

## Deployment

### GitHub Pages

The repository includes `.github/workflows/static.yml`, which deploys the static site to GitHub Pages. The workflow:

- Runs on pushes to `main`
- Supports manual runs from the GitHub Actions tab
- Uploads the repository contents as a Pages artifact
- Deploys with `actions/deploy-pages`

### Other static hosts

You can also deploy the repository contents to any static host, including Netlify, Vercel, shared hosting, or a VPS. No build command is required. For nginx, point the server root at this directory and serve `index.html` for `/`.

## Content planning

The site copy follows the editorial plan in `docs/content-outline.md`. Review that file before making larger content changes so the rendered page and planning notes stay aligned.

## Goals

- Present sustainable finance topics in a clear, professional, finance-native voice
- Keep the site fast, accessible, and readable without JavaScript
- Avoid unnecessary tooling until the project needs it
- Make future handoff to a CMS, backend, or analytics layer straightforward
