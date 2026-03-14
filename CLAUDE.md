# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio site for John Warmann — a single-file static site deployed to Vercel. No build step, no package manager, no framework.

## Development

Open `index.html` directly in a browser, or use any static file server:

```sh
npx serve .
# or
python3 -m http.server 8080
```

Deployment is automatic via Vercel on push to `main`.

## Architecture

The entire site lives in `index.html` — CSS, HTML, and JavaScript are all inline in one file. Structure:

- **`<style>`** — all CSS, organized with section comments (`/* === NAV === */`, etc.)
- **`<body>`** — six sections in order: `#opening`, `#foundation`, `#mobile`, `#web3`, `#ai`, `#wwm` (Work With Me)
- **`<script>`** — keyboard navigation, scroll-based active section tracking, IntersectionObserver animations, parallax backgrounds

### Design system
- Fonts: `Sora` (display headings) via `--font-display`, `JetBrains Mono` (body/mono) via `--font-mono`
- Base background: `#050507`; base text: `#e8e6e1`
- Each wave section (`wave-foundation`, `wave-mobile`, `wave-web3`, `wave-ai`) has its own accent color defined in CSS

### JS behaviors
- Arrow key / `j`/`k` keyboard navigation between the six sections
- Scroll spy updates `nav` active dot indicator
- `.animate-in` class toggled by IntersectionObserver for scroll animations
- Parallax effect on `.wave-bg` elements via scroll listener
