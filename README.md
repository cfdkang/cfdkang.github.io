<p align="center">
  <img src="/assets/KDH_Google1.png" width="140px" style="border-radius: 50%; display: block;" />
</p>

<h2 align="center">Donghun Kang</h2>
<p align="center"><em>Postdoctoral Researcher · UC San Diego</em></p>

---

## About Me

I am a postdoctoral researcher in the Department of Mechanical and Aerospace Engineering at UC San Diego, working with Dr. John Hwang in the Large-Scale Design Optimization (LSDO) Lab since 2024. I earned my Ph.D. from UC Davis under the guidance of Dr. Seongkyu Lee.

My research lies at the intersection of aeroacoustics and aerodynamic shape optimization using computational fluid dynamics (CFD). I aim to elucidate the fundamental mechanisms of noise generation in turbulent flows and develop efficient methods for optimizing aircraft performance and design.

---

## Research Interests

### 1. Aerodynamics and Computational Fluid Dynamics (CFD)

- Investigated unsteady and turbulent flow physics for a wide range of aerospace configurations, including generic fighter aircraft (KF-21), VTOL aircraft, ducted fan and vane, blended-wing body (BWB), and canonical airfoils using high-fidelity CFD simulations.
- Performed 6-DOF aerodynamic simulations involving control surface deflection, thrust vectoring, and stability & control (S&C) analysis.
- Modified and utilized CFD solvers including:
  - `OpenFOAM v2012` (wall-resolved LES)
  - `DAFoam v4.0`, `SU2 v8.2.0` (RANS and adjoint)
  - Home-grown FVM solver (hybrid RANS/LES)
  - `Star-CCM+ v15.02` (unsteady RANS)
- Skilled in pre- and post-processing tools:
  - **CAD**: CATIA, OpenVSP  
  - **Meshing**: pyHyp, Pointwise, Gmsh  
  - **Visualization**: Tecplot, ParaView, FieldView

<div align="center">
  <div style="display: inline-block; text-align: center;">
    <img src="./assets/figures/Airplane1_jet.png" width="300"/>
    <img src="./assets/figures/Airplane2_vtol.png" width="300"/>
    <br/>
    <em style="font-size: 0.95em;">
      Figure. Hybrid RANS/LES simulation of a generic aircraft for predicting vertical-tail buffeting (left) and URANS simulation of ducted-fan vane to examine swirling flow impact using Star-CCM+ (right).
    </em>
  </div>
</div>

---

### 2. Aeroacoustics

- Investigated **airframe noise** using large-eddy simulations (LES) coupled with:
  - **FW-H solver** (e.g., PSU-WOPWOP)
  - Analytical and empirical models (e.g., Amiet's formulation, BPM model)
- Developed spectral tools for acoustic analysis: cross-spectrum method
- Applied time-frequency techniques: SPOD, DMD, wavelet denoising, and wavenumber-frequency analysis
- Implemented **Farassat’s 1A FW-H formulation** in Python using `CSDL` and integrated it with design workflows
- Collaborated with **Stanford CTR** on **wavelet-based pressure decomposition** for airfoil noise at low Mach number

<div align="center">
  <div style="display: inline-block; text-align: center;">
    <img src="./assets/figures/spod_1_sweep0deg_1kHz.gif" width="300"/>
    <img src="./assets/figures/spod_2_sweep45deg_1kHz.gif" width="300"/>
    <br/>
    <em style="font-size: 0.95em;">
      Figure. SPOD (St ≈ 15) of trailing-edge noise sources under straight flow (left) and 45° misaligned flow (right). Spanwise anti-phase coherence plays a key role in noise reduction.
    </em>
  </div>
</div>

---

### 3. Aerodynamic Shape Optimization (ASO)

- Built a modular **ASO framework** using `CSDL`, interfaced with:
  - `lsdo_geo` for geometry parameterization
  - `IDWarp` for mesh deformation
  - `DAFoam` for primal/adjoint flow solution
  - `modopt` for gradient-based optimization
- Applied **discrete adjoint methods** and **automatic differentiation** for scalable gradient evaluation
- Implemented **LSPG-type projection-based reduced-order models (pROM)** in SU2 for rapid BWB optimization

<p align="center">
  <img src="./assets/figures/aso_rom.png" width="600"/>
  <br/>
  <em>Figure. Comparison of Cp, state vector, and lift coefficient between FOM and pROM in SU2. pROM achieves an 11.6× speedup at the prediction point.</em>
</p>

---

📄 [View Full CV](./CV_Donghun_Kang_Git.pdf)  
📧 [Email me](mailto:d8kang@ucsd.edu)
