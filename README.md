# Drannel Website

A sleek, dark-themed **music producer portfolio website** for "Drannel" — showcasing beats, licensing options, and a contact section. Designed as a beat-seller landing page (BeatStars-style) with an interactive animated background, hero section, license pricing tiers, about section, and contact form.

## What it does

- **Hero section** — bold intro for the producer with an interactive animated background
- **Beats section** — beat listing layout (mock data; ready to wire to BeatStars or any beat API)
- **License options** — pricing tiers for beat licenses (e.g. basic / premium / unlimited)
- **About section** — producer bio
- **Contact section** — contact form for licensing inquiries
- **Header/Footer** — sticky navigation and footer
- **Dark theme** — immersive dark aesthetic with custom styling

## Tech stack

| Layer        | Tech |
|--------------|------|
| Framework    | Next.js 15 (App Router, static export) |
| Language     | TypeScript |
| UI           | React 19, Tailwind CSS, shadcn/ui (Radix primitives) |
| Icons        | Lucide React |
| Animation    | Custom interactive background components |

## Quick start

Prerequisites: Node.js 18+.

```bash
npm install          # or: pnpm install
npm run dev          # dev server at http://localhost:3000
```

Build a static export:

```bash
npm run build        # outputs to ./out
```

Serve the static build:

```bash
npx serve out        # or deploy ./out anywhere static
```

## Project structure

```
app/                # Next.js App Router (page, layout)
app/components/     # Page sections: Header, HeroSection, BeatsSection,
                    # LicenseOptionsSection, AboutSection, ContactSection,
                    # Footer, InteractiveBackground
components/ui/      # shadcn/ui primitives (button, card, input, textarea)
lib/                # Shared utilities
styles/             # Global styles
public/             # Static assets
```

## Environment variables

None required — fully client-side, no backend or API keys. The beats list is mock data; to go live, connect a real beat API (e.g. BeatStars) in `app/page.tsx` / `BeatsSection`.

## Deployment

The project is configured for static export (`output: "export"` in `next.config.mjs`). `npm run build` produces the `./out` directory, which can be hosted on GitHub Pages, Netlify, Cloudflare Pages, or any static host.

Live demo: https://girishlade111.github.io/drannelwebsite/

---

Built by Girish Lade — https://ladestack.in
