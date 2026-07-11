# AGENTS.md — GreenLedger

Guidelines for AI agents working in this repository.

## Project overview

GreenLedger is a static, single-page sustainable finance website. It has no build step, no framework, no backend. The entire site is three files: `index.html`, `styles.css`, and `script.js`.

## Repository layout

```
greenledger-site/
├── index.html          — all markup; one file, sections ordered as rendered
├── styles.css          — all styles; organised top-to-bottom by component
├── script.js           — all JS; minimal, wrapped in IIFE
├── docs/
│   └── content-outline.md   — editorial content plan
├── AGENTS.md           — this file
└── README.md           — project overview and development notes
```

## Rules for agents

### What to do
- Keep changes contained to the three core files unless explicitly asked to add new files.
- Match the existing code style: 2-space indentation, single-quote strings in JS, kebab-case CSS class names.
- Preserve the CSS custom property system (`--green-*`, `--ink-*`). Do not introduce inline colour values.
- Keep JavaScript minimal and dependency-free.
- Accessibility: always include `alt` on images, `aria-label` on icon-only buttons, proper `<label>` on form inputs.

### What not to do
- Do not add npm, a bundler, or a framework without being asked.
- Do not add new CSS files or `<style>` blocks — put all styles in `styles.css`.
- Do not add `console.log` statements or commented-out code.
- Do not reorder the CSS file sections arbitrarily — follow the existing top-to-bottom component order.

### Commit messages
Use the imperative mood and keep the subject line under 72 characters.

Examples:
- `Add mobile nav toggle animation`
- `Fix stat card border colour in dark mode`
- `Update hero copy`

### Testing
This is a static site — open `index.html` in a browser to verify changes. Check at 320 px, 768 px, and 1280 px viewport widths.
