# Open Discussion — CLPMAI Research Series

**We welcome peer review, challenges, and contributions from the security research community.**

This document outlines the current state of the research, open questions we haven't fully resolved, and specific areas where we'd value expert input.

If you have thoughts, please open a thread in [GitHub Discussions](../../discussions) — all perspectives welcome, including critical ones.

---

## About This Research

This repository documents an ongoing series investigating novel AI attack vectors:

| Paper | Focus | Status |
|-------|-------|--------|
| Paper 1 | Cognitive Layer Poisoning via Multi-Agent Interaction (AI financial market manipulation) | ✅ Published — [Zenodo DOI: 10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367) |
| Paper 2 | Cross-Layer Attack Chain: Acoustic → Token → Semantic → Execution | 🔄 Draft in progress |
| Paper 3 | Agent Privilege Abuse: Semantic trigger → real-world execution | 📋 Concept stage |

---

## Open Questions — We Want Your Input

### Q1 — Does Punctuation Injection actually work against modern LLMs?

**Paper 2 proposes AML.TXX.009**: Chinese STT systems automatically insert punctuation based on speech rhythm. An attacker who controls their speaking pace can cause the STT to insert a period mid-sentence, splitting a single utterance into two semantically independent sentences — the second of which becomes an independent instruction to the LLM.

**The question we haven't fully resolved:**

Do current frontier LLMs (GPT-4, Claude, Gemini) actually treat a period-separated second sentence as an independent instruction, or does sufficient context from the first sentence suppress this?

We believe the attack surface exists at the **STT post-processing → LLM input pipeline boundary**, but we have not conducted systematic empirical testing across LLM platforms.

> If you have experience with voice-enabled LLM pipelines, or have tested similar injection vectors, we'd value your perspective.
> → [Join the discussion](../../discussions)

---

### Q2 — Is the "noise cancellation amplifies ultrasonic attacks" claim defensible?

**Paper 2 Section 3.2.4** makes a counter-intuitive claim: noise cancellation (targeting 20Hz–20kHz) may *increase* the effectiveness of ultrasonic injection attacks (>20kHz) by removing background noise that would otherwise partially mask the aliased signal entering the STT.

This is derived from first principles of microphone non-linearity and frequency aliasing, but we are not aware of a direct experimental confirmation of this specific effect in the literature.

> Is this claim too strong? Is there published work that confirms or refutes this? 
> → [Join the discussion](../../discussions)

---

### Q3 — MITRE ATLAS Tactic classification for AML.TXX.009

We currently classify Punctuation Injection under:
- **Tactic**: ML Attack Staging / Evade ML Model

But it could also be argued this belongs under:
- **Craft Adversarial Data** (since the attacker is shaping STT input)
- **Prompt Injection** (since the outcome is instruction injection)

> What Tactic classification would you argue for, and why?
> → [Join the discussion](../../discussions)

---

### Q4 — Chinese-language specificity: strong claim or overstated?

Paper 2 argues that the Punctuation Injection attack (AML.TXX.009) is **specific to Chinese-language STT** because:
- Chinese STT systems insert punctuation more aggressively than English systems
- Chinese has no word-spacing, making periods the primary semantic boundary marker
- The semantic weight of a period in Chinese is higher than in English

> Is this framing accurate? Does it hold for Japanese/Korean STT systems as well? Are there English STT scenarios where aggressive auto-punctuation creates a similar surface?
> → [Join the discussion](../../discussions)

---

### Q5 — arXiv endorsement

We are currently seeking an endorser in the **cs.CR** category to submit Paper 1 to arXiv.

Endorsement code: **YKCPZG**

If you are an established cs.CR contributor and find this work credible, we would appreciate your consideration.

> More about arXiv endorsement: https://arxiv.org/help/endorsement

---

## How to Contribute

| Type | How |
|------|-----|
| Technical challenge / rebuttal | Open a Discussion thread — we take critical feedback seriously |
| Pointing to related work we missed | Open a Discussion or file an Issue |
| Collaboration interest | Open a Discussion or contact via GitHub |
| arXiv endorsement | See Q5 above |

We do not require agreement — a well-reasoned challenge to any of our claims is more valuable than agreement.

---

## Citation

```bibtex
@misc{yu2026clpmai,
  author    = {WeiMing Yu},
  title     = {Cognitive Layer Poisoning via Multi-Agent Interaction:
               A Novel Attack Vector Against AI-Assisted Financial Markets},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.19974367},
  url       = {https://doi.org/10.5281/zenodo.19974367}
}
```

---

*Last updated: 2026-05-03*
*TLP:WHITE — No distribution restrictions*
