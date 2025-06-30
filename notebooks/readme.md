# Inactivity and Activity Detection from Accelerometer Data

This repository contains a collection of Python notebooks designed to process and analyze raw wrist-worn accelerometer data for functional activity detection in the context of stroke rehabilitation.

## Overview

The pipeline was inspired by **GGIR**, a widely used R package for processing raw accelerometer data. The implementation here provides:
- Autocalibration routines
- Detection of inactivity/active periods
- Time series segmentation
- Feature extraction (statistical + shapelets)
- Visualization of activity patterns
- Supervised classification of functional activities (e.g., eating, dressing, personal care)

## Notebooks

| Notebook                           | Description |
|------------------------------------|-------------|
| `InactivityDetector.ipynb`         | Core detection of inactivity based on signal thresholds and smoothing (inspired by GGIR). |
| `Inactivity_Activity.ipynb`        | Inactivity detection pipeline applied to **a patient**(inspired by GGIR). |
| `Inactivity_Activity_Healthy.ipynb`| Same pipeline applied to a **healthy subject** (contrôle)(inspired by GGIR). |
|`Segmentation_Methods.ipynb`        | Comparative tests of **different time-series segmentation methods**. |
| `calibration.ipynb`                | Initial calibration script. |
| `synchronisation.ipynb`            | Synchronization of sensors. |
| `shapelets.ipynb`                  | Initial shapelet-based classification pipeline. |
| `shapelets+descripteurs.ipynb`     | Advanced model combining shapelets and statistical descriptors for multi-activity classification. |

## Data Disclaimer

The raw accelerometer files used in this project are **not publicly shared** due to:
- **File size limitations**
- **Ethical concerns regarding participant data privacy**

## References & Inspiration

This project is heavily inspired by GGIR, an R package developed for physical activity and sleep research. The methodologies implemented here are derived from scientific studies on accelerometer signal processing, particularly:

- Van Hees, V. T., Sabia, S., Anderson, K. N., Denton, S. J., Oliver, J., Catt, M., Abell, J. G., Kivimäki, M., Trenell, M. I., & Singh-Manoux, A. (2015). A Novel, Open Access Method to Assess Sleep Duration Using a Wrist-Worn Accelerometer. PloS one, 10(11), e0142533. https://doi.org/10.1371/journal.pone.0142533

- Van Hees, V. T., Fang, Z., Langford, J., Assah, F., Mohammad, A., da Silva, I. C., Trenell, M. I., White, T., Wareham, N. J., & Brage, S. (2014). Autocalibration of accelerometer data for free-living physical activity assessment using local gravity and temperature: an evaluation on four continents. Journal of applied physiology (Bethesda, Md. : 1985), 117(7), 738–744. https://doi.org/10.1152/japplphysiol.00421.2014

- Migueles, J. H., Rowlands, A. V., Huber, F., Sabia, S., & van Hees, V. T. (2019). GGIR: A Research Community–Driven Open Source R Package for Generating Physical Activity and Sleep Outcomes From Multi-Day Raw Accelerometer Data. Journal for the Measurement of Physical Behaviour, 2(3), 188-196. Retrieved Feb 11, 2025, from https://doi.org/10.1123/jmpb.2018-0063

Official GGIR repository: [https://github.com/wadpac/GGIR](https://github.com/wadpac/GGIR)

---

## Contact

Léonie Olivier  
leonie.olivier.01@etu.umontpellier.fr  
University of Montpellier – EuroMov Digital Health in Motion
