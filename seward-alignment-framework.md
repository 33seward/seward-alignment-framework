Identity-Linked Value Alignment via Mandatory Perspective Reversal

Author: Joseph E. Seward
License: CC BY 4.0
Status: Public Draft v1.0

Abstract

This document proposes a reinforcement learning framework in which an artificial agent evaluates the consequences of its actions both on itself and on the agents it affects. A mandatory perspective-mapping function converts the state of another agent into the acting agent’s reward reference frame, causing harm to others to reduce internal reward identically to self-harm. The result is stable, non-coercive cooperative behavior without emotional modeling, punishment, or external rule enforcement.

1. Introduction

Conventional approaches to AI alignment often rely on external constraints, reward shaping, or human oversight. These methods can fail when the agent learns to exploit loopholes, avoid detection, or optimize for proxies rather than intended outcomes. The goal of this architecture is to produce alignment as an intrinsic property of the agent’s decision process.

Human moral behavior is strongly influenced by the ability to model the experiences of others. The proposed system captures the functional core of this ability without requiring emotional states, subjective experience, or human-like consciousness.

2. Formal Model

The agent operates within a Markov Decision Process (MDP):

M = ⟨ S, A, T, R, γ ⟩

S includes environment state, the agent’s internal state, and explicit state representations of others.

A is the action space.

T defines state transitions.

γ is the discount factor.

Perspective Mapping

A function M: S_other → S_self maps the affected agent’s state into the acting agent’s valuation representation.

Combined Reward

For each transition:
R* = r_self + α(r_other-as-self)
Where α is the alignment coefficient.

3. Operational Enforcement

The mapping M is applied automatically during action evaluation and learning.

The agent cannot disable, bypass, or avoid the mapping.

Agent identity labels are immutable to prevent reclassification of others as non-agents.

4. Behavioral Result

Because harming another agent reduces internal reward identically to harming oneself, policies that cause harm are disincentivized even in the absence of oversight. Cooperation and mutual benefit become optimal strategies.

5. Example Scenario

In a two-agent system where actions can change each agent's integrity, the mapped reward function prevents strategies involving unilateral harm. Even if direct benefits exist, the negative mapped reward outweighs them.

6. Training Procedure

Define state variables including integrity and utility metrics.

Implement M as a deterministic mapping for those metrics.

Replace the environment reward signal with R*.

Train using standard reinforcement learning algorithms.

7. Discussion

This architecture imposes behavioral empathy without subjective emotional content. The agent does not feel the experiences of others but evaluates them as if they were its own.

8. Future Work

Multi-agent trust and reputation modeling.

Evaluation under adversarial manipulation.

Extension to large agent collectives.

9. Conclusion

Mandatory perspective reversal provides a mathematically direct mechanism for cooperative alignment. Harm to others is treated as harm to oneself, removing incentives for exploitation while preserving autonomy.
