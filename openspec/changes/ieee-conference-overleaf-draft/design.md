# Design: OpenSpec-to-Overleaf IEEE Conference Manuscript Pipeline

## Context
AirGuard AI already maintains canonical specifications (`data-pipeline`, `agent-architecture`, `domain-rules`, `evaluation-benchmark`) and a refactored A–Z proposal (`Proposal_Refactored.md`). DIC4 extends this repository with an English two-column `IEEEtran` conference paper ready for immediate upload to Overleaf.

## Architectural Mapping (Source -> IEEE Conference Manuscript)

| Source Artifact | IEEE Manuscript Section | Verification Gate |
|---|---|---|
| `Proposal_Refactored.md` (Stage 3 IEEE Abstract & A–F) | Abstract, IEEE Keywords, Section I (Introduction) | Audited counts (`970,296 -> 606,137`, `88` stations, `13` conflicts) match `data-pipeline/spec.md` |
| `Proposal_Refactored.md` (M–O & References `[1]`–`[18]`) | Section II (Related Work), Table I, `overleaf/references.bib` | 1/2 AI + 1/2 Domain balance; 100% BibTeX key resolution |
| `DESIGN.md` §5–§10 & `agent-architecture` / `domain-rules` | Section III (Architecture, TikZ Fig. 1, Eqs. (1)–(4), Alg. 1) | 9-stage decoupling, `O3_8hr` vs `O3`, 75% gate, `SourceRowID` guard |
| `evaluation-benchmark/spec.md` & `Proposal_Refactored.md` Q–V | Section IV (`AirGuard-Eval-60`) & Table II | Explicit proposal-stage disclaimer; zero fabricated results |
| `DESIGN.md` §13 & `Proposal_Refactored.md` W–Z | Section V (Limitations, Future Work, Conclusion) | Partial-year Jan–Oct 2026 scope & `DataCreationDate` caveat stated |

## Key Design Decisions
1. **Self-Contained TikZ Vector Architecture Diagram**: Instead of referencing external raster images that can fail path resolution or look blurry in two-column print, Fig. 1 is rendered natively via TikZ inside `overleaf/main.tex`.
2. **pdfLaTeX-Safe Encoding**: Avoid raw Unicode math/Greek characters (`μ`, `≥`, `–`) in `.tex` prose in favor of standard LaTeX commands (`\mu`, `\ge`, `--`) with `inputenc`/`fontenc` so Overleaf's default `pdfLaTeX` engine compiles cleanly.
3. **Zero-Dependency Overleaf ZIP Packaging**: `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip` bundles `main.tex` and `references.bib` at archive root for one-click Overleaf upload.

## Risks and Mitigations
- **Risk**: Broken BibTeX keys or unescaped underscores (`_`) causing LaTeX compilation errors on Overleaf.
  - **Mitigation**: Automated Python audit script checks brace balance, environment matching, citation completeness across all 18 entries, and ZIP contents before pushing to GitHub.
