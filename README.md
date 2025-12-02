# Channel Geometry Optimization & Data Visualization

This project explores how to maximize the cross-sectional area of a bent metal channel under a fixed sheet width. I model the geometry, derive constraints on the design variables, and use optimization and visualization to understand where the channel holds the most water.

Live notebook: [Open in Colab](https://colab.research.google.com/drive/1XccrUYB7w7yC2omUcjzLEDpU4q8B3GXS?usp=sharing)

## Problem Setup

The channel is built from a flat metal sheet of width **W = 3 m** and bent into three parts: right wall **a**, base **b**, and left wall. When the right wall is bent at an angle **θ**, the geometry must satisfy

**b = W − a(1 + sin θ), with b ≥ 0.**

The goal is to choose **a** and **θ** to maximize the cross-sectional area of the channel while remaining feasible.

## Visualizations

The project uses several visualizations to tell the story:

- **Contour and surface plots** of the area **A(a, θ)** over the feasible region, showing how different choices of **a** and **θ** change the area and where the global maximum lies.
- **Optimization trajectories** for multiple starting points, overlaid on the contour plot, to show how different methods move through the landscape and converge.
- **Comparison table/plots** summarizing convergence speed and performance of several algorithms (Armijo gradient descent, fixed-step gradient descent, nonlinear conjugate gradient, momentum).

Each figure is labeled with units and uses a consistent color scale so that trade-offs between geometry and area are visually clear.

## Methods & Tools

- Derived first-order conditions analytically and confirmed the maximizer using the Hessian and boundary analysis.
- Implemented several gradient-based optimization methods in Python.
- Generated all plots with **NumPy** and **Matplotlib** and wrote the report in **LaTeX**.

## What this demonstrates

This project shows how I use data visualization to:

- Turn a complex geometric optimization problem into intuitive contour and surface plots.
- Compare optimization algorithms by visualizing their trajectories and convergence.
- Communicate insights through a combination of math, code, and carefully designed figures.

The full report with all figures is available in the PDF in this repository.
