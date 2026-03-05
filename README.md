# Probability Density Function Learning using Statistical Modeling and GANs

## Overview
This repository contains two assignments focused on learning Probability Density Functions (PDFs) from transformed NO₂ concentration data using:

1. Statistical PDF estimation
2. Generative Adversarial Networks (GANs)

The assignments demonstrate both analytical and deep learning approaches for modeling probability distributions.

---

## Dataset
- India Air Quality Dataset
- Feature used: NO₂ concentration values

---

# Assignment 1 — Statistical PDF Learning

## Objective
To transform NO₂ concentration data using a roll-number-parameterized non-linear transformation and estimate the probability density function analytically.

---

## Transformation Function

The transformed variable is defined as:

z = x + ar * sin(br * x)

For Roll Number: `102303356`

- r mod 7 = 1
- r mod 5 = 1

Therefore:

- ar = 0.05
- br = 0.6

Final transformation:

z = x + 0.05 * sin(0.6x)

---

## Estimated PDF

The probability density function considered:

p(z) = c * e^(-λ(z-μ)^2)

Estimated Parameters:

| Parameter | Value |
|----------|-------|
| μ | 41.82 |
| λ | 0.0019 |
| c | 0.0245 |

---

## Methodology
- Applied non-linear transformation on NO₂ values
- Computed transformed mean and variance
- Estimated PDF parameters
- Compared histogram with fitted distribution

---

# Assignment 2 — GAN Based PDF Learning

## Objective
To learn the probability density function directly from transformed data samples using a Generative Adversarial Network (GAN).

---

## Transformation Function

For Roll Number: `102303356`

- ar = 0.5
- br = 0.6

Final transformation:

z = x + 0.5 * sin(0.6x)

---

## GAN Architecture

### Generator
- Input: Random noise N(0,1)
- Dense Layer: 64 neurons + ReLU
- Dense Layer: 128 neurons + ReLU
- Output Layer: 1 neuron

### Discriminator
- Dense Layer: 128 neurons + LeakyReLU
- Dense Layer: 64 neurons + LeakyReLU
- Output Layer: Sigmoid activation

---

## Training Details

| Parameter | Value |
|-----------|-------|
| Epochs | 3000 |
| Batch Size | 64 |
| Optimizer | Adam |
| Learning Rate | 0.0002 |

---

## GAN Workflow
- Train discriminator on real and generated samples
- Train generator to fool discriminator
- Generate synthetic transformed samples
- Apply Kernel Density Estimation (KDE)
- Compare generated distribution with real data

---

## Observations

### Statistical PDF Learning
- Bell-shaped distribution observed
- Estimated PDF closely matched transformed data

### GAN-Based Learning
- GAN captured major distribution peaks
- KDE closely matched real data distribution
- Minor deviations observed in tail regions

---

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- SciPy
- TensorFlow / Keras
- Scikit-learn

---

## Conclusion
This project demonstrates two different approaches for probability density function learning:

1. Analytical/statistical estimation
2. Deep learning based generative modeling using GANs

Both methods successfully modeled the transformed NO₂ concentration distribution and highlighted the effectiveness of statistical as well as data-driven PDF learning techniques.

---

## Author
**Niyati**  
Roll Number: 102303356
