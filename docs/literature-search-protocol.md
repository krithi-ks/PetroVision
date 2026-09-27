# PetroVision — Literature Search Protocol

## 1. Purpose

This protocol defines the systematic approach used to identify, screen,
and analyze research related to petroleum contamination detection and
classification in aquatic environments.

The objective is to build a reproducible literature base for:

* The PetroVision project
* The project report
* The systematic literature review
* Identification of research gaps
* Selection of relevant datasets
* Selection of suitable machine-learning and computer-vision methods

---

# 2. Research Scope

The literature search covers four major research streams:

### A. Sensor-Based Detection

Research using physical, chemical, or water-quality sensors together with
machine learning for petroleum/oil contamination detection or
classification.

### B. Computer Vision

Research using RGB images, photographs, aerial imagery, or video for
petroleum/oil detection, classification, localization, or segmentation.

### C. Remote Sensing

Research using:

* SAR
* Optical satellite imagery
* Multispectral imagery
* Hyperspectral imagery
* Thermal imagery

for petroleum/oil-spill monitoring.

### D. Multimodal and Data Fusion

Research combining multiple sensing modalities, such as:

* Sensor + image
* SAR + optical
* Multiple sensor types
* Remote sensing + machine learning
* Multi-sensor data fusion

---

# 3. Research Questions for the Literature Review

### LRQ1

What sensing modalities are currently used for petroleum/oil
contamination detection in aquatic environments?

### LRQ2

What machine-learning algorithms are used for sensor-based petroleum
contamination detection and classification?

### LRQ3

How are CNNs and other deep-learning architectures used for visual
petroleum/oil detection and segmentation?

### LRQ4

What publicly available datasets can support petroleum/oil detection,
classification, and segmentation research?

### LRQ5

What are the major limitations of existing datasets and methods?

### LRQ6

How are SAR, optical imagery, and other remote-sensing modalities used
for large-scale oil-spill monitoring?

### LRQ7

What opportunities exist for combining sensor-based machine learning
with computer vision?

### LRQ8

What computational and deployment considerations are relevant for
real-time or low-cost petroleum contamination monitoring?

---

# 4. Search Databases

The following sources will be considered for literature discovery:

* IEEE Xplore
* ScienceDirect
* SpringerLink
* MDPI
* PubMed
* ACM Digital Library
* Google Scholar
* Semantic Scholar

Search results will be verified against the original publication or
publisher page whenever possible.

---

# 5. Search Keywords

## Core Terms

* "oil spill detection"
* "petroleum contamination detection"
* "oil contamination water"
* "petroleum pollution detection"
* "oil spill classification"

## Machine Learning Terms

* "oil spill" AND "machine learning"
* "petroleum contamination" AND "machine learning"
* "oil spill" AND "sensor" AND "classification"
* "oil contamination" AND "sensor" AND "machine learning"
* "oil spill" AND "TinyML"

## Computer Vision Terms

* "oil spill" AND "computer vision"
* "oil spill" AND "CNN"
* "oil spill" AND "deep learning"
* "oil spill" AND "image segmentation"
* "oil spill" AND "semantic segmentation"
* "oil spill" AND "U-Net"
* "oil spill" AND "RGB image"

## Remote Sensing Terms

* "oil spill" AND "SAR"
* "oil spill" AND "Sentinel-1"
* "oil spill" AND "optical remote sensing"
* "oil spill" AND "hyperspectral"
* "oil spill" AND "multispectral"

## Fusion Terms

* "oil spill" AND "data fusion"
* "oil spill" AND "multimodal"
* "oil spill" AND "sensor fusion"
* "oil spill" AND "SAR" AND "optical"
* "oil spill" AND "sensor" AND "image"

---

# 6. Time Range

The primary review will emphasize research published from:

**2016–2026**

Earlier highly influential papers may be included when they provide
important foundational methods, datasets, or concepts.

Recent work from 2024–2026 will receive particular attention when
positioning the current state of the field.

---

# 7. Inclusion Criteria

A paper may be included when it satisfies one or more of the following:

1. Addresses petroleum/oil contamination or oil-spill detection in an
   aquatic environment.

2. Uses machine learning or deep learning for detection,
   classification, localization, or segmentation.

3. Uses sensor measurements relevant to petroleum contamination.

4. Uses RGB, aerial, satellite, SAR, optical, hyperspectral, or thermal
   imagery for oil-spill monitoring.

5. Introduces or evaluates a relevant public dataset.

6. Provides a relevant methodology, benchmark, or evaluation protocol.

7. Provides useful information for understanding limitations or research
   gaps in the field.

---

# 8. Exclusion Criteria

A paper will normally be excluded when:

1. It is unrelated to petroleum/oil contamination.

2. It focuses exclusively on unrelated water-quality problems without a
   petroleum/oil component.

3. It contains no meaningful relevance to detection, classification,
   segmentation, monitoring, sensing, or related analysis.

4. It is only a duplicate publication of an already included study.

5. Only an abstract is available and sufficient technical information
   cannot be obtained.

6. The paper is primarily commercial material, a product page, or
   non-peer-reviewed promotional content.

7. Its reported task is substantially different from the research
   questions of PetroVision.

---

# 9. Screening Procedure

The literature-selection process will follow these stages:

### Stage 1 — Identification

Collect candidate papers using the defined search keywords.

### Stage 2 — Duplicate Removal

Remove duplicate records referring to the same publication.

### Stage 3 — Title Screening

Remove papers whose titles clearly fall outside the research scope.

### Stage 4 — Abstract Screening

Evaluate the abstract against the inclusion and exclusion criteria.

### Stage 5 — Full-Text Screening

Read the complete paper when necessary to determine whether it provides
sufficient relevance.

### Stage 6 — Final Inclusion

Add relevant papers to the final literature-review database.

---

# 10. Paper Extraction Fields

For every included paper, record:

| Field                 | Description                               |
| --------------------- | ----------------------------------------- |
| Paper ID              | Unique identifier                         |
| Title                 | Full paper title                          |
| Authors               | Authors                                   |
| Year                  | Publication year                          |
| Venue                 | Journal/conference                        |
| DOI                   | Persistent identifier                     |
| Research Area         | Sensor/CV/Remote Sensing/Fusion           |
| Modality              | Sensor/RGB/SAR/etc.                       |
| Dataset               | Dataset used                              |
| Dataset Size          | Number of samples/images                  |
| Labels                | Target classes/annotations                |
| Method                | ML/DL architecture                        |
| Task                  | Classification/segmentation/etc.          |
| Evaluation Metrics    | Accuracy/F1/IoU/etc.                      |
| Main Findings         | Source-reported findings                  |
| Limitations           | Reported or clearly evidenced limitations |
| PetroVision Relevance | Why the paper matters                     |
| Included?             | Yes/No                                    |
| Reason                | Inclusion/exclusion reason                |

---

# 11. Evidence Classification

Information extracted from literature will be classified as:

### SOURCE RESULT

A result explicitly reported by the original paper.

### SOURCE CLAIM

An interpretation or claim made by the paper's authors.

### OUR ANALYSIS

An interpretation made during the PetroVision literature analysis and
supported by multiple sources where possible.

### PETROVISION RESULT

A result generated by experiments conducted as part of PetroVision.

These categories must not be mixed.

---

# 12. Dataset Evaluation Criteria

A dataset will be considered for PetroVision only after checking:

* Relevance to petroleum/oil contamination
* Image/sensor modality
* Annotation quality
* Number of samples
* Class distribution
* Public accessibility
* License
* Train/validation/test organization
* Geographic/environmental diversity
* Potential data leakage
* Compatibility with the intended task

A larger dataset will not automatically be considered better.

---

# 13. Literature Matrix

The final literature matrix will contain at least:

| ID  | Year | Modality | Dataset | Method | Task | Metric | Limitation | PetroVision Relevance |
| --- | ---: | -------- | ------- | ------ | ---- | ------ | ---------- | --------------------- |
| P01 |      |          |         |        |      |        |            |                       |
| P02 |      |          |         |        |      |        |            |                       |
| P03 |      |          |         |        |      |        |            |                       |

The matrix will be expanded as additional papers are screened.

---

# 14. Search Transparency

For important searches, the following information will be recorded:

* Database/source
* Search query
* Search date
* Number of candidate results when available
* Number screened
* Number included
* Main exclusion reasons

This allows the literature-review process to be reproduced and audited.

---

