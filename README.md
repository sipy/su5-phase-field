# SU(5) Phase-Field Cosmology & Topological Matter Simulations

This repository contains the high-resolution, GPU-accelerated PyTorch tensor simulations supporting the phenomenological framework of spacetime as an oscillatory $SU(5)$ phase field.

### Author
**Simeon Ivaylov Petrov** Team Leader & Web Developer | BSc Computer Science | Sofia, Bulgaria

### Overview
These notebooks utilize PyTorch's `float64` Autograd engine to compute 4th-order spatial finite differences across massive ($128^3$) 3D grids. By evaluating the non-linear sigma model alongside Faddeev-Skyrme geometric stabilization and explicit chiral symmetry breaking ($m_\pi=0.15$), these simulations prove that Derrick's Theorem can be defeated on a discretized lattice, halting vacuum collapse and allowing for the emergence of stable topological matter.

### Files

1. **`1_B1_Particle_Crystallization.ipynb`** Demonstrates the stabilization of a single $B=1$ topological seed into a massive fundamental fermion (Proton/Lepton prototype) with a stable rest-mass plateau ($E_{rest} \approx 7.24$).

2. **`2_DT_Nuclear_Fusion.ipynb`** Demonstrates the stereographic merging of $B=2$ (Deuterium) and $B=3$ (Tritium) seeds. The simulation natively captures the strong force energy drop and the geometric decay of the unstable $B=5$ intermediate into a stable $B=4$ Alpha particle and a fast $B=1$ neutron.

3. **`3_Heavy_Nuclei_Crystallization.ipynb`** Explores the "Stability Window" for higher-order topological charge. This notebook demonstrates how a $B=7$ (Lithium/Beryllium) seed can be stabilized into a symmetric polyhedral (Platonic) manifold by tuning vacuum pressure ($m_\pi$) and Skyrme repulsion ($e$), preventing lattice evaporation.

4. **`4_Matter_Antimatter_Annihilation.ipynb`** Evaluates CPT-invariance and topological conservation laws. This experiment simulates the collision of $B=1$ and $B=-1$ seeds, resulting in perfect topological cancellation ($\Delta B < 10^{-5}$) and the conversion of rest-mass energy into high-frequency phase oscillations (radiation).

### Usage
These notebooks are designed to be run directly in Google Colab using a T4 GPU (or higher) with at least 16GB of VRAM. To ensure accuracy, the environment is strictly set to `torch.float64`. 

*Note: Due to high VRAM usage, it is recommended to "Restart Session" in Colab between running different notebooks to clear the GPU cache.*
