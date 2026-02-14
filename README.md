# APS-DGM: Adaptive Prioritized Sampling in the Deep Galerkin Method

**Prioritized Sampling for Scalable Neural Network Solutions to Complex Partial Differential Equations**  
Idriss Barbara, Elmehdi Amhraoui, Tawfik Masrour, Mohammed Hadda

This repository provides the official Python implementation of the method proposed in the article:

"Prioritized Sampling for Scalable Neural Network Solutions to Complex Partial Differential Equations"

The project introduces a novel adaptive sampling strategy for training neural networks to solve partial differential equations (PDEs). The method dynamically reallocates computational effort toward regions of the spatiotemporal domain where the solution exhibits complex behavior, leading to improved accuracy and faster convergence without increasing computational cost.

The implementation is built upon the Deep Galerkin Method (DGM) framework and integrates a probabilistic importance sampling mechanism for collocation point selection.

**The code implements:**

- **APS-DGM** — Adaptive Prioritized Sampling integrated with the Deep Galerkin Method (DGM)  
- Baseline **DGM** implementation for comparison  
- Numerical experiments presented in the paper:
  - Poisson problem with a centered sharp peak
  - Problem with a less-regular solution
  - Time-dependent Heat equation 
  - Nonlinear Burgers’ equation 
  - High-dimensional elliptic example 

