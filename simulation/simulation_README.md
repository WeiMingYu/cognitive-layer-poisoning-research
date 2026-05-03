# CLPMAI Simulation — Educational Scope Notice

## What This Is

`clpmai_simulation.html` is a purely educational, narrative-driven interactive demonstration of the CLPMAI attack concept.

It is designed to help readers understand *why* cognitive layer poisoning is difficult to detect by walking through the attacker's perspective in a scenario format.

## What This Is Not

- This simulation contains **no executable attack code**
- It makes **no real API calls** to any AI service
- It does **not** demonstrate actual model poisoning or prompt injection
- All "AI responses" shown are pre-written narrative scripts, not live model outputs

## Technical Implementation

The simulation is a static HTML file. All interactivity is handled by JavaScript that:
- Switches between pre-written scenario cards based on user role selection
- Updates UI state (progress dots, card colors, text content)
- Links to the published research paper at the end

No network requests are made. No data is collected. No external scripts are loaded.

## Intended Audience

- AI security researchers seeking an intuitive entry point to the CLPMAI concept
- Developers evaluating their own toolchain exposure
- Financial professionals assessing AI-assisted decision workflow risks
- Educators teaching AI safety and adversarial ML concepts

---

*Part of the CLPMAI Research Series — WeiMing Yu, 2026*  
*Full paper: [DOI 10.5281/zenodo.19974367](https://doi.org/10.5281/zenodo.19974367)*
