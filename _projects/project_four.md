---
title: (@NYU) Climate AI
order: 15
image: projects/salta.png
---

Coastal flood risk is growing due to climate change, particularly from rising sea levels and the construction of engineered shoreline protections such as seawalls. These interventions can significantly reshape flood dynamics and lead to highly complex interactions across the coastal landscape.

Traditionally, researchers have relied on physics-based hydrodynamic simulators to understand and forecast coastal flooding. These simulators account for tidal forcing, wind effects, seabed friction, and other environmental factors, generating fine-resolution flood maps through numerical modeling. However, they are extremely computationally expensive. For example, simulating just one protection scenario for the Abu Dhabi coastline can take several days to weeks on high-performance computing clusters, and exploring the full design space of shoreline configurations may require months (Karapetyan et al., 2024).

To overcome these limitations, data-driven methods have emerged as a promising alternative. These models, including deep learning-based approaches, aim to approximate the outputs of hydrodynamic simulators while dramatically reducing computational costs, notably reducing the computational cost of producing a flood inundation map from days to milliseconds. Within this context, the CASPIAN model was introduced as a vision-based convolutional neural network designed specifically for coastal flood prediction. CASPIAN v1 focused on a single region (Abu Dhabi) under a fixed sea level rise condition. CASPIAN v2 extended this to a multi-region setting, including San Francisco and multiple SLR levels. Both models demonstrated strong performance compared to traditional methods, achieving high accuracy across various metrics.

However, a key limitation remains: when deployed in new regions with only a handful of labeled scenarios, fully trained CASPIAN models tend to underperform. This leads to the next challenge: how can we make CASPIAN adapt effectively to unfamiliar flood scenarios or geographic locations using only a few examples?

Various strategies could be considered to address the challenge of adapting to new flood-prone regions with limited labeled data. These include regression-based adaptation techniques that leverage small sample sets, as well as more structured approaches like transfer learning, few-shot domain adaptation via causal mechanism transfer, and domain-adaptive few-shot learning. Each of these methods offers different trade-offs in terms of generalizability and complexity.
Meta-learning offers a complementary direction by framing the problem as “learning how to learn”. Rather than fine-tuning a pre-trained model on each new region, meta-learning trains a model to rapidly adapt to new tasks by optimizing for quick adaptability during training. In our case, we adopt Model-Agnostic Meta-Learning (MAML), a gradient-based meta-learning algorithm that is both flexible and compatible with our convolutional model architecture. MAML enables the CASPIAN model to generalize across regions and flood scenarios by training it to adapt rapidly to new tasks using only a few labeled examples, without requiring extensive retraining.

One of the primary challenges in building a flexible flood prediction model lies in the high-dimensional nature of the outputs. Each flood scenario requires predicting a full-resolution flood map, represented as a 1024 by 1024 grid. This translates to over a million output values per scenario. To make this more manageable, the original CASPIAN pipeline applies a region-specific mask that focuses only on relevant coastal cells, reducing the number of outputs to tens of thousands per scenario. Despite this reduction, the problem remains highly complex, especially when dealing with limited training data from each region.

The objective of this project is to find a solution that allows the model to adapt to new regions and scenarios with minimal data, building on the foundation of the CASPIAN model. Initially, I started with an existing MAML implementation provided by Bilal Hassan, a postdoctoral researcher and member of the lab. My goal was to experiment with different variations, hyperparameters, and configurations of MAML to determine the most effective approach for achieving rapid adaptation and high accuracy in new, low-data regions.

[Project Final Report](https://docs.google.com/document/d/1pjJMlg3qMVF_2nQw1nVOe4nnAHHw5YRxRzee-22UBzQ/edit?usp=sharing)
[Github Repository](https://github.com/Aya0813/CASPIAN-MAML)


Supervisor: [Prof. Samer Madanat](https://nyuad.nyu.edu/en/academics/divisions/engineering/faculty/samer-madanat.html)
