# Manuscript and presentation alignment

The website follows the active manuscript and the supplementary presentation
in the source package. This review changes website prose; it does
not modify the manuscript, slide deck, or narrated film.

## Central story

Policy alignment addresses one part of the planning–learning loop. PL-MPC
modifies critic supervision, terminal-value evaluation, and planner-to-policy
transfer. Its largest gains occur on balance-hard and hurdle, where successful
seeds demonstrate full-episode balancing and successive hurdle traversal.
Simulation-trained world models also support zero-shot online planning on the
real robot and on object sizes unseen during training.

The opening, abstract, method explanation, demonstrations, and final take-home
points now follow this same sequence.

## Claim mapping

| Website content | Authoritative source | Meaning preserved |
| --- | --- | --- |
| Motivation and three interfaces | Abstract; introduction; method; slide narration 2–6 | Planning determines learning experience; critic and actor shape future plans. Policy alignment does not address every interface. |
| Hybrid multi-step TD targets (MTD) | Method; slide 7; terminology review | Observed replay rewards reach earlier targets; model predictions under the current actor complete the target beyond replay, followed by a critic bootstrap. The fall–survival illustration is schematic. |
| Adaptive terminal estimates (ATE) | Method; slide 8; terminology review | Target-critic disagreement penalizes the online-critic terminal score during MPPI planning. ATE does not change the TD target. Disagreement is an uncertainty proxy. |
| Return-weighted actor distillation (RAD) | Method; slide 9; terminology review | Source-episode realized returns weight additional imitation of planner-executed actions. Weights are clipped and fixed during the actor update; a fixed warmup delays this additional loss. |
| Humanoid behavioral gains | Experiments; conclusions; slides 10–12 | Full-episode balancing and hurdle traversal distinguish successful seeds from survival-only return. Best-seed success is 50.9% and 58.0%; mean success is 19% on each task. |
| Broader results and ablations | Experiments; conclusions | Performance remains task and seed dependent. MTD has the largest leave-one-out effect on balance-hard; removing it improves hurdle in that study. Component effects are conditional, not additive. |
| Real-robot transfer | Real-robot section; slides 13–16 | The world model is trained in simulation and used for online planning without real-world fine-tuning. Observed success is higher on the training size and both unseen sizes. |
| Scope and future work | Conclusions | Rare useful trajectories limit RAD's signal; activation timing motivates adaptive warmup. Evaluation is on TD-M(PC)²; transfer to other backbones remains future work. |

## Editorial changes

- Replaced generic slogans with the manuscript's mechanism names and concrete
  behavioral findings.
- Removed repeated trial counts, separate-trial labels, checkpoint counters,
  and process-oriented notes from the demonstration narrative.
- Consolidated reproducibility details under **Evaluation protocol** and the
  result tables. Kept sample counts, confidence intervals, successful-trial-only
  metrics, benchmark budgets, and the fixed main warmup accessible there.
- Replaced the limitation-led ending with three contribution-led take-home
  points. Kept the manuscript's scope and future directions in a disclosure.
- Preserved all result tables, downloadable data, demonstration clips, film
  narration, and necessary qualifiers. No claims of uniform gains, statistical
  significance, calibrated uncertainty, or demonstrated cross-backbone transfer
  were introduced.
