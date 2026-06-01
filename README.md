# trauma-evidence-forge — ARCHIVED 2026-06-01

> **⚠ This repository has been ARCHIVED. It is read-only and no longer maintained.**
>
> `trauma-evidence-forge` (TEF) was **folded into [`academic-surgery-forge`](https://github.com/HELIOS516/claude-skills/tree/main/skills/academic-surgery-forge)** (ASF) — the unified academic-surgery research + education workbench (trauma, EGS, surgical critical care, global surgery).

## Where everything went

TEF's keyword-slide Gamma pipeline now lives inside ASF as an **opt-in strict mode** (`--mode strict`, alias `--strict` on `generate_gamma_params.py`):

- **Mode-gated card thresholds** (tighter `body_max` budgets) + the **Marine** Gamma `themeId`
- **Always-on advisory slide diagnostics** (D9–D13, validators 18–19) — non-failing in default mode
- **Declarative `<!-- type: X -->` card parser**

ASF's **default-mode output is byte-identical to pre-fold** — strict mode is purely additive.

| TEF component                                                | New home in `academic-surgery-forge`                                                      |
| ------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| Skill + scripts                                              | `skills/academic-surgery-forge/` (strict mode)                                            |
| Templates                                                    | `templates/presentation-{compact,shelf-review,medium-keyword}.md`                         |
| Lightweight Pending projects                                 | `projects/Pending/` (xabcde-primary-survey gold standard + KB stubs)                      |
| `trauma-shelf-review` (133 MB DICOM viewer + rendered decks) | **retained here only** — intentionally not migrated into the 3-machine-synced skills repo |

## Why

Consolidation removed real ASF↔TEF duplication (shared scripts/templates/references) and made skill-trigger routing deterministic. clinical-forge and the legal skills were left untouched.

Plan of record: `~/.omc/plans/forge-consolidation-2026-06-01.md` · merged to `claude-skills@main` (`25cd8c0`).
