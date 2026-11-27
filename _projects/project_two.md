---
title: (@MBZUAI) RL-based Curriculum Learning
order: 15
image: projects/salta.png
---

Large language model (LLM) post-training typically samples training examples uniformly or follows a predefined data schedule, despite the fact that the utility of different examples may change substantially as the model learns. Curriculum learning offers an alternative by controlling which data the learner encounters over time. Recent methods for LLM reasoning and post-training have explored adaptive data selection, including distribution-level curricula such as DUMP and competence-based prompt selection such as Prompt Curriculum Learning (PCL). However, these approaches primarily construct curricula through predefined scheduling or model-derived selection criteria rather than learning an explicit teacher policy that adapts the student's training distribution through interaction.

We investigate whether an LLM can instead learn more effectively when its curriculum is learned online through reinforcement learning. Our formulation builds on the classical Teacher-Student Curriculum Learning (TSCL) framework, in which a teacher learns to select tasks according to the student's learning progress, and extends this teacher-student paradigm to LLM post-training. The student is an autoregressive language model trained through supervised fine-tuning, while a lightweight neural teacher controls the distribution from which each student minibatch is sampled. Training examples are partitioned into difficulty buckets, and at each training step the teacher observes a compact representation of the student's evolving learning state, including per-bucket loss statistics and learning progress. The teacher outputs a probability distribution over buckets, defining the mixture used to construct the student's next training batch. Following the student update, the teacher receives a reward based on improvement on held-out validation data and learns its curriculum policy through policy-gradient optimization.

Our ongoing experiments use mathematical reasoning as a controlled setting with human-annotated difficulty levels. We compare the learned curriculum against uniform sampling and non-learned curriculum strategies under matched initialization, training budgets, and evaluation data. We will evaluate whether the learned teacher (1) improves held-out reasoning performance, (2) reaches a target performance with fewer training examples or less compute, and (3) learns interpretable scheduling behavior that evolves with student competence. We additionally examine whether human-defined difficulty corresponds to the student's empirical difficulty and whether model-based learning-progress signals provide a more informative basis for curriculum decisions.

To our knowledge, recent work has studied curriculum learning for LLM post-training and classical work has studied RL-trained teacher-student curricula, but these directions have largely remained separate. Our work connects them by learning a lightweight RL teacher that directly controls the student's batch distribution and is optimized from the student's validation improvement. Rather than filtering examples according to a fixed criterion or prescribing an easy-to-hard trajectory, our framework treats the curriculum itself as a policy to be learned from the evolving student.

Preliminary results of the project are to be presented at a Workshop at NeurIPS Atlanta 2026;[OpenReview](https://openreview.net/forum?id=ngn5HGKLbO&referrer=%5BAuthor%20Console%5D(%2Fgroup%3Fid%3DNeurIPS.cc%2F2026%2FWorkshop%2FWiML%2FAuthors%23your-submissions)). 

*This project is still under progress currently and this page will be updated with the results later.*

Supervisors: [Prof. Salem Lahlou](https://lahlou.org/) and [Prof. Martin Takáč](https://mtakac.com/News)

