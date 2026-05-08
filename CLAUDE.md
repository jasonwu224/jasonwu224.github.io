# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static personal website for Jason Wu (Physics & CS @ Brown), hosted on GitHub Pages at `jasonwu224.github.io`. No build step, no framework, no package manager — just HTML and CSS served directly.

## Development

Preview locally by opening any `.html` file in a browser, or serve with:

```bash
python3 -m http.server 8000
```

Deploy by pushing to the `main` branch — GitHub Pages serves it automatically.

## Site Structure

- **Top-level pages**: `index.html`, `photography.html`, `projects.html`, `yapping.html`, `systems.html`
- **Shared stylesheet**: `style.css` — used by all pages
- **Assets**: `assets/` — static files

## Layout

The site uses a left sidebar layout via CSS Flexbox on `<body>`. Each page has a `<nav class="sidebar">` with "Jason" (`.site-name`) at the top linking to `index.html`, followed by the five nav links. There is no `<header>` or `<footer>` element. Main content lives in `<main>`.

## Conventions

When adding a new page, copy the `<nav class="sidebar">` block from an existing page verbatim and update the `<title>` and `<meta name="description">` tags.

Nav links use relative paths from the page's location (e.g. pages in subdirectories use `../page.html`).
