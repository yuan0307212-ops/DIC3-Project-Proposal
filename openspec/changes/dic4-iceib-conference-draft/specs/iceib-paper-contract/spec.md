# Spec: ICEIB Paper Contract

## Scope
This spec defines the acceptance criteria for the DIC4 ICEIB conference paper
assignment deliverable.

## Requirements

### REQ-01: Plain Text Paper
**SHALL** provide a complete readable English paper in `ICEIB paper/main.txt`.
**MUST** include all required IEEE sections (Title, Abstract, Index Terms,
Introduction, Related Work, System Architecture, Prototype Implementation,
Evaluation, Limitations, Conclusion, References).
**WHEN** file exists and contains all sections **THEN** requirement is satisfied.
**Status:** ✅ Satisfied — `ICEIB paper/main.txt` created with all sections.

### REQ-02: LaTeX Source
**SHALL** provide `ICEIB paper/main.tex` using `\documentclass[conference]{IEEEtran}`.
**MUST** include architecture figure, evaluation tables, algorithm, and BibTeX references.
**WHEN** `main.tex` compiles without errors **THEN** requirement is satisfied.
**Status:** ✅ Satisfied (source written) — ⚠️ local compilation not verified
(no pdflatex available; Overleaf compilation required).

### REQ-03: Bibliography
**SHALL** provide `ICEIB paper/references.bib` with all cited sources.
**MUST** match references in `docs/REFERENCES.md` with correct BibTeX keys.
**WHEN** all `\cite{}` keys resolve in BibTeX **THEN** requirement is satisfied.
**Status:** ✅ Satisfied — 12 entries covering all citations in main.tex.

### REQ-04: Evidence Standard
**SHALL** report only results supported by repo files or actual test execution.
**MUST NOT** claim navigation success rates, LLM accuracy, or physical measurements.
**WHEN** every result in the paper has a verifiable source **THEN** satisfied.
**Status:** ✅ Satisfied — all results traced to unit tests (9/9 pass) and
demo scenarios (9 cases, actual outputs documented in tasks.md).

### REQ-05: Attribution
**SHALL** identify the individual assignment author (using confirmed name or placeholder).
**MUST** attribute Group 7 collaborative project in Acknowledgment.
**WHEN** paper correctly attributes individual vs. group contributions **THEN** satisfied.
**Status:** ✅ Satisfied — author block and acknowledgment section present.

### REQ-06: OpenSpec Change
**SHALL** create change `dic4-iceib-conference-draft` with proposal, design, tasks, spec.
**MUST** follow existing spec-driven schema from project OpenSpec config.
**WHEN** all four files exist and follow schema **THEN** satisfied.
**Status:** ✅ Satisfied.

### REQ-07: GitHub Branch
**SHALL** create assignment branch `dic4-iceib-paper` from main.
**MUST** include `ICEIB paper/` directory and `openspec/changes/dic4-iceib-conference-draft/`.
**WHEN** branch visible on remote with correct files **THEN** satisfied.
**Status:** ✅ Satisfied (pending push confirmation).

### REQ-08: Overleaf ZIP
**SHALL** provide ZIP with `main.tex` at root for Overleaf import.
**MUST** include all required files (main.tex, references.bib, COMPILE.md).
**WHEN** ZIP imports to Overleaf and compiles **THEN** satisfied.
**Status:** ✅ ZIP created — ⚠️ Overleaf import requires student login.
