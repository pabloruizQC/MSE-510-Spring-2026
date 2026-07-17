# MSE 510 — Machine Learning for Materials Science

**University of Tennessee, Knoxville · Spring 2026 · Prof. Sergei V. Kalinin**

My coursework portfolio for MSE 510: a semester-long progression from classical numerical methods to machine-learning-driven and autonomous experimentation for materials science. The course's central theme: ML in the real world is not just training good models — it's understanding how physical objects become mathematical ones, how models compete to explain data, and how algorithms can propose the next experiment. All work was developed and run in Google Colab.

```
my-work/     my homework, hackathon, and exam solutions
lectures/    course lecture notebooks (modules 1-6), included for reference
             MIT-licensed, from SergeiVKalinin/MSE_Spring_2026
```

## The class, part by part

**Module 1 — Numerical foundations.** How continuous physics becomes discrete computation: floating-point precision and its failure modes, interpolation (nearest-neighbor → splines), numerical integration (rectangle, trapezoid, Simpson), and root-finding for nonlinear equations (bisection, false position, Newton-Raphson) — with emphasis on when and why each method breaks.

**Module 2 — From data to equations.** Fitting as modeling: linear/polynomial/exponential regression, then symbolic regression — first built from scratch with genetic algorithms, then with PySR applied to Ising models — plus generative statistical models (diffusion-limited aggregation, cellular automata, Game of Life) and automated PySR + GPax pipelines that fit and validate candidate equations.

**Module 3 — Dynamics.** Differential equations end to end: numerical derivatives (forward/backward/central), ODE integration from Euler to adaptive RK4 (chaotic double pendulum as the stress test), and PDE boundary-value problems via relaxation methods.

**Module 4 — Physics-informed machine learning.** Where deep learning meets physical law: NN regression with uncertainty from ensembles; PINNs that embed governing equations in the loss (Newton cooling, diffusion, Burgers); Neural ODEs for system identification and parameter estimation; PI-DeepONets for operator learning; and equation/parameter discovery on the Van der Pol oscillator — including the practical pathologies (spectral bias, derivative quality).

**Module 5 — Bayesian reasoning.** Probability as the language of experiment: priors, likelihoods, and posteriors from coin tosses to PyMC models; Bayesian curve fitting with GPax; and the key question of experimental science — comparing competing models against the same data.

**Module 6 — Gaussian processes and the automated scientist.** The capstone: GP regression and kernels, Bayesian optimization with acquisition functions, structured GPs (physics-informed mean functions), scaling beyond 1D with GPyTorch/BoTorch — culminating in closed-loop active learning where the algorithm decides which measurement to take next.

## My work

### Exams

| Notebook | What it does |
|---|---|
| `exams/Midterm_1.ipynb` ⏳ | Computational physics + model discovery: RC-circuit discharge, nonlinear pendulum ODEs, and recovering governing equations from data with symbolic regression |
| `exams/Midterm_2_Part_I_Active_Learning.ipynb` ⏳ | **"The automated scientist":** actively learns a hidden noisy function behind a live API using 8 competing models — 4 scikit-learn GPs (RBF, Matérn, Matérn+linear, quasi-periodic kernels) vs 4 GPyTorch GPs (incl. linear-mean and RBF+periodic additive) — combined by Bayesian model averaging with a weighted-UCB + model-disagreement acquisition function. Correctly identified the quasi-periodic structure of the hidden function in 30 queries |
| `exams/Midterm_2_Part_II_Drift.ipynb` ✅ | Drift correction in simulated atomic-resolution microscopy: lattice generation, drift modeling, and image reconstruction |
| `exams/Final_Active_Experimental_Design.ipynb` ⏳ | Active experimental design under noise and measurement-budget constraints: Bayesian optimization with GP surrogates deciding where to measure next |

### Hackathons (timed in-class sprints)

| Notebook | What it does |
|---|---|
| `hackathons/Hackathon_1_Numerical_Methods.ipynb` ✅ | Interpolating a sparse phase diagram, root-finding in nonlinear const