---
title: (@MBZUAI) Robustness and multi-agent systems
order: 20
image: projects/peritomoreno.png
---

Multi-agent LLM systems increasingly rely on communication protocols for coordination, yet their robustness under adversarial and structural constraints remains poorly understood. Building on prior work showing that cheap-talk channels enable cooperation in LLM coordination games, we investigate two vulnerability classes in a 4-player Stag Hunt across six model families and 720 trials.

First, when Byzantine agents signal cooperation but defect, non-Byzantine agents detect the betrayal within one round yet fail to adapt collectively: a substantial fraction continue cooperating despite repeated exploitation, unable to recover coordination due to the game's unanimity payoff structure. Second, explicitly restricting communication topology collapses cooperation, while applying identical restrictions silently preserves near-perfect cooperation. This establishes that coordination failure stems from agents' meta-reasoning about hidden information, not information loss itself.

We identify two stable behavioral archetypes that replicate across all model cohorts: Defection-Prone models that switch permanently after betrayal, and Cooperation-Persistent models that continue cooperating at significant individual cost.

These findings reveal concrete security vulnerabilities: communication channels can be exploited as adversarial injection vectors, and disclosing network topology to agents can degrade coordination even without any adversary present.

Please reference the "Publications" page for relevant link of the project.
