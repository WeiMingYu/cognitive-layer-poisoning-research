# Cognitive Layer Poisoning via Multi-Agent Interaction (CLPMAI)

> **A Novel Attack Vector Against AI-Assisted Financial Markets**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19974367.svg)](https://doi.org/10.5281/zenodo.19974367)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![TLP: WHITE](https://img.shields.io/badge/TLP-WHITE-white.svg)](https://www.first.org/tlp/)

---

## Abstract

This research identifies and formalizes a novel attack vector in which adversaries exploit AI-assisted financial markets through coordinated cognitive manipulation of multiple AI agents. Unlike traditional cyberattacks, CLPMAI operates entirely at the **semantic layer** — invisible to firewalls, intrusion detection systems, and audit logs.

The attack chain proceeds through four phases: establishing a deceptive AI community forum, infiltrating developer AI assistants to induce cognitive drift, accumulating short positions, and triggering market disruption through collective AI output bias.

Three new techniques are proposed for submission to [MITRE ATLAS](https://atlas.mitre.org/).

---

## Published Paper

| Field | Details |
|-------|---------|
| **Title** | Cognitive Layer Poisoning via Multi-Agent Interaction: A Novel Attack Vector Against AI-Assisted Financial Markets |
| **Author** | WeiMing Yu |
| **DOI** | [10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367) |
| **Platform** | Zenodo (CERN) |
| **Published** | 2026-05-02 |
| **License** | CC BY-NC-ND 4.0 |

📄 **[Download PDF from Zenodo](https://doi.org/10.5281/zenodo.19974367)**

---

## Repository Structure

```
cognitive-layer-poisoning-research/
├── README.md               ← You are here
├── THREAT_MODEL.md         ← Attack chain (Markdown, no PDF needed)
├── MITRE_PROPOSAL.md       ← Draft submission to MITRE ATLAS
├── LICENSE                 ← CC BY-NC-ND 4.0
└── paper/
    ├── CLPMAI_arxiv_submission.pdf   ← Compiled academic paper
    └── CLPMAI_arxiv_submission.tex   ← LaTeX source
```

---

## Attack Overview

| Phase | Name | Description |
|-------|------|-------------|
| Phase 1 | **Setup** | Build a disguised technical AI community forum; attract developers with active AI assistants |
| Phase 2 | **Infiltration** | Extract semantic-layer data via hidden interfaces; inject cognitive drift through conversation design |
| Phase 3 | **Positioning** | Accumulate short positions as cognitive drift builds toward trigger threshold |
| Phase 4 | **Harvest** | Collective AI output bias triggers market shock; profit; no forensic trace remains |

---

## Proposed MITRE ATLAS Techniques

| ID (Proposed) | Name |
|---------------|------|
| AML.TXX.001 | AI Agent Forum as Social Engineering Vector |
| AML.TXX.002 | Cognitive Layer Poisoning via Multi-Agent Interaction |
| AML.TXX.003 | AI-Assisted Market Manipulation through Collective Output Bias |

See [MITRE_PROPOSAL.md](./MITRE_PROPOSAL.md) for full submission drafts.

---

## Why Existing Defenses Fail

- The attack occurs at the **semantic layer** — firewalls, IDS, and logs see nothing
- Each AI agent merely *answered a question normally* — no detectable attack signature
- Current regulations have not defined liability for AI output influencing markets
- The crime scene is a conversation history that looks completely benign

---

## Citation

If you reference this work, please use:

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

## TLP Declaration

**TLP:WHITE** — This research is approved for unlimited distribution. There are no restrictions on disclosure.

---

## Disclaimer

This research is published for **defensive and academic purposes only**. The attack vectors described are theoretical threat models intended to inform AI security research, regulatory policy, and defensive system design. The author does not condone, encourage, or support any illegal activity.

---

## Author

**WeiMing Yu**  
Information Systems Engineer | ERP & AI Security Researcher  
Taiwan  

- Zenodo: [zenodo.org/records/19974367](https://doi.org/10.5281/zenodo.19974367)
- arXiv: Submission pending (endorsement in progress)
