# Are We Okay? — Retirement Readiness Workspace

An interactive retirement-readiness tool for **Marcus**, a Denver financial planner, built for Clief Notes Weekly Competition #2 ("The Artifact Sprint"). See [_shared/source/marcus-client-brief.md](_shared/source/marcus-client-brief.md) for the original brief.

Prospects fill it out before their first meeting with Marcus, see where they stand against the 25x rule, and — if they're behind — see a real path to closing the gap instead of just a number. Deliverable: the interactive artifact plus a 100-word writeup.

**Live app:** _deployed via GitHub Actions on every push to `main` once the build stage has output — see [.github/workflows/pages.yml](.github/workflows/pages.yml)._

## Start here

[CLAUDE.md](CLAUDE.md) is the entry point — it routes to everything below in one screen.

- **[_shared/](_shared/)** — the factory: Marcus's voice, the visual/brand system, and the original brief (`source/`). Stable reference, read by every stage.
- **[stages/](stages/)** — the three-stage pipeline: `01_objectives` (requirements from the brief) → `02_design` (methodology, UX, copy) → `03_build` (the artifact + writeup).

## Why it's structured this way

Built with [`icm-architect`](https://github.com/RinDig/icm-architect), a Claude Code skill (tooling used to build this — not vendored in this repo): numbered folders carry sequencing, folder hierarchy carries context scoping, and plain markdown carries state — so a human (or an AI) can open any folder and see exactly what it's for, without a wiki or a framework. Every working folder has a `CONTEXT.md` stating its inputs, its job, its outputs, and what a human should check before moving on.
