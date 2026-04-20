# TJNAI Memory

## Owner
**Tim Nichols** — Founder, TJNAI AI Creative Studio
Email: timothy.james.nichols@gmail.com
GitHub: scratchcat69

## Projects
| Name | What | Status |
|------|------|--------|
| **TJNAI Landing** | V4 website — tjnai.ai | Built, pending content review before go-live |
| **Tianna** | AI avatar/digital representative | Active — gallery + voice live |
| **Live Groove Finder** | Mobile app (React Native/iOS) | In Claude_Code/ |

## Key Terms
| Term | Meaning |
|------|---------|
| **TJNAI** | TJ Nichols AI — AI creative studio, North Carolina |
| **Tianna** | AI-generated digital avatar and creative rep for TJNAI |
| **V4** | Current version of the landing site (full redesign) |
| **matrix intro** | Cinematic matrix rain → Tianna face reveal page |
| **the gallery** | tianna-gallery-v4.html — Tianna photo gallery with lightbox |
| **the landing** | index.html — main TJNAI V4 landing page |

## Services TJNAI Offers
- Digital Avatars
- iOS App Development
- AI Video & Imagery
- AI Asset Packaging (JSON metadata)

## Tech Stack — TJNAI Landing Site
| Tool | Use |
|------|-----|
| Custom Canvas 2D/3D engine | 3D hero animation (no Three.js) |
| Space Grotesk + Inter | Fonts (Google CDN) |
| CSS Glassmorphism | Service cards |
| ElevenLabs TTS | Tianna's voice |
| Base64 embedded images | Self-contained HTML files |

## Infrastructure
| What | Value |
|------|-------|
| Domain | tjnai.ai (GoDaddy) |
| GitHub repo | github.com/scratchcat69/TJNAI-landing |
| Hosting (planned) | GitHub Pages → tjnai.ai |
| Email | info@tjnai.ai |

## Tianna — AI Avatar
- Voice ID (ElevenLabs): `glrBkwkHobj1LYL2YW02`
- Voice line: *"Hello... I'm Tianna. Welcome to TJNAI."*
- API key stored in: index.html (ElevenLabs — Text to Speech, Voices, Models, History scopes)
- Portrait: base64-embedded in tianna-intro.html and index.html
- Gallery: 12 images, categories: Professional / Lifestyle / Adventure / Wellness

## Site Files (GitHub repo)
| File | Description |
|------|-------------|
| index.html | V4 landing page + matrix overlay + ElevenLabs voice |
| tianna-intro.html | Standalone matrix rain → Tianna face reveal |
| tianna-gallery-v4.html | Photo gallery with filter pills + lightbox |

## Pending Before Go-Live
- [ ] Stats bar real numbers (currently 0%, iOS, JSON, NC placeholders)
- [ ] CTA link destinations ("Let's Build Something", "Let's Talk")
- [ ] Confirm iOS App Development service still relevant
- [ ] Confirm info@tjnai.ai is active and routing
- [ ] Enable GitHub Pages (repo settings → Pages → main branch / root)
- [ ] Add GoDaddy DNS records + enable Enforce HTTPS

## GitHub Pages DNS Records (GoDaddy)
| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | scratchcat69.github.io |

## Local Paths (Mac)
- Repo: ~/Downloads/TJNAI-landing
- TJNAI folder: ~/Documents/TJNAI
- Tianna assets: ~/Documents/TJNAI/Avatars/Tianna
