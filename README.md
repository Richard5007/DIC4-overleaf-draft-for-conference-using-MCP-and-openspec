# DIC4: Overleaf Draft for IEEE Conference using MCP and OpenSpec

**AirGuard AI: A Deterministic and Row-Level Provenance-Grounded Conversational Agent for Taiwan Air Quality Analysis**

[![OpenSpec](https://img.shields.io/badge/OpenSpec-SDD%20Strict%20Verified-blue)](https://github.com/Fission-AI/OpenSpec)
[![LaTeX](https://img.shields.io/badge/LaTeX-IEEEtran%20Conference-008080)](https://www.overleaf.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📌 作業摘要 (DIC4 Overview)

本 Repository 為 **DIC4 作業** 之獨立專案，依據 [DIC3 AirGuard AI 提案與工程設計](https://github.com/Richard5007/DIC3-Project-Proposal-Refactor-using-Openspec) 產出完整 **IEEE Conference (`IEEEtran` 雙欄) Overleaf LaTeX 論文草稿**，並透過 **OpenSpec 規範驅動開發（SDD）** 於 GitHub 進行規格驗證與版本控管。

> **提案階段與學術誠信聲明（Proposal Stage Only）**：本專案目前仍處於提案與架構設計階段，論文第四節與 Table II 之 `AirGuard-Eval-60` 指標皆明確標示為「規劃驗收目標（Planned Targets）」，未包含任何虛構或已執行之實驗數據。

---

## 📦 核心交付項目 (Deliverables)

### 1. Overleaf IEEE Conference Draft (`overleaf/`)
- **[`overleaf/main.tex`](overleaf/main.tex)**：完整英文 `\documentclass[conference]{IEEEtran}` 雙欄會議論文草稿，包含：
  - Title、Authors（占位羅馬拼音與系所資訊）、Abstract（IEEE 摘要）與 IEEE Keywords
  - **Section I. Introduction**：2025 *State of Global Air*、WHO 2025 `B09461`、台灣環境部 2025 年 1 月 1 日 $\text{PM}_{2.5}\ 12\ \mu\text{g/m}^3$ 新制與午後臭氧橘色提醒、`AQX_P_488`（970,296 → 606,137 筆、88 站、13 組衝突鍵）稽核與 *TableBench*/*RAGTruth* 幻覺脈絡
  - **Section II. Related Work**：1/2 AI 方法 + 1/2 空品感測領域文獻（8 篇）與跨欄比較表 `Table I`
  - **Section III. Proposed Architecture and Methodology**：原生 **TikZ** 九階段解耦架構圖（`Fig. 1`）、MOENV AQI 數學公式（Eqs. 1–4）、`Algorithm 1` 與 OpenSpec SDD 流程說明
  - **Section IV. Evaluation Plan and Expected Outcomes**：`AirGuard-Eval-60`（45 可回答 + 15 邊界拒答）、三組基準比較與 `Table II` 規劃指標
  - **Section V. Limitations, Future Work, and Conclusion**
- **[`overleaf/references.bib`](overleaf/references.bib)**：完整 18 筆經查核之 BibTeX 文獻庫（`[1]`–`[18]`）。
- **[`overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip`](overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip)**：可直接上傳至 Overleaf 編譯的專案壓縮檔。

#### Overleaf 上傳與編譯步驟
1. 登入 [Overleaf](https://www.overleaf.com/)，點選 **New Project → Upload Project**。
2. 選擇 `overleaf/AirGuard_AI_IEEE_Conference_Overleaf.zip`。
3. 確認左上角 **Menu → Compiler** 為 **pdfLaTeX**，點擊 **Recompile** 即可產出雙欄 IEEE 會議論文 PDF。
4. 視需要於 `main.tex` 的 `\author{...}` 區塊替換實際系所與電子郵件。

---

### 2. OpenSpec on GitHub (`openspec/`)
- **Canonical Specs (`openspec/specs/`)**：
  - `data-pipeline/spec.md`
  - `agent-architecture/spec.md`
  - `domain-rules/spec.md`
  - `evaluation-benchmark/spec.md`
  - `ieee-conference-draft/spec.md`（DIC4 IEEE 會議論文格式、18 筆引用完整性、學術誠信與 Overleaf 封裝規範）
- **Change Proposal (`openspec/changes/ieee-conference-overleaf-draft/`)**：
  - `proposal.md`、`design.md`、`specs/ieee-conference-overleaf-draft/spec.md`、`tasks.md`

#### 驗證指令 (OpenSpec CLI)
```bash
openspec list --specs
openspec validate --all --strict
```

---

## 📂 專案結構 (Repository Structure)

```text
DIC4-overleaf-draft-for-conference-using-MCP-and-openspec/
├── overleaf/
│   ├── main.tex
│   ├── references.bib
│   ├── AirGuard_AI_IEEE_Conference_Overleaf.zip
│   └── README.md
├── openspec/
│   ├── config.yaml
│   ├── specs/
│   │   ├── agent-architecture/spec.md
│   │   ├── data-pipeline/spec.md
│   │   ├── domain-rules/spec.md
│   │   ├── evaluation-benchmark/spec.md
│   │   └── ieee-conference-draft/spec.md
│   └── changes/
│       ├── archive/.gitkeep
│       └── ieee-conference-overleaf-draft/
│           ├── proposal.md
│           ├── design.md
│           ├── specs/ieee-conference-overleaf-draft/spec.md
│           └── tasks.md
├── DESIGN.md
├── .gitignore
└── README.md
```

---

## 👥 專案組員 (Team Members)
- 許景翔（Ching-Hsiang Hsu）
- 李君衛（Chun-Wei Li）
- 吳誠哲（Cheng-Che Wu）
- 更新日期：2026 年 11 月
