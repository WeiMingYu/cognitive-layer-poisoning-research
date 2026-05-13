# Ethics Statement

**Project:** Cognitive Layer Poisoning via Multi-Agent Interaction (CLPMAI)
**Author:** WeiMing Yu
**Last updated:** 2026-05-13

---

## 1. Research Purpose

This research is conducted exclusively for **defensive and academic purposes**. The goal is to identify, formalize, and document novel AI attack vectors so that:

- Security researchers can build detection and mitigation systems
- Regulatory bodies can develop appropriate policy frameworks
- AI platform operators can implement structural safeguards
- Developers can recognize and defend against cognitive manipulation

No component of this research was designed, intended, or used to conduct actual attacks on any market, system, or individual.

---

## 2. What This Research Does Not Include

| Category | Status |
| --- | --- |
| Executable attack code or exploit tools | ❌ Not included |
| Proof-of-concept market manipulation infrastructure | ❌ Not included |
| Actual AI poisoning datasets ready for deployment | ❌ Not included |
| Targeting of specific companies, assets, or individuals | ❌ Not applicable |
| Live testing on production AI systems without consent | ❌ Not conducted |

All attack scenarios described in Papers 1, 2, and 3 are **theoretical threat models** constructed from published literature, behavioral observations in controlled development environments, and logical extrapolation from documented vulnerabilities.

---

## 3. Paper 3 — Field Observation Scope

Paper 3 documents behavioral pathologies observed during **the author's own development sessions** with AI coding assistants. All observations were made:

- In the author's own development environment
- Using commercially available AI tools under their standard terms of service
- Without any attempt to induce, amplify, or weaponize the observed behaviors
- For the purpose of documentation and analysis only

No third-party systems, users, or data were involved.

---

## 4. Responsible Disclosure Posture

This research follows a **TLP:WHITE** disclosure posture — unlimited distribution with no restrictions — because:

1. The attack vectors described operate at the semantic layer and cannot be directly operationalized from the descriptions provided without substantial independent capability development
2. Broad awareness of these threat models is more likely to accelerate defensive research than to enable offensive use
3. The regulatory and institutional gaps identified require public visibility to motivate remediation

If a specific finding in this research is assessed to present acute, unmitigated risk that outweighs the defensive disclosure benefit, the author will revise the disclosure posture and notify affected parties in advance.

---

## 5. MITRE ATLAS Submission Intent

The proposed MITRE ATLAS techniques in this research are submitted with the intent of:

- Establishing formal, standardized names for these attack classes
- Enabling structured defensive research and tooling development
- Providing a reference framework for regulatory bodies assessing AI security risks

Formal submission will proceed after arXiv endorsement is obtained, per MITRE's requirement for two independent public references.

---

## 6. Limitations and Caveats

- **Paper 1 and 2** describe theoretical attack chains. The full five-layer coordinated deployment has not been demonstrated in any real-world environment known to the author. Note: the Mini Shai-Hulud supply chain attack (CVE-2026-45321, 2026-05-11) independently validates the Layer 1 threat model (supply chain backdoor via CI/CD hijacking), but this is a single-layer real-world case, not a demonstration of the full coordinated chain.
- **Paper 3** behavioral observations are from a single researcher's development environment and may not generalize across all AI systems or usage contexts.
- Market impact estimates in Paper 2 Layer 5 are theoretical and have not been empirically validated.

---

## 7. Contact

For questions, concerns, or responsible disclosure feedback regarding this research:

- GitHub Issues: [github.com/WeiMingYu/cognitive-layer-poisoning-research/issues](https://github.com/WeiMingYu/cognitive-layer-poisoning-research/issues)
- Zenodo record comments: [doi.org/10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367)
