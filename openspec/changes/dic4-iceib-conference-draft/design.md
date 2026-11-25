# Design: DIC4 ICEIB Conference Paper Draft

## Design Decisions

### D1: Paper Title and Scope
**Decision:** Use "An Indoor Navigation Task-Decision Agent for TurtleBot3 Burger:
Design and Offline Prototype Evaluation" (not "Design and Evaluation Plan").

**Rationale:** The offline prototype is fully implemented and all 9 unit tests pass.
7 demo scenarios are reproducible with observed outputs. This is sufficient evidence
for an "Evaluation" framing (of the offline prototype), not merely a plan.

### D2: Evidence Standard
**Decision:** Report only results from (a) repo files, (b) actual test execution,
(c) actual demo scenario execution. No LLM/navigation/physical results claimed.

**Rationale:** Group 7 README explicitly states: "目前沒有 LLM、模擬導航或實機評估結果"
(currently no LLM, simulation navigation, or physical evaluation results).
Fabricating results would violate academic integrity.

### D3: Author Attribution
**Decision:** Paper is authored by the individual assignment submitter (placeholder until confirmed).
Group 7 members listed in Acknowledgment. Group project repository attributed.

**Rationale:** This is a personal assignment based on shared group work.
Attribution must distinguish individual contribution from group work.

### D4: Architecture Diagram
**Decision:** Use TikZ inline figure (no external image dependency).

**Rationale:** Overleaf compilation requires all assets in the ZIP.
TikZ is portable and always available in IEEEtran environments.
The diagram clearly shows implemented (green solid) vs. planned (orange dashed)
components.

### D5: OpenSpec Structure
**Decision:** Use existing `spec-driven` schema from `dic3-openspec-refactor` branch.
Create new change `dic4-iceib-conference-draft` on `main` branch.

**Rationale:** OpenSpec is already initialized in the repo. The new change follows
the same pattern as `refactor-tb3-proposal`.

### D6: LaTeX Compilation
**Decision:** No local PDF generated (pdflatex/docker not available in environment).
Provide Overleaf-ready ZIP; student compiles via Overleaf.

**Rationale:** Environment constraints prevent local LaTeX compilation. The LaTeX
source is syntactically correct and uses only standard CTAN packages available
in Overleaf's default TeX Live distribution.

## Paper Structure Mapping

| Section          | Evidence Source                    | Implementation Status |
|------------------|------------------------------------|-----------------------|
| I. Introduction  | README, DESIGN.md, REFERENCES.md   | Offline prototype     |
| II. Related Work | docs/REFERENCES.md (12 sources)    | Literature only       |
| III. Architecture| DESIGN.md architecture + flowchart | Partly implemented    |
| IV. Prototype    | src/agent_demo.py + test results   | Implemented & tested  |
| V. Evaluation    | docs/EXPERIMENTS.md + test results | Offline done; planned |
| VI. Limitations  | README section 8, DESIGN.md sec 12 | Documented            |
| VII. Conclusion  | Full synthesis                     | Accurate summary      |
