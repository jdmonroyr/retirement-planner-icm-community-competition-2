# 01_objectives — extract requirements from the brief

One job: turn Marcus's brief into an explicit, checkable requirements list — nothing invented, nothing dropped.

## Inputs
- Working (this run): ../../_shared/source/marcus-client-brief.md

Do NOT load: `_shared/voice.md`, `_shared/brand-guidelines.md` — not needed to extract requirements; they get applied starting in 02_design.

## Process
1. Read the brief in full.
2. Extract, as an explicit list: the required inputs and their cap (name each field, note the "no 12th field" ceiling), the exact question the tool must answer ("are we okay?" — on track / behind / ahead, by how much), the default methodology (25x rule, 7% return) and the license to swap it if explained, the mandatory "show a path, not a verdict" behavior for bad news, the output-format freedom, and the three judging criteria in their stated order.
3. Do not add requirements the brief doesn't state (no accuracy targets, no extra fields, no compliance disclaimers) — that's over-building, which the brief explicitly warns against.

## Outputs
- `requirements.md` → output/

## Human check
Read `output/requirements.md` next to the brief — confirm every line traces back to something Marcus actually said, and nothing he said is missing.
