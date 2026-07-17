# MSE 510 — Machine Learning for Materials Science

**University of Tennessee, Knoxville · Spring 2026 · Prof. Sergei V. Kalinin**

My complete coursework for MSE 510: a semester-long progression from classical numerical methods to machine-learning-driven and autonomous experimentation for materials science. The course's central question: once ML enters the lab, how do real objects become mathematical ones — and how do algorithms decide what experiment to run next? All work developed and executed in Google Colab.

## Structure

```
my-work/       my solutions, organized by course module
lectures/      course lecture notebooks per module (MIT-licensed, for reference)
tools/         repository utilities
```

## Module 1 — Numerical foundations

How continuous physics becomes discrete computation: floating-point precision and its failure modes, interpolation, numerical integration (rectangle to Simpson), and root-finding for nonlinear equations (bisection, false position, Newton-Raphson).

| My work | Summary |
|---|---|
| `Homework_1` | Python + GitHub onboarding |
| `Homework_2` | Numerical foundations problem set: interpolation, integration, root-finding |
| `Hackathon_1_Numerical_Methods` | Sparse phase-diagram interpolation, root-finding in nonlinear constitutive models with Newton failure-regime analysis, potential-energy-surface reconstruction from noisy force data ([standalone repo](https://github.com/pabloruizQC/MSE--1-Hackathon)) |

## Module 2 — Symbolic regression: from data to equations

Fitting as modeling: linear/polynomial/exponential regression, genetic-algorithm symbolic regression built from scratch, PySR applied to Ising models, generative statistical models (DLA, cellular automata), and automated PySR + GPax pipelines.

| My work | Summary |
|---|---|
| `Homework_4` | Function fitting and symbolic regression problem set |
| `Hackathon_2_Symbolic_Regression` | Timed sprint: recovering governing equations from data |

## Module 3 — Differential equations

Numerical derivatives, ODE integration from Euler to adaptive RK4 (double-pendulum chaos as the stress test), and PDE boundary-value problems via relaxation methods.

| My work | Summary |
|---|---|
| `Midterm_1` | RC-circuit discharge, nonlinear pendulum dynamics, and data-driven model discovery with symbolic regression |

## Module 4 — Physics-informed machine learning

NN regression with ensemble uncertainties; PINNs embedding governing equations in the loss (Newton cooling, diffusion, Burgers); Neural ODEs for system identification and parameter estimation; PI-DeepONets; equation and parameter discovery on the Van der Pol oscillator.

| My work | Summary |
|---|---|
| `Hackathon_3_Neural_Networks` | Timed sprint: neural network fundamentals |
| `Hackathon_4_STM_Analysis` | Scanning tunneling microscopy image analysis: physical models of STM height profiles |

## Module 5 — Bayesian methods

Priors, likelihoods, and posteriors from coin tosses to PyMC models; Bayesian curve fitting with GPax; quantitative comparison of competing models against the same data.

| My work | Summary |
|---|---|
| `Homework_7` | Bayesian inference problem set |
| `Homework_9` | Bayesian inference, Gaussian processes, and Bayesian optimization |

## Module 6 — Gaussian processes & active learning

GP regression and kernels, Bayesian optimization and acquisition functions, structured GPs with physics-informed mean functions, GP/sGP beyond 1D (GPyTorch + BoTorch) — culminating in closed-loop autonomous experimentation.

| My work | Summary |
|---|---|
| `Hackathon_5_Gaussian_Processes` | GP fundamentals sprint |
| `Midterm_2_Part_I_Active_Learning` | Active learning of a hidden noisy function behind a live API: 8 competing Bayesian models (scikit-learn GPs with RBF/Matern/quasi-periodic kernels vs GPyTorch GPs with linear-mean and additive kernels), Bayesian model averaging, weighted-UCB + model-disagreement acquisition — identified the function's quasi-periodic structure in 30 queries |
| `Midterm_2_Part_II_Drift_Correction` | Drift correction in simulated atomic-resolution microscopy: lattice generation, drift modeling, reconstruction |
| `Final_Active_Experimental_Design` | Active experimental design under noise and measurement-budget constraints with GP surrogates |

## Toolbox

Python · NumPy · SciPy · matplotlib · scikit-learn · PyTorch · GPyTorch · BoTorch · GPax/JAX · PySR · PyMC · Google Colab

## Credit

Lecture notebooks under `lectures/` are from the course's MIT-licensed repository [SergeiVKalinin/MSE_Spring_2026](https://github.com/SergeiVKalinin/MSE_Spring_2026) (© Sergei V. Kalinin), included with attribution. Everything under `my-work/` is my own. `tools/sync_notebooks.ipynb` synchronizes this repository with my Colab workspace.
