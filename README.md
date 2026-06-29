# Mira & Co. — Salon Landing Page

A fully hand-coded salon landing page built as a portfolio project, exploring claymorphism UI, scroll-driven animations, and conversion-focused design patterns.

![Mira & Co. Salon Landing Page](https://raw.githubusercontent.com/sakshamisonline/SalonLandingPage/main/preview.png)

**Live demo →** `[paste your GitHub Pages / Netlify link here]`

---

## What's in it

| Section | What it does |
|---|---|
| Hero | Claymorphism layout with real salon photo, cycling headline animation (Care → Style → Love), floating trust chips |
| Services | 5 service cards with hover tilt and clay shadow |
| Pricing | Transparent pricing list — hover any row to reveal a pre-filled booking CTA |
| Booking | 4-field form (service, date, time, mobile) with WhatsApp fallback and scarcity signal |
| Footer | Address, hours, contact |

---

## Design decisions worth noting

**Claymorphism** — every surface uses a double shadow: `inset` white shadow for the inflated feel, `drop shadow` for depth. No libraries, all pure CSS custom properties.

**Scroll-driven background** — `IntersectionObserver` watches which section occupies the viewport midpoint and transitions `body { background }` between the four palette colours (`#E8D7FF` → `#DFFFD6` → `#FFD3E8` → `#F3FFE1`). No GSAP, no scroll libraries.

**Word-swap headline** — a vertical `flex-column` of three words inside a clipped container, animated with a single `@keyframes` that slides the track upward. Avoids the collapsed-width bug that `position: absolute` word-swap implementations hit.

**Pricing → booking pre-fill** — clicking a pricing row sets the `<select>` value via JS and smooth-scrolls to the form. Reduces form friction at the exact moment purchase intent is highest.

**Button hover** — all CTAs rotate `−3deg` on hover (anticlockwise) with a spring cubic-bezier, giving a tactile clay-like feel without JS.

**Mobile** — sticky bottom booking bar on screens under 860px, since most salon traffic arrives on phone.

---

## Tech stack

- Vanilla HTML, CSS, JavaScript — zero dependencies, zero build step
- Google Fonts: Fraunces (display) + DM Sans (body)
- `IntersectionObserver` for scroll animations and background transitions
- CSS custom properties for the full design token system

---

## Colour palette

| Token | Hex | Used for |
|---|---|---|
| Lavender | `#E8D7FF` | Hero background |
| Mint | `#DFFFD6` | Services background |
| Pink | `#FFD3E8` | Pricing background |
| Lime | `#F3FFE1` | Booking background |
| Peach | `#FFD7D5` | Accent blobs |
| Ink | `#2D1A50` | Primary text + buttons |

---

## What I'd add if this were a real project

- [ ] Backend booking confirmation (Supabase or Firebase)
- [ ] Real-time slot availability from a calendar API
- [ ] GSAP ScrollTrigger for the services section
- [ ] Instagram feed embed in the gallery section
- [ ] WhatsApp Business API integration

---

## Licence

Built for portfolio purposes. The salon "Mira & Co." is fictional. Hero photo is a used from internet for no commercial use
