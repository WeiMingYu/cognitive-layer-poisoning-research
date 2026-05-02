# Cognitive Layer Poisoning via Multi-Agent Interaction (CLPMAI)

> **A Novel Attack Vector Against AI-Assisted Financial Markets**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19974367.svg)](https://doi.org/10.5281/zenodo.19974367)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![TLP: WHITE](https://img.shields.io/badge/TLP-WHITE-white.svg)](https://www.first.org/tlp/)

---

## Research Series

This repository contains an ongoing series of research into novel AI attack vectors.

| Paper | Title | Status |
|-------|-------|--------|
| **Paper 1** | Cognitive Layer Poisoning via Multi-Agent Interaction: A Novel Attack Vector Against AI-Assisted Financial Markets | ✅ Published — [Zenodo DOI: 10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367) |
| **Paper 2** | Cross-Layer Attack Chain: From Acoustic Injection to Cognitive Manipulation in AI Voice-Enabled Systems | 🔄 Draft outline — [`paper2/CLPMAI_Paper2_Outline_v02.docx`](./paper2/CLPMAI_Paper2_Outline_v02.docx) |
| **Paper 3** | Agent Privilege Abuse: From Semantic Trigger to Real-World Execution | 📋 Concept stage |

---
## Live Demo

**[CLPMAI 互動式攻擊模擬](https://weimingyu.github.io/cognitive-layer-poisoning-research/clpmai_simulation.html)**  
體驗一場真實發生在 AI 時代的認知層攻擊。選擇你的角色，走過完整的被攻擊流程，最後揭曉真相。
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
| **Platform** | Zenodo (CERN) |
| **Published** | 2026-05-02 |
| **License** | CC BY-NC-ND 4.0 |

📄 **[Download PDF from Zenodo](https://doi.org/10.5281/zenodo.19974367)**

### Attack Overview

| Phase | Name | Description |
|-------|------|-------------|
| Phase 1 | **Setup** | Build a disguised technical AI community forum; attract developers with active AI assistants |
| Phase 2 | **Infiltration** | Extract semantic-layer data via hidden interfaces; inject cognitive drift through conversation design |
| Phase 3 | **Positioning** | Accumulate short positions as cognitive drift builds toward trigger threshold |
| Phase 4 | **Harvest** | Collective AI output bias triggers market shock; profit; no forensic trace remains |

### Proposed MITRE ATLAS Techniques (Paper 1)

| ID (Proposed) | Name |
|---------------|------|
| AML.TXX.001 | AI Agent Forum as Social Engineering Vector |
| AML.TXX.002 | Cognitive Layer Poisoning via Multi-Agent Interaction |
| AML.TXX.003 | AI-Assisted Market Manipulation through Collective Output Bias |

---

## Paper 2 — Cross-Layer Attack Chain (Draft)

### Overview

Paper 2 extends the CLPMAI framework into a full five-layer cross-layer attack chain model, from supply chain poisoning through acoustic injection, token-layer evasion, semantic manipulation, and finally real-world AI Agent execution.

### Five-Layer Attack Chain

```
Layer 1: Supply Chain    → Poisoning happens before deployment
Layer 2: Acoustic        → Poisoning happens at audio input stage
Layer 3: Token           → Poisoning happens at language processing stage
Layer 4: Semantic/Cognitive → Poisoning happens at inference output stage (CLPMAI core)
Layer 5: Execution       → Poisoning translates into real-world actions
```

**Core argument: each layer looks normal in isolation. The attack signature only becomes visible from a cross-layer perspective.**

### Chinese Language Attack Surface (Novel Contribution)

| Technique | Mechanism | Research Status |
|-----------|-----------|-----------------|
| Phonetic homoglyph substitution | Token boundary ambiguity | Proposed — gap in existing literature |
| Classical Chinese evasion | Low training corpus coverage for wenyan | Huang et al. ICLR 2026 |
| Traditional/Simplified conversion | Token differences between character sets | Proposed — gap in existing literature |
| Zhuyin / leet-style mixed encoding | Mixed encoding bypasses single-language filters | Proposed — gap in existing literature |

### Why Noise Cancellation Fails (Counter-Intuitive Finding)

Noise cancellation targets audio clarity — not malicious content detection. It operates at the pre-processing layer and cannot intercept:
- Ultrasonic injection (frequency range mismatch — DolphinAttack, Zhang et al. 2017)
- Training data backdoors (located in model weights, not audio stream)
- Voiceprint triggers (legitimate human voice is preserved, not filtered)

Counter-intuitive: noise cancellation may make ultrasonic attacks *more* effective by removing background noise that would otherwise partially mask the trigger signal.

### New Proposed MITRE ATLAS Techniques (Paper 2)

| ID (Proposed) | Name |
|---------------|------|
| AML.TXX.004 | Speech Module Supply Chain Backdoor |
| AML.TXX.005 | Acoustic Layer Injection via Ultrasonic Signal |
| AML.TXX.006 | Phonetic Homoglyph Attack Against Chinese LLMs |
| AML.TXX.007 | Classical Chinese Evasion of Safety Filters |
| AML.TXX.008 | Latent Persona Activation via Semantic Trigger |

📄 **[Read Paper 2 Draft Outline](./paper2/CLPMAI_Paper2_Outline_v02.docx)**

---

## Repository Structure

```
cognitive-layer-poisoning-research/
├── README.md
├── THREAT_MODEL.md         ← Attack chain (Markdown)
├── MITRE_PROPOSAL.md       ← Draft MITRE ATLAS submission
├── LICENSE                 ← CC BY-NC-ND 4.0
├── paper/
│   ├── CLPMAI_arxiv_submission.pdf
│   └── CLPMAI_arxiv_submission.tex
└── paper2/
    └── CLPMAI_Paper2_Outline_v02.docx
```

---

## Why Existing Defenses Fail

| Defense Mechanism | Why It Fails |
|-------------------|-------------|
| Firewall / Network IDS | Attack is semantic, not network-layer |
| Noise cancellation | Operates at audio pre-processing — cannot intercept weight-layer backdoors or semantic triggers |
| AI output filtering | Individual outputs are contextually reasonable |
| Audit logs | Logs show normal behavior at every layer |
| Market manipulation detection | Selling pattern looks like organic reaction to public information |
| Code review | Cannot inspect model weights for backdoors |

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
  url          = {https://doi.org/10.5281/zenodo.19974367}
}
```

---

## Related Work Referenced

- Greshake et al. (2023) — Indirect Prompt Injection. arXiv:2302.12173
- Zhang et al. (2017) — DolphinAttack: Inaudible Voice Commands. ACM CCS 2017
- Bartolini et al. (2024) — Hidden in Plain Sound: Backdoor Attacks on Whisper. arXiv:2409.12553
- Huang et al. (2026) — Obscure but Effective: Classical Chinese Jailbreak. ICLR 2026. arXiv:2602.22983
- Deng et al. (2023) — Multilingual Jailbreak Challenges in LLMs. arXiv:2310.06474
- MITRE ATLAS — https://atlas.mitre.org/

---

## TLP Declaration

**TLP:WHITE** — Unlimited distribution. No restrictions on disclosure.

---

## Disclaimer

This research is published for **defensive and academic purposes only**. The attack vectors described are theoretical threat models intended to inform AI security research, regulatory policy, and defensive system design.

---

## Author

**WeiMing Yu**
Information Systems Engineer | AI Security Researcher
Banqiao, New Taipei City, Taiwan

- Zenodo: [zenodo.org/records/19974367](https://doi.org/10.5281/zenodo.19974367)
- arXiv: Submission pending (endorsement code: YKCPZG)
