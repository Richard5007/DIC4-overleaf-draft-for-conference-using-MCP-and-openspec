# Change Proposal: DIC4 IEEE Conference Overleaf Draft with OpenSpec

## Why
Building on the DIC3 OpenSpec-refactored AirGuard AI proposal (`Proposal_Refactored.md`, `DESIGN.md`, and canonical `openspec/specs/`), DIC4 requires converting the research proposal into an Overleaf-ready IEEE two-column conference manuscript (`IEEEtran`) governed by OpenSpec specifications on GitHub.

## What Changes
1. **Overleaf IEEE Conference Project (`overleaf/`)**:
   - Author `overleaf/main.tex` using `\documentclass[conference]{IEEEtran}` with Sections I–V, a native TikZ 9-stage architecture diagram, MOENV AQI mathematical equations, Algorithm 1, Related Work comparison table, `AirGuard-Eval-60` planned evaluation targets, and proposal-stage integrity notices.
   - Author `overleaf/references.bib` with all 18 verified references (`[1]`–`[18]`) matching `Proposal_Refactored.md`.
   - Package `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip` and add `overleaf/README.md` with Overleaf upload instructions.
2. **Canonical OpenSpec Specification (`openspec/specs/ieee-conference-draft/spec.md`)**:
   - Define verifiable requirements for `IEEEtran` formatting, BibTeX citation integrity, proposal-stage academic honesty, and OpenSpec-to-Overleaf traceability.
3. **Repository Documentation & Git Configuration**:
   - Update `openspec/config.yaml`, `README.md`, and `.gitignore` for LaTeX build artifacts and DIC4 deliverables, then validate and push to GitHub.
