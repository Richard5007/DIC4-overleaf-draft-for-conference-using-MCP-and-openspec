# IEEE Conference Draft Specification

## Purpose

Defines formatting, citation integrity, academic honesty, and OpenSpec traceability standards for the Overleaf-ready IEEE two-column conference manuscript of AirGuard AI.

## Requirements

### Requirement: IEEEtran Two-Column Conference Format Compliance
The Overleaf manuscript (`overleaf/main.tex`) SHALL use `\documentclass[conference]{IEEEtran}` with `pdfLaTeX`-compatible packages, self-contained vector figures (TikZ), mathematical formulations, Algorithm 1, and comparative tables covering Sections I through V.

#### Scenario: Compiling the Overleaf project cleanly
- **WHEN** `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip` is uploaded to Overleaf and compiled with `pdfLaTeX`
- **THEN** all figures, tables, equations, and algorithm blocks render within IEEE two-column bounds without external asset dependencies

### Requirement: Verified BibTeX Citations and Cross-Reference Integrity
Every in-text citation in `overleaf/main.tex` SHALL resolve to a verified entry in `overleaf/references.bib` covering all 18 canonical references (`[1]`–`[18]`), and every figure, table, equation, and algorithm label SHALL match its cross-reference.

#### Scenario: Auditing BibTeX keys and references
- **WHEN** the manuscript and BibTeX database are cross-checked prior to GitHub commit
- **THEN** 100% of `\cite{...}` keys exist in `overleaf/references.bib` and all 18 verified references from `Proposal_Refactored.md` are cited

### Requirement: Proposal-Stage Academic Integrity in Manuscript
The IEEE conference manuscript SHALL explicitly label the `AirGuard-Eval-60` benchmark and comparison table as proposal-stage planned targets and MUST NOT present unexecuted projections as measured experimental results.

#### Scenario: Reviewing Section IV and Table II claims
- **WHEN** Section IV (`Evaluation Plan and Expected Outcomes`) and Table II are audited
- **THEN** both include explicit proposal-stage disclaimers clarifying that benchmark evaluation has not yet been executed

### Requirement: OpenSpec-to-Overleaf Traceability and Packaging
Every system audit figure (970,296 raw rows, 606,137 clean rows, 88 stations, 13 conflict keys), architectural stage, and rule in `overleaf/main.tex` SHALL match `DESIGN.md` and `openspec/specs/`, and be packaged into `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip`.

#### Scenario: Verifying OpenSpec alignment and Overleaf archive
- **WHEN** `openspec validate --all --strict` and archive checks are executed
- **THEN** all specs pass strict validation and `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip` contains `main.tex` and `references.bib`
