---
type: product
stage: 02_design
inputs:
  - ../../01_objectives/output/requirements.md
  - ../../../_shared/voice.md
  - ../../../_shared/brand-guidelines.md
---

# Design spec — methodology, form, result experience

## 1. Methodology (25x rule, made runnable)

The brief's 25x rule is stated in terms of **annual expenses**, but the five allowed inputs don't include expenses — only income. That's the one gap between the brief's math and its own input list, and it has to be closed here, explicitly, so it can be stated plainly in the final writeup rather than discovered mid-build.

**Assumption (to disclose in the writeup):** annual expenses ≈ annual income − annual savings. In other words, we treat "what you don't save, you spend." It's a simplification, not a budget audit — consistent with "it doesn't need to be perfect financial modeling."

Formula, in the order it runs:
1. `annual_savings = monthly_savings × 12`
2. `annual_expenses = income − annual_savings`
3. `target_nest_egg = 25 × annual_expenses`
4. `years_to_retire = target_retirement_age − age`
5. `projected_nest_egg = current_savings × (1.07)^years_to_retire + annual_savings × [((1.07)^years_to_retire − 1) / 0.07]`
   (current savings compounds at 7%/yr; the monthly amount is treated as a level annual contribution — annual compounding, not monthly, to keep the math explainable in one sentence in the writeup)
6. `gap = target_nest_egg − projected_nest_egg`

**State bands** (avoids a jarring cliff at exactly 100%):
- `gap ≤ 0` → **ahead** (report the surplus, `−gap`)
- `0 < gap ≤ 5% of target_nest_egg` → **on track**
- `gap > 5% of target_nest_egg` → **behind** (report `gap`)

## 2. Path-forward math (behind state only)

Two levers — chosen because they're the brief's own examples, and two is enough ("give them a path," not a spreadsheet):

- **Save more per month.** Solve for the extra monthly amount that closes `gap` by `target_retirement_age`, using the same annuity formula from step 5 solved for the added contribution.
- **Retire later.** Solve for the smallest whole number of extra years `n` such that projected nest egg at `target_retirement_age + n` (same monthly savings, same starting point) closes the gap. This also covers the brief's third example ("worked one extra year at the current rate") — same lever, framed as years.

Round the money lever to the nearest $25/month and the years lever to the nearest whole year — false precision undercuts trust more than it builds it.

## 3. Flow — welcome, then one question at a time

Revised from a single-screen form: a bare five-field form reads cold, closer to the "bank calculator" brand-guidelines explicitly rules out. brand-guidelines.md's Elements line already leaves both doors open ("one field at a time *or* a short single-screen form") — this spec takes the paced door. Same five required fields, same cap, only the pacing changes — plus one optional first-name field on the welcome screen (see below), which sits outside the cap by design.

**Screen 0 — Welcome**
- Headline: "Before we sit down, let's get you a real answer."
- Line 1 (the hook): "Every client asks me the same thing in our first meeting: am I okay, or are we okay?"
- Line 2 (why it matters — the retirement stake, not just the math): "That question was never really about the number. It's about whether you get to spend your time the way you want, with the people you want to spend it with."
- Line 3 (logistics): "Five quick questions, about three minutes, and you'll know where you stand before we ever talk."
- Optional field: "What's your first name?" — clearly marked optional, doesn't block the button either way. Outside the 5-field cap (see `_shared/brand-guidelines.md` Elements section for the rationale); used only to personalize the result headline and to tell Marcus who filled it out.
- Button: "Let's find out" (momentum-building — the "Are we okay?" line is saved for the reveal, not spent here)

Line 2 is the one addition worth flagging: research on retirement satisfaction consistently finds the account balance matters less than purpose, connection, and freedom to spend time on what matters ([Vantage Financial](https://www.vantagefinancial.com/blog/2026/04/30/why-retirement-happiness-is-about-purpose-and-connection/); [Psychology Today](https://www.psychologytoday.com/us/blog/sex-life-of-the-american-male/202511/successful-retirement-according-to-psychology)). Marcus wouldn't cite the research, but he'd say the plain version of it — which is what line 2 is. Kept to one sentence so it doesn't tip into "purpose coach" territory, which would break voice as badly as sterile math would.

**Screens 1–5 — one field per step**, each a short framing line (the "thinking beat" — what Marcus would say between whiteboard questions) then the question. A minimal step indicator ("3 of 5") keeps the 3-minute promise visible; this is a progress dot, not a gauge, so it doesn't conflict with the no-dashboard-widgets rule. Back navigation available at every step — nobody should feel funneled.

| # | Framing line | Field | Label copy | Input type |
|---|---|---|---|---|
| 1 | "First, the basics." | Age | "How old are you?" | number |
| 2 | "This one's just between us — no judgment, just math." | Income | "What do you make a year, before taxes?" | dollar |
| 3 | "Now let's see what you've already got working for you." | Current savings | "What have you got saved for retirement so far?" | dollar |
| 4 | "And what you're currently putting away." | Monthly savings | "How much are you putting toward retirement each month?" | dollar |
| 5 | "Last one — the finish line. This is the age you get to spend on your own terms — more time with the people you actually want to be around." | Target retirement age | "What age do you want to retire?" | number |

Final button (step 5, triggers the calculation): **"Are we okay?"** — Marcus's own phrase, held back until the moment it pays off.

No sixth field, and no added screens beyond welcome + 5 + result — pacing changed, scope didn't. No expenses field, even though the math implies one (see §1) — asking for it directly would break the 3-minute promise and duplicates what income minus savings already approximates.

## 4. Result experience

Revised layout (v2, matches the whiteboard rebuild): **eyebrow → hero number (the projected total, $X, hand-circled) → caption ("what you're on pace for by age {retirement age}") → headline verdict → the comparison (**$Z** needed, plus **$Y** ahead / gap) → path forward if behind → closer.** $X gets its own hero treatment instead of being repeated in the body copy, since the circled number is the one visual focal point per screen. Numbers are rounded to the nearest $1,000, no cents.

Headline personalization: if the optional first-name field was filled in, prefix the headline with it ("David, you're ahead of where you need to be."); otherwise the generic version runs unchanged. One touchpoint only — not threaded through every line, which would tip into forced-familiarity territory.

**Ahead**
- Headline: "[{Name}, ]You're ahead of where you need to be."
- Body: "You need around **$Z** — that's **$Y** ahead. Nice work."
- Closer: "That's not just enough — that's room to actually enjoy it, not just get by."

**On track**
- Headline: "[{Name}, ]You're on track."
- Body: "That's right around the **$Z** you need. Keep doing what you're doing."
- Closer: "That's real room to spend that time on what matters, not just get through it."

**Behind**
- Headline: "[{Name}, ]You're behind — here's the gap, and here's how to close it."
- Body: "You need around **$Z**. That's a **$gap** gap."
- Path forward (both shown together, not one-or-the-other):
  - "Save about **$A more a month** between now and {retirement age}, and you close it."
  - "Or keep saving what you're saving now, and push retirement to **{retirement age + n}**, and you close it that way instead."
- Closer: "This isn't only a math gap — it's the difference between retiring on your terms and stretching to make it work. Neither path above is a verdict; that's what our first call is for: figuring out which one fits the life you're picturing."

The closer does double duty in every state: it reconnects the number to what it's actually for (not just "give a path, not a verdict" for the behind case), and it hands the prospect back to Marcus's actual meeting, which is the whole point of the tool.

**Post-reveal action:** below the closer, an "Email these results to Marcus" button (secondary, Marker Blue) opens a `mailto:` link pre-filled with a plain-text summary — status, the pace number, the target, and (if behind) the gap and both levers — signed with the optional name if given. This is a real, functional action (opens the user's mail client), not a fake booking flow, which matters for the "would Marcus actually send this?" test. The address is a placeholder (`marcus@example.com`) to swap for Marcus's real inbox on deployment — flagged in the code comment next to it. "Start over" stays below it as the lower-emphasis fallback action.

## 5. Voice pass

Every string above was checked against `_shared/voice.md` line by line: plain words, no jargon ("nest egg" and "gap" instead of "corpus" or "shortfall"), second person, contractions where a person would use them, direct about the number before softening into the path. The button copy borrowing Marcus's own "are we okay?" line is the clearest single voice anchor in the whole tool.

## 6. Visual tie-in

Field and result layout defer to `_shared/brand-guidelines.md`'s Visual system section (colors, type, spacing) — not restated here. One addition specific to this spec: on the result screen the hero number ($X) is the single largest, heaviest element — the circled focal point — with the headline verdict as secondary emphasis below it; the path-forward lines are equal-weight to each other and always both visible when behind, never behind a toggle. The minimal signature footer (Marcus's name + one grounding line, per brand-guidelines.md) is persistent across every screen, not just the result screen — it's identity, not a per-screen element.
