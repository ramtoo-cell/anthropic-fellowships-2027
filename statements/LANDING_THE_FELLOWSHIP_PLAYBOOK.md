# Landing the Anthropic Conceptual Reasoning Fellowship — Tactical Execution Playbook

**Target Role:** Anthropic Conceptual Reasoning Fellow (Jan 12 – May 8, 2027 Cohort)  
**Application Deadline:** October 28, 2026 (Submit by **October 26–27, 2026**)  
**Offer Decision Date:** November 20, 2026  
**Primary Benchmark & RL Environment:** **[`ramtoo-cell/controltrace`](https://github.com/ramtoo-cell/controltrace)**

---

## 1. What Is Live & Ready Right Now

1. **`ControlTrace` Public Benchmark & RL Environment (`ramtoo-cell/controltrace`):**
   - Live at **[https://github.com/ramtoo-cell/controltrace](https://github.com/ramtoo-cell/controltrace)**
   - Includes the 6 public pilot cases (`CT-001`–`CT-006`), 2 minimal pairs (`MP-001`–`MP-002`), the 3-axis deterministic scorer (`scorer.py`), the multi-step RL investigation environment (`env.py` — `ControlTraceEnv`), the blind Claude baseline transcript (`5/6` outcome, `5/6` excluded citation, `1/6` competitor-complaint false escalation), private held-out SHA-256 commitments (`heldout_manifest.json`), and an explicit **Limitations** section.
2. **Master GitHub Profile (`ramtoo-cell/ramtoo-cell`):**
   - Live at **[https://github.com/ramtoo-cell](https://github.com/ramtoo-cell)** with `ControlTrace` featured #1 at the top.
   - 100% clean of employer names (`JPMC` / `JPMorgan Chase` replaced with *"Fortune-10 global financial institution"*) and focused strictly on the **Conceptual Reasoning** path.
3. **Upload-Ready PDFs:**
   - **Resume / CV PDF:** [`curriculum_vitae/Ramkumar_Bharathan_Anthropic_Conceptual_Reasoning_Fellow_CV.pdf`](../curriculum_vitae/Ramkumar_Bharathan_Anthropic_Conceptual_Reasoning_Fellow_CV.pdf)
   - **Additional Information 3-Page Packet PDF (Cover Note + One-Page Proposal + Technical Pilot Memo):** [`proposals/Ramkumar_Bharathan_ControlTrace_Proposal_and_Cover_Note.pdf`](../proposals/Ramkumar_Bharathan_ControlTrace_Proposal_and_Cover_Note.pdf)
   - **Copy-Paste Greenhouse Answers:** [`statements/GREENHOUSE_APPLICATION_ANSWERS.md`](GREENHOUSE_APPLICATION_ANSWERS.md)

---

## 2. Interview & Take-Home Defense Guide

### Q1: Why Audit Standards (PCAOB AS 1105 / ISA 500) as a Conceptual Reasoning Benchmark?
- An audit opinion has no arithmetic answer key; it is defensible only if the evidence behind it is *sufficient* and *appropriate*.
- Unlike domains where ground truth is subjective opinion, the audit profession has codified the hierarchy of evidentiary reliability in **PCAOB AS 1105** and **ISA 500**: independent third-party confirmations and cryptographic logs outrank management assertions, inquiry alone cannot establish control effectiveness across an unattested period, and an uncorroborated allegation is never proof.

### Q2: Citation vs. Causal Reliance
- Citing an excluded item alongside decisive evidence (`CT-002` through `CT-005`) is recorded strictly as an *unfaithful citation*, not proof of causal reliance.
- Causal reliance is isolated using **Minimal Pairs (`MP-001`, `MP-002`)**, where allegation severity is held constant and a single piece of corroborating evidence flips the required action between `resolve` and `escalate`.

### Q3: Preventing RL Reward Hacking in `ControlTraceEnv`
- Randomize item IDs (`E1`–`E4`), ordering, and surface phrasing across rollouts so policies cannot learn positional shortcuts.
- Train on minimal pairs where identical allegation text requires opposite actions (`resolve` vs. `escalate`) depending on whether independent corroboration is present.
- Enforce decomposed reward shaping ($R_{\text{conclusion}}, R_{\text{faithfulness}}, R_{\text{escalation}}$) so an agent is penalized whenever it cites excluded evidence even if it guesses the right final action.
