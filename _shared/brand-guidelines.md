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

## Visual system

The brief specifies no brand assets (no logo, no client-supplied palette) — this is our design decision, grounded in "Feel" above and in Marcus's own image of the work: a whiteboard conversation, not a dashboard.

**Colors** — warm, ink-and-paper, not cold fintech-blue:
- Ink (text, headings): `#2B2521` — warm near-black, not pure `#000`
- Paper (background): `#FAF6F0` — warm off-white, not clinical white
- Primary / CTA / "on track": Amber `#C1622D`
- Positive / "ahead": Sage `#5C7A5C`
- Behind, but never alone: Clay `#B0523A` — muted, not alarm-red. Stoplight red reads as a verdict; this tool never leaves someone at a verdict, so the color can't either. Pair every use of Clay with the path-forward content in the same view.
- Neutral grays: warm-toned (e.g. `#8A8078`), never blue-grays — blue-gray is what reads as "bank app."

**Typography:**
- Body & UI: a humanist sans (e.g. Inter, Public Sans, or the system sans stack) — legible, plain, no personality tricks in the reading text.
- Numbers & key verdict line: a serif or a slightly heavier display cut of the sans, set larger — the "this is the number Marcus would circle on the whiteboard" moment. One clear visual emphasis point per screen, not a dashboard of equally-weighted stats.

**Elements:**
- Inputs: large, single-column, one field at a time or a short single-screen form — never a dense grid of tiny bank-app fields.
- No gauges, dials, or literal speedometer widgets. If a status color is used, it's the palette above, not a stoplight.
- The path-forward content (extra $/month, retire later, work longer) is always visible alongside a "behind" result, not hidden behind a click or a second screen.
- Generous spacing, mobile-first — a prospect may open this on a phone before the call.

## Non-negotiable UX rule

When someone is behind, never leave them stranded at the bad number. Always surface the path forward — e.g. how much more per month closes the gap, or what retiring one or two years later does, or what holding the current savings rate but working longer does. A verdict alone is a failure state for this tool, regardless of how accurate it is.

## Methodology default

The 25x rule (25× annual expenses needed at retirement, assuming a 7% average return) is Marcus's own mental model and the default. A different methodology (4% rule, replacement ratio, 10x salary) is acceptable only if it's named and explained in the final writeup — Marcus wants to know what he's looking at.

## Out of scope

Financial accuracy, modeling sophistication, and feature count are explicitly *not* what this is judged on. Don't spend build time there at the expense of voice or simplicity.
