---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

Open-source tools I develop for the numerical analysis of nonlinear dynamical systems.

<div class="project">
  <h2 id="pynamicalsys" class="project__title">
    <img class="project__logo project__logo--light" src="/images/pynamicalsys_light.png" alt="pynamicalsys">
    <img class="project__logo project__logo--dark" src="/images/pynamicalsys_dark.png" alt="pynamicalsys">
  </h2>
  <p class="project__tagline">A Python toolkit for the analysis of dynamical systems</p>
  <p class="project__badges">
    <a href="https://pypi.org/project/pynamicalsys/"><img src="https://img.shields.io/pypi/v/pynamicalsys.svg" alt="PyPI version"></a>
    <a href="https://pypi.org/project/pynamicalsys/"><img src="https://img.shields.io/pypi/pyversions/pynamicalsys.svg" alt="Python versions"></a>
    <a href="https://pynamicalsys.readthedocs.io/en/latest/"><img src="https://readthedocs.org/projects/pynamicalsys/badge/?version=latest" alt="Documentation status"></a>
    <a href="https://www.gnu.org/licenses/gpl-3.0"><img src="https://img.shields.io/badge/License-GPLv3-blue.svg" alt="License: GPL v3"></a>
    <a href="https://doi.org/10.1016/j.chaos.2025.117269"><img src="https://img.shields.io/badge/DOI-10.1016%2Fj.chaos.2025.117269-blue.svg" alt="DOI"></a>
  </p>
  <p class="project__links">
    <a class="project__btn" href="https://github.com/mrolims/pynamicalsys">GitHub</a>
    <a class="project__btn" href="https://pynamicalsys.readthedocs.io/en/latest/">Documentation</a>
    <a class="project__btn" href="https://pypi.org/project/pynamicalsys/">PyPI</a>
  </p>
</div>

pynamicalsys is an open-source Python package for the analysis of nonlinear dynamical systems. It provides a unified interface to discrete maps, continuous flows, and Hamiltonian systems, together with a broad set of chaos indicators and transport measures. The numerical core is compiled with Numba, which brings the performance close to that of a compiled language while keeping a high-level Python interface.

### Installation

```bash
pip install pynamicalsys
```

pynamicalsys supports Python 3.10 to 3.13 and depends only on NumPy and Numba.

### What it does

<div class="feature-grid">
  <div class="feature-card"><h4>Maps and sections</h4><p>Bifurcation diagrams, Poincaré sections, and stroboscopic maps for discrete systems.</p></div>
  <div class="feature-card"><h4>Hamiltonian systems</h4><p>Symplectic integrators for the time evolution of Hamiltonian flows.</p></div>
  <div class="feature-card"><h4>Chaos indicators</h4><p>Linear dependence index and indicators based on weighted Birkhoff averages.</p></div>
  <div class="feature-card"><h4>Recurrence analysis</h4><p>Recurrence plots and recurrence time statistics.</p></div>
  <div class="feature-card"><h4>Transport and diffusion</h4><p>Statistical measures of transport and diffusion in phase space.</p></div>
  <div class="feature-card"><h4>Orbits, manifolds, and basins</h4><p>Periodic orbit computation, stability analysis, manifolds, and basin quantification.</p></div>
</div>

The package is organized around the classes `DiscreteDynamicalSystem`, `ContinuousDynamicalSystem`, `HamiltonianSystem`, `TimeSeriesMetrics`, `BasinMetrics`, and `PlotStyler`, and reaches speedups of up to 130x over pure-Python implementations.

### Quick example

```python
from pynamicalsys import DiscreteDynamicalSystem

# Logistic map in the chaotic regime
system = DiscreteDynamicalSystem(model="logistic map")
trajectory = system.trajectory(0.2, 100, parameters=[3.8])
```

A complete tour of the API, with tutorials for discrete, continuous, and Hamiltonian systems, is available in the [documentation](https://pynamicalsys.readthedocs.io/en/latest/).

### Citation

If pynamicalsys is useful in your research, please cite:

**M. R. Sales**, L. C. de Souza, D. Borin, M. Mugnaine, J. D. Szezech Jr., R. L. Viana, I. L. Caldas, E. D. Leonel, and C. G. Antonopoulos, _pynamicalsys: A Python toolkit for the analysis of dynamical systems_, [Chaos, Solitons & Fractals 201, 117269 (2025)](https://doi.org/10.1016/j.chaos.2025.117269).

```bibtex
@article{pynamicalsys,
  title={pynamicalsys: A Python toolkit for the analysis of dynamical systems},
  author={Matheus Rolim Sales and Leonardo Costa de Souza and Daniel Borin and Michele Mugnaine and José Danilo Szezech and Ricardo Luiz Viana and Iberê Luiz Caldas and Edson Denis Leonel and Chris G. Antonopoulos},
  journal={Chaos, Solitons & Fractals},
  volume={201},
  pages={117269},
  year={2025},
  doi={https://doi.org/10.1016/j.chaos.2025.117269},
  url={https://www.sciencedirect.com/science/article/pii/S0960077925012822},
}
```
