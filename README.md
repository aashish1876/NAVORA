# NAVORA — Travel With Confidence

A cinematic, scroll-driven product showcase for **NAVORA**, an AI-powered unified and adaptive travel intelligence platform.

The site explains the product. The real application is the demonstration:

**Live demo:** https://plan-my-tripp.vercel.app/

Every "Explore Navora", "Try Navora", and "Launch live demo" button links directly to that URL (same tab). No fake demo is built into the site.

---

## Quick start

It is one self-contained file with no build step, no dependencies and no API keys.

```
navora.html   ← open in any modern browser
```

To host it, drop `navora.html` on any static host (Vercel, Netlify, GitHub Pages) and rename it to `index.html` if you like.

---

## The story (section order)

| # | Section | Idea |
|---|---------|------|
| 1 | Hero | NAVORA / Travel With Confidence — "the travel plan that **understands** the journey" over a live journey network |
| 2 | Scale reveal | India tourism numbers revealed one at a time, then "Travel is big. Travel is complex." |
| 3 | Fragmentation | Services drift apart, then collapse into one **Journey** |
| 4 | Manifesto | "Most travel apps help you plan. NAVORA understands the journey." |
| 5 | Connected Journey | Eight systems orbiting one Journey; they respond to your cursor |
| 6 | Travel Brain | Signals converge into **Understanding** (data → context → understanding) |
| 7 | Digital Twin | Rain hits a static itinerary; the impact chain propagates |
| 8 | What-If Simulator | Interactive: ask → analyze → 3 futures → compare → apply |
| 9 | Stay | A hotel isn't a separate booking; it joins the Journey |
| 10 | Intelligence Loop | Plan → Understand → Detect → Analyze → Simulate → Recommend → Approve → Adapt |
| 11 | Demo | Tilted browser + phone composition → live demo link |
| 12 | Comparison | Traditional travel vs NAVORA, plus Discover/Book/Plan vs Understand/Simulate/Adapt |
| 13 | Finale | 4.287B → "What if millions could?" → NAVORA → CTA |

---

## Honesty notes (please keep these)

- **Illustrative content.** The Goa journey (3 days, 2 travelers, ₹30,000), the What-If options, and the budget scenario (₹30,000 → ₹24,000) are **illustrative simulations**, labelled as such on the page. They are not live provider prices or live travel data.
- **Hotel.** No hotel prices or availability are shown.
- **Tourism statistics** (used for scale only, not as NAVORA usage):
  - 4.287 billion domestic tourist visits (2025)
  - 20.22 million international tourist arrivals (2025)
  - 5.22% tourism share of GDP
  - 84.63 million tourism jobs
  - Source as supplied: Ministry of Tourism, Government of India — India Tourism Dashboard, 2025. **Verify against the dashboard before publishing.**
- **Vision statement.** "What if millions could?" is a future vision, not a claim about current users.
- **Government context.** The page notes that India's Incredible India Digital Platform already offers AI personalization, real-time weather and service integrations, and positions NAVORA as exploring *adaptive journey intelligence* as the next layer.
- Add or remove capability claims only if the real app supports them.

---

## How it's built

- **Stack:** HTML + CSS + vanilla JavaScript. Canvas for the hero network, SVG for the Journey, Brain, Stay and Loop graphics, CSS 3D for the demo composition.
- **Scroll scenes:** tall sections (`.sc` with a `data-n` step count) contain a sticky full-screen stage. A small `scene(id, fn)` helper maps scroll progress to steps for the scale reveal, fragmentation, manifesto, Digital Twin and finale.
- **What-If data:** the `SC` array in the script holds the scenarios (question, analyzed signals, original state, three options with time / travel / budget).
- **Motion layer:** loader, hero choreography, word-mask headline reveals, count-up stats, scroll-velocity lean, ambient glow, film grain, trailing cursor (desktop), glass spotlight, and a chapter rail.

### Common edits

| To change | Where |
|-----------|-------|
| Demo URL | Find/replace `https://plan-my-tripp.vercel.app/` |
| Colors | CSS variables at the top of the `<style>` block (`--bg`, `--ink`, `--gold` …) |
| What-If scenarios | `const SC=[...]` in the script |
| Stats copy | `const ST=[...]` in the script |
| Scene length | `data-n` on the `.sc` element (more steps = longer scroll) |
| Chapter rail labels | `const CH=[...]` near the end of the script |

---

## Accessibility and performance

- Semantic headings, keyboard-focusable controls, visible focus rings, ARIA labels on SVG graphics, and the What-If prompt as a live region.
- `prefers-reduced-motion` is respected: the intro, grain, skew and parallax are disabled and content shows in its final state.
- Canvas and SVG animations only run while on screen. No images, video, fonts or external requests are used (system font stack).
- Mobile: the nav collapses into a compact menu, the chapter rail and custom cursor are hidden, and layouts stack.

---

## Known limitations

- Built and syntax-checked, but not yet reviewed in a real browser by the author. Please test at 1440 / 1280 / 1024 px and 390 / 430 px.
- The loop's travelling dot is time-based, not scroll-driven.
- The Travel Brain and Digital Twin use scroll-driven highlights and SVG, not WebGL or true 3D.
- The demo section links out; it does not embed the app.

---

## SEO

- **Title:** NAVORA — Travel With Confidence
- **Description:** NAVORA is an AI-powered unified and adaptive travel intelligence platform that understands the journey, simulates change, and helps travelers adapt with confidence.
