# Clickpros

**Performance creative studio — Dubai · DIFC.**

> 🔗 **Live site:** [https://clickpros.vercel.app/](https://clickpros.vercel.app/)

A 5-page marketing-studio website built as a vanilla, dependency-light static site, styled in a blend of **Apple, Framer, BMW, Nike,** and **Liquid Glass** design languages. Animated with **GSAP + ScrollTrigger** and **Motion (motion.dev)** springs. Includes a full **WCAG 2.1 AA / IS 5568** accessibility widget and an Apple/Framer-tuned **Light Mode**.

---

## Pages

| Page | Purpose |
|---|---|
| **Home** | Hero, partners marquee, services preview, Apple-style tile stack, NIKE-color service cards, industries, testimonial, CTA |
| **Services** | Strategy · Paid Media · Creator · Brand · Content · Web (deep-linked) |
| **Work** | Case grid + filter pills + recognition |
| **About** | Values · Origin · Team |
| **Contact** | Form + FAQ |

All pages share an adaptive Liquid Glass nav (with hover-dropdown sub-menus on desktop, FAQ-accordion drawer on mobile) and a unified footer.

---

## Highlights

- **Liquid Glass UI** — gradient + 0.5 px hairline + inset gloss + `backdrop-filter: blur()`
- **Adaptive nav** — flips between dark and light glass based on the section beneath it
- **Accessibility widget** — text-size zoom (7 steps), grayscale, high contrast, light mode, underline links, readable font, pause motion, big cursor; state persists in `localStorage`
- **Light Mode** — Apple/Framer-inspired palette with Framer Sky Blue (`#0099ff`) accent on light surfaces; lime brand accent (`#deff20`) preserved on intentionally-dark sections
- **Mobile** — content cards collapse into FAQ-style accordions; the Process section becomes a horizontal-scroll snap track of Liquid Glass cards
- **NIKE-style service tiles** — unique colored variants (violet, orange, pink, lime, teal, blue)
- **Dubai · DIFC** — all locale references unified

---

## Tech

- **Vanilla HTML / CSS / JS** — no build step, no framework
- **GSAP 3 + ScrollTrigger** — entrance, reveal-on-scroll, parallax, counters
- **Motion (motion.dev) 11.11.17** — soft hover springs (loaded with 2.5 s timeout + GSAP fallback)
- **Inter** — clean BMW-style sans-serif (Google Fonts)
- **Vercel** — static hosting

---

## Performance / fail-soft

- rAF-debounced `scroll` handler with `passive:true`
- GPU-accelerated marquee (`translate3d`)
- Counters & reveals use `once:true` ScrollTrigger
- Motion has a 2.5 s timeout with GSAP fallback springs
- `boot()` is wrapped in try/catch with a CSS failsafe that force-reveals all `.reveal` elements — no blank pages on JS error

---

## Status

This is the public info repo. The full source code lives in a private repository.

> 🔗 **Live site:** [https://clickpros.vercel.app/](https://clickpros.vercel.app/)
