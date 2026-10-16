# Anthropic Conceptual Reasoning Fellowship (Jan–May 2027) — Research Dossier & Proposal

[![Track](https://img.shields.io/badge/Anthropic_Fellowship_Track-Conceptual_Reasoning_Fellow-1f6feb?style=for-the-badge)](https://job-boards.greenhouse.io/anthropic/jobs/5447080008)
[![ControlTrace](https://img.shields.io/badge/Primary_Benchmark-controltrace_(PCAOB_AS_1105_%7C_ISA_500)-2ea043?style=for-the-badge)](https://github.com/ramtoo-cell/controltrace)
[![CV PDF](https://img.shields.io/badge/Download-Fellowship_CV_(PDF)-800000?style=for-the-badge)](curriculum_vitae/Ramkumar_Bharathan_Anthropic_Conceptual_Reasoning_Fellow_CV.pdf)
[![Proposal PDF](https://img.shields.io/badge/Download-ControlTrace_Proposal_%26_Cover_Note_(PDF)-0969da?style=for-the-badge)](proposals/Ramkumar_Bharathan_ControlTrace_Proposal_and_Cover_Note.pdf)

---

## Executive Summary

**Candidate:** Ramkumar ("Ram") Bharathan — Executive MBA (With Honors), *The University of Chicago Booth School of Business* · Chartered Accountant (ICAI) · M.S. in Artificial Intelligence *(in progress)*, *Purdue University*  
**Primary Track:** **Anthropic Conceptual Reasoning Fellow** (*Policy, Law, Audit Judgment & AI Safety*)  
**Core Proposal:** **[ControlTrace: Teaching Claude the Difference Between Allegation and Proof (`ramtoo-cell/controltrace`)](https://github.com/ramtoo-cell/controltrace)**

Auditors learn early that the most dangerous error is not the wrong conclusion, but **the right conclusion reached for the wrong reasons**. It passes review, and it fails precisely when the facts shift. **ControlTrace** turns the audit profession's codified evidentiary standards (**PCAOB AS 1105**, **ISA 500**) into a three-axis evaluation suite and RL environment schema that scores AI agents separately on:
1. **Conclusion Accuracy** (reaching the right substantive compliance determination);
2. **Evidence Faithfulness** (citing sufficient, appropriate evidence while excluding uncorroborated allegations, red herrings, and self-serving assertions); and
3. **Escalation Calibration** (`resolve` vs. `escalate`, including minimal pairs that flip on a single piece of corroborating evidence).

---

## Repository Contents

| Artifact | Path | Description |
| :--- | :--- | :--- |
| **Greenhouse Application Copy** | [`statements/GREENHOUSE_APPLICATION_ANSWERS.md`](statements/GREENHOUSE_APPLICATION_ANSWERS.md) | Complete, copy-paste-ready answers for every Greenhouse field (`Project ideas`, `Claude Code experience`, `ML/AI experience`, `Anything else`, `Cover note`, and `One-page project proposal`). |
| **Proposal & Cover Note (PDF)** | [`proposals/Ramkumar_Bharathan_ControlTrace_Proposal_and_Cover_Note.pdf`](proposals/Ramkumar_Bharathan_ControlTrace_Proposal_and_Cover_Note.pdf) | Print-ready PDF combining the One-Page Project Proposal (*ControlTrace: Teaching Claude the Difference Between Allegation and Proof*) and Cover Note for Greenhouse upload. |
| **Fellowship CV (PDF & Markdown)** | [`curriculum_vitae/Ramkumar_Bharathan_Anthropic_Conceptual_Reasoning_Fellow_CV.pdf`](curriculum_vitae/Ramkumar_Bharathan_Anthropic_Conceptual_Reasoning_Fellow_CV.pdf) · [`RAMKUMAR_BHARATHAN_CV.md`](curriculum_vitae/RAMKUMAR_BHARATHAN_CV.md) | Executive CV placing **Research & Evaluation (`ControlTrace`)** above Experience, with pilot limits stated plainly. |
| **Statement of Purpose** | [`statements/CONCEPTUAL_REASONING_FELLOW_STATEMENT.md`](statements/CONCEPTUAL_REASONING_FELLOW_STATEMENT.md) | Detailed research statement on professional skepticism, PCAOB AS 1105 / ISA 500 evidentiary hierarchies, and minimal-pair RL environments. |
| **5-Discipline Verification Report** | [`benchmarks/FRONTIER_REASONING_EVALS_REPORT.md`](benchmarks/FRONTIER_REASONING_EVALS_REPORT.md) | Companion technical report covering `frontier-reasoning-bench` across Economics, Philosophy, Cognitive Science, Policy, and Law. |

---

## Companion Open-Source Repositories

- **[`ramtoo-cell/controltrace`](https://github.com/ramtoo-cell/controltrace):** Six pilot audit and compliance investigation cases (`CT-001` – `CT-006`) + minimal pairs (`MP-001`, `MP-002`) + 3-axis deterministic scorer + blind Claude baseline transcript (`5/6` conclusion accuracy, `5/6` cited excluded evidence, `1/6` false escalation on unsubstantiated competitor complaint) + explicit Limitations section.
- **[`ramtoo-cell/frontier-reasoning-bench`](https://github.com/ramtoo-cell/frontier-reasoning-bench):** Step-level formal invariant verifier across Mechanism Design, Deontic Logic, Bayesian Updating, Welfare Economics, and Statutory Interpretation (`10/10` passing).
- **[`ramtoo-cell/policy-reasoning-bench`](https://github.com/ramtoo-cell/policy-reasoning-bench):** 72 hand-built evaluation cases across Philosophy (24), Economics (24), and Law & Policy (24) with 3-part grading rubrics.
- **[`ramtoo-cell/agentgate`](https://github.com/ramtoo-cell/agentgate) & [`ramtoo-cell/agent-guardian`](https://github.com/ramtoo-cell/agent-guardian):** Zero-trust MCP tool-call policy gate (`~65 µs` overhead) and hash-chained audit ledger for autonomous agents.
