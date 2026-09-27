# PetroVision — Literature Review

## 1. Purpose

This document records and organizes research relevant to petroleum
contamination detection and classification in aquatic environments.

The literature review will be used to:

- Understand existing approaches
- Identify commonly used datasets
- Identify machine-learning and deep-learning methods
- Understand sensing modalities
- Identify research gaps
- Position PetroVision relative to existing work
- Support the survey/review paper
- Support the final project report

---

# 2. Literature Categories

The reviewed literature will be organized into the following categories.

## Category A — Sensor-Based Detection

Research using physical or chemical sensors for petroleum/oil
contamination detection.

Examples of relevant topics:

- Water-quality sensors
- Petroleum-sensitive sensors
- Sensor arrays
- Wireless sensor networks
- Machine-learning classification
- TinyML
- Edge/embedded detection

---

## Category B — Computer Vision

Research using RGB images, photographs, video, or cameras for visible
oil/petroleum contamination detection.

Relevant topics include:

- Image classification
- Object detection
- Semantic segmentation
- Instance segmentation
- CNNs
- Lightweight deep-learning models
- Real-time image analysis

---

## Category C — Remote Sensing

Research using remotely sensed imagery for oil-spill detection.

Relevant modalities include:

- SAR
- Optical satellite imagery
- Multispectral imagery
- Hyperspectral imagery
- Thermal imagery
- Multimodal remote sensing

This category provides broader research context for petroleum
contamination monitoring.

---

## Category D — Multimodal / Data Fusion

Research combining multiple sources of information.

Potential combinations include:

- Sensor + image
- Optical + SAR
- Multiple sensor types
- Sensor + remote sensing
- Machine-learning-based data fusion

This category is particularly relevant to the possible future extension
of PetroVision.

---

# 3. Paper Analysis Table

Each important paper will be recorded using the following information:

| Paper | Year | Modality | Dataset | Method | Task | Main Result | Limitation | Relevance to PetroVision |
|---|---:|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |  |

---

# 4. Dataset Tracking

For every dataset identified in the literature, record:

| Dataset | Modality | Images/Samples | Labels | Public? | License | Task | Source | Potential Use |
|---|---|---:|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |  |

A dataset will not be used merely because it is related to water quality.
It must be relevant to the specific research task and have appropriate
labels or measurements.

---

# 5. Method Tracking

Important methods identified across the literature will be grouped into:

### Classical Machine Learning

- MLP
- SVM
- RBF
- NLR
- Decision Tree
- Random Forest
- KNN
- Other relevant methods

### Deep Learning

- CNN
- U-Net
- Lightweight segmentation models
- Other relevant architectures

### Remote Sensing

- SAR-based methods
- Optical-image methods
- Hyperspectral methods
- Multimodal approaches

---

# 6. Research Gaps

Potential research gaps will be added only after reviewing the literature.

Each proposed gap must be supported by multiple relevant sources where
possible.

No research gap will be claimed solely because a particular method was
not found in a small number of papers.

---

# 7. PetroVision Positioning

After completing the literature review, this section will explain how
PetroVision relates to existing work.

The positioning will distinguish between:

- Existing approaches
- The 2026 IEEE base paper
- PetroVision's sensor-ML component
- PetroVision's computer-vision component
- Potential future multimodal integration
- Future hardware/edge deployment

---

# 8. Review Status

Papers reviewed:

**0**

Datasets identified:

**0**

Important research gaps confirmed:

**Not yet determined**

This section will be updated as the literature review progresses.

1. 2026 IEEE base paper
Intelligent WSN Sensor Node for Oil Spill Detection and Classification: A TinyML and IoT Approach
This is your direct foundation: sensor measurements → ML classification → embedded deployment.

2. LADOS — 2025
Aerial Imagery Dataset for Oil Spill Detection, Classification, and Localization Using Semantic Segmentation

This is especially important for PetroVision because it provides 3,388 RGB images with pixel-level annotations across Oil, Emulsion, Sheen, Ship, Oil-platform and Background.

It is also publicly available, with train/validation/test sets of 2,370 / 675 / 343 images.

3. RGB/U-Net segmentation — 2026
Pixel-level detection and classification of marine oil spills in aerial imagery with annotation uncertainty handling

This is highly relevant because it specifically studies RGB imagery + pixel-level segmentation + U-Net, rather than only satellite/SAR imagery.

4. Drone RGB dataset — 2024
A dataset of drone-captured, segmented images for oil spill detection in port environments

It contains 1,268 images categorized as oil, water and other, and uses U-Net for segmentation.

5. CNN oil-spill classification/segmentation — 2021
This work used VGG16 for classification and Mask R-CNN/PSPNet for segmentation, demonstrating that different computer-vision tasks can address different aspects of oil-spill monitoring.

6. Remote-sensing/AI review — 2025
A recent review specifically examines AI + remote sensing for oil-spill detection, classification and thickness estimation and discusses public datasets and multimodal data fusion.

7. Remote-sensing systematic review — 2026
A large systematic review analyzed 2,856 documents from 2000–2026, providing useful background for your survey paper on SAR, optical sensing, AI and multimodal approaches.