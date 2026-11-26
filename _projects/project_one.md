---
title: (@MBZUAI) Synthetic QA generation and data quality
order: 20
image: projects/peritomoreno.png
---

Large language models increasingly rely on synthetic question-answer (QA) pipelines to create domain-specific training data. We argue that their primary challenge is not generating data, but defining quality. Through a petroleum-engineering case study, we show that quality is neither a single property of the final QA pair nor fixed in advance, but emerges through iterative refinement involving subject-matter experts (SMEs) and ML engineers, with domain- and task-dependent criteria.

In our usecase of downstream GRPO training, PINE, our resulting QA dataset, improves performance on three held-out petroleum-engineering QA benchmarks: EarthSE Geo QA and SEG QA by +4.1 points each, and DISKOS QA by +2.1, while an in-house baseline saturates and regresses. We further introduce Learning Potential (LP), an RL-aware criterion for identifying useful training signal: on the saturated baseline, high-LP selection yields +9.4 on EarthSE Geo QA versus +4.9 for random selection. Experiments on GSM8K, Qwen3.5-4B, and an independent QA-generation pipeline further support this relationship while showing that LP is policy-dependent.

Overall, synthetic QA quality must be defined throughout the pipeline and aligned with its downstream use.

Please reference the "Publications" page for relevant link of the project.
