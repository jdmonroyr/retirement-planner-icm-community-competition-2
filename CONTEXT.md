# Marcus retirement artifact — the pipeline

The flow in one line: extract requirements, design the math/UX/voice, build and write it up.

| Stage | Job | Input | Output | Human check |
|---|---|---|---|---|
| `01_objectives` | Extract requirements from the brief | `_shared/source/marcus-client-brief.md` | `output/requirements.md` | Every line traces to the brief; nothing invented |
| `02_design` | Choose methodology, design UX/copy, voice pass | 01's output + `_shared/` | `output/design-spec.md` | Sounds like Marcus; behind-shows-a-path is designed in |
| `03_build` | Build the artifact + write the 100-word writeup | 02's output + `_shared/` | `output/writeup.md`, `output/artifact-link.md` | Scored against the brief's 3 judging criteria |

Factory (stable, every run): `_shared/source/marcus-client-brief.md`, `_shared/voice.md`, `_shared/brand-guidelines.md`
Product (new each run): each stage's `output/`

Status is whatever exists: a stage is COMPLETE when its `output/` holds files.
