# Benchmark Evidence for Software Requirement Decisions

Master's thesis repository (Ontario Tech University, `MastersDoctoralThesis` LaTeX template) uniting two empirical studies on artificial intelligence benchmark evaluation and software requirement decisions:

1. **MESA (Chapter 3):** Unifying seven AI benchmark review frameworks (280 items, 30 shared concerns) into a 39-criterion evidence rubric evaluated across four benchmarks and two reviewer model families.
2. **Requirement Decisions (Chapter 4):** A fail-closed, three-step requirement decision method operationalizing MESA ratings and exact one-sided 95% binomial bounds, evaluated across 88 SymPy coding-agent sessions.

## Repository Layout

| Path | Contents |
|---|---|
| `main.tex` | Root Ontario Tech University thesis document (`MastersDoctoralThesis` class). |
| `Frontmatter/` | `customPackages.tex`, `thesisInfo.tex`, `customFormatting.tex`, `titlepage.tex`, `preliminaryPages.tex`, `abbreviations.tex`. |
| `Chapters/` | `Chapter1.tex` (Introduction) through `Chapter6.tex` (Conclusion and Future Work). |
| `Appendices/` | `AppendixA.tex` (MESA concerns and 39-criterion rubric) and `AppendixB.tex` (decision policies, statistical cut points, and artifacts). |
| `BibFiles/references.bib` | Shared BibTeX bibliography (`biblatex`, `backend=bibtex`, `style=numeric`, `natbib=true`). |
| `Figures/` | Study overview figures (`mesa_study_overview.pdf`, `decisions_study_overview.pdf`). |
| `tools/verify_thesis.py` | Offline checker for includes, citations, labels, figure paths, and LaTeX compilation. |

## Template Setup

Place the Ontario Tech University School of Graduate and Postdoctoral Studies `MastersDoctoralThesis.cls` file in the repository root (and replace any `Frontmatter/*.tex` stubs with the official SGS frontmatter files if desired), then fill in the remaining `% TODO` metadata placeholders in `main.tex`.

## Verification and Building

Run offline structural and citation checks:

```sh
python3 tools/verify_thesis.py
```

Once `MastersDoctoralThesis.cls` is present in the repository root, compile the thesis PDF:

```sh
python3 tools/verify_thesis.py --compile
```

Or manually with TeX Live (`pdflatex` and `bibtex`):

```sh
pdflatex -interaction=nonstopmode main.tex
bibtex main
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
```
