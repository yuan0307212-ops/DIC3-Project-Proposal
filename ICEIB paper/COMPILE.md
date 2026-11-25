# ICEIB Paper — Compile Instructions

## Files in This Directory

| File             | Purpose                                       |
|------------------|-----------------------------------------------|
| `main.tex`       | LaTeX source (IEEEtran, conference format)    |
| `main.txt`       | Plain-text version of the full paper          |
| `references.bib` | BibTeX bibliography (12 entries)              |
| `COMPILE.md`     | This file                                     |

## How to Compile on Overleaf

1. Upload all files in this directory as a ZIP (root = `main.tex`)
2. Set the main document to `main.tex`
3. Set the LaTeX engine to `pdfLaTeX`
4. Click **Recompile**

The paper uses only standard CTAN packages (`cite`, `amsmath`, `graphicx`,
`hyperref`, `booktabs`, `tikz`, `algorithmic`). No custom packages or fonts
are needed.

## How to Compile Locally

```bash
# Requires: texlive-full or MacTeX (pdflatex + bibtex)
cd "ICEIB paper"
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Or with latexmk:

```bash
latexmk -pdf main.tex
```

## Expected Output

- `main.pdf`: ~5–7 pages, double-column IEEEtran format
- 1 TikZ figure (system architecture)
- 2 tables (demo results, evaluation plan)
- 12 bibliography entries
- No missing citation warnings (all \cite{} keys are in references.bib)

## Author Placeholder Note

The author block contains placeholder strings for affiliation and email
(marked with `--- to be confirmed`). Replace before final submission:
- University/Department name
- Student email address

## Assignment Context

- Course: DIC4
- Student: 邱秝美 (Chiu Li-Mei), Student ID 7115064159
- Conference target: ICEIB (https://www.iceib.asia/)
- Source repo: https://github.com/hank050392/tb3-navigation-agent
- Assignment branch: dic4-iceib-paper
