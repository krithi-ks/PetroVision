# LADOS Dataset — PetroVision

This directory contains the local copy of the LADOS semantic-segmentation dataset used for PetroVision computer-vision experiments.

## Dataset

**LADOS: Aerial Imagery Dataset for Oil Spill Detection, Classification, and Localization Using Semantic Segmentation**

* Images: 3,388
* Task: Semantic segmentation
* Image modality: RGB aerial imagery
* Annotation type: Pixel-level semantic masks
* License: CC BY 4.0
* Dataset version used by PetroVision: Roboflow Version 1

## Local Split

| Split      |    Images |     Masks |
| ---------- | --------: | --------: |
| Train      |     2,370 |     2,370 |
| Validation |       675 |       675 |
| Test       |       343 |       343 |
| **Total**  | **3,388** | **3,388** |

The local dataset was exported as **Semantic Segmentation Masks** from the PetroVision Roboflow dataset version.

No Roboflow preprocessing or augmentation was applied during dataset-version creation.

## Important

The image and mask files are intentionally excluded from the Git repository because the dataset is large.

Only this README is tracked in Git.

The dataset should be obtained from the documented LADOS source and the PetroVision Roboflow dataset version used for the experiments.

## Research Integrity

The dataset split and annotation encoding will be inspected and verified locally before model training.

No model performance results should be reported until the dataset has been validated and experiments have been completed.
