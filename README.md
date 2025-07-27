<p align="left">
  <img src="/assets/KDH_Google1.png" width="130px" style="border-radius: 50%; margin-right: 20px;" />
</p>

## About Me

I am a postdoctoral researcher in the Department of Mechanical and Aerospace Engineering at UC San Diego, working with Dr. John Hwang in the Large-Scale Design Optimization (LSDO) Lab since 2024. I earned my Ph.D. from UC Davis under the guidance of Dr. Seongkyu Lee.

My research lies at the intersection of aeroacoustics and aerodynamic shape optimization using computational fluid dynamics (CFD). I aim to elucidate the fundamental mechanisms of noise generation in turbulent flows and develop efficient methods for optimizing aircraft performance and design.

---

## Research Interests

### 1. Aerodynamics and Computational Fluid Dynamics (CFD)

- Investigated unsteady and turbulent flow physics for a wide range of aerospace configurations, including fighter aircraft (KF-21), VTOL, ducted fans, BWB, and airfoils using high-fidelity CFD.
- Performed 6-DOF aerodynamic simulations involving control surface deflection, thrust vectoring, and stability & control (S&C) analysis.
- Modified and used solvers including:
  - `OpenFOAM v2012` (wall-resolved LES)
  - `DAFoam v4.0`, `SU2 v8.2.0` (RANS and adjoint)
  - Home-grown FVM solver (hybrid RANS/LES)
  - `Star-CCM+ v15.02` (unsteady RANS)
- Pre/post-processing tools:
  - **CAD**: CATIA, OpenVSP  
  - **Meshing**: pyHyp, Pointwise, Gmsh  
  - **Visualization**: Tecplot, ParaView, FieldView

<p align="center">
  <img src="/assets/figures/Airplane1_jet.png" width="350"/>
  <img src="/assets/figures/Airplane2_vtol.png" width="350"/>
  <br/>
  <em>
    Figure. Hybrid RANS/LES (left) and URANS (right) simulations of aircraft buffeting and swirling-flow interaction using custom solvers and Star-CCM+.
  </em>
</p>

---

### 2. Aeroacoustics
- Investigated **airframe noise** using large-eddy simulations (LES) coupled with:
  - **FW-H solver** (e.g., PSU-WOPWOP)
  - Analytical and empirical model (e.g., Amiet's formulation, Brooks, Pope, and Marcolini (BPM) model)
- Developed spectral tool for acoustic analysis: cross-spectrum method
- Utilized advanced time-frequency methods: Spectral POD (SPOD), DMD, wavelet-denoising algorithm, wavenumber-frequency spectrum
- Implemented **Farassat’s 1A FW-H formulation** in `Python` using `CSDL`, integrated with design optimization workflows
- Collaborated with **Stanford CTR** on **wavelet-based pressure decomposition** for airfoil noise in low-Mach-number flows

<p align="center">
  <img src="/assets/figures/spod_1_sweep0deg_1kHz.gif" width="350"/>
  <img src="/assets/figures/spod_2_sweep45deg_1kHz.gif" width="350"/>
  <br/>
  <em>
    Figure. SPOD (St ≈ 15) of noise source structures under straight (left) and 45° misaligned flow (right). Spanwise coherence is key for noise reduction.
  </em>
</p>

---

### 3. Aerodynamic Shape Optimization (ASO)
- Built a modular **ASO framework** using **Computational System Design Language (`CSDL`)** , interfaced with **`DAFoam`** and key design components:
  - `lsdo_geo` for geometric parametrization
  - `IDWarp` for mesh deformation
  - `DAFoam v4.0` for primal/adjoint
  - `modopt` for gradient-based optimization
- Utilized **discrete adjoint methods** and **automatic differentiation** for efficient gradient evaluation and design iteration under HPC cluster.
- Implemented and tested **projection-based reduced-order models (pROM)** (LSPG-type) in SU2 for rapid shape optimization of BWB aircraft.

<p align="center">
  <img src="/assets/figures/aso_rom.png" width="600"/>
  <br/>
  <em>
    Figure. Comparison between FOM and pROM in SU2. pROM yields 11.6× speedup with consistent accuracy.
  </em>
</p>

---

* For the full list of journal papers and conference proceedings, please see the [CV](./CV_Donghun_Kang_Git.pdf)  
* For questions or collaborations, feel free to reach out via [email](mailto:d8kang@ucsd.edu).


