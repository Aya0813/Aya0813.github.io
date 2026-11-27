---
title: (@NYU) Multimodal LLMs and healthcare
order: 15
image: projects/NYUAD_capstone.PNG
---

The critical shortage of medical professionals in low-resource countries, notably in Africa, hinders adequate health-care delivery. AI, particularly Multimodal Large Language models (MLLMs), can enhance the efficiency of healthcare systems by assisting in medical image analysis and diagnosis. However, the deployment of state-of-the-art MLLMs is limited in these regions due to the high computational demands that exceed the capabilities of consumer-grade GPUs.

This paper presents a framework for optimizing MLLMs for resource-constrained environments. We introduce optimized medical MLLMs including TinyLLaVA-Med-F, a medical fine-tuned MLLM, and quantized variants (TinyLLa VA - Med- FQ4, Tiny LLa VA - Med- FQ8, LLa VA - Med-Q4, and LLaVA-Med-Q8) that demonstrate substantial reductions in memory usage without significant loss in accuracy.

Specifically, TinyLLaVA-Med-FQ4 achieves the greatest reductions, lowering dynamic memory by approximately 89% and static memory by 90% compared to LLaVA-Med. Similarly, LLaVA-Med-Q4 reduces dynamic memory by 65% and static memory by 67% compared to state-of-the-art LLaVA-Med. These memory reductions make these models feasible for deployment on consumer-grade GPUs such as RTX 3050.

This research underscores the potential for deploying optimized MLLMs in low-resource settings, providing a foundation for future developments in accessible AI-driven healthcare solutions.

[Github Repository](https://github.com/AyaLukeloCapstone/TinyLLaVA-Med-F)
[Paper](https://ieeexplore.ieee.org/abstract/document/10913565): Published in main conference proceedings of the IEEE EMBS BHI (Biomedical and Health Informatics) peer-reviewed international conference (less than 30% acceptance rate).
