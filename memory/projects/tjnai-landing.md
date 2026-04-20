# Project: TJNAI Landing Site (V4)

**Repo:** https://github.com/scratchcat69/TJNAI-landing
**Domain:** tjnai.ai
**Status:** Built — awaiting content review + DNS setup before go-live
**Last updated:** March 2026

---

## Files

| File | Size | Description |
|------|------|-------------|
| index.html | ~216KB | Main V4 landing page |
| tianna-intro.html | ~65KB | Matrix rain cinematic intro |
| tianna-gallery-v4.html | ~661KB | Photo gallery (base64 images) |

---

## index.html — Architecture

**Sections (top to bottom):**
1. Nav — logo, Services / Meet Tianna / About / Get in Touch
2. Hero — 3D canvas (icosahedra + particle field), orbital ring animation, headline
3. Proof strip — scrolling ticker (Brands & Creators, iOS Developers, etc.)
4. Services — 4 glassmorphism cards with tilt on hover
5. Meet Tianna — full-bleed split layout (image + text)
6. About — animated stat counters + tech stack tags
7. CTA — grid-line background, email CTA
8. Footer

**Key JS systems:**
- Custom Canvas 2D/3D engine — perspective projection, icosahedron + octahedron wireframes, particle field
- IntersectionObserver scroll reveal
- Animated stat counters (cubic ease-out)
- 3D card tilt on mousemove
- **Matrix intro overlay** — full-screen overlay triggered by "Meet Tianna" click, no page navigation needed

**Matrix Overlay flow:**
1. Click "Meet Tianna" → overlay fades in
2. Green matrix rain falls (Phase 1: 0–1.8s)
3. Tianna's face forms from locked characters (Phase 2: 1.8–5.2s)
4. Color transitions green → full color (Phase 3: 5.2–7.0s)
5. "Meet Tianna" title + subtitle appear (6.0s) → ElevenLabs voice plays
6. CTA button + 5s countdown → navigates to tianna-gallery-v4.html

---

## ElevenLabs Voice Integration

- **Voice ID:** glrBkwkHobj1LYL2YW02 (Tianna — custom voice)
- **Voice line:** "Hello... I'm Tianna. Welcome to TJNAI."
- **Model:** eleven_turbo_v2_5
- **Settings:** stability 0.45, similarity_boost 0.80, style 0.15
- **Trigger:** T_TITLE (6.0s into animation)
- **Fetch:** Browser-side (CORS-safe), pre-fetches when overlay opens
- **Fallback:** Silently degrades if API unavailable
- **Scopes enabled:** Text to Speech, Voices, Models, History
- ⚠️ API key is embedded in index.html client-side — use backend proxy for production

---

## tianna-intro.html — Standalone Page

Same matrix animation as the overlay but as a standalone page.
Navigates to tianna-gallery-v4.html on completion.
Use this if you want a direct URL to the intro experience.

---

## tianna-gallery-v4.html — Gallery

- 12 images (base64 embedded), categories: Professional / Lifestyle / Adventure / Wellness
- Sticky filter pills
- 3-column card grid (3:4 portrait ratio)
- Premium lightbox: split layout, prev/next, keyboard nav
- Back to Home → index.html

---

## Content Pending Review (before go-live)

| Item | Current | Needs |
|------|---------|-------|
| Stats bar | 0%, iOS, JSON, NC | Real numbers from Tim |
| "Let's Build Something" CTA | No link | Calendly / contact form / email |
| "Let's Talk" CTA | No link | Same as above |
| iOS App Development service | Listed | Confirm still offered |
| info@tjnai.ai | In footer/CTA | Confirm active + routing |

---

## Deployment Checklist

- [x] Files committed to GitHub (main branch)
- [ ] GitHub Pages enabled (repo → Settings → Pages → main / root)
- [ ] Custom domain set to tjnai.ai in Pages settings
- [ ] GoDaddy A records added (×4 GitHub IPs)
- [ ] GoDaddy CNAME www → scratchcat69.github.io
- [ ] DNS propagation confirmed (~15–30 min)
- [ ] Enforce HTTPS enabled in GitHub Pages settings
- [ ] Content review completed
- [ ] Pushed final content to GitHub

---

## Build History

| Version | What changed |
|---------|-------------|
| V1–V3 | Earlier iterations (not in repo) |
| V4 | Full redesign — 3D canvas, glassmorphism, Space Grotesk |
| V4 + Tianna intro | Added matrix rain page (tianna-intro.html) |
| V4 + Gallery V4 | Gallery redesign matching V4 visual system |
| V4 + Voice | ElevenLabs TTS embedded in matrix overlay |
