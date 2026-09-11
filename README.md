# Smarpit Malik — portfolio

`smarpitm.github.io` is the live portfolio site for **Smarpit Malik**: one HTML file, zero frameworks, renders from disk, hosted on GitHub Pages off the `main` branch at `smarpitm.github.io`.

What this is: a hand-built personal site. ML & full-stack positioning, a project index, hackathon history, and a contact block. It's a profile instrument, not a product.

---

## What's in this repo

| File | What it does |
|------|--------------|
| `index.html` | The site. All content, styles, and scripts inline — no build step, no local dependencies. |

The page is a single document. No JS framework, no bundler, no local package. Fonts come from Google Fonts; the rest is static and ships as-is. That means `index.html` is the only artifact users ever see, and the only artifact git tracks.

---

## What the page is

Editorial, personal, hand-coded. A serif display face (`Instrument Serif`) for the big type, a utilitarian sans (`Inter`) for body copy, and a mono (`JetBrains Mono`) for labels and the terminal-flavored bits — config readout, nav, stats captions, the theme toggle. One accent colour throughout. Film grain as a tiny SVG noise layer. A neural-constellation canvas in the hero as ambient motion, tuned down so it stays quiet.

The page reads top-to-bottom in five sections:

- **Hero** — name, one-line positioning, a link stack (portfolio / LinkedIn / email), a tiny stats strip (repos / hacks / stars), and a typed "whoami" line that cycles a few role strings.
- **Marquee** — a slow repeating strip of topics. Decorative, not an index.
- **About** — a short lead, two paragraphs of context, plus a side card styled as `smarpit.config.yaml` (the personal-readout bit) and a second card that mirrors the GitHub README metadata in the same config-card layout.
- **Toolchain** — categorized stack rows, monospaced categories paired with inline tool chips.
- **Selected work** — a numbered, link-backed index of projects, each with a short description, a language tag, and a one-word live badge where applicable. PRAMANAM is `/001` with a live Vercel link.
- **Hackathons** — a compact grid of the eight hackathons with dates, titles, and one-line notes, plus a cadence line.
- **Contact** — a serif headline, one mailto link, and a footer that repeats GitHub + email.

---

## Theming

Two palettes, driven by `[data-theme]` on `<html>`:

- `dark` — the default moody look.
- `light` — the same page, flipped to a cream surface with ink text and the same vermilion accent.

The choice is:

1. Pulled from `localStorage.theme` if it exists.
2. Otherwise inferred from `prefers-color-scheme`.
3. Toggled by a control in the nav, labelled as a terminal readout (`lights: out` / `lights: on`).

The toggle fires a custom `themechange` event, and the canvas particle renderer listens for it so the ambient motion stays consistent with the active palette. No full-page re-render — just palette tokens and particle colours.

---

## Design notes

- **Type carries the personality.** The serif is restrained to display sizes; body copy is the sans; labels, captions, and the terminal-flavoured bits are mono. Three roles, used on purpose.
- **Structure is information.** Numbered section markers `(01)` … `(05)` only appear where they actually mean something in the page's own reading order. They're not decoration noise.
- **One accent, everywhere.** The vermilion is used for the live badge, the nav focus ring, the marquee separator, the theme toggle on hover, the `::selection`, and the code-ish labels that borrow the accent. Not everywhere, just where it's doing real signposting work.
- **Motion is deliberate and quiet.** The typewriter, the marquee, the grain, and the canvas all run at low intensity. `prefers-reduced-motion` kills animations outright.

---

## Tech stack

| Layer | What's used |
|-------|-------------|
| Page | Static HTML, all inline |
| Type | Instrument Serif, Inter, JetBrains Mono — via Google Fonts |
| Style | Hand-written CSS only, no preprocessor, no utility framework |
| Motion/behaviour | Vanilla JS — IntersectionObserver for scroll reveals, a small counter animation for the stats strip, a marquee duplicate-and-scroll loop, a typewriter, and the canvas renderer |
| Hosting | GitHub Pages on the `main` branch |

---

## What's not here

- No backend, no forms handling, no analytics.
- No build process. If you want to change the site, edit `index.html` directly.
- No component library, no framework, no npm anything. This repo is intentionally boring.

---

## Owner and contact

- **Owner:** Smarpit Malik
- **Site:** `smarpitm.github.io`
- **GitHub:** `github.com/smarpitm`
- **Email:** `smarpitmalik@gmail.com`
- **LinkedIn:** `linkedin.com/in/smarpit-malik-518250289`

---


