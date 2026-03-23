# SU(5) Phase-Field Cosmology & Topological Matter Simulations

This repository contains GPU-accelerated PyTorch notebooks exploring a **phenomenological phase-field framework** in which spacetime is modeled as an oscillatory field with topological excitations.

The current numerical work is focused on a computationally tractable **SU(2) / O(4) topological subsector** motivated by a broader gauged **SU(5) prototype**. The goal of these simulations is not to claim a complete first-principles derivation of modern physics, but to test whether topological stabilization, lattice binding, quench dynamics, and multi-soliton interactions exhibit the qualitative behavior required by the broader framework.

## Author

**Simeon Ivaylov Petrov**  
Sofia, Bulgaria

## Overview

These notebooks use PyTorch with `torch.float64` precision and GPU acceleration to evaluate 3D non-linear sigma / Faddeev-Skyrme-type dynamics on large lattices (typically up to `128^3`).

The repository explores several linked questions:

- Can localized topological seeds remain stable under lattice relaxation?
- Can higher-charge configurations exhibit binding, decay channels, and stability windows resembling qualitative nuclear behavior?
- Can post-quench field dynamics generate persistent topological remnants from a high-entropy initial state?
- Can matter-antimatter configurations exhibit topological cancellation while conserving total energy numerically?

The simulations are intended as **exploratory numerical evidence** for the viability of the stabilization mechanism and the broader phenomenological program.

## Scientific Scope

This repository currently supports the following claims:

- numerical exploration of topological stabilization in an SU(2) / O(4) sector
- qualitative study of binding, fusion-like decay pathways, and annihilation
- high-resolution GPU relaxation of localized topological seeds
- exploratory quench simulations motivated by Kibble-Zurek-type phase ordering

This repository does **not** yet provide:

- a full 3D lattice simulation of the complete 5×5 SU(5) field dynamics
- a first-principles derivation of the Standard Model spectrum
- a first-principles derivation of the inflationary potential
- continuum-extrapolated or fully quantized results

## Repository Structure

### `0_Kibble-Zurek_Engine.ipynb`
Explores a 3D quench scenario in which a high-entropy initial field relaxes toward a lower-energy vacuum configuration. The notebook tracks the reduction of total winding complexity and the emergence of persistent localized topological hotspots.

### `1_B1_Particle_Crystallization.ipynb`
Studies the relaxation of a localized `B = 1` topological seed into a stabilized soliton-like configuration with a non-zero rest-energy plateau.

### `2_DT_Nuclear_Fusion.ipynb`
Simulates the interaction of `B = 2` and `B = 3` topological seeds and examines whether the combined configuration exhibits binding, transient composite behavior, and decay into lower-energy products.

### `3_Heavy_Nuclei_Crystallization.ipynb`
Explores higher-charge configurations, including whether a `B = 7` seed can be stabilized into a long-lived polyhedral structure under modified parameter choices.

### `4_Matter_Antimatter_Annihilation.ipynb`
Studies the collision of `B = 1` and `B = -1` configurations and tracks topological cancellation together with the redistribution of energy into oscillatory radiation-like modes.

## Numerical Setup

The notebooks are designed for **Google Colab** or another CUDA-enabled environment with a GPU comparable to a **T4 or better**, ideally with at least **16 GB VRAM**.

### Core numerical features

- PyTorch-based tensor simulation
- `torch.float64` precision
- 3D lattices up to `128^3`
- 4th-order finite-difference spatial stencils
- gradient-flow relaxation
- explicit symmetry-breaking terms where needed to control topological tails and lattice-boundary effects

## Usage

Open the notebooks in Google Colab or a local CUDA-enabled Jupyter environment.

Recommended workflow:

1. Run one notebook at a time
2. Keep precision at `torch.float64`
3. Restart the runtime between notebooks to clear GPU memory
4. Save generated plots, topological diagnostics, and energy traces after each run

## Important Notes

Because these simulations are computationally heavy, GPU memory can become fragmented between runs. In Colab, it is recommended to use **Runtime → Restart session** between major notebooks.

The results should be interpreted as **numerical experiments inside a phenomenological prototype**, not as definitive proof of a full unified theory.

## Interpretation and Limitations

The repository is meant to test whether the geometric and topological mechanisms proposed in the accompanying manuscript are numerically viable.

Current limitations include:

- reliance on a reduced topological subsector rather than full SU(5) lattice evolution
- sensitivity to lattice size, resolution, and boundary effects
- fitted phenomenological parameters in some sectors
- absence of continuum extrapolation and full quantum corrections

## Related Manuscript

This code accompanies the paper:

[**“Spacetime as an Oscillatory Phase Field: Semiclassical Dynamics, Topological Mass Spectra, and Cosmology in a Gauged SU(5) Prototype”**](https://drive.google.com/file/d/1lilhGr5TrhsMojbvZNKShBLQ52LQKSEe/view?usp=sharing)

## Citation

If you use or discuss this repository, please cite the associated manuscript and link back to this repository.

## License

All rights reserved
