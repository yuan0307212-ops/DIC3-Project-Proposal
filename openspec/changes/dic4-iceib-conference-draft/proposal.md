# Proposal: DIC4 ICEIB Conference Paper Draft

## Change ID
`dic4-iceib-conference-draft`

## Author
Chiu Li-Mei (邱秝美), Student ID 7115064159 — DIC4 Personal Assignment

## Source Project
Group 7 collaborative project: https://github.com/hank050392/tb3-navigation-agent  
Source commit: `1c322b8` (main branch, 2026-11-25)

## Objective

Produce a complete IEEE conference paper draft for submission to ICEIB
(https://www.iceib.asia/), based on the TurtleBot3 Burger indoor navigation agent
group project, as a DIC4 personal assignment. The paper must:

1. Report only evidence supported by the repository or actual test execution.
2. Clearly distinguish implemented offline behavior from planned integration.
3. Conform to IEEEtran double-column conference format.
4. Be deliverable as an Overleaf project and a GitHub branch.

## Evidence Standard

All results reported in the paper are sourced from:
- Actual unit test execution: `python3 -m unittest discover -s tests -v`
  → Ran 9 tests in 0.001s — OK (all pass)
- Actual demo scenario execution:
  → 9 scenarios, observed outputs logged (see tasks.md evidence section)
- Repository files: README.md, DESIGN.md, docs/EXPERIMENTS.md, docs/REFERENCES.md,
  config/landmarks.json, src/agent_demo.py, tests/test_agent_demo.py

No navigation success rates, LLM accuracy figures, or physical timing measurements
are claimed. No results have been fabricated.

## Deliverables

| Deliverable               | Location                              | Status     |
|---------------------------|---------------------------------------|------------|
| Plain-text paper          | `ICEIB paper/main.txt`                | ✅ Done    |
| LaTeX source              | `ICEIB paper/main.tex`                | ✅ Done    |
| BibTeX bibliography       | `ICEIB paper/references.bib`          | ✅ Done    |
| Compile instructions      | `ICEIB paper/COMPILE.md`              | ✅ Done    |
| OpenSpec change           | `openspec/changes/dic4-iceib-…/`     | ✅ Done    |
| Overleaf-ready ZIP        | `ICEIB_paper_overleaf.zip` (artifact) | ✅ Done    |
| GitHub assignment branch  | `dic4-iceib-paper`                    | ✅ Done    |
| PDF compilation           | Overleaf (requires upload by student) | ⚠️ Pending |

## Limitations Acknowledged

- Local LaTeX compilation not available (no pdflatex in environment).
- Overleaf project creation requires student login; ZIP is provided for import.
- Author affiliation and email are placeholder strings pending confirmation.

## Attribution

The offline prototype, system design, and project documentation were developed
collaboratively by Group 7. This paper is submitted as an individual assignment by
Chiu Li-Mei, focusing on design analysis and offline evaluation, with appropriate
attribution to the group project.
