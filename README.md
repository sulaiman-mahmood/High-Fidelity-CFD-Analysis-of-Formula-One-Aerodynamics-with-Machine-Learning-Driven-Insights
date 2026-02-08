High-Fidelity CFD Analysis of Formula One Aerodynamics with Machine Learning–Driven Insights
Overview

This project presents a high-fidelity aerodynamic analysis of a Formula One–style vehicle using Computational Fluid Dynamics (CFD) coupled with a machine learning (ML) pipeline to extract, analyze, and model aerodynamic performance.

The work demonstrates:

Industry-standard OpenFOAM CFD workflows

Robust mesh generation and turbulence modeling

Force and pressure data extraction

A data-driven ML approach for aerodynamic insight and prediction

The goal is to bridge physics-based simulation with data-driven modeling, reflecting modern motorsport and engineering workflows.

CFD Methodology
Geometry

Formula One–inspired vehicle geometry

STL-based surface definition

Scaled and validated for physical consistency

Mesh

Base mesh generated with blockMesh

Geometry refinement using snappyHexMesh

Local refinement in:

Underbody

Rear wake

Wheel regions

Boundary layer resolution designed for low y⁺ operation

Solver

OpenFOAM

Steady-state incompressible solver: simpleFoam

Turbulence Model

k-ω SST

Selected for accurate near-wall behavior and wake prediction

Boundary Conditions

Velocity inlet

Pressure outlet

No-slip walls on vehicle surfaces

Ground modeled to capture underbody effects

Simulation Outputs

The CFD simulation produces:

Pressure and velocity fields

Wake structures and flow separation regions

Integrated aerodynamic forces:

Drag

Lift / Downforce

Key outputs are exported for post-processing and machine learning analysis.

Data Extraction & Post-Processing

Force coefficients extracted from OpenFOAM logs

Surface pressure and flow features exported via ParaView

Processed datasets stored in CSV format for ML usage

Visualization includes:

Pressure contours

Velocity magnitude

Wake and vortex structures

Machine Learning Pipeline
Objective

Use CFD-generated data to:

Learn aerodynamic trends

Predict aerodynamic metrics

Demonstrate physics-informed data modeling

Workflow

Import CFD-derived datasets

Feature preprocessing and normalization

Model training and evaluation

Interpretation of aerodynamic relationships

Tools

Python

Jupyter Notebooks

Scikit-learn

Pandas / NumPy

Matplotlib

Example notebook:

aero_ML.ipynb

Repository Structure
├── constant/                # Physical properties and mesh data
├── system/                  # Solver and simulation configuration
├── 0/                       # Initial and boundary conditions
├── aero_ML.ipynb            # Machine learning analysis notebook
├── cfd_forces.csv           # Extracted aerodynamic force data
├── README.md
├── .gitignore


Generated solver outputs, virtual environments, and large artifacts are intentionally excluded to keep the repository lightweight and reproducible.

How to Run the CFD Case
blockMesh
snappyHexMesh -overwrite
simpleFoam


Post-processing:

paraFoam

Key Skills Demonstrated

High-fidelity CFD setup and execution

Turbulence modeling and mesh refinement

Aerodynamic force extraction

Data engineering from physics simulations

Machine learning applied to engineering data

Clean, reproducible research workflows

Motivation

Modern motorsport and engineering increasingly combine CFD, data science, and ML.
This project reflects that hybrid approach by showing how simulation data can be transformed into predictive insight.

Future Work

Transient simulations (DES / LES)

Parametric geometry studies

Physics-informed neural networks (PINNs)

Surrogate models for real-time aero prediction

Author

Sulaiman Mahmood
## Research Summary
A detailed CFD case study is available here:  
[PDF – CFD Analysis of an F1-Style Vehicle Using OpenFOAM](docs/CFD%20Analysis%20of%20an%20F1-Style%20Vehicle%20Using%20OpenFOAM.pdf)
