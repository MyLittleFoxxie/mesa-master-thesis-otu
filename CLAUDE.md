# Claude Code Guide

Read [`AGENTS.md`](AGENTS.md) first (authoritative rules for source provenance, verified numbers, and privacy boundaries) and [`README.md`](README.md) for the thesis directory layout.

- **Source papers:** Sync all empirical counts, tables, and figures strictly from `../MESA-meta-evaluation-standard-for-ai/` (`main`) and `../benchmark-evidence-requirement-decisions/` (`main`).
- **Literature SSOT:** Consult `../thesis-literature/` (`catalog.md`, `markdown/<bib_key>.md`, `slr-mesa/`, `slr-decisions/`) for reference verification, and never mention or link that private repository in any `.tex` file or `README.md`.
- **GitHub authentication:** Use the `MyLittleFoxxie` GitHub account for remote Git/GitHub operations (`gh auth switch -u MyLittleFoxxie`, using `/opt/homebrew/bin/gh` if `gh` is not on `PATH`), then switch back to the previously active account afterward.
- **Verification:** Run `python3 tools/verify_thesis.py` after edits (and `--compile` once `MastersDoctoralThesis.cls` is present).
