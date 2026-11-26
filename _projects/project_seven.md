---
title: (@TUM) Detection of artefacts in EEG data
order: 15
image: projects/Bumblekite_Machine_Learning_Summer_School_2024_Zurich-119.jpg
---

Electroencephalography (EEG) data, acquired simultaneously with magnetic resonance imaging (MRI), must be corrected for artefacts related to MR gradient switches (GS) and the cardioballistic (CB) effect. Canonical approaches require additional signal acquisition for artefact detection (e.g., MR volume onsets, ECG), without which the EEG data would be rendered uncleanable from these artefacts.

We present two broadly applicable methods for artefact detection based on peak detection combined with temporal constraints with respect to periodicity directly from the EEG data itself; no additional signals are required.

We validated the performance of our methods versus the two canonical approaches for detection of GS/CB artefact, respectively, on 26 healthy human EEG-functional MRI resting-state datasets. Utilising various performance metrics, we found our methods to perform as well as – and sometimes better than - the canonical standard approaches. With as little as one EEG channel recording, our methods can be applied to detect GS/CB artefacts in EEG data acquired simultaneously with MRI in the absence of MR volume onsets and/or an ECG recording. The detected artefact onsets can then be fed into the standard artefact correction software.

[Paper](https://www.sciencedirect.com/science/article/pii/S2215016123003722)
[Code](https://github.com/rachelnutt3012/Artifind)
