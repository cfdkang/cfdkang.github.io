# About Me

I am a postdoctoral researcher in the Department of Mechanical and Aerospace Engineering at UC San Diego, working with Dr. John Hwang in the Large-Scale Design Optimization (LSDO) Lab since 2024. I earned my Ph.D. from UC Davis under the guidance of Dr. Seongkyu Lee.

My research lies at the intersection of aeroacoustics and aerodynamic shape optimization using computational fluid dynamics (CFD). I aim to elucidate the fundamental mechanisms of noise generation in turbulent flows and develop efficient methods for optimizing aircraft performance and design.

---

# Research Interests

## 1. Aerodynamics and Computational Fluid Dynamics (CFD)

- Investigated unsteady and turbulent flow physics for a wide range of aerospace configurations, including generic fighter aircraft (KF-21), VTOL aircraft, ducted fan and vane, blended-wing body (BWB), and canonical airfoils using high-fidelity CFD simulations.
- Performed 6-DOF aerodynamic simulations involving control surface deflection, thrust vectoring, and stability/control (S&C) analysis.
- Modified and utilized CFD solvers including:
  - `OpenFOAM v2012` (wall-resolved LES)
  - `DAFoam v4.0`, `SU2 v8.2.0` (RANS and adjoint)
  - In-house Fortran-based FVM solver (hybrid RANS/LES)
  - `Star-CCM+ v15.02` (unsteady RANS)
- Skilled in pre- and post-processing tools:
  - **CAD**: CATIA, OpenVSP   
  - **Meshing**: pyHyp, Pointwise, Gmsh  
  - **Visualization**: Tecplot, ParaView, FieldView

<p align="center">
  <table>
    <tr>
      <td><img src="./assets/figures/Airplane1_jet.png" width="300"/></td>
      <td><img src="./assets/figures/Airplane2_vtol.png" width="300"/></td>
    </tr>
  </table>
  <br/>
  <em>Figure. Hybrid RANS/LES simulation of a generic aircraft for predicting vertical-tail buffeting using the in-house FVM flow solver (left) and URANS simulation of ducted-fan vane to examine the impact of swirling flow on the vane using Star-CCM+ v15.02.</em>
</p>


## 2. Aerodynamic Shape Optimization (ASO)

- Built a modular **ASO framework** using **CSDL**, interfaced with **DAFoam** and key design components:
  - `pyHyp` for volume meshing
  - `IDWarp` for mesh deformation
  - `modopt` for gradient-based optimization
- Implemented and tested **projection-based reduced-order models (pROM)** (LSPG-type) in SU2 for rapid shape optimization of BWB aircraft.
- Utilized **discrete adjoint methods** and **automatic differentiation** for efficient gradient evaluation and design iteration under HPC cluter.

<p align="center">
  <img src="./assets/figures/aso_rom.png" width="600"/>
  <br/>
  <em> Figure. Comparison of pressure coefficient, state vector, and lift coefficient between full-order model (FOM) and pROM in SU2 v8.2.0. pROM achieves an 11.6x speedup compared to the FOM at the prediction point.</em>
</p>

## 3. Aeroacoustics

- Investigated **airframe noise** using large-eddy simulations (LES) coupled with:
  - **FW-H solver** (e.g., PSU-WOPWOP)
  - Analytical and empirical model (e.g., Amiet's formulation, Brooks, Pope, and Marcolini (BPM) model)
- Developed spectral tool for acoustic analysis: cross-spectrum method
- Utilized advanced time-frequency methods: Spectral POD (SPOD), DMD, wavelet-denoising algorithm, wavenumber-frequency spectrum
- Implemented **Farassat’s 1A FW-H formulation** in Python using **CSDL**, integrated with design optimization workflows
- Collaborated with **Stanford CTR** on **wavelet-based pressure decomposition** for airfoil noise in low-Mach-number flows

<p align="center">
  <table>
    <tr>
      <td><img src="./assets/figures/spod_1_sweep0deg_1kHz.gif" width="300"/></td>
      <td><img src="./assets/figures/spod_2_sweep45deg_1kHz.gif" width="300"/></td>
    </tr>
  </table>
  <br/>
  <em>Figure. SPOD (St &asymp; 15) of trailing-edge noise source structures under straight flow (left) and 45-degree misaligned flow (right) using OpenFOAM v2012. Spanwise anti-phase coherent flow is critical for the noise reduction mechanism.</em>
</p>

---

*For the full list of journal papers and conference proceedings, please see the [CV](./CV_Donghun_Kang_Git.pdf)*  
*For questions or collaborations, feel free to reach out via [email](mailto:d8kang@ucsd.edu).*
