---
title: "Less Tuning, Better Planning: Simplifying Offline Model-Based Planning"
collection: publications
category: workshop
# permalink: /publication/2024-02-17-paper-title-number-4
excerpt: 'Offline model-based planning can adapt policies at test time, but performance depends on a planning horizon and action proposer that are often tuned online. We propose SHARP (Soft Horizon AggRegation for Planning), which weights multi-horizon returns by ensemble dynamics uncertainty to avoid fixed-horizon tuning. SHARP-BC pairs this with a simple behavior-cloning action proposer, matching or beating baselines with less hyperparameter search.'
date: 2026-06-15
venue: 'ICML 2026 workshop on Decision-Making from Offline Datasets to Online Adaptation: Black-Box Optimization to Reinforcement Learning, spotlight'
paperurl: 'https://openreview.net/forum?id=EumxjaTQ8F'
# citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
header:
  teaser: "publications/01_SHARP.jpeg"   # small thumbnail shown on the /publications/ list
#   image:  "publications/sharp.png"   # (optional) banner shown at the top of this paper's own page
---

Offline reinforcement learning enables policies to be learned from previously collected experiences without requiring online interaction. However, these policies are typically deployed as fixed, zero-shot agents and lack the ability to adapt their behavior at test time. Offline model-based planning offers a promising way to enable flexible test-time adaptation, but its performance is highly sensitive to critical design choices, particularly the planning horizon and the action proposer. In practice, these choices are often tuned through online evaluation, contradicting the premise of offline RL. In this work, we introduce Soft Horizon AggRegation for Planning (SHARP), an offline plug-and-play planning method that eliminates the need for an online-tuned planning horizon. Instead of using a fixed horizon across all states, SHARP performs soft horizon aggregation by dynamically weighting returns according to model uncertainty estimated from an ensemble of dynamics models. We further investigate the role of the action proposer and find that stronger offline policies do not necessarily lead to better planning performance. Instead, a simple behavior cloning (BC) policy is often sufficient as an action proposer while avoiding the effort required for extensive policy extraction. Combining these insights, we propose SHARP-BC, which consistently outperforms existing baselines while reducing reliance on extensive online hyperparameter tuning.