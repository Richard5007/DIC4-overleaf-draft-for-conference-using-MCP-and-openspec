# Overleaf IEEE Conference Draft — AirGuard AI

This directory contains the publication-ready **IEEEtran (`conference`)** two-column LaTeX draft for **AirGuard AI**, prepared for **DIC4** using OpenSpec SDD.

## Contents

- `main.tex`: Complete IEEE two-column conference manuscript (`\documentclass[conference]{IEEEtran}`), including Title, Authors, Abstract, IEEE Keywords, Sections I–V, TikZ 9-stage architecture diagram, MOENV AQI mathematical formulations, Algorithm 1, comparative Related Work table, `AirGuard-Eval-60` planned evaluation targets, and bibliography call.
- `references.bib`: Verified BibTeX database containing all 18 citations (`[1]`–`[18]`) aligned with `Proposal_Refactored.md`.
- `AirGuard_AI_IEEE_Conference_Overleaf.zip`: Ready-to-upload Overleaf project archive containing `main.tex` and `references.bib`.

## How to Upload to Overleaf

1. Open [Overleaf](https://www.overleaf.com/) and sign in.
2. Click **New Project** -> **Upload Project**.
3. Select `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip`.
4. In Overleaf **Menu** -> **Compiler**, confirm **pdfLaTeX** is selected (default) and click **Recompile**.
5. Replace the placeholder affiliation and email addresses in `main.tex` (`\author{...}`) with your actual university/department details and target conference if needed.

## Proposal-Stage Academic Integrity Note

Consistent with `openspec/specs/evaluation-benchmark/spec.md` and `openspec/specs/ieee-conference-draft/spec.md`, all metrics in Section IV and Table II (`AirGuard-Eval-60`) are explicitly labeled as **Planned Targets / Expected Outcomes** at the proposal stage, with zero fabricated experimental results.
