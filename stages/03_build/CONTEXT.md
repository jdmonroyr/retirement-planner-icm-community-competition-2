# 03_build — build the artifact and write it up

One job: build the interactive retirement-readiness tool per the design spec, and write the 100-word deliverable writeup.

## Inputs
- Working (this run): ../02_design/output/design-spec.md
- Reference (every run): ../../_shared/voice.md
- Reference (every run): ../../_shared/brand-guidelines.md

Do NOT load: `01_objectives/output/` — the design spec already carries forward everything from requirements that matters at build time.

## Process
1. Build the interactive artifact exactly per design-spec.md — same fields, same copy, same result/path-forward behavior. Stack: plain HTML/CSS/JS, one self-contained file, no framework, no build step — GitHub Pages is the only deployment target, and `.github/workflows/pages.yml` already uploads this folder as-is with zero compile step.
2. Write the 100-word writeup: who it's for, what it does, one design choice and why.
3. Run the walk test from the brief's own judging criteria: does it solve Marcus's problem, does it sound like Marcus, is it simple enough that a real person finishes it?

## Outputs
- `index.html` → output/ (the artifact itself — self-contained, this is what GitHub Pages serves)
- `writeup.md` → output/ (the 100-word deliverable text)
- `artifact-link.md` → output/ (the live GitHub Pages URL — filled in after the repo is created and pushed)

## Human check
Score it against the brief's three judging criteria, in that order. If any fails, fix the artifact — don't patch it with more writeup explanation.
