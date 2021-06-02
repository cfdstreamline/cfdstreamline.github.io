---
layout: single
---

## Aerospace - External Aerodynamics


### 2D Cases


#### [NACA-0012 Airfoil](https://turbmodels.larc.nasa.gov/naca0012_val.html)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases:
  * M = 0.15
  * Re = 6E6
  * AoA = -17.3deg. to +17.3deg.


#### [NACA-4412 Airfoil](https://turbmodels.larc.nasa.gov/naca4412sep_val.html)
* Objective: Trailing edge separation.
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Case:
  * M = 0.09
  * Re = 1.52E6
  * AoA = 13.87 deg.


#### [RAE-2822 Airfoil](https://www.grc.nasa.gov/WWW/wind/valid/raetaf/raetaf.html)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Case:
  * M = 0.725
  * Re = 6.5E6
  * AoA = 2.92 deg.


#### [NLR Airfoil with Flap](https://www.grc.nasa.gov/WWW/wind/valid/nlrflap/nlrflap.html)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases:
  * M = 0.20
  *   * P = 14.7 Psia
  * T = 520 R
  * AoA = 10 deg.


#### [Axisymmetric SWBLI near M=7](https://turbmodels.larc.nasa.gov/axiswblim7_val.html)
* Experimental data: publically available
* Grids: not available
* Numerical results: publically available
* Case:
  * M = 7.11
  * Re = 57060 per cm
  * AoA = 20 deg.



### 3D Cases


#### [Onera M6 Wing](https://www.grc.nasa.gov/WWW/wind/valid/m6wing/m6wing.html)
* Experimental data: publically available
* Grids: not available
* Numerical results: publically available
* Case:
  * M = 0.8395
  * Re = 11.72E6
  * AoA = 3.06 deg.
* [CFL3D site](https://cfl3d.larc.nasa.gov/Cfl3dv6/cfl3dv6_testcases.html#onera)


#### [ARA M100 Wing-Body](https://cfl3d.larc.nasa.gov/Cfl3dv6/cfl3dv6_testcases.html#ara)[i](https://cfl3d.larc.nasa.gov/Cfl3dv6/cfl3dv6_testcases.html#ara)[te](https://cfl3d.larc.nasa.gov/Cfl3dv6/cfl3dv6_testcases.html#ara)
* Experimental data: publically available
* Grids: not available
* Numerical results: publically available
* Case:
  * M = 0.8027
  * Re = 13.1E6
  * AoA = 2.873 deg.


#### [Delta Wing](https://cfl3d.larc.nasa.gov/Cfl3dv6/cfl3dv6_testcases.html#delta)
* Experimental data: publically available
* Grids: not available
* Numerical results: publically available
* Case:
  * M = 0.3
  * Re = 0.5E6
  * AoA = 20.5 deg.


#### [DPW Series](https://aiaa-dpw.larc.nasa.gov/)

##### [DPW-1](https://aiaa-dpw.larc.nasa.gov/Workshop1/workshop1.html)
* Experimental data: publically available
* Grids: not available
* Numerical results: publically available
* Case:
  * M = 0.8395
  * Re = 11.72E6
  * AoA = 3.06 deg.

##### [DPW-2](https://aiaa-dpw.larc.nasa.gov/Workshop2/workshop2.html)
* 2nd AIAA CFD Drag Prediction Workshop
* Model: DLR-F6
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases (required):
  * Single point grid convergence study for wb and wbpn
    * M = 0.75
    * Re = 3E6 (c=141.2 mm)
    * CL = .500 ± .001
    * “Fully turbulent” solution
  * Drag Polar for wb and wbpn
    * M = 0.75
    * Re = 3E6 (c=141.2 mm)
    * AoA (deg.) = -3°, -2°, -1.5°, -1°,0°, 1°, 1.5°
    * Boundary layer transition or “fully turbulent”
* Cases (optional):
  * Comparison of “tripped” and “fully turbulent” solutions
    * M = 0.75
    * Re = 3E6 (c=141.2 mm)
    * CL = .500 ± .001
  * Drag rise for for wb and wbpn (very optional)
    * M = 0.50, 0.60, 0.70, 0.72, 0.74, 0.75, 0.76, 0.77
    * CL = 0.500 ± .001

##### [DPW-3](https://aiaa-dpw.larc.nasa.gov/Workshop3/workshop3.html)
* 3rd AIAA CFD Drag Prediction Workshop
* Model: DLR-F6
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases
  * DLR-F6 wb with and without FX2B fairing
    * For all cases
      * Re = 5E6 (cref = 141.2 mm)
      * T = 580R (322.22 K)
    * DLR-F6 wb with FX2B fairing and without fairing
      * Grid convergence study
        * M = 0.75
        * CL = 0.500 ±0.001
      * Drag polar (medium grid)
        * M = 0.75
        * AoA = -3, -2, -1, -0.5, 0, 0.5, 1, 1.5 deg.
  * Wing alone comparison: DPW-W1 (baseline) vs. DPW-W2 (simple optimization)
    * Re = 5E6 (cref = 197.556 mm)
    * T = 580R (322.22 K)
    * M = 0.76
    * Grid convergence
      * AoA = 0.5 deg.
    * Drag polar (medium grid)
      * AoA = -1, 0, 0.5, 1, 1.5, 2, 2.5, 3 deg.

##### [DPW-4](https://aiaa-dpw.larc.nasa.gov/Workshop4/workshop4.html)
* 4th AIAA CFD Drag Prediction Workshop
* Model: NASA Common Research Model (CRM)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases:
  * Grid convergence and downwash studies:
    * M=0.85
    * Re = 5E6 (cref = 275.80 in)
    * T = 100F
    * Grid convergence study
      * CL=0.500 ±0.001
    * Downwash study
      * Drag Polars for AoA = 0.0, 1.0, 1.5, 2.0, 2.5, 3.0, 4.0 deg.
      * Trimmed drag polar (cg at reference center) derived from polars at iH = -2, 0, +2 deg.
      * Delta drag polar of tail off vs. tail on (i.e. wb vs. wbh trimmed)
  * Mach sweep study (optional):
    * Re = 5E6 (cref = 275.80 in)
    * T = 100F
    * Drag Polars at M = 0.70, 0.75, 0.80, 0.83, 0.85, 0.86, 0.87
    * Drag rise curves at CL = 0.400, 0.450, 0.500 (±0.001 or extracted from polars)
  * Reynolds number study (optional):
    * Compare Re = 5E6 results with Re = 20E6 results (cref = 275.80 in)
    * M = 0.85
    * CL = 0.500 ±0.001
    * T = -250F (for Re = 20E6)

##### [DPW-5](https://aiaa-dpw.larc.nasa.gov/Workshop5/workshop5.html)
* 5th AIAA CFD Drag Prediction Workshop
* Model: NASA Common Research Model (CRM)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases:
  * Wing-body grid convergence study:
    * M = 0.85
    * CL = 0.500 ±0.001
    * Re = 5E6 (cref = 275.80 in)
    * T = 100F
    * Provided grid series (required)
    * Participant developed grids (optional)
  * Wing-body buffet study:
    * M = 0.85
    * Drag polar for AoA = 2.50, 2.75, 3.00, 3.25, 3.50, 3.75, 4.00 deg.
    * Re = 5E6 (cref = 275.80 in)
    * T = 100F

##### [DPW-6](https://aiaa-dpw.larc.nasa.gov/Workshop6/workshop6.html)
* 6th AIAA CFD Drag Prediction Workshop
* Model: NASA Common Research Model (CRM)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases:
  * M = 0.85
  * Re = 5E6
  * CL = 0.5 ±0.001

##### [DPW-7](https://aiaa-dpw.larc.nasa.gov/)
* 7th AIAA CFD Drag Prediction Workshop
* Model: NASA Common Research Model (CRM)
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* Cases:
  * Required
    * Case 1: Grid Convergence Study
    * Case 2: Alpha Sweeps at Constant Re
    * Case 3: Re Sweep at Constant CL
  * Optional
    * Case 4: Solution-Adapted Grid
    * Case 5: Beyond RANS: URANS, DDES, WMLES, Lattice-Boltzmann, etc.
    * Case 6: Coupled Aero-Structural Simulation



#### [HLPW Series](https://hiliftpw.larc.nasa.gov)

##### [HLPW-1](https://hiliftpw.larc.nasa.gov/index-workshop1.html)
* 1st AIAA CFD High Lift Prediction Workshop
* Model: NASA Trap Wing
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* [Cases](https://hiliftpw.larc.nasa.gov/Workshop1/testcases.html)

##### [HLPW-2](https://hiliftpw.larc.nasa.gov/index-workshop2.html)
* 2nd AIAA CFD High Lift Prediction Workshop
* Model: DLR F-11
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* [Cases](https://hiliftpw.larc.nasa.gov/Workshop2/testcases.html)

##### [HLPW-3](https://hiliftpw.larc.nasa.gov/index-workshop3.html)
* 3rd AIAA CFD High Lift Prediction Workshop
* Model: JAXA JSM
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* [Cases](https://hiliftpw.larc.nasa.gov/Workshop3/OfficialTestCases-HiLiftPW-3-2017_v9.pdf)

##### [HLPW-4](https://hiliftpw.larc.nasa.gov/)
* 4th AIAA CFD High Lift Prediction Workshop
* Model: NASA CRM-HL
* Experimental data: publically available
* Grids: publically available
* Numerical results: publically available
* [Cases](https://aiaa-dpw.larc.nasa.gov/Workshop6/DPW6_Test_Cases_2016-04-21.pdf)














