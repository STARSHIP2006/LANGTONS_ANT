# Langton's Ant — Simulation, Visualizer & Pheromone-Enhanced Variants

A compact, configurable implementation of **Langton’s Ant** extended with biological-inspired features such as **pheromone deposition & decay**, multi-ant interactions, configurable rulesets, and notebook-driven experiments. This README is ready to paste into your repository and intentionally contains no logos or image badges.

---

## Overview

This project provides:
- A straightforward Langton’s Ant simulator (single- and multi-ant).
- An extended variant with **pheromone trails**: ants deposit pheromone as they move, pheromone **decays** over time, and ants can **sense** and bias movement by local pheromone concentrations.
- Utilities for ASCII, PNG frame, and GIF output.
- A Jupyter notebook (`Task 1.ipynb`) with examples, visualizations and experiments demonstrating pheromone dynamics, parameter sweeps, and analysis plots.

Together these let you explore emergent behavior from (1) the classical two-state rule and (2) biologically-inspired foraging behaviors that use pheromone signalling.

---

## Key Features

### Classical Langton’s Ant
- Standard two-color rule (`"RL"`) and multi-color generalization (e.g. `"RRL"`, `"LRR"`).
- Single or multiple ants on a shared grid.
- Configurable grid size, start positions, and directions.

### Pheromone System (included in `Task 1.ipynb`)
- **Pheromone deposition:** each ant deposits an amount of pheromone on the cell it leaves or visits.
- **Pheromone decay:** pheromone values on the grid decay each time step by a configurable decay factor.
- **Pheromone sensing:** ants can sample neighboring cells and choose turns probabilistically biased by pheromone strength.
- **Stochastic behavior:** turn decisions can use a probability distribution combining rule-based turning and pheromone attraction (temperature/noise parameter).
- **Parameterizable**: deposition amount, decay rate, diffusion coefficient, sensing radius, and stochasticity.

### IO & Visualization
- Terminal ASCII preview for quick checks.
- Export frames (PNG) and generate animated GIFs.
- Notebook plots (matplotlib) tracking pheromone statistics, ant trajectories, and pattern emergence.

### Experiments & Analysis
- `Task 1.ipynb` contains:
  - Example configurations (classic, pheromone-guided, multi-ant).
  - Parameter sweeps (decay vs deposition) and result visualizations.
  - Metrics collected: pheromone total, entropy of grid, cluster detection, and mean-squared displacement of ants.

---

## Requirements

- Python 3.8+
- Recommended packages (for Notebook & visualization):
  - `numpy`
  - `matplotlib`
  - `pillow` (optional, for PNGs)
  - `imageio` (optional, for GIFs)
  - `jupyter` / `notebook` (to run `Task 1.ipynb`)

Install with pip:

```bash
pip install numpy matplotlib pillow imageio jupyter
