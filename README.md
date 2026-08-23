# Dissertation Code

This repository contains the Python code used for the numerical experiments in Section 4 of my MSc dissertation.

The dissertation studies a singular finite-particle FBSDE with endogenous moving boundaries and investigates neural approximation methods based on the recursive cascade of Jettkant and Søjmark.

## Files

### `Benchmark_and_Direct_Application.ipynb`

Contains the preliminary Deep BSDE experiments

- Black--Scholes--Barenblatt benchmark with analytical and finite-difference comparisons
- direct application to the singular \(N=2\) system
- post-training structural diagnostics for the direct formulation

### `Neural_Approximation_Attempt.ipynb`

Contains the final restarted cascade implementation

- restarted sampling in time and state
- recursive training and freezing of lower-level fields
- Brownian-bridge first-passage correction
- exact terminal completion
- sorted-coordinate networks
- \(Z=\sigma\nabla v\) by automatic differentiation
- \(N=2\) analytical and exact-geometry validation
- \(N=3\) dimensional-reduction and multiple-boundary consistency checks

The main singular experiments use \(T=\sigma=\alpha=1\), with the \(N=2\) cascade trained on \([1,4]^m\) and the \(N=3\) cascade on \([1,7]^m\).

The analytical singleton and independent reference calculations are used only for post-training validation and are not supplied as training targets.

## Notes

The \(N=2\) experiments provide the main quantitative validation. The \(N=3\) results are intended as consistency checks rather than independent error estimates.

The notebooks contain the code used to generate the numerical results, tables and figures reported in the dissertation.
