# Implicit Neural Representations with Periodic Activation Functions (SIREN)

This repository provides an implementation and explanation of **SIREN** (Sinusoidal Representation Networks) — a powerful neural architecture for learning **Implicit Neural Representations (INRs)** of signals such as images, videos, and 3D shapes.  

SIREN replaces traditional activation functions (like ReLU or Tanh) with **sinusoidal activations**, enabling smooth and high-frequency signal modeling with remarkable precision.

---

##  Overview

**Implicit Neural Representations (INRs)** represent data (e.g., images, shapes, sound, scenes) as **continuous functions** parameterized by neural networks.  
Instead of storing pixels or voxels directly, the network learns a function:
\[
f_\theta : \mathbb{R}^n \to \mathbb{R}^m
\]
that maps input coordinates (e.g., spatial positions) to output signals (e.g., RGB values).

**SIREN** introduces periodic activations that make it possible to model complex, high-frequency details while keeping gradients stable during training.

---

##  Paper Reference

**Title:** Implicit Neural Representations with Periodic Activation Functions  
**Authors:** Vincent Sitzmann, Julien N. P. Martel, Alexander W. Bergman, David B. Lindell, Gordon Wetzstein  
**Conference:** NeurIPS 2020  
**Paper Link:** [arXiv:2006.09661](https://arxiv.org/abs/2006.09661)

---

##  Key Idea

Traditional activations (ReLU, Sigmoid, Tanh) are not ideal for representing signals with **fine details or oscillations**.  
SIREN solves this by using a **sinusoidal activation**:

\[
\sigma(x) = \sin(\omega_0 x)
\]

- The frequency parameter **ω₀** controls the periodicity.  
- Proper initialization ensures stable signal propagation and gradient flow.  
- The network learns rich, continuous, and differentiable signal representations.

---
