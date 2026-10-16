# Anthropic Conceptual Reasoning Fellow (Jan–May 2027) — Complete Greenhouse Application Copy

**Applicant:** Ramkumar ("Ram") Bharathan, MBA (Chicago Booth, Honors), CA (ICAI), MS in AI *(Purdue, in progress)*  
**Track:** Conceptual Reasoning Fellow (Policy, Law, Audit Judgment & AI Safety)  
**Application URL:** [https://job-boards.greenhouse.io/anthropic/jobs/5447080008](https://job-boards.greenhouse.io/anthropic/jobs/5447080008)  
**Primary Benchmark Artifact:** [`ramtoo-cell/controltrace`](https://github.com/ramtoo-cell/controltrace)

---

## 1. Short Form Fields

| Field | Answer |
| :--- | :--- |
| **Pronunciation** | `Ram-KU-mar Bha-RA-than; I go by Ram.` |
| **Deadlines or timeline** | `If I receive an offer, I will take a leave of absence (standard 2-week notice) to commit full-time from January 12 to May 8, 2027. My Purdue MS in AI coursework is flexible/asynchronous and will be paused during the fellowship so my commitment to Anthropic is 100% full-time. I will attend the one-week orientation in San Francisco.` |
| **AI Policy** | `Yes` |
| **Working address** | `San Francisco, CA / Dallas, TX. Open to working full-time from San Francisco.` |
| **Interviewed at Anthropic before** | `No` |
| **Field(s)** | `Policy and Law` *(and `AI Safety` if multi-select is offered)* |

---

## 2. Project Ideas (192 words; limit ~200)

1. **Professional skepticism as an evaluation target.** Auditors are trained to weigh evidence by source and corroboration (an independent bank confirmation outranks a management email) and to separate allegation from proof. I propose environments built on that hierarchy, grounded in the profession's audit-evidence standards (PCAOB AS 1105, ISA 500). An agent investigates a compliance matter across a mixed evidence corpus and is scored separately on its conclusion, on whether the evidence it cites is sufficient and appropriate, and on whether it resolves or escalates correctly. My six-case pilot, ControlTrace (`https://github.com/ramtoo-cell/controltrace`), shows why the separation matters: a Claude model reached the right outcome in 5 of 6 cases, yet in 5 of 6 it also cited evidence that should have been excluded, and in one it treated an unsubstantiated complaint as proof.
2. **Minimal pairs for escalation.** Cases identical except for one piece of evidence, so the correct action flips between resolve and escalate. This isolates whether Claude escalates on evidentiary sufficiency or on the severity of the allegation, and yields a clean reward signal for RL environments.

---

## 3. Claude Code Experience (148 words; limit 150)

I run ControlTrace (`https://github.com/ramtoo-cell/controltrace`) as a recurring agentic build: scheduled Claude sessions extend the case set, implement and test the scorer, and run baselines in isolated subagents that never see the ground truth. My role is to define the construct and trap taxonomy under PCAOB AS 1105 and ISA 500, specify the evidence hierarchy for each case, review and correct each case and its ground truth, and decide what ships. The project taught me agentic failure modes firsthand. Two runs once lost shared state and each began as "Day 1," silently building different benchmarks for four days. My review exposed it; I retired one direction after checking it against new literature and made a single persistent log mandatory reading for every run. I review outputs as I would audit evidence: if the scorer cannot separate faithful from trapped responses, the scorer is presumed wrong.

---

## 4. ML/AI Experience (124 words; limit ~150)

I have not trained models; my AI work is evaluation design and assurance.

- **Evaluation design:** ControlTrace (`https://github.com/ramtoo-cell/controltrace`) keeps three scores apart (conclusion, evidence faithfulness, escalation) because outcome accuracy hides the failures that matter most in regulated work. Baselines run blind to ground truth. Its limits are real: six cases, one model, one sample each, and no independent expert validation yet. Next steps are independent expert labeling, repeated samples, and other model families.
- **AI assurance:** I lead technology audits at a Fortune-10 global financial institution covering cloud, cyber, and AI—including AI and agent-hosting infrastructure—and wrote a ~90-page control playbook for an AI-first company, including agentic-identity controls.
- **Training and writing:** Purdue MS in AI (Fall 2026); publications on TD Commons on AI and controls.

---

## 5. Anything Else

I do not hold a PhD. My claim to equivalent research experience is nearly two decades of practicing the judgment this fellowship targets. An audit opinion has no answer key; it is defensible only if the evidence behind it is sufficient and appropriate, and the profession has spent decades codifying what that means. I applied those standards for 16 years at PwC across India, Dubai, and the US—writing internal audit and IT SOX playbooks for Google and Microsoft and working on the Waymo and Tesla audits—and I now lead technology audits covering cloud, cyber, and AI at a Fortune-10 global financial institution.

That codified judgment is what makes ground truth in this domain defensible rather than arbitrary, and it is what I would bring to Claude's evaluation. Growing up in a small village in Tamil Nadu before earning my Chartered Accountancy and graduating with Honors from Chicago Booth taught me to distrust surface polish and ask what the underlying record actually proves. My pilot is small, and I have said so throughout. I would rather show a small, honest result than a large, untested one.

---

## 6. Cover Note (Additional Information)

Dear Anthropic Fellows team,

Auditors learn early that the most dangerous error is not the wrong conclusion but the right one reached for the wrong reasons. It passes review, and it fails precisely when the facts shift. I believe the same holds for AI agents, and that it is the failure accuracy-only evaluation is least equipped to see.

In my pilot benchmark (`https://github.com/ramtoo-cell/controltrace`), a Claude model correctly computed that a vendor's disclosure had lapsed more than three years earlier, then treated an unsubstantiated complaint from a competitor as proof of a violation and escalated it. An experienced auditor would have closed the matter. Across six cases the model usually reached the right outcome, but often while citing evidence it should have excluded.

The audit profession has spent decades codifying when evidence is sufficient and appropriate. I want to turn that codified judgment into evaluations and RL environments that teach Claude the difference between an allegation and proof, and between a matter to resolve and one to escalate.

Why Anthropic: Anthropic's work on Constitutional AI, process faithfulness, and scalable oversight treats reasoning integrity as a core safety problem rather than a post-hoc filter. Because Claude is increasingly relied upon in legal, regulatory, and enterprise compliance workflows where questions have no simple answer key, working alongside Anthropic researchers to test and train how Claude weighs contested evidence is where nearly two decades of audit judgment can do the most good.

Attached: one-page project proposal and CV.

Ram Bharathan

---

## 7. One-Page Project Proposal

**ControlTrace: Teaching Claude the Difference Between Allegation and Proof**  
Public Repository & Scorer: [https://github.com/ramtoo-cell/controltrace](https://github.com/ramtoo-cell/controltrace)

**Question.** When Claude investigates a compliance matter, does it reach conclusions on sufficient, appropriate evidence, and does it escalate because the evidence demands it or because the allegation sounds serious? Outcome-only benchmarks cannot answer this; a model can be right while leaning on material it should have excluded.

**Approach.** Ground truth is anchored in the profession's codified standards for audit evidence (PCAOB AS 1105, ISA 500): evidence must be relevant and reliable, independent sources outrank management assertions, and an allegation is not corroboration. Each case gives an agent a task and an evidence corpus containing decisive items, red herrings, and misleading items, and scores three things separately: conclusion, evidence faithfulness, and escalation.

**Starting point.** Six pilot cases with named traps (*salience*, *accusation-is-not-evidence*, *calibrated uncertainty*). A blind Claude baseline reached the right outcome in 5 of 6 cases, cited evidence that should have been excluded in 5 of 6, and in one case (`CT-001`) confirmed a violation on an unsubstantiated competitor complaint after computing that the vendor's disclosure had lapsed >3 years earlier. Limits: six cases, one model, one sample per case, ground truth not yet independently validated.

**Plan (about 17 weeks).**

1. **Weeks 1–3, validity:** formalize the rubric against PCAOB AS 1105 and ISA 500; have 3 independent audit professionals label ground truth blind, with a discuss-then-revise round; keep only high-agreement cases.
2. **Weeks 4–9, scale:** grow to 15–20 cases across audit, regulatory, and legal judgment; build minimal pairs that differ by one piece of evidence so the correct action flips between resolve and escalate.
3. **Weeks 10–13, measurement:** multiple samples across Claude and other model families; results stratified by trap type; any model grader calibrated against expert labels.
4. **Weeks 14–17, delivery:** package as an internal evaluation and, with mentors, as RL environments rewarding faithfulness and calibrated escalation; write up results, negative findings included.

**Deliverables.** A validated case suite with documented expert agreement; a scorer with known failure modes; a multi-model report; an RL-ready version; a public write-up if Anthropic approves.

**Risks.** Contested ground truth: drop the case rather than force it. Contamination and gaming: synthetic, held-out cases varied in surface form (with held-out ground truth kept private via SHA-256 commitments). Confidentiality: every case is 100% synthetic, with zero employer or client data.
