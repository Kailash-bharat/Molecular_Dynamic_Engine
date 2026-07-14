# Molecular Dynamics Engine – Argon Phase Transition

## Overview
This project implements a complete Molecular Dynamics (MD) engine in Python to simulate the **solid-to-liquid phase transition of Argon**. The engine is built from first principles and integrates key physical models and numerical methods to reproduce realistic atomic behavior.

## Features
- **Lennard-Jones (LJ) Potential** with shifted-force correction
- **Periodic Boundary Conditions (PBC)** and Minimum Image Convention
- **Velocity Verlet Integrator** for stable, time-reversible dynamics
- **FCC Lattice Initialization** for realistic starting configurations
- **Verlet Neighbor Lists** for performance optimization (O(N) scaling)
- **Equilibration & Production Runs** with Maxwell-Boltzmann velocity initialization
- **Analysis Tools**: Radial Distribution Function (g(r)) and Self-Diffusion Coefficient

## Simulation Details
- Species: Argon (Ar)
- LJ Parameters: σ = 3.405 Å, ε/kB = 119.8 K
- Atoms: N = 108
- Cutoff radius: r_c = 2.5 σ
- Temperature range: T* = 0.2 → 1.2
- Time step: dt* = 0.005
- Equilibration: 1000 steps | Production: 500 steps

## Results
- **Phase Transition**: Solid → Liquid confirmed via g(r)
- **Melting Temperature**: Simulated T_melt ≈ 100–120 K (experimental: 83.8 K)
- **Self-Diffusion Coefficient**: D = 0.177 Å²/ps at T* = 1.00 (120 K), matching experimental values

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
