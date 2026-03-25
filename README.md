# Monte Carlo Simulation of a Magnet
- Author: Gustavo Aguilar

This repository contains a Jupyter notebook that demonstrates how to simulate the behavior of a 2D array of magnetic moments (spins) using a Monte Carlo approach. It visualizes a random initial configuration of unit-length magnetic moments on a square lattice — a starting point for studying ferromagnetism, paramagnetism, and phase transitions.

## Overview

This project creates and visualizes an initial random configuration of classical magnetic moments (vectors of fixed length |m| = 1) arranged on a square lattice. Each moment is assigned a random orientation using spherical coordinates. The notebook uses Matplotlib's 3D quiver plot to show the directions of all spins, providing an intuitive picture of a high-temperature (paramagnetic) state where total magnetization is near zero. This is the typical starting configuration used in Monte Carlo simulations of classical Heisenberg or XY models — foundational tools for understanding magnetism, critical phenomena, and statistical mechanics.

## Physics / Math Background

We model a 2D lattice of N × N classical magnetic moments (spins) with fixed magnitude |mᵢ| = 1. Each spin has a random orientation defined by spherical coordinates:

- θᵢ ∈ [0, π]     (polar angle)  
- φᵢ ∈ [0, 2π)    (azimuthal angle)

The Cartesian components are:

mᵢ = (cos φᵢ sin θᵢ, sin φᵢ sin θᵢ, cos θᵢ)

At high temperature (or in the absence of interactions / external field), spins point in random directions → total magnetization M = Σ mᵢ ≈ 0 (paramagnetic phase).  
This notebook generates and visualizes such a random initial state — the usual starting point before applying Monte Carlo updates (Metropolis or heat-bath) to study ordering, domain formation, or hysteresis.

## Methods

- **Model**: Classical vector spins (Heisenberg-like) on a 2D square lattice  
- **Initialization**: Uniform random orientations via spherical coordinates  
- **Visualization**: 3D quiver plot showing every spin vector  
- **Languages and Libraries**:
  - Python 3
  - NumPy — array operations and random number generation
  - Matplotlib — 3D quiver and scatter plotting

## Results

The notebook produces:

- A 3D quiver plot of a 40×40 lattice (1600 spins) with:
  - Red dots at each lattice site
  - Arrows showing the direction of each magnetic moment
  - Title indicating "Paramagnet (Total magnetization is near zero)"
- Clear visual demonstration of completely random orientations (no net magnetization)
- Adjustable lattice size (`length = 40` by default)

This is the typical disordered starting configuration used before running Monte Carlo steps to observe ferromagnetic ordering at low temperature.
