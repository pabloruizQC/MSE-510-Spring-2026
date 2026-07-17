# MSE--1-Hackathon
Inaugural scientific hackathon portfolio: Advanced numerical analysis of nonlinear physical systems and energy landscape reconstruction. Features robust solver benchmarking, stability analysis, and integration-based surface recovery."


# Scientific Computing Portfolio: Nonlinear Dynamics & Surface Reconstruction

This repository documents my first intensive scientific hackathon experience. The project focuses on two core challenges: solving complex, nonlinear physical equations and reconstructing potential energy surfaces from discrete force data.

## 🚀 The Hackathon Challenge
This portfolio demonstrates the ability to implement, benchmark, and analyze numerical algorithms under pressure, focusing on physical interpretability and the identification of numerical failure modes.

## 📂 Featured Modules

### 1. Nonlinear System Solvers & Stability Analysis (Problem 2)
* **Scientific Goal:** Solving implicit constitutive equations for nonlinear system responses (e.g., stress-strain relations).
* **Technical Approach:** Developed and compared **Bisection**, **Secant**, and **Newton-Raphson** methods from scratch.
* **Key Discovery:** Conducted a deep dive into **algorithmic failure regimes**. By modeling an "unstable material" ($\alpha < 0$), I demonstrated exactly how and why Newton’s method fails at zero-slope points, while more robust methods like Bisection maintain convergence.

### 2. Energy Landscape & Surface Reconstruction (Problem 3)
* **Scientific Goal:** Reconstructing global potential energy surfaces (PES) from sparse, noisy force-vector measurements.
* **Technical Approach:** Evaluated multiple interpolation frameworks—**Polynomial**, **Cubic Spline**, and **Smoothing Splines**—coupled with **Cumulative Trapezoidal integration**.
* **Key Discovery:** Performed a full **Equilibrium & Stability Analysis**, classifying stable minima and unstable maxima across different reconstruction methods. Conducted a **convergence study** (RMSE vs. N-points) to identify the most data-efficient modeling approach.

## 🛠️ Technical Stack
* **Algorithms:** Root-finding (Newton, Secant, Bisection), Numerical Integration (Trapezoidal), Interpolation (Splines).
* **Tools:** Python, NumPy, SciPy (Optimization & Integration), Matplotlib.

## 📊 Performance Insights
My analysis focuses not just on finding a solution, but on understanding the **limits of the solvers**. The code includes rigorous error handling and convergence benchmarking to ensure physical results are both accurate and numerically stable.
