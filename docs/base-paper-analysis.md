# 2026 IEEE Base Paper Analysis

## Paper

**Title:** Intelligent WSN Sensor Node for Oil Spill Detection and Classification: A TinyML and IoT Approach

**Authors:** Yan Ferreira da Silva, Raimundo Carlos Silvério Freire, João Viana da Fonseca Neto

**Publication:** IEEE Access, 2026

**Publication Date:** June 12, 2026

**Volume:** 14

**Pages:** 92436–92455

**DOI:** 10.1109/ACCESS.2026.3703356

---

# 1. Research Problem

The paper investigates the detection and classification of petroleum
products in aquatic environments using a wireless sensor network,
machine learning, and TinyML/IoT deployment.

The work focuses on developing a sensor node capable of detecting and
classifying fuel contamination while considering computational and energy
constraints of an embedded platform.

---

# 2. Main Objective of the Paper

The paper proposes an intelligent WSN sensor node for oil spill detection
and classification using machine-learning algorithms and TinyML-oriented
embedded deployment.

The study evaluates multiple machine-learning approaches and investigates
their suitability for implementation on an ESP32-based sensor node.

---

# 3. Dataset

The paper reports:

- 1,984 instances
- 4 variables
- 7,936 sensor readings in total
- Independent test set containing 80 samples
- 5-fold cross-validation

The four variables used in the multicriteria machine-learning experiment
are:

1. pH
2. Liquid temperature
3. Ambient temperature
4. Turbidity

The paper discusses conductivity as part of its overall sensing architecture,
but the multicriteria experiment described in the paper uses the four
variables listed above.

---

# 4. Data Processing

The paper discusses normalization of input variables.

The multicriteria experimental section reports z-score standardization.

This should be treated carefully when attempting an independent
implementation because other parts of the paper describe min-max
normalization.

PetroVision will not assume that these two descriptions are identical.
The preprocessing protocol will be documented explicitly in any
independent experiment.

---

# 5. Machine-Learning Models

The paper evaluates:

- Multilayer Perceptron (MLP)
- Radial Basis Function (RBF)
- Support Vector Machine with RBF kernel (SVM-RBF)
- Nonlinear Regression (NLR)

---

# 6. MLP Architecture

The reported MLP architecture is:

```text
4 input neurons
      ↓
3 hidden neurons
      ↓
1 output neuron

The paper reports:

Sigmoid activation
Learning rate: 0.0001
Gaussian-initialized weights
Mean = 0
Variance = 1
Classification threshold = 0.5

An output greater than 0.5 is classified as class 1; otherwise it is
classified as class 0.

7. MLP Equations

The forward propagation can be represented as:

z_hidden = X · W_input_hidden + b_hidden

a_hidden = σ(z_hidden)

where:

σ(z) = 1 / (1 + e^(-z))

The output layer is:

z_output = a_hidden · W_hidden_output + b_output

a_output = σ(z_output)

The paper also describes error calculation and backpropagation updates.

For an independent implementation, the mathematical implementation will
be checked against the standard backpropagation equations rather than
blindly copying potentially inconsistent notation in the source.

8. RBF Model

The reported RBF model uses:

4 input variables
20 Gaussian radial centers
1 output

The paper discusses the computational characteristics of the RBF model
and its behavior under different training-set sizes.

9. SVM-RBF

The paper uses an SVM with an RBF kernel.

The reported trained model contains 22 support vectors.

10. Nonlinear Regression

The paper evaluates nonlinear regression using the four input variables
and a scalar output.

The model is fitted using a nonlinear parametric formulation and
least-squares-based fitting.

11. Reported Results

The paper reports an overall MLP accuracy of approximately 85%.

The reported confusion matrix contains:

620 true fuel-contaminated classifications
400 true clean classifications
100 false positives
80 false negatives

Reported metrics include:

Sensitivity: 86.11%
Specificity: 83.33%
Precision: 88.57%
F1-score: 87.32%

The reported five-fold cross-validation average accuracy for MLP is:

84.38% ± 1.91%

The individual fold results reported are:

87.37%
84.38%
83.63%
84.38%
82.12%

These values are results reported by the source paper and are not
PetroVision results.

12. Training-Size Experiment

The paper investigates how model performance changes with training-set
size.

The reported experiments show that model behavior is not necessarily
monotonic with increasing training data.

In particular, the paper reports instability in RBF performance at some
training-set sizes, while MLP, SVM, and NLR show comparatively more
stable behavior.

PetroVision will independently evaluate training-size sensitivity rather
than assuming the same behavior will occur on another dataset.

13. Noise-Robustness Experiment

The paper investigates model behavior under Gaussian noise.

The experiment evaluates the robustness of the machine-learning models
when noise is introduced into the input data.

The paper reports comparatively stable behavior for the evaluated models,
with MLP showing notable stability in the reported experiments.

PetroVision may use a similar robustness experiment where appropriate,
but the resulting values will be treated as PetroVision experimental
results only after actually running the experiment.

14. Embedded Deployment

The paper investigates implementation on an ESP32-based embedded platform.

It considers:

Inference latency
Memory consumption
Energy consumption
Throughput
TinyML deployment
Quantization/deployment considerations

The paper reports approximately 44.7% power-consumption reduction using
Deep Sleep in its monitoring setup.

These are source-paper results and are not measurements from PetroVision.

15. Why the Paper Is Relevant to PetroVision

The paper provides the foundation for the sensor-data machine-learning
component of PetroVision.

PetroVision takes inspiration from:

Petroleum contamination detection
Sensor-based classification
Machine-learning model comparison
Robustness evaluation
Embedded/edge-oriented considerations
16. What PetroVision Adds

PetroVision extends the research direction by investigating computer
vision as an additional source of information.

The planned computer-vision component includes:

RGB image analysis
CNN-based analysis
Image segmentation
Visible contamination localization
Image-based coverage estimation
Webcam-based demonstration

The computer-vision component is not claimed to chemically identify
petroleum products from RGB images.

17. Important Differences
Base Paper	PetroVision
Sensor-based detection	Sensor-data ML + computer vision
WSN / IoT	Software-first research in 7th semester
ESP32 deployment	Future 8th-semester extension
Sensor measurements	Sensor data + RGB images
Embedded TinyML	CNN/segmentation research
Physical sensing	Webcam/image demonstration
Hardware-focused deployment	Research + interactive software platform
18. Reproduction Policy

PetroVision will not claim to reproduce the original paper unless the
original experimental data and complete experimental conditions are
available.

The original dataset will not be fabricated.

If a compatible public dataset is identified, it will be documented as
an independent dataset.

If synthetic data is used for development, it will be explicitly labelled
as synthetic and will not be presented as real-world experimental
evidence.

19. Methodological Issues to Track

The following points require attention during independent implementation:

Availability of the original dataset
Exact preprocessing procedure
Dataset-label definitions
Train/test separation
Reproducibility of reported results
Mathematical details of model implementation
Differences between source-paper methodology and PetroVision's
experimental setup

These issues will be documented rather than silently resolved.

20. PetroVision Experimental Plan Inspired by the Paper

Where a legitimate compatible dataset is available, PetroVision may
investigate:

MLP
RBF
SVM-RBF
NLR
Additional appropriate baseline models

Evaluation may include:

Accuracy
Precision
Recall
F1-score
Balanced accuracy
Confusion matrix
Cross-validation
Training-size sensitivity
Noise robustness
Inference time
Model size

The exact experiments will be finalized after the dataset investigation.

21. Source vs PetroVision Results
Source Paper

All numerical results in this document under "Reported Results",
"Embedded Deployment", and other explicitly source-labelled sections
belong to the 2026 IEEE paper.

PetroVision

PetroVision results will only be added after the corresponding experiment
has actually been conducted.

No source-paper accuracy will be copied into PetroVision's results as if
it were independently obtained.

Source

da Silva, Y. F., Freire, R. C. S., & da Fonseca Neto, J. V.

"Intelligent WSN Sensor Node for Oil Spill Detection and Classification:
A TinyML and IoT Approach."

IEEE Access, 2026.

DOI: 10.1109/ACCESS.2026.3703356


### One important point

We're **not yet deciding which algorithms or datasets PetroVision will finally use**.

This document records the base paper first. Later, after we investigate legitimate datasets, we'll make our own experimental decisions and document them.