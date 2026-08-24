# Dissertation Code

Python code for the numerical experiments in Section 4 of my MSc dissertation on a singular
forward–backward stochastic system with moving boundaries and its neural approximation.

Both notebooks run top to bottom and print their results. Requires Python 3.10 or later with
`torch`, `numpy`, `pandas` and `matplotlib`.

## Files

**`Benchmark_and_Direct_Application.ipynb`** — Black–Scholes–Barenblatt benchmark against the
analytical and Crank–Nicolson solutions; direct terminal-loss Deep BSDE applied to the singular
two-particle system; structural checks on the learned field; independent exact-geometry reference.

**`Neural_Approximation_Attempt.ipynb`** — restarted neural cascade with Brownian-bridge first-passage
correction, exact terminal completion and `Z = sigma * grad v` by automatic differentiation; `N = 2`
validation against the analytical singleton and an exact-geometry reference; error propagation, seed
and volatility studies; `N = 3` consistency checks.
