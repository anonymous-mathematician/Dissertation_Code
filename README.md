# Dissertation Code

This repository contains the Python code used for the numerical experiments in Section 4 of my MSc dissertation at the London School of Economics and Political Science.

The dissertation studies a singular forward-backward stochastic differential equation with endogenous moving boundaries and investigates neural approximation methods for the associated restarted cascade.

## Files

### `Benchmark_and_Direct_application.ipynb`

This notebook contains the preliminary Deep BSDE experiments.

It includes

- a Black--Scholes--Barenblatt benchmark used to validate the standard Deep BSDE implementation
- comparison with analytical and finite-difference reference solutions
- the direct application of the same Deep BSDE framework to the singular moving-boundary problem
- diagnostics illustrating why the direct terminal-loss formulation is insufficient for the singular problem

### `Neural_approximation_attempt.ipynb`

This notebook contains the main neural approximation experiments developed for the singular FBSDE.

It includes

- the restarted cascade Deep BSDE method
- fresh initial conditions across restart times throughout the time interval
- recursive training of lower-dimensional decoupling fields
- explicit treatment of first-exit and moving-boundary conditions
- analytical validation of the singleton level
- the full two-particle experiment
- independent Monte Carlo validation of the two-particle decoupling field
- the three-particle extension
- symmetry, boundary, terminal and range diagnostics
- a held-out dimensional-reduction comparison from the three-particle model to the independently trained two-particle model

The two-particle case is the principal numerical experiment. The three-particle case is included to examine whether the recursive construction continues to behave consistently beyond the main two-particle setting.

## Running the code

The notebooks were run in Google Colab using Python and PyTorch.

Run the cells in order from the beginning of each notebook. Random seeds, model architectures, optimisation settings, simulation parameters and validation settings used for the dissertation experiments are specified directly in the notebooks.

The main numerical experiments use simulated Brownian paths and therefore benefit substantially from GPU acceleration.

## Reproducibility

The notebooks contain the training and diagnostic code required to reproduce the numerical results reported in Section 4 of the dissertation.

Due to stochastic simulation and neural-network optimisation, small numerical differences may occur between runs even when the same settings are used.

## Dissertation

The accompanying dissertation develops the mathematical moving-boundary and decoupling-field framework before introducing the numerical methods implemented here. The code in this repository is intended to accompany the numerical analysis rather than replace the mathematical arguments given in the dissertation.
