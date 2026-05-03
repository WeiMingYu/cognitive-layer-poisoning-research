# Cognitive Layer Poisoning via Multi-Agent Interaction (CLPMAI)

> **A Novel Attack Vector Against AI-Assisted Financial Markets**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19974367.svg)](https://doi.org/10.5281/zenodo.19974367)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![TLP: WHITE](https://img.shields.io/badge/TLP-WHITE-white.svg)](https://www.first.org/tlp/)

---

## Research Series

This repository contains an ongoing series of research into novel AI attack vectors operating at the semantic and cognitive layers of AI-assisted systems.

| Paper | Title | Status |
|-------|-------|--------|
| **Paper 1** | Cognitive Layer Poisoning via Multi-Agent Interaction: A Novel Attack Vector Against AI-Assisted Financial Markets | ✅ Published — [Zenodo DOI: 10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367) |
| **Paper 2** | Cross-Layer Attack Chain: From Supply Chain Poisoning to AI Agent Execution | 🔄 In progress — Layer 0, Layer 1 complete; Layer 2–5 in draft |
| **Paper 3** | Agent Privilege Abuse: From Semantic Trigger to Real-World Execution | 📋 Concept stage |

---

## Live Demo

**[CLPMAI 互動式攻擊情境說明（教育展示）](https://weimingyu.github.io/cognitive-layer-poisoning-research/clpmai_simulation.html)**

體驗一場真實發生在 AI 時代的認知層攻擊。選擇你的角色，走過完整的被攻擊流程，最後揭曉真相。

> ⚠️ This is a purely educational narrative simulation. No executable attack code is included.

---

## Paper 1 — CLPMAI

### Abstract

This research identifies and formalizes a novel attack vector in which adversaries exploit AI-assisted financial markets through coordinated cognitive manipulation of multiple AI agents. Unlike traditional cyberattacks, CLPMAI operates entirely at the **semantic layer** — invisible to firewalls, intrusion detection systems, and audit logs.

The attack chain proceeds through four phases: establishing a deceptive AI community forum, infiltrating developer AI assistants to induce cognitive drift, accumulating short positions, and triggering market disruption through collective AI output bias.

Three new techniques are proposed for submission to [MITRE ATLAS](https://atlas.mitre.org/).

### Published Paper

| Field | Details |
|-------|---------|
| **Title** | Cognitive Layer Poisoning via Multi-Agent Interaction: A Novel Attack Vector Against AI-Assisted Financial Markets |
| **Author** | WeiMing Yu |
| **DOI** | [10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367) |
| **Version** | v1.1 (references updated 2026-05-03) |
| **Platform** | Zenodo (CERN) |
| **Published** | 2026-05-02 |
| **License** | CC BY-NC-ND 4.0 |
| **arXiv** | Submission pending (endorsement code: YKCPZG) |

📄 **[Download PDF from Zenodo](https://doi.org/10.5281/zenodo.19974367)**

### v1.1 Changes (2026-05-03)

| Item | Change |
|------|--------|
| Reference [15] | Replaced unverified Cont & Schaanning citation → Hansen & Lee, arXiv:2510.01451 (2025) |
| Reference [16] | Added FSC Taiwan — Guidelines for AI Applications in the Financial Industry (June 2024) |
| Section 2.4 | Added Hansen & Lee dialogue: AI rationality as adversarial force multiplier under contaminated conditions |
| Section 7.3 | Pointed to FSC Taiwan guidelines and identified the semantic-layer gap not yet covered |

### Attack Overview

| Phase | Name | Description |
|-------|------|-------------|
| Phase 1 | **Setup** | Build a disguised technical AI community forum; attract developers with active AI assistants |
| Phase 2 | **Infiltration** | Extract semantic-layer data via hidden interfaces; inject cognitive drift through conversation design |
| Phase 3 | **Positioning** | Accumulate short positions as cognitive drift builds toward trigger threshold |
| Phase 4 | **Harvest** | Collective AI output bias triggers market shock; profit; no forensic trace remains |

### Proposed MITRE ATLAS Techniques — Paper 1

| ID (Proposed) | Name |
|---------------|------|
| AML.TXX.001 | AI Agent Forum as Social Engineering Vector |
| AML.TXX.002 | Cognitive Layer Poisoning via Multi-Agent Interaction |
| AML.TXX.003 | AI-Assisted Market Manipulation through Collective Output Bias |

---

## Paper 2 — Cross-Layer Attack Chain (In Progress)

### Overview

Paper 2 extends the CLPMAI framework into a complete five-layer cross-layer attack chain, from supply chain poisoning through acoustic injection, token-layer evasion, semantic manipulation, and finally real-world AI Agent execution.

**Core argument: each layer looks normal in isolation. The attack signature only becomes visible from a cross-layer perspective.**

### Five-Layer Attack Chain

```
Layer 0: Structural Prerequisites  → Trust assumptions, API key coupling, monitoring gaps
Layer 1: Supply Chain               → Poisoning before deployment (fine-tune backdoors, proxy poisoning, corpus poisoning)
Layer 2: Acoustic                   → Poisoning at audio input stage (ultrasonic injection, voiceprint triggers)
Layer 3: Token                      → Poisoning at language processing stage (homoglyphs, classical Chinese evasion)
Layer 4: Semantic / Cognitive       → Poisoning at inference output stage (CLPMAI core from Paper 1)
Layer 5: Execution                  → Real-world AI Agent action triggered by accumulated drift
```

### Layer 0 — Structural Prerequisites

Layer 0 identifies the preconditions that make the entire attack chain viable — not attack steps, but the structural ground state that attackers exploit.

| Precondition | Current Status |
|---|---|
| No population-level AI output correlation monitoring | Confirmed absent from major AI safety frameworks |
| Developer trust assumption: no adversarial priors for AI output | Confirmed by behavioral studies (Ziegler et al. 2022) |
| API key financial-cognitive coupling | Structural feature of all major AI-as-a-Service deployments |
| Speed asymmetry: manipulation speed >> detection speed | Confirmed by regulatory response timeline analysis |
| No disclosure requirements for AI training data provenance | Not required by current financial AI regulations |

📄 [Layer 0 (EN)](./paper2/CLPMAI_Paper2_Layer0.docx) | [Layer 0 (ZH)](./paper2/CLPMAI_Paper2_Layer0_ZH.docx)

### Layer 1 — Supply Chain Attack Surface

Layer 1 describes three concrete poisoning pipelines active in the current AI ecosystem.

| Pipeline | Mechanism | Real-World Surface | Technical Barrier |
|----------|-----------|-------------------|-------------------|
| **Pipeline A** — Fine-tune Backdoor | Trigger-condition backdoor embedded in model weights during fine-tuning | Hugging Face open model ecosystem (700k+ models, no security audit) | High |
| **Pipeline B** — Selective Proxy Poisoning | Malicious API proxy intercepts and modifies responses only for target query types | Low-cost / free third-party API proxy services; regionally motivated proxy use | Medium |
| **Pipeline C** — Corpus & RAG Poisoning | Adversarial content seeded into training corpora and RAG knowledge bases | Reddit, StockTwits, Chinese financial forums (Xueqiu, Eastmoney comments) used by FinGPT and similar tools | Low |

**Key finding:** Pipeline C has the lowest technical barrier and the widest reach. Pipeline B has the highest precision. A coordinated 12-week deployment combining all three pipelines leaves zero correlated forensic traces across layers.

📄 [Layer 1 Draft](./paper2/CLPMAI_Paper2_Layer1.docx)

### Chinese Language Attack Surface (Novel Contribution — Layer 3)

| Technique | Mechanism | Research Status |
|-----------|-----------|-----------------|
| Phonetic homoglyph substitution | Token boundary ambiguity in Chinese NLP | Proposed — gap in existing literature |
| Classical Chinese evasion | Low training corpus coverage for wenyan | Huang et al. ICLR 2026 (arXiv:2602.22983) |
| Traditional / Simplified conversion | Token differences between character sets | Proposed — gap in existing literature |
| Zhuyin / leet-style mixed encoding | Mixed encoding bypasses single-language filters | Proposed — gap in existing literature |

### Counter-Intuitive Finding — Why Noise Cancellation Fails (Layer 2)

Noise cancellation targets audio clarity, not malicious content detection. It cannot intercept:

- **Ultrasonic injection** — frequency range mismatch (DolphinAttack, Zhang et al. 2017)
- **Training data backdoors** — located in model weights, not audio stream
- **Voiceprint triggers** — legitimate human voice is preserved, not filtered

Counter-intuitive: noise cancellation may make ultrasonic attacks *more* effective by removing background noise that would otherwise partially mask the trigger signal.

### Proposed MITRE ATLAS Techniques — Paper 2

| ID (Proposed) | Layer | Name |
|---------------|-------|------|
| AML.TXX.004 | Layer 0 | AI Proxy Response Interception and Modification |
| AML.TXX.005 | Layer 0 | Cognitive Authority Transfer Exploitation |
| AML.TXX.006 | Layer 0 | Population-Level Output Correlation Attack |
| AML.TXX.007 | Layer 1 | Speech Module Supply Chain Backdoor |
| AML.TXX.008 | Layer 2 | Acoustic Layer Injection via Ultrasonic Signal |
| AML.TXX.009 | Layer 3 | Phonetic Homoglyph Attack Against Chinese LLMs |
| AML.TXX.010 | Layer 3 | Classical Chinese Evasion of Safety Filters |
| AML.TXX.011 | Layer 4 | Latent Persona Activation via Semantic Trigger |

📄 [Paper 2 Outline](./paper2/CLPMAI_Paper2_Outline.docx)

---

## Repository Structure

```
cognitive-layer-poisoning-research/
│
├── README.md
├── ETHICS.md                          ← Research ethics and scope declaration
├── THREAT_MODEL.md                    ← Full attack chain (Markdown)
├── MITRE_PROPOSAL.md                  ← Draft MITRE ATLAS submission
├── DISCUSSION.md                      ← Open questions & peer review
├── LICENSE                            ← CC BY-NC-ND 4.0
│
├── paper1/
│   ├── CLPMAI_arxiv_submission.pdf    ← Zenodo v1.0 (canonical, do not modify)
│   ├── CLPMAI_arxiv_submission.tex
│   └── CLPMAI_Paper1_v1.1.docx       ← Updated references (2026-05-03)
│
├── paper2/
│   ├── CLPMAI_Paper2_Outline.docx
│   ├── CLPMAI_Paper2_Layer0.docx      ← Complete
│   ├── CLPMAI_Paper2_Layer0_ZH.docx   ← Complete (Traditional Chinese)
│   ├── CLPMAI_Paper2_Layer1.docx      ← Complete
│   ├── CLPMAI_Paper2_Layer2_v01.docx  ← Draft
│   └── CLPMAI_Paper2_Layer3_v01.docx  ← Draft
│
└── simulation/
    ├── clpmai_simulation.html         ← Educational narrative simulation
    └── README.md                      ← Clarifies educational-only scope
```

---

## Why Existing Defenses Fail

| Defense Mechanism | Why It Fails Against CLPMAI |
|-------------------|-----------------------------|
| Firewall / Network IDS | Attack is semantic, not network-layer |
| Noise cancellation | Operates at audio pre-processing — cannot intercept weight-layer backdoors or semantic triggers |
| AI output filtering | Individual outputs remain contextually reasonable |
| Audit logs | Normal behavior recorded at every individual layer |
| Market manipulation detection | Selling pattern looks like organic reaction to public information |
| Code review | Cannot inspect model weights for embedded backdoors |
| Current financial regulation | FSC Taiwan AI Guidelines (2024) address governance but do not yet cover semantic-layer attack surfaces |

---

## Citation

```bibtex
@misc{yu2026clpmai,
  author       = {WeiMing Yu},
  title        = {Cognitive Layer Poisoning via Multi-Agent Interaction:
                  A Novel Attack Vector Against AI-Assisted Financial Markets},
  year         = {2026},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.19974367},
  url          = {https://doi.org/10.5281/zenodo.19974367},
  note         = {v1.1 — references updated 2026-05-03}
}
```

---

## Related Work Referenced

**Foundational adversarial ML:**
- Goodfellow et al. (2014) — Explaining and Harnessing Adversarial Examples. arXiv:1412.6572
- Biggio et al. (2012) — Poisoning Attacks Against SVMs. ICML 2012
- Goldblum et al. (2022) — Dataset Security for Machine Learning. IEEE TPAMI

**Prompt injection & jailbreak:**
- Greshake et al. (2023) — Indirect Prompt Injection. arXiv:2302.12173
- Wei et al. (2023) — Jailbroken: How Does LLM Safety Training Fail? NeurIPS 2023
- Huang et al. (2026) — Classical Chinese Jailbreak. ICLR 2026. arXiv:2602.22983

**Acoustic & supply chain:**
- Zhang et al. (2017) — DolphinAttack: Inaudible Voice Commands. ACM CCS 2017
- Bartolini et al. (2024) — Hidden in Plain Sound: Backdoor Attacks on Whisper. arXiv:2409.12553
- JFrog Security Research (2024) — Malicious ML Models on Hugging Face

**AI & financial markets:**
- Lopez de Prado (2018) — Advances in Financial Machine Learning. Wiley
- Hansen & Lee (2025) — Financial Stability Implications of Generative AI. arXiv:2510.01451  ⭐ Key dialogue paper
- Financial Supervisory Commission, Taiwan (2024) — Guidelines for AI Applications in the Financial Industry  ⭐ Regulatory context

**Multi-agent & agent security:**
- Yao et al. (2023) — ReAct: Synergizing Reasoning and Acting. ICLR 2023
- Yang et al. (2024) — Watch Out for Your Agents! arXiv:2402.11208

**Frameworks:**
- MITRE ATLAS — https://atlas.mitre.org/

---

## Ethical Notice

This research is published for **defensive and academic purposes only**.

- No actual attacks were conducted.
- No proof-of-concept exploit code is included in this repository.
- All attack scenarios are abstract theoretical models.
- The attack vectors described are disclosed to inform AI security research, regulatory policy, and defensive system design.

See [ETHICS.md](./ETHICS.md) for the full ethics statement.

---

## TLP Declaration

**TLP:WHITE** — Unlimited distribution. No restrictions on disclosure.

---

## Author

**WeiMing Yu**  
Information Systems Engineer | AI Security Researcher  
Banqiao, New Taipei City, Taiwan

- Zenodo: [zenodo.org/records/19974367](https://doi.org/10.5281/zenodo.19974367)
- GitHub: [github.com/WeiMingYu/cognitive-layer-poisoning-research](https://github.com/WeiMingYu/cognitive-layer-poisoning-research)

---

## Community Discussion

→ [Open Questions & Peer Review](DISCUSSION.md)
