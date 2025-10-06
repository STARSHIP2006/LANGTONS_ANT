# Langton's Ant — Simulation & Visualizer

A compact, configurable implementation of **Langton’s Ant** — the simple Turing-like cellular automaton that produces surprisingly complex behaviour from very small rules.  
This README is a ready-to-paste, all-purpose `README.md` you can drop into the repository. It intentionally uses no logos or badges.

---

## Overview

Langton’s Ant is a 2D grid automaton where one or more "ants" move on a grid of colored cells. Each ant follows simple rules:

1. At each time step the ant **reads** the color of the cell it is standing on.
2. Based on the color it **turns** (e.g. left or right), **flips** the color of the cell, and then **moves forward** one cell.
3. Repeat.

Despite the simplicity, the system can show chaotic patterns and, after many steps, a characteristic emergent "highway" pattern.

This project provides:
- A readable implementation of the rules (single and multi-ant).
- A simple CLI to run simulations.
- Options for ASCII, PNG frame, and GIF output.
- Easy hooks for experimenting with custom rule sets (multi-color automata).

---

## Features

- Single and multiple ants.
- Configurable grid size, steps, and initial conditions.
- Custom turn rules (e.g. `"RL"`, `"LRR"`, or extended multi-color rules).
- Output options:
  - Terminal / ASCII preview
  - Sequence of PNG frames
  - Animated GIF
- Lightweight, dependency-minimal by default; optional libraries for image/GIF output.

---

## Quick start

> The examples below assume a Python implementation named `langtons_ant.py`. If your main file or language differs, adapt the commands accordingly.

### Requirements

- Python 3.8+ (if using the included Python implementation)
- Optional (for image/GIF output):
  - `Pillow` (`pip install Pillow`)
  - `imageio` (`pip install imageio`)

### Install

```bash
git clone https://github.com/<your-username>/LANGTONS_ANT.git
cd LANGTONS_ANT
