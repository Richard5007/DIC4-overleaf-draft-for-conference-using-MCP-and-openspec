# Spec Delta

## Purpose

Extends the AirGuard AI OpenSpec specification suite with formal requirements for the DIC4 Overleaf-ready IEEE conference manuscript (`overleaf/main.tex`, `overleaf/references.bib`, and `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip`).

## ADDED Requirements

### Requirement: Overleaf IEEEtran Conference Manuscript Generation
The repository SHALL include an English `IEEEtran` two-column conference manuscript (`overleaf/main.tex`) and BibTeX database (`overleaf/references.bib`) derived directly from `Proposal_Refactored.md`, `DESIGN.md`, and canonical OpenSpec specs.

#### Scenario: Preparing the Overleaf upload package
- **WHEN** a user uploads `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip` to Overleaf with `pdfLaTeX`
- **THEN** the project contains `main.tex` and `references.bib` at the root with a self-contained TikZ architecture diagram, equations, Algorithm 1, tables, and 18 verified references

### Requirement: Manuscript-to-Spec Consistency and Integrity
All dataset counts, architectural gates, and evaluation targets in `overleaf/main.tex` SHALL match `openspec/specs/` and preserve proposal-stage academic honesty.

#### Scenario: Auditing manuscript metrics and disclaimers
- **WHEN** Section I, Section III, and Section IV of `overleaf/main.tex` are checked against canonical OpenSpec specs
- **THEN** audited numbers (`970,296` raw, `606,137` clean, `88` stations, `13` conflicts, `75%` coverage) match and Table II is explicitly marked as planned targets only
