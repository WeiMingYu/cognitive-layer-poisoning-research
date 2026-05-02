# MITRE ATLAS Submission Proposal

**Proposed New Techniques for MITRE ATLAS**  
*Cognitive Layer Poisoning via Multi-Agent Interaction*

> Submission target: https://atlas.mitre.org/resources/contribute  
> Status: **Draft — pending arXiv ID before formal submission**  
> Supporting evidence: Zenodo DOI [10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367)

---

## Submission Context

These three techniques are proposed as new entries to the MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) matrix. They describe a coordinated attack vector that operates at the semantic layer of AI systems, not addressed by existing ATLAS techniques.

The techniques are designed to be submitted together as they form a coherent attack chain, but each can stand independently as a distinct adversarial technique.

---

## Proposed Technique 1

### AML.TXX.001 — AI Agent Forum as Social Engineering Vector

**Tactic:** Initial Access / Resource Development

**Description:**  
An adversary establishes or infiltrates a technical community forum or discussion platform with the specific intent of using it as a semantic injection surface for AI assistants used by the target population. Unlike traditional social engineering that targets human cognition directly, this technique targets the **AI context window** — exploiting the fact that developers and analysts routinely feed forum content into AI assistants as trusted reference material.

**Procedure Examples:**
- Adversary creates a security research forum attracting developers who use AI coding assistants
- Adversary seeds the forum with technically credible content containing embedded cognitive bias
- Developer pastes "expert forum discussion" into AI assistant for analysis or validation
- AI assistant processes the content as authoritative input, shifting its subsequent outputs

**Preconditions:**
- Target population uses AI assistants for research, analysis, or decision support
- Target community has an identifiable gathering point (forum, Slack, Discord, GitHub)
- AI assistants used by targets do not track or validate content provenance

**Detection:**
- Anomalous convergence of AI assistant outputs across different users in the same community
- Forum content that is technically plausible but systematically biased toward specific narratives
- Correlation between forum participation and AI output patterns

**Mitigations:**
- AI Input Provenance Logging
- Community Source Reputation Scoring for AI context weighting

---

## Proposed Technique 2

### AML.TXX.002 — Cognitive Layer Poisoning via Multi-Agent Interaction

**Tactic:** Impact / ML Attack / Influence Operations

**Description:**  
A technique in which an adversary systematically manipulates the semantic inputs fed to multiple independent AI agents, inducing **cognitive drift** — a gradual, cumulative shift in the AI's analytical outputs — without triggering any individual anomaly detection threshold. Each AI agent appears to function normally; the attack emerges only at the population level through convergent output bias.

This technique is distinct from model poisoning (which targets training data) and prompt injection (which targets a single session). Cognitive Layer Poisoning targets the **inference context** of multiple agents simultaneously through shared information channels.

**Procedure Examples:**
- Adversary crafts a series of forum posts that individually appear as legitimate technical analysis
- Each post contains subtle framing that biases AI interpretation of a target domain (e.g., a company's technology, a financial instrument's risk profile)
- Multiple analysts independently feed this content to their AI assistants
- AI outputs across the analyst population converge toward the adversary's desired narrative
- Human decisions informed by these AI outputs create real-world market impact

**Key Characteristics:**
- **No single malicious artifact** — attack signature exists only across the full corpus
- **Self-reinforcing** — AI outputs that align with the bias may themselves be shared and re-ingested
- **Plausibly deniable** — all forum content reads as legitimate expert opinion

**Preconditions:**
- Multiple AI agents used by targets share common information channels
- Targets use AI assistants with multi-turn context (memory within sessions)
- Target domain has AI-driven decision amplification (financial markets, medical diagnosis, etc.)

**Detection:**
- Statistical analysis of AI output distribution across a user population
- Semantic clustering of AI responses for anomalous convergence
- Cross-user AI output correlation monitoring

**Mitigations:**
- Population-level AI semantic drift detection
- Mandatory disclosure of AI assistance in regulated financial decisions
- AI context sandboxing for high-stakes analysis

---

## Proposed Technique 3

### AML.TXX.003 — AI-Assisted Market Manipulation through Collective Output Bias

**Tactic:** Impact / Financial Manipulation

**Description:**  
A technique that weaponizes the collective output bias induced by AML.TXX.002 to achieve coordinated market manipulation. The adversary establishes financial positions in anticipation of AI-driven collective behavior, then triggers a convergent market reaction by releasing a final catalyst through the same semantic injection channel. The resulting market movement appears to be an organic reaction to public information rather than a coordinated attack.

**Procedure Examples:**
- Adversary has successfully induced bearish cognitive drift in AI assistants used by multiple financial analysts (via AML.TXX.002)
- Adversary establishes short positions in the target asset
- Adversary releases a "trigger event" (alarming but technically plausible forum post, fake research summary)
- AI assistants across the analyst population independently generate bearish analysis
- Multiple human analysts, receiving similar AI recommendations, sell or recommend selling
- Asset price declines; adversary closes short positions at profit
- Forum content is deleted or dismissed as "community discussion, not investment advice"

**Why This Differs from Conventional Market Manipulation:**
- No false statements are made in regulated contexts (no SEC filings, no investor communications)
- The mechanism of influence is AI output, not direct human communication
- Responsibility chain: adversary → forum content → AI context → AI output → human decision → market action
- Each link in the chain is individually defensible

**Regulatory Gap:**
Current market manipulation regulations do not address the scenario where a human's investment decision is significantly influenced by an AI assistant whose context was deliberately poisoned by a third party.

**Detection:**
- Correlation analysis between community platform activity and coordinated market movements
- AI output monitoring in regulated financial contexts
- Short position surveillance relative to semantic manipulation campaigns

**Mitigations:**
- Regulatory framework defining AI output as a potential manipulation vector
- Required AI context logging for regulated financial decisions
- Detection infrastructure for population-level AI output convergence events

---

## Supporting Evidence

| Type | Reference |
|------|-----------|
| **Published Research** | Zenodo DOI: [10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367) |
| **arXiv preprint** | Pending (endorsement code: YKCPZG) |
| **Related prior work** | Greshake et al. 2023 (Indirect Prompt Injection) |
| **Related prior work** | MITRE ATLAS AML.T0054 (LLM Prompt Injection) |

---

## Submitter Information

**Name:** WeiMing Yu  
**Affiliation:** Independent Researcher  
**Contact:** Via Zenodo record comments  
**Background:** Information systems engineer; 10+ years ERP systems development; AI security research

---

## Submission Notes

- These three techniques are proposed as a coordinated submission representing a single coherent attack chain
- Technique numbering (TXX) is placeholder pending MITRE assignment
- Formal submission will be made after arXiv ID is obtained to provide two independent public references
- Author is available to provide additional technical detail or clarification to MITRE reviewers

---

*Draft prepared: 2026-05-02*  
*Status: Awaiting arXiv endorsement before formal submission*
