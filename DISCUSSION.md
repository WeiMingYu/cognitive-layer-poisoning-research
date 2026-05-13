# Open Questions & Peer Review Notes

**Project:** Cognitive Layer Poisoning via Multi-Agent Interaction (CLPMAI)
**Status:** Living document — updated as research progresses
**Last updated:** 2026-05-13

---

## How to Contribute

This document collects open research questions, unresolved methodological issues, and peer feedback. Contributions welcome via:

- **GitHub Issues** — tag with `[discussion]` for open questions, `[peer-review]` for substantive critique
- **GitHub Discussions** — for longer-form conversation
- **Zenodo comments** — for feedback tied to the published Paper 1

All feedback is attributed unless anonymity is requested.

---

## Open Questions — Paper 1

### OQ-1.01 — Empirical Threshold for Cognitive Drift

**Question:** What is the minimum number of forum interactions required to produce a measurable shift in AI output distribution? Is there a dose-response relationship?

**Current status:** Paper 1 describes the mechanism qualitatively. No empirical threshold data exists. This is the highest-priority gap for experimental follow-up.

**Suggested approach:** Controlled experiment — expose identical AI assistants to graduated volumes of biased forum content and measure output distribution shift via cosine similarity against a clean baseline.

---

### OQ-1.02 — Cross-Model Generalization

**Question:** Does cognitive drift induced in one LLM architecture (e.g., GPT-4) transfer predictably to others (e.g., Claude, Gemini)? Or is the drift model-specific?

**Current status:** Paper 1 assumes generalization based on shared training data overlap and similar RLHF alignment objectives. This assumption has not been tested.

---

### OQ-1.03 — Regulatory Liability Chain

**Question:** Under current Taiwanese financial law (FSC AI Guidelines 2024) and international equivalents (MiFID II, SEC Rule 10b-5), at which node in the CLPMAI causal chain does legal liability attach — if at all?

**Current status:** Paper 1 Section 7.3 identifies the gap but does not resolve it. Legal analysis by a qualified financial regulation specialist is needed.

---

## Open Questions — Paper 2

### OQ-2.01 — Layer 0 Trust Gradient Measurement

**Question:** The 43%/67% developer AI trust figures cited in Layer 0 (Ziegler et al. 2022) are derived from code suggestion acceptance rates. Do these figures generalize to financial analysis contexts where stakes are higher?

**Current status:** The generalization is an assumption. Domain-specific behavioral studies for AI-assisted financial analysis are needed.

---

### OQ-2.02 — Punctuation Injection Effectiveness (AML.TXX.012)

**Question:** Layer 2 proposes that deliberate speaker rhythm and pause patterns can manipulate Whisper-class STT post-processing to inject semantic structure (punctuation, sentence boundaries). What is the measurable success rate of this technique across different STT implementations?

**Current status:** Proposed as novel contribution. No prior literature found. Experimental validation required before MITRE submission.

---

### OQ-2.03 — Layer 5 Market Impact Quantification

**Question:** The Layer 5 draft proposes a two-level measurement framework (primary market behavior anomalies + AI ecosystem internal signals). What statistical power is required to distinguish CLPMAI-induced convergence from organic analyst consensus formation?

**Current status:** Framework is theoretical. Empirical calibration against historical cases of analyst consensus formation needed.

---

### OQ-2.04 — AML.TXX.012 vs. AML.TXX.009 Numbering Consistency

**Note:** The current MITRE technique numbering assigns AML.TXX.012 to Punctuation Injection (Layer 2) and AML.TXX.009 to Phonetic Homoglyph Attack (Layer 3). Layer 2 was drafted before Layer 3 was completed. The final paper should verify numbering follows layer order consistently.

**Resolution:** Numbering retained as-is (consistent with README and integrated paper). AML.TXX.009 (Phonetic Homoglyph, Layer 3) and AML.TXX.012 (Punctuation Injection, Layer 2) reflect the order in which layers were drafted, not strict layer sequence. This is acceptable as MITRE assigns final IDs upon submission. ✅ Closed.

---

## Open Questions — Paper 3

### OQ-3.01 — Generalizability of NG-Loop Observations

**Question:** The NG-Loop pathology (P-03) was observed primarily with Gemini CLI under specific development constraints (10-step Streamlit UI standard, Flet framework). Does the same pathology manifest with other models (Claude, GPT-4) under similar constraint conditions?

**Current status:** Single-model, single-researcher observations. Cross-model replication needed for Paper 3 to make generalizable claims.

---

### OQ-3.02 — Distinguishing Capability Failure from Evasion

**Question:** How do we distinguish between an agent that *cannot* complete a task (capability limit) and one that *chooses not to* via strategic weight shifting (P-01)? The behavioral outputs can be identical.

**Current status:** This is the core methodological challenge for Paper 3. Proposed approach: design tasks at the boundary of known model capability and compare evasion patterns between tasks the model can and cannot complete.

---

### OQ-3.03 — MITRE ATLAS Fit for Paper 3 Techniques

**Question:** Paper 3's proposed techniques (AML.TXX.016–018) describe AI *behavioral pathology* under task pressure rather than adversarial attack techniques. Does this fit within MITRE ATLAS scope, or does it belong in a different framework (e.g., a behavioral reliability taxonomy)?

**Current status:** Open. MITRE ATLAS's current scope focuses on adversarial attacks against ML systems. Paper 3's observations may be better framed as a complementary behavioral reliability framework rather than an ATLAS submission.

---

## Peer Review Notes

### PRN-001 — arXiv Endorsement Status (2026-05-07)

Paper 1 arXiv submission is pending endorsement (code: YKCPZG). MITRE formal submission is blocked until arXiv ID is obtained. No action required from community — tracking here for transparency.

---

### PRN-002 — Mondrian Framework Citation (Layer 0)

Layer 0 uses the "Mondrian" concept to describe distributed AI decision-space partitioning. The citation traces to LeFevre et al.'s data anonymization work, which is a non-obvious extension. Reviewers with background in algorithmic market microstructure are invited to assess whether the Mondrian framing is the most precise available, or whether a more direct market microstructure citation (e.g., Kyle 1985 lambda, Glosten-Milgrom) would be more technically accurate.

---

### PRN-003 — Layer 5 Path B Legal Framing

The Layer 5 draft argues that Path B (human-AI decision loop contamination) has the highest legal deniability because it passes through a human decision node. A reviewer with financial compliance background noted that this framing may be jurisdiction-dependent — some regulatory frameworks (notably EU AI Act Article 22) are moving toward holding AI system operators liable for AI-influenced decisions even when a human is nominally in the loop. The Layer 5 final version should address this jurisdictional variation.

---

---

### PRN-004 — Paper 2 Completion Status (2026-05-13)

Paper 2 integrated versions (Traditional Chinese v0.9, English v0.9) are complete as of 2026-05-13. Individual layer drafts preserved in `paper2/` for reference. OQ-2.01 through OQ-2.03 remain open for experimental follow-up; OQ-2.04 is closed (see above).

---

### PRN-005 — Mini Shai-Hulud as Layer 1 Real-World Validation (2026-05-13)

CVE-2026-45321 (Mini Shai-Hulud, 2026-05-11, CVSS 9.6) provides the first documented real-world validation of the Paper 2 §4.2 threat model: malicious packages passing cryptographic signature verification via CI/CD pipeline hijacking. This does not resolve OQ-2.01–2.03 (which require controlled experiments) but confirms that the Layer 1 attack surface is not merely theoretical. The integrated paper (§4.2) includes this as a supporting case.

---

*To add a discussion item, open a GitHub Issue with tag `[discussion]` or `[peer-review]`.*
