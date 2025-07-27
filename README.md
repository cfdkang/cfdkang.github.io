<div style="display: flex; align-items: center; margin-top: 1em; margin-bottom: 1.5em;">
  <img src="/assets/KDH_Google1.png" width="130px" style="border-radius: 50%; margin-right: 20px;" />
  <div>
    <!-- 이름과 소속은 상단에 자동 출력되므로 여기선 생략 -->
  </div>
</div>

<div style="color: black;">

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

<div align="center">
  <img src="/assets/figures/Airplane1_jet.png" width="350"/>
  <img src="/assets/figures/Airplane2_vtol.png" width="350"/>
  <br/>
  <em>
    Figure. Hybrid RANS/LES (left) and URANS (right) simulations of aircraft buffeting and swirling-flow interaction using custom solvers and Star-CCM+.
  </em>
</div>

---

### 2. Aeroacoustics

- Simulated **airframe noise** using LES + FW-H solvers (e.g., PSU-WOPWOP)
- Applied empirical models (e.g., Amiet, BPM) for validation
- Developed acoustic tools: cross-spectrum analysis, SPOD, DMD, wavelet denoising
- Implemented **Farassat’s 1A formulation** in Python with `CSDL` and used in design loops
- Collaborated with Stanford CTR on **wavelet-based pressure decomposition**

<div align="center">
  <img src="/assets/figures/spod_1_sweep0deg_1kHz.gif" width="350"/>
  <img src="/assets/figures/spod_2_sweep45deg_1kHz.gif" width="350"/>
  <br/>
  <em>
    Figure. SPOD (St ≈ 15) of noise source structures under straight (left) and 45° misaligned flow (right). Spanwise coherence is key for noise reduction.
  </em>
</div>

---

### 3. Aerodynamic Shape Optimization (ASO)

- Built a modular ASO pipeline using `CSDL` + `DAFoam`, including:
  - `lsdo_geo` for geometry
  - `IDWarp` for mesh deformation
  - `DAFoam` for flow/adjoint
  - `modopt` for optimization
- Used discrete adjoint + autodiff for scalable gradients
- Implemented **LSPG-type pROM** in SU2 for fast BWB optimization

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

</div>
