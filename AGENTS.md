# Agent Instructions

Use this file as the repository guide for AI coding and research agents working on the Ontario Tech University Master's thesis (`mesa-master-thesis-otu`). Read [`README.md`](README.md) first, then the relevant chapter or companion-paper files before editing.

## Thesis Scope and Source Provenance

This thesis integrates two companion empirical papers from sibling repositories in the workspace:
- **Chapter 3 (Paper 1 — MESA):** `../MESA-meta-evaluation-standard-for-ai/mesa_paper.tex` (`main` branch), mapping 280 items from seven benchmark review frameworks onto 30 shared concerns and evaluating the 39-criterion MESA rubric across Claude and Gemini on four benchmarks.
- **Chapter 4 (Paper 2 — Requirement Decisions):** `../benchmark-evidence-requirement-decisions/decisions_paper.tex` (`main` branch), operationalizing MESA ratings in a fail-closed three-step decision method across 88 SymPy coding-agent sessions.
- **Shared Literature SSOT:** Consult `../thesis-literature/` (`catalog.md`, `pdfs/<key>.pdf`, `markdown/<key>.md`, `slr-mesa/`, `slr-decisions/`, and `references.bib`) when verifying citations or syncing `BibFiles/references.bib`.

## Writing & Scientific Integrity Rules

- Always verify reported numbers directly against the latest `main` verification scripts in the two companion repositories (`checks/check_paper_numbers.py` in MESA; `analysis/check_decisions_numbers.py` and `analysis/step2_decisions_analyses.py` in Requirement Decisions). Do not copy outdated counts from earlier drafts or seminar scripts.
- Keep existing BibTeX keys in `BibFiles/references.bib` aligned with `../thesis-literature/references.bib`.
- **Privacy rule:** Never cite, link, or mention `../thesis-literature/` (or `../literature/`) inside `main.tex`, `Frontmatter/`, `Chapters/`, `Appendices/`, `BibFiles/`, or `README.md`.
- Preserve the Ontario Tech University `MastersDoctoralThesis` template structure in `main.tex`.

## GitHub Authentication

- This repository belongs to the `MyLittleFoxxie` GitHub account. Before running remote Git or GitHub operations (`git fetch`, `git pull`, `git push`, `gh`), check the active `gh` account (use `/opt/homebrew/bin/gh` if `gh` is not on `PATH`), switch to `MyLittleFoxxie` (`gh auth switch -u MyLittleFoxxie`), and switch back to the previously active account immediately afterward.

## Verification

Run from the repository root:
- `python3 tools/verify_thesis.py` — validates included `.tex` files, BibTeX keys, `\ref`/`\label` links, figure paths, and privacy rules.
- `python3 tools/verify_thesis.py --compile` — compiles `main.pdf` via `pdflatex` and `bibtex` (requires `MastersDoctoralThesis.cls` in the repository root; TeX Live is at `/Library/TeX/texbin`).
