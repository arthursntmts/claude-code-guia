# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A single-file static reference guide (`index.html`) for Claude Code features, written in Brazilian Portuguese (pt-BR). No build system, no dependencies — open the file directly in a browser or via a local server (e.g., VS Code Live Server or `! npx serve .`).

## Architecture

Everything lives in `index.html`:

- **CSS** — embedded in `<style>` using CSS custom properties (`--bg`, `--accent`, etc.) for theming. Dark color scheme with purple accents.
- **HTML sections** — each major section has an `id` matching the nav links: `#comandos`, `#skills`, `#integracoes`, `#criar-projetos`, `#dicas`.
- **JavaScript** — inline at the bottom; handles wizard tab switching (`showTab()`), scroll-based fade-in via `IntersectionObserver`, and active nav highlighting.
- **SVGs** — all diagrams are inline `<svg>` elements with hardcoded coordinates. Arrow markers are defined with `<defs>` locally inside each SVG; marker IDs must be unique across the page.

## Key conventions

- Grid layouts use `.grid-2`, `.grid-3`, `.grid-4` classes (CSS `auto-fit` columns).
- Cards: `.card` (feature cards), `.cmd-card` (command entries), `.integration-card` (integration blocks).
- Callout styles: `.tip` (green left-border) and `.warn` (orange left-border).
- The project wizard uses `.wizard-tab` / `.wizard-panel` with `active` class toggling.
- All text content is in Portuguese (pt-BR); keep additions in the same language.
