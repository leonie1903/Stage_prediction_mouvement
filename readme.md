# Stage 2025
## Functional Activity Detection from Wrist Accelerometer Data (Post-Stroke Context)

This repository contains the code developed during my Master's thesis (M2 Sciences et Numérique pour la Santé, Université de Montpellier, 2025). The project aims to detect and classify functional upper-limb activities from wrist-worn accelerometer data, in the context of post-stroke rehabilitation monitoring.

## Objective

To design and evaluate a complete pipeline to:
- Segment accelerometric signals into relevant movement periods
- Extract meaningful time-series features (statistical, fractal, and shapelets)
- Classify functional activities such as eating, dressing, or personal care
- Adapt to real-world conditions and motor asymmetries found in post-stroke individuals

## Notebooks

Two main Jupyter Notebooks illustrate the core methodology:

###  `Inactivity_Activity_Marion.ipynb`
This notebook detects periods of inactivity and activity from raw accelerometer signals. It applies filtering, norm computation, and sliding-window detection to reduce data volume and focus on meaningful sequences.

###  `shapelets+descripteurs.ipynb`
This notebook classifies the segmented windows into functional activities using:
- A combination of statistical and fractal features (e.g., mean, std, DFA)
- Shapelet-based pattern learning (with `tslearn`)
- A supervised classification pipeline with confidence filtering and post-processing

Additional scripts and notebooks are included to test other approaches or visualize intermediate results.

### Methods Summary

### Segmentation
- Window-based detection of inactivity using acceleration norms
- Thresholds and smoothing based on literature and empirical tuning

### Feature Extraction
- **Statistical**: mean, std, skewness, kurtosis, energy
- **Fractal**: DFA (Detrended Fluctuation Analysis)
- **Shapelets**: learned discriminative patterns via `tslearn.shapelets`

### Classification
- Supervised models trained on labeled activity logs
- Confidence filtering and post-processing to smooth predictions

##  Data

Data used in this study are 3-axis wrist accelerometry signals (Axivity AX3, 50 Hz), annotated with manually written activity logs. Due to confidentiality, no raw data is shared in this repository.



