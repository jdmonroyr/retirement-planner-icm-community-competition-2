---
type: factory
---

# Design & brand guidelines

Companion to [[voice.md]] — that file governs the words, this one governs the shape and feel of the artifact itself.

## Feel

Warm and human, the opposite of a "bank calculator." No sterile finance-app aesthetic: no gauge dials, dense gridlines, or corporate-blue dashboard chrome. It should feel closer to a conversation with Marcus than to a spreadsheet.

## Simplicity ceiling

A prospect finishes in under three minutes. Inputs are capped at what the brief names explicitly — age, income, current savings, monthly savings rate, target retirement age (5 fields). Marcus's own line: *"If you find yourself adding a twelfth input field, you've gone too far."* Treat 5–6 fields as a hard ceiling, not a starting point.

## Output format

Open by design — a number, a paragraph, a chart, a traffic light, a conversation. No format is prescribed. The only test that matters: **would Marcus actually send this to a prospect?**

## Visual system (v2 — whiteboard, not stationery)

The brief specifies no brand assets (no logo, no client-supplied palette) — this is our design decision. **v1** of this system (ink-and-paper, terracotta accent, serif numerals) was grounded in "Feel" above but, on review, reads as a generic warm-editorial default rather than something specific to Marcus. **v2** replaces it with a system grounded in something Marcus actually does, not just a mood: he works this math out **on a whiteboard, live, in front of the client**. That's a real, distinctive visual world — not a metaphor to gesture at in copy, the literal source of the palette, texture, and one signature interaction.

Backed by two current trends worth naming: distinctive brands are increasingly defined by one deliberate accent system rather than a "safe" default, used strategically rather than everywhere ([Figma](https://www.figma.com/resource-library/web-design-trends/), [Lounge Lizard](https://www.loungelizard.com/blog/web-design-color-trends/)); and hand-drawn, "authored imperfection" styling is a live 2026 direction explicitly called out as well-suited to financial branding, because it signals humanity over corporate polish ([Fontfabric](https://www.fontfabric.com/blog/10-design-trends-shaping-the-visual-typographic-landscape-in-2026/), [Krumzi](https://www.krumzi.com/blog/12-graphic-design-trends-shaping-2026-and-how-ai-is-changing-the-game)).

**Colors** — a marker set on a whiteboard, not an earth-tone accent on cream:
- Board (background): `#F5F5F2` — off-white with a faint cool-neutral cast, like a whiteboard surface, not cream paper and not clinical `#FFF`
- Ink (text, headings): `#20241F` — near-black with a warm-charcoal cast, like dry-erase marker black
- Marker Blue (structural — progress dots, links, secondary emphasis): `#2C6E8F`
- Marker Amber (primary / CTA / "on track"): `#D9660A` — more saturated than v1's terracotta; reads as a marker, not a ceramic glaze
- Marker Green ("ahead"): `#2E8B57`
- Marker Coral ("behind," but never alone): `#D14D3E` — still muted relative to true alarm-red, still always paired with the path-forward content in the same view, per the non-negotiable rule below
- Neutral grays: warm-charcoal-tinted (e.g. `#8B8880`), never blue-gray — blue-gray is what reads as "bank app"

**Typography** — two roles, used unevenly on purpose:
- Body & UI: Inter (or the system sans stack) — legible, plain, does all the reading work, carries none of the personality.
- The marker accent: **Kalam** (a handwriting face with real marker-like weight, not a thin cursive script) — used *only* for the "Are we okay?" eyebrow and the big verdict number on the result screen. One clear emphasis point per screen; if the handwriting face shows up everywhere it stops reading as a marker and starts reading as a font choice.

**The signature moment:** on the result screen, a hand-drawn circle (a simple SVG path, drawn on with a short stroke animation, respecting `prefers-reduced-motion`) closes in around the verdict number — the visual equivalent of Marcus circling the number on the whiteboard for you. This is the one deliberate flourish in the whole system; everything else stays quiet around it.

**Texture:** a faint dot-grid across the background (like whiteboard/graph-paper texture) — low-contrast enough that it never competes with text, just enough to keep "Board" from reading as flat white.

**Elements:**
- Inputs: large, single-column, one field at a time — never a dense grid of tiny bank-app fields.
- No gauges, dials, or literal speedometer widgets. Status is color + the marker circle, not a stoplight.
- Buttons and cards: flatter, thicker-bordered (2px, ink-colored) — closer to something drawn on a board than a soft drop-shadow SaaS pill. Avoid default `rounded-lg`-everywhere styling.
- The path-forward content (extra $/month, retire later, work longer) is always visible alongside a "behind" result, not hidden behind a click or a second screen.
- Generous spacing, mobile-first — a prospect may open this on a phone before the call.

## Non-negotiable UX rule

When someone is behind, never leave them stranded at the bad number. Always surface the path forward — e.g. how much more per month closes the gap, or what retiring one or two years later does, or what holding the current savings rate but working longer does. A verdict alone is a failure state for this tool, regardless of how accurate it is.

## Methodology default

The 25x rule (25× annual expenses needed at retirement, assuming a 7% average return) is Marcus's own mental model and the default. A different methodology (4% rule, replacement ratio, 10x salary) is acceptable only if it's named and explained in the final writeup — Marcus wants to know what he's looking at.

## Out of scope

Financial accuracy, modeling sophistication, and feature count are explicitly *not* what this is judged on. Don't spend build time there at the expense of voice or simplicity.
