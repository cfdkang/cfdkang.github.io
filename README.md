<p align="left">
  <img src="/assets/KDH_Google1.png" width="130px" style="border-radius: 50%; margin-right: 20px;" />
</p>

## About Me

I am a postdoctoral researcher in the Department of Mechanical and Aerospace Engineering at UC San Diego, as a member of Dr. John Hwang's Large-Scale Design Optimization (LSDO) Lab since 2024. I earned my Ph.D. from UC Davis under the guidance of Dr. Seongkyu Lee.

My research lies at the intersection of aeroacoustics and aerodynamic shape optimization using computational fluid dynamics. I aim to conduct research on problems related to fluid dynamics, turbulence, and noise reduction, as well as optimization of aircraft design and performance, by integrating theoretical development, advanced numerical techniques, and practical application.


---

## Expertise and Interests

### 1. Aerodynamics and Computational Fluid Dynamics (CFD)

- Investigated unsteady and turbulent flow physics for a wide range of aerospace configurations, including fighter jet (KF-21), VTOL aircraft, ducted fan with vane, and airfoils using high-fidelity CFD
- Performed 6-DOF aerodynamic simulations involving control surface deflection, thrust vectoring driven by ducted fan with vane, and stability & control (S&C) analysis
- Modified and used solvers including:
  - `Home-grown FVM flow solver` (hybrid RANS/LES)
  - `Star-CCM+ v15.02` (unsteady RANS)
  - `OpenFOAM v2012` (LES)
  - `DAFoam v4.0`, `SU2 v8.2.0` (RANS and adjoint)
  
- Pre/post-processing tools:
  - **CAD modeling**: CATIA, OpenVSP  
  - **Meshing**: Gmsh, Pointwise, pyHyp
  - **Visualization**: Tecplot, ParaView, FieldView

<p align="center">
  <img src="/assets/figures/Airplane1_jet.png" width="350"/>
  <img src="/assets/figures/Airplane2_vtol.png" width="350"/>
  <br/>
  <em>
    Figure. 1 Numerical simulations using a hybrid RANS/LES turbulence model for predicting aircraft buffeting with a home-grown FVM flow solver (left), and URANS simulations of swirling-flow interaction in a ducted fan with vane, showing axial velocity contour using Star-CCM+ (right). The ducted fan with control vane is a system designed for thrust generation and roll & yaw maneuvering of an unmanned VTOL aircraft during hovering and transitional flight operations.
  </em>
</p>

---

### 2. Aeroacoustics
- Investigated **flow-induced noise** using large-eddy simulations (LES) coupled with:
  - Ffowcs Williams and Hawkings (FW-H) code (e.g., PSU-WOPWOP)
  - Analytical and empirical model (e.g., Amiet's theory, Brooks, Pope, and Marcolini (BPM) model)
 
<p align="center">
  <img src="/assets/figures/TEN_scattering.gif" width="600"/>
  <br/>
  <em>
    Figure. 2 Sound wave propagation due to scattering of turbulent boundary layer flow around NACA 0012 airfoil.
  </em>
</p>

- Developed spectral tool for acoustic analysis: **cross-spectrum method**
- Utilized **data-driven and advanced time-frequency methods**: Spectral POD (SPOD), DMD, wavelet-denoising algorithm, wavenumber-frequency spectrum
- Participated in the summer program at Center for Turbulence Research (CTR) at Stanford for **collaborative research** on **wavelet-based pressure decomposition** for airfoil noise in low-Mach number flows
- Achieved up to 5.5 dBA **reduction in sound pressure level (SPL)** through flow misalignment, and 2.0 dBA through trailing-edge morphing

<p align="center">
  <img src="/assets/figures/spod_1_sweep0deg_1kHz.gif" width="350"/>
  <img src="/assets/figures/spod_2_sweep45deg_1kHz.gif" width="350"/>
  <br/>
  <em>
    Figure. 3 SPOD (St ≈ 15) of noise source structures under straight (left) and 45° misaligned flows (right). Spanwise anti-phase coherent convection under flow misalignment is critical for the noise reduction mechanism.
  </em>
</p>

---

### 3. Aerodynamic Shape Optimization (ASO)
- Estabilshed a modular **ASO framework** using **Computational System Design Language (`CSDL`)**, interfaced with **`DAFoam`** and key design components:
  - `lsdo_geo` for geometric parametrization
  - `IDWarp` for mesh deformation
  - `DAFoam v4.0` for primal/adjoint
  - `modopt` for gradient-based optimization
<p align="center">
  <img src="/assets/figures/aso_xdsm.pdf" width="600"/>
  <br/>
  <em>
    Figure. 4 Extended design-structure matrix for aerodynamic shape optimization. $x$ : design variables.
  </em>
</p>

- Utilized **discrete adjoint methods** and **automatic differentiation** for efficient gradient evaluation and design iteration under HPC cluster
- Developed a `CSDL`-based implementation of **Farassat’s 1A FW-H formulation** and Fourier transform to integrate the advanced acoustic method into multidisciplinary design optimization (MDO)
- Implemented and tested **projection-based reduced-order models (pROM)** (LSPG-type) in SU2 for rapid shape optimization of a generic aircraft

<p align="center">
  <img src="/assets/figures/aso_rom.png" width="600"/>
  <br/>
  <em>
    Figure. 5 Comparison of pressure coefficient, state vector, and lift coefficient between full-order model (FOM) and pROM in SU2. pROM achieves an 11.6x speedup with consistent accuracy at the prediction point.
  </em>
</p>

---

* For a complete overview of my professional experience and publications, please see the [CV](./CV_Donghun_Kang.pdf).
* For any questions, feel free to reach out via [d8kang@ucsd.edu](mailto:d8kang@ucsd.edu).


