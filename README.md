# Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox

[🇨🇳 简体中文](readme_cn.md) | [🇬🇧 English](README.md)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18957726.svg)](https://doi.org/10.5281/zenodo.19677694)

## 1. Introduction
This repository contains all the numerical simulation code and plotting scripts for the paper **"Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the $3x+1$ Problem"**.

We propose a coarse-grained transient dynamics framework that translates the discrete $3x+1$ (Collatz conjecture) arithmetic rules into a continuous Logistic dynamical sandbox locked in the period-3 window ($\mu \approx 1.7549$). The code reproduces the construction of the customized threshold partition, the eigenspectrum of the Perron-Frobenius transfer operator, null-model control experiments, run-length distribution comparisons, and the stopping-time decay alignment experiment.

## 2. Main Results
Through large-sample numerical simulations, operator spectral analysis, and rigorous null-model controls, we demonstrate that the Logistic sandbox captures aspects of the **global** stopping-time distribution that a generic forbidden-11 Markov chain does not, while honestly showing that **local** run-length statistics are better reproduced by the simpler null model. The sandbox is thus a partial surrogate with explicitly characterized success and failure modes.

### Operator Eigenspectrum and Invariant Density
![Figure 6: Operator Eigenspectrum and Invariant Density](fig6.png)
*(Corresponding to Figure 6 in the paper)*

### Time Renormalization and Large-Sample Decay Alignment
![Figure 7: Time Renormalization and Large-Sample Decay Alignment](fig7.png)
*(Corresponding to Figure 7 in the paper)*

## 3. Code Description
The core code is provided as Jupyter Notebooks (`.ipynb`), relying on standard libraries (`numpy`, `matplotlib`, `scipy`, `numba`). Click the **"Open in Colab"** badges to run in your browser.

### Original Figures (1-7)

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure1-Customized%20Markov%20Partition%20.ipynb) **Figure 1 - Customized Markov Partition**: Builds the customized threshold partition and topological sandbox based on the unstable fixed point $x^*$.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure2-Establishment%20of%20the%20Topological%20Skeleton.ipynb) **Figure 2 - Topological Skeleton**: Plots the topological skeleton and interval mapping relationships.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure3-Microscopic%20Grammar%20Emergence.ipynb) **Figure 3 - Grammar Emergence**: Verifies the "forbidden word 11" in the transition matrix and Shannon entropy collapse.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure4-stopping%20time%20distribution%20histogram.ipynb) **Figure 4 - Stopping Time Distribution**: Compares continuous transient behavior with real large integer stopping times.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure5-Invariant%20Measure.ipynb) **Figure 5 - Invariant Measure**: Calculates the invariant density and the 2:1 measure ratio.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure6-Operator%20Eigenspectrum%20and%20Invariant%20Density.ipynb) **Figure 6 - Operator Eigenspectrum**: Constructs the empirical transfer matrix and extracts its eigenspectrum.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure7-Time%20Renormalization%20and%20Large-Sample%20Decay%20Alignment..ipynb) **Figure 7 - Decay Alignment**: Verifies the decay rate alignment with $10^6$ large integers in $[10^{11}, 10^{13}]$.

### New Figures (8-11): Robustness, Controls, and Run-Length Analysis

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure8-Transfer%20Operator%20Convergence%20Study.ipynb) **Figure 8 - Convergence Study**: Varies grid size $N$ and kernel width $\sigma/h$, compares Gaussian kernel vs Ulam discretization, validates against direct trajectory survival.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure8b-Epsilon%20Sensitivity%20Analysis.ipynb) **Figure 8b - $\varepsilon$ Sensitivity**: Tests robustness of the transient decay rate across absorbing neighborhood sizes $\varepsilon \in [10^{-5}, 5\times10^{-2}]$.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure9-Null%20Model%20Control%20Experiment.ipynb) **Figure 9 - Null Model Control**: Compares stopping-time distributions of real Collatz, Logistic sandbox, and a generic forbidden-11 Markov chain.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure10-Parameter%20Sensitivity%20and%20PWL%20Control.ipynb) **Figure 10 - $\mu$ Sweep & PWL Control**: Sweeps $\mu$ across the period-3 window and tests a piecewise-linear map with the same symbolic grammar.
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure11-Run-Length%20Distribution%20Comparison.ipynb) **Figure 11 - Run-Length Statistics**: Compares consecutive even-step run-length distributions ($\nu_2$-valuation analog) across Collatz, sandbox, and null Markov model.

## 4. Citation
If you use the code or are inspired by this research, please cite our work:

**APA Format:**
> Wang, L. (2026). Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the $3x+1$ Problem (v2.0). Zenodo. https://doi.org/10.5281/zenodo.19677694

**BibTeX Format:**
```bibtex
@misc{wang2026spectral,
  title={Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the 3x+1 Problem},
  author={Wang, Liang},
  year={2026},
  publisher={Zenodo},
  version={v1.0},
  doi={10.5281/zenodo.18957726},
  url={https://doi.org/10.5281/zenodo.18957726}
}
```
