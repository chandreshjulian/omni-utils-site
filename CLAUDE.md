# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static marketing/landing page for the **OmniUtils** browser extension. No build step, no framework, no dependencies — just `index.html`, `style.css`, and `assets/`.

To preview: open `index.html` directly in a browser, or run any static file server, e.g.:

```sh
npx serve .
# or
python3 -m http.server
```

## Design system

All design tokens are CSS custom properties defined at `:root` in `style.css`:

| Token | Purpose |
|---|---|
| `--bg` / `--surface` / `--surface-2` | Dark background layers |
| `--border` | Subtle dividers |
| `--text` / `--text-muted` | Foreground hierarchy |
| `--accent` | Blue highlight (`#58a6ff`) |
| `--font-sans` | DM Sans (body) |
| `--font-mono` | JetBrains Mono (slugs, title, footer) |

The hero uses a CSS-only dot-grid + radial glow background (no JS, no images).

## Structure

- `index.html` — single-page layout: hero → 4-column feature grid → footer
- `style.css` — all styles; responsive breakpoints at 600 px (2-col) and 1024 px (4-col)
- `assets/` — extension screenshots (`format.png`, `clipboard.png`, `codec.png`, `settings.png`) and the extension icon (`icon128.png`)
