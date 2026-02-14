******Prioritized Sampling for Scalable Neural Network Solutions to Complex Partial Differential Equations
Overview******

This repository provides the official Python implementation of the method proposed in the article:

"Prioritized Sampling for Scalable Neural Network Solutions to Complex Partial Differential Equations"

The project introduces a novel adaptive sampling strategy for training neural networks to solve partial differential equations (PDEs). The method dynamically reallocates computational effort toward regions of the spatiotemporal domain where the solution exhibits complex behavior, leading to improved accuracy and faster convergence without increasing computational cost.

The implementation is built upon the Deep Galerkin Method (DGM) framework and integrates a probabilistic importance sampling mechanism for collocation point selection.

**Motivation**

Solving PDEs using neural networks can be interpreted as a semi-supervised learning problem:

Exact solution values are known only at initial and boundary conditions.

Interior collocation points across the domain are unlabeled.

The distribution of collocation points strongly impacts training efficiency and accuracy.

Standard uniform sampling strategies often fail to adequately capture regions with sharp gradients, localized peaks, irregular structures, or high-dimensional complexity.

To address this limitation, this repository implements a prioritized adaptive sampling distribution that:

Dynamically identifies regions requiring higher information density.

Concentrates training samples in areas with larger residuals or complex dynamics.

Maintains computational cost comparable to standard DGM approaches.

**Key Contributions Implemented**

Adaptive probability distribution for collocation sampling

Integration with the Deep Galerkin Method (DGM)

Residual-based importance sampling

Efficient training without increasing the total number of collocation points

Validation on benchmark PDE problems including:

- Sharp localized peak solutions

- Irregular solution profiles

- Time-dependent PDEs

- Nonlinear Problem

- High-dimensional problems

**Methodology**

1. PDE Formulation

The PDE problem is formulated as a minimization of a loss function composed of:

Interior residual loss

Boundary condition loss

Initial condition loss (for time-dependent problems)

2. Prioritized Adaptive Sampling

Instead of sampling collocation points uniformly, the method:

Evaluates the PDE residual over candidate points.

Constructs a probability distribution based on residual magnitude.

Resamples collocation points according to this distribution.

Updates the distribution dynamically during training.

This adaptive mechanism allows the network to focus on difficult regions while preserving stability.

3. Integration with DGM

The prioritized sampling mechanism is fully integrated into the Deep Galerkin Method framework, ensuring:

Scalability to high-dimensional PDEs

Stable optimization

No additional computational overhead

**Keywords**

Partial Differential Equations (PDEs); Deep Learning; Adaptive Sampling; Importance Sampling; Deep Galerkin Method.
