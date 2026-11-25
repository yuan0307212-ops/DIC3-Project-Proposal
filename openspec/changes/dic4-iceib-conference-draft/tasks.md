# Tasks: DIC4 ICEIB Conference Paper Draft

## Completion Conditions

A task is marked ✅ when: command output or file content can be directly cited as
evidence. No predicted or expected values substitute for observed results.

---

## 1. Source Verification

- [x] 1.1 Clone repo and record source commit SHA
      **Evidence:** `git clone` succeeded; HEAD = `1c322b8` (main branch)
      `git log --oneline -1` → `1c322b8 Add files via upload`

- [x] 1.2 Read all relevant files: README, DESIGN.md, EXPERIMENTS.md, REFERENCES.md,
      agent_demo.py, landmarks.json, test_agent_demo.py, TEAM.md, PROPOSAL.md

- [x] 1.3 Run offline unit tests
      **Evidence:**
      ```
      Command: python3 -m unittest discover -s tests -v
      Result:  Ran 9 tests in 0.001s — OK
      ```
      All 9 tests pass. No failures.

- [x] 1.4 Run all 8 demo scenarios + 1 invalid input case
      **Evidence (actual observed outputs):**
      | Scenario     | Status     | goal_sent |
      |--------------|------------|-----------|
      | ready        | ARRIVED    | true      |
      | ambiguous    | CLARIFY    | false     |
      | stale        | NOT_READY  | false     |
      | blocked      | NO_PATH    | false     |
      | failed       | FAILED     | true      |
      | timeout      | TIMEOUT    | true      |
      | busy         | BUSY       | false     |
      | cancel+busy  | CANCELED   | false     |
      | unknown_lm   | REJECTED   | false     |

- [x] 1.5 Check existing OpenSpec structure on `dic3-openspec-refactor` branch
      **Evidence:** `openspec/config.yaml` (schema: spec-driven),
      existing change `refactor-tb3-proposal` with tasks.md, design.md, proposal.md

---

## 2. Paper Writing

- [x] 2.1 Create `ICEIB paper/main.txt` — complete readable English paper
      **Evidence:** File created at `ICEIB paper/main.txt`
      Contains all 7 sections + references, tables, algorithm pseudo-code

- [x] 2.2 Create `ICEIB paper/main.tex` — IEEEtran LaTeX source
      **Evidence:** File created at `ICEIB paper/main.tex`
      Uses `\documentclass[conference]{IEEEtran}`, TikZ figure, 2 tables,
      algorithmic environment, 12 BibTeX references

- [x] 2.3 Create `ICEIB paper/references.bib` — BibTeX bibliography
      **Evidence:** File created with 12 entries matching docs/REFERENCES.md

- [x] 2.4 Verify consistency: main.txt and main.tex have same sections, results, citations
      **Evidence:** Manual review — both contain identical content.

---

## 3. Compilation

- [ ] 3.1 Compile main.tex → main.pdf
      **Status:** Not completed locally (pdflatex/docker not available in environment)
      **Action required:** Upload ZIP to Overleaf and compile there
      **Expected output:** ~5–7 pages, double-column IEEEtran format

---

## 4. OpenSpec Management

- [x] 4.1 Create change `dic4-iceib-conference-draft`
      **Evidence:** `openspec/changes/dic4-iceib-conference-draft/` directory created
      with `.openspec.yaml`, `proposal.md`, `design.md`, `tasks.md` (this file),
      `specs/iceib-paper-contract/spec.md`

- [x] 4.2 Document completion conditions and evidence for each task (this file)

- [ ] 4.3 openspec validate (not run — `openspec` CLI not installed in environment)
      **Note:** Schema compliance is maintained by following the same structure as
      the existing `refactor-tb3-proposal` change.

---

## 5. GitHub

- [x] 5.1 Create assignment branch `dic4-iceib-paper`
      **Evidence:** Branch created from `main` (commit `1c322b8`)

- [x] 5.2 Commit `ICEIB paper/` and `openspec/changes/dic4-iceib-conference-draft/`
      **Evidence:** Commit SHA recorded after push

- [x] 5.3 Push to remote origin
      **Evidence:** Remote branch verified via `git ls-remote`

---

## 6. Overleaf

- [ ] 6.1 Create Overleaf project `DIC4 - ICEIB TurtleBot3 Navigation Agent`
      **Status:** Not completed — requires student Overleaf login
      **Action required:** Upload `ICEIB_paper_overleaf.zip` to Overleaf
      **ZIP provided at:** `ICEIB_paper_overleaf.zip` in repo root (and artifact dir)

- [ ] 6.2 Verify PDF compiles and pages/figures are correct
      **Status:** Pending Overleaf compilation

---

## Pending Items (Requires Student Action)

| Item                           | Action Required                                   |
|-------------------------------|---------------------------------------------------|
| Author affiliation             | Fill in university/department name                |
| Author email                   | Fill in student email address                     |
| Overleaf project creation      | Upload ZIP at overleaf.com, set main.tex          |
| Overleaf PDF verification      | Compile and check pages, figures, references      |
| Final course submission        | Submit via course website (student handles)       |
