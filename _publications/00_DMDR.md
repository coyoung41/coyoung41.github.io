---
title: "Restoring Noisy Demonstration for Imitation Learning With Diffusion Models"
collection: publications
category: manuscripts
# permalink: /publication/2024-02-17-paper-title-number-4
excerpt: 'Most imitation learning methods assume perfect expert demonstrations, yet real data is often noisy. We propose a filter-and-restore framework that isolates clean samples and uses conditional diffusion models to recover noisy demonstrations. Experiments on robot arm manipulation, dexterous manipulation, and locomotion show consistent improvements over existing methods, with ablations confirming robustness to diverse noise types and levels.'
date: 2026-01-01
venue: 'IEEE Transactions on Neural Networks and Learning Systems'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/11168119'
# citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---

Imitation learning (IL) aims to learn a policy from expert demonstrations and has been applied to various applications. By learning from the expert policy, IL methods do not require environmental interactions or reward signals. However, most existing IL algorithms assume perfect expert demonstrations, but expert demonstrations often contain imperfections caused by errors from human experts or sensor/control system inaccuracies. To address the above problems, this work proposes a filter-and-restore framework to best leverage expert demonstrations with inherent noise. Our proposed method first filters clean samples from the demonstrations and then learns conditional diffusion models to recover the noisy ones. We evaluate our proposed framework and existing methods in various domains, including robot arm manipulation, dexterous manipulation, and locomotion. The experiment results show that our proposed framework consistently outperforms existing methods across all the tasks. Ablation studies further validate the effectiveness of each component and demonstrate the framework’s robustness to different noise types and levels. These results confirm the practical applicability of our framework to noisy offline demonstration data.