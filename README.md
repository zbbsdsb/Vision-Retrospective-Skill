# Vision Retrospective Skill (愿景回溯)

A scientific AI skill that turns **hollow visions into actionable paths**.

> **The problem.** "Vision-Driven Development" asks the AI to write a vision, then
> implement it. The gap between a vague vision and working code gets filled with
> plausible but ungrounded content — the output looks complete and is hollow.
>
> **The fix.** *Vision Retrospective (愿景回溯)* moves **backward**: it treats the
> vision as a *claim to verify*, anchors every claim to observable evidence, then
> decomposes only the anchored claims into a verifiable implementation path.

## What's inside

```
vision-retrospective/
├── SKILL.md                              # Skill entry point (VR Loop)
├── scripts/
│   └── hollowness_scorer.py             # Deterministic hollowness detector (0–100)
├── references/
│   ├── methodology.md                    # Full VR Loop methodology + worked example
│   └── templates.md                      # Artifact templates (report, path, table)
└── assets/
    └── vision_retrospective_report.md    # Fill-in report scaffold
```

## The VR Loop

| Phase | Name | Output |
|-------|------|--------|
| 0 | Intake & Hollow-Scan | Hollowness score + flagged terms |
| 1 | Intent Excavation (回溯意图) | Grounded vision, resolved assumptions |
| 2 | Claim Decomposition & Anchoring (拆解+锚定) | Claims → verification anchors |
| 3 | Backward Path Synthesis (回溯路径) | Epic→Task→Atomic-Step path |
| 4 | Anti-Hollow Verification (反空洞校验) | Solid plan + score delta |

A healthy run shows a **falling hollowness score**: input (high) → output (low).

## Quick start — the scorer

```bash
# English
python vision-retrospective/scripts/hollowness_scorer.py \
  --text "I want a beautiful, seamless, intuitive app that helps people."

# Chinese
python vision-retrospective/scripts/hollowness_scorer.py \
  --text "做一个美观流畅易用的智能系统，帮助用户提升体验。"

# Machine-readable
python vision-retrospective/scripts/hollowness_scorer.py --text "..." --json

# CI gate: fail if score > 60
python vision-retrospective/scripts/hollowness_scorer.py --text "..." --fail-above 60
```

## Install the skill

**As a user skill (recommended for personal use):**
```bash
# unzip the packaged skill into your user skills dir
unzip vision-retrospective.zip -d ~/.workbuddy/skills/
```

**As a project skill (share with a repo's collaborators):**
```bash
unzip vision-retrospective.zip -d .workbuddy/skills/
```

Then mention a vision or "愿景回溯" and the skill triggers automatically.

## License

MIT — see [LICENSE](LICENSE).
