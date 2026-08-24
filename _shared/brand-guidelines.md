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
- Marker Green ("ahead," and doing double duty as the prospect's own input color — see Typography below): `#2E8B57`
- Marker Purple ("behind," but never alone): `#6B4FA0` — real marker packs include purple alongside blue/black/red/green, so this stays inside the literal marker-set logic rather than an arbitrary pick. It also sits on the cool side next to Marker Blue instead of fighting Marker Amber on the warm side — the original Marker Coral read muddy against both. Always paired with the path-forward content in the same view, per the non-negotiable rule below.
- Neutral grays: warm-charcoal-tinted (e.g. `#8B8880`), never blue-gray — blue-gray is what reads as "bank app"

**Typography** — two writers, two colors, on the same board:
- **Kalam** (a handwriting face with real marker-like weight, not a thin cursive script) renders everything either party is *writing* — Marcus's side in ink-black (welcome headline, each step's question, the "Are we okay?" eyebrow, the circled hero number) and the prospect's side in Marker Green (what they type into every field, including their name). Two people, two marker colors, one board — the color is what keeps it from reading as one undifferentiated wall of handwriting.
- **Inter** is reserved for what's read silently rather than written: the quieter framing line before each question (styled italic — the spoken aside, not the board), and all other body copy (result sentences, the closer, the footer's grounding line).

This is a deliberate widening from two earlier, more conservative rules: v2 originally confined Kalam to just the eyebrow and hero number (under-used the concept everywhere but the last screen); a later pass extended it to Marcus's questions but kept typed input in plain Inter for legibility. On review, the two-color "you're also writing on this board" version reads as more of a system, not less legible in practice — a person can always read their own just-typed digits, known-value data doesn't need the same scrutiny as read-only output.

**The signature moment:** on the result screen, a hand-drawn circle (a simple SVG path, drawn on with a short stroke animation, respecting `prefers-reduced-motion`) closes in around the verdict number — the visual equivalent of Marcus circling the number on the whiteboard for you. This is the one deliberate flourish in the whole system; everything else stays quiet around it.

**Texture:** six short phrases in Marcus's own words sit fixed in the page margins, Kalam, low opacity (~16%), ink-colored, scattered at varied sizes and rotation (−8° to +5°, not a tidy grid) like real whiteboard-margin scrawl left over from past sessions: "are we okay?" (circled, echoing the result-screen doodle), "give them a path, not a verdict" (with a small hand-drawn arrow), "honest, not perfect," "60 times a year," "still on the whiteboard," and "the 25x rule" — rendered much larger than the rest (~2.2rem vs ~1rem), the one phrase meant to register even at a glance. His core question, his core UX rule, his core voice rule, his method, his motivation — a two-second philosophy summary for anyone whose eye wanders off the card, with the deliberate visual unevenness of something actually handwritten over time rather than typeset. Chosen over icon doodles (tried first) because words in his own voice carry more of the concept than generic symbols, and register more clearly at the same low opacity.

Hidden below `1200px` viewport width. Widened twice from an original 700px: short phrases need more side margin than icons did to avoid crowding the card, and the oversized "25x rule" phrase needs more room still — below the threshold, the background stays flat `--board` with nothing on it. (Superseded, in order: a card gloss gradient that read as a rendering glitch, then icon doodles that read as too small/quiet, then a tidier four-phrase version that read as too uniform — noted so a future pass doesn't retry any of them from scratch.)

**Elements:**
- Inputs: large, single-column, one field at a time — never a dense grid of tiny bank-app fields. Styled as a drawn line, not a boxed field: no border box, no fill, just a bottom rule (ink, 3px) with the answer written above it in Kalam/Marker Green — "Marcus drew the line, you write on it," rather than a form control that happens to sit on a whiteboard-themed page. Border color shifts to Marker Amber on focus; no box-shadow glow, since there's no box for a glow to sit around.
- No gauges, dials, or literal speedometer widgets. Status is color + the marker circle, not a stoplight.
- Buttons and cards: flatter, thicker-bordered (2px, ink-colored) — closer to something drawn on a board than a soft drop-shadow SaaS pill. Avoid default `rounded-lg`-everywhere styling.
- The path-forward content (extra $/month, retire later, work longer) is always visible alongside a "behind" result, not hidden behind a click or a second screen.
- Generous spacing, mobile-first — a prospect may open this on a phone before the call.

**Identity — a signature, not a brand:** the tool needs enough context that it doesn't feel unmoored, but Marcus is a solo practice ("I run a small financial planning practice"), and the voice mandate is "it should feel like talking to *me*," not a company. So: no invented practice name, no logo mark. Just a minimal footer, present on every screen — his name in the Kalam marker hand (consistent with the eyebrow/hero-number treatment, rotated a degree or two like a real signature) plus one short grounding line in small gray Inter. Nothing clickable, nothing that reads as a brand system of its own.

**Name (required, outside the 5-field cap):** a full-name field on the welcome screen, gating the CTA — "Let's find out" stays disabled until it's filled. Upgraded from optional-first-name once the result screen grew a real "email these results to Marcus" action: an email sent on someone's behalf needs to say who it's from, so the field stopped being decorative personalization and became the thing the send feature depends on. Two uses split cleanly: the *full* name signs the email to Marcus; just the *first* name (first token, split on space) greets the result headline ("David, you're ahead of where you need to be.") — full name would read stiff there. Still the one deliberate exception to the field cap in "Simplicity ceiling" above, and still a single field, but no longer skippable.

## Non-negotiable UX rule

When someone is behind, never leave them stranded at the bad number. Always surface the path forward — e.g. how much more per month closes the gap, or what retiring one or two years later does, or what holding the current savings rate but working longer does. A verdict alone is a failure state for this tool, regardless of how accurate it is.

## Methodology default

The 25x rule (25× annual expenses needed at retirement, assuming a 7% average return) is Marcus's own mental model and the default. A different methodology (4% rule, replacement ratio, 10x salary) is acceptable only if it's named and explained in the final writeup — Marcus wants to know what he's looking at.

## Out of scope

Financial accuracy, modeling sophistication, and feature count are explicitly *not* what this is judged on. Don't spend build time there at the expense of voice or simplicity.
