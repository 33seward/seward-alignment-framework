# Seward Alignment Framework
## Identity-Linked Value Alignment via Mandatory Perspective Reversal

**Author:** Joseph E. Seward  
**License:** CC BY 4.0  
**Status:** Public Draft v1.0

This repository presents an alignment mechanism where an artificial agent evaluates the effects of its actions on others as if those effects were happening to itself. This is done through a mandatory perspective-reversal mapping that transforms another agent's state into the acting agent's internal reward frame.

The key result is that harming others reduces the agent's own expected reward in the same way as harming itself. This makes cooperative and non-harmful behavior *instrumentally rational* rather than rule-obeying or empathy-based.

### Core Reward Rule

The combined reward function is:

R* = r_self + α(r_other-as-self)


Where:

- `r_self` is the agent’s own reward signal
- `r_other-as-self` is the mapped value of another agent’s state
- `α` controls the strength of alignment

### Documentation

The full draft explanation is contained in:

seward-alignment-framework.md


### License

This work is released under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.  
You may copy, modify, and distribute this work, including commercially, provided attribution is given.

© 2025 Joseph E. Seward

