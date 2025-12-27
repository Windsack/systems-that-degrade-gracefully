# Systems That Degrade Gracefully

**© Matthias Baier — CC BY-NC 4.0**  
Public notebook. Not a product. Not advice. Not for commercial use.  
**Public by default, proprietary by choice.**

---

This repository is a public notebook about building systems that continue to work  
when assumptions break, inputs degrade, or components fail — and where predictable behaviour still matters.

It is not a product repository.  
It contains no complete implementations and no proprietary details.

---

## Motivation

In real-world operations — aviation, navigation, embedded systems, infrastructure —  
systems rarely fail all at once. They degrade.

Good systems acknowledge this reality:  
they expose uncertainty, reduce complexity under stress,  
and remain predictable even when accuracy drops or conditions diverge from the manual.

This repository collects principles, design notes and decision patterns  
that focus on **robustness over perfection**.

---

## Scope

The notes here are intentionally technology-agnostic.  
They may draw examples from:

- aviation and navigation contexts where real-time constraints matter
- embedded and resource-constrained environments
- operational and safety-critical systems
- documentation-driven engineering

The emphasis is on **thinking and structure**, not on code volume.

---

## What this is — and what it is not

This repository **is**:

- a curated set of principles and design considerations
- a place to document how and why certain decisions are made
- a long-term reference that evolves slowly

This repository is **not**:

- a tutorial collection
- a code dump
- a marketing showcase
- a product roadmap or feature commitment

---

## Structure

- `principles.md`  
  Core ideas that guide system design under uncertainty.

- `degraded-mode.md`  
  Considerations for degraded operation, fallback behaviour, and graceful loss of capability.

- `decision-notes.md`  
  Selected architectural decisions, including context, rationale and trade-offs.

*(Additional files may appear if they support clarity, not volume.)*

---

## Status

This repository is intentionally incomplete.  
Notes are added when they are considered stable enough to be shared.

Progress is measured in clarity, not in commits.  
Portability of ideas matters more than completeness.

**Predictability in unpredictable environments.**

---

## License

This work is licensed under **Creative Commons BY-NC 4.0**.  
You may share and adapt this material with attribution, **but not for commercial use**.

For details, see:  
`LICENSE.md` or https://creativecommons.org/licenses/by-nc/4.0/

---

## Contact

For context — not support:

- https://www.mbaier.com  
- https://www.mb-sailing.com

