# Chew — Masterclass edition

A brand-new, single-page marketing website for **Chew**, a women-owned coffee shop, café &amp; bakery at 76 Church Street, Wynberg, Cape Town.

Built following **Jack Roberts' "Website Masterclass"** (Claude Code Course · AI Automations by Jack) — see [`MASTERCLASS_NOTES.md`](./MASTERCLASS_NOTES.md) for the extracted framework and [`best-principles.md`](./best-principles.md) for the data-driven competitive-intelligence blueprint that drove the design.

> This is a **separate** site from the existing `chew-wynberg` project — a fresh, masterclass-driven build.

## Stack
- Static, zero-build: a single `index.html` with inline CSS + vanilla JS.
- Editorial café photography generated for this build (`/assets`).
- Deployed on Vercel.

## Structure
`index.html` · `404.html` · `sitemap.html` · `sitemap.xml` · `robots.txt` · `llms.txt` · `site.webmanifest` · `vercel.json` · `/assets`

## Features
- Sticky nav with scrollspy, mobile menu (Esc to close), smooth anchor scroll
- Light/dark theme toggle (remembers choice)
- Interactive menu category tabs
- "Build your morning" order widget → prefilled WhatsApp message
- Swipeable testimonial carousel (real Google reviews)
- WhatsApp contact form, FAQ accordion, lazy-loaded map
- IntersectionObserver scroll reveals, full reduced-motion fallback
- Local SEO: `CafeOrCoffeeShop` + `BreadcrumbList` JSON-LD, OG/Twitter, sitemap, robots

## Local preview
Serve the folder with any static server, e.g. `npx serve .`
