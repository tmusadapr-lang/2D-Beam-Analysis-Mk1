[2D Beam Analysis README.md](https://github.com/user-attachments/files/35132494/2D.Beam.Analysis.README.md)
# 2D Beam Analysis

**2D Beam Analysis** is an interactive, browser-based structural engineering application for analyzing two-dimensional linear-elastic beams. Powered by numerical finite element matrix techniques (the direct stiffness method), it solves statically determinate and indeterminate beam systems while generating the exact closed-form piecewise analytical equations that describe the evaluated internal forces, slopes, and deflections.

## Table of Contents

* [Overview](#overview)
* [Key Features](#key-features)
  * [Beam, Material & Unit Controls](#beam-material--unit-controls)
  * [Cross-Section Library](#cross-section-library)
  * [Supports & Loading Conditions](#supports--loading-conditions)
  * [Interactive Schematic & Internal Force Diagrams](#interactive-schematic--internal-force-diagrams)
  * [Stress & Failure Analysis](#stress--failure-analysis)
  * [Verification, Reporting & UI Themes](#verification-reporting--ui-themes)
* [Workflow](#workflow)
* [Methodology & Accuracy](#methodology--accuracy)
* [Future Work](#future-work)
* [License](#license)

## Overview

Evaluating beam behavior often requires switching between hand calculations, spreadsheets, and heavyweight finite element packages. **2D Beam Analysis** bridges the gap between numerical solvers and textbook hand calculations—using matrix-based numerical methods to solve arbitrary support and load configurations while presenting users with the exact closed-form equations governing every span segment, alongside stress diagnostics and automated report generation.

## Key Features

### Beam, Material & Unit Controls

* **Geometry & Material Properties:** Configure total beam length, elastic modulus ($E$), yield and ultimate strengths ($S_y$, $S_{ut}$, $S_{uc}$), and material density ($\rho$).
* **Built-In Material Presets:** Quickly select from standard engineering materials—including structural steels, stainless steel 304, aluminium 6061-T6, and cast iron—or define custom material properties.
* **Per-Field Unit Conversion:** Switch seamlessly between metric and imperial units on an individual per-field basis.
* **Preloaded Examples:** Explore and modify 8 built-in example beams covering common structural configurations.

### Cross-Section Library

* **Standard & Custom Profiles:** Model I-sections, C-sections, solid rectangles, rectangular hollow sections (RHS), solid rounds, round tubes, or enter custom geometric properties directly.
* **Live Dimensioned Preview:** View an automatically updated, dimensioned cross-section drawing as dimensions change.
* **Automated Section Properties:** Automatically computes cross-sectional area ($A$), second moment of area ($I$), section modulus ($Z$), and flexural rigidity ($EI$).

### Supports & Loading Conditions

* **Flexible Boundary Conditions:** Place standard **Pin**, **Roller**, and **Fixed** supports, or configure custom degree-of-freedom restraints ($U_x$, $U_y$, $R_z$).
* **Comprehensive Load Types:** Apply inclined point forces, uniform or trapezoidal distributed loads, and concentrated bending moments anywhere along the span.
* **Automatic Self-Weight:** Toggle automatic gravitational self-weight loading ($\rho g A$) derived from section area and material density.

### Interactive Schematic & Internal Force Diagrams

* **Interactive Beam Canvas:** Inspect the structural model with smooth zoom and pan controls, hover value readouts, and an optional scaled deflected-shape overlay.
* **Diagrams & Closed-Form Piecewise Equations:** Generate high-precision plots alongside exact closed-form analytical expressions for every evaluated segment:
  * Shear Force ($V(x)$)
  * Bending Moment ($M(x)$)
  * Slope ($\theta(x)$)
  * Deflection ($v(x)$)
  * Axial Force ($N(x)$)
  * Static self-weight deflection

### Stress & Failure Analysis

* **Through-Depth Stress Profiles:** Inspect normal bending/axial stress ($\sigma_x$) and transverse shear stress ($\tau_{xy}$) distributions across the cross-section depth.
* **2D & 3D Stress Visualization:** Examine 2D stress elements (standard orientation, principal stresses, and maximum in-plane shear) alongside an interactive 3D stress cube.
* **Multi-Theory Safety Factor Checks:** Evaluate structural safety factors across five classical failure theories:
  1. von Mises (Distortion Energy)
  2. Tresca (Maximum Shear Stress)
  3. Maximum Normal Stress
  4. Coulomb-Mohr
  5. Modified Mohr

### Verification, Reporting & UI Themes

* **Benchmark Verification:** Compare numerical solver outputs directly against closed-form textbook solutions.
* **Multi-Format Export:** Export individual plots and schematics as **SVG**, **PNG**, or **JPEG** files.
* **Automated Word Reports:** Generate a formatted Microsoft Word (`.docx`) engineering report complete with embedded diagrams, calculation summaries, and technical appendices.
* **Customizable Interface:** Choose from **21 visual UI themes** to suit your workspace preferences.

## Workflow

1. **Define Geometry & Material:** Set the beam span, choose a material preset (or enter custom $E$, $S_y$, $S_{ut}$, $S_{uc}$, and $\rho$ values), and select preferred units.
2. **Select Cross-Section:** Pick a profile from the cross-section library and verify $A$, $I$, $Z$, and $EI$ in the live dimensioned preview.
3. **Apply Supports & Loads:** Add boundary restraints ($U_x$, $U_y$, $R_z$) and external loads (point forces, distributed loads, moments, and optional self-weight).
4. **Analyze Diagrams, Equations & Stresses:** Inspect $V(x)$, $M(x)$, $\theta(x)$, $v(x)$, and $N(x)$ diagrams and their closed-form piecewise equations, evaluate $\sigma_x$ and $\tau_{xy}$ profiles, and review safety factors across all five failure theories.
5. **Verify & Export:** Cross-check results against built-in analytical benchmarks and export figures or a complete `.docx` engineering report.

## Methodology & Accuracy

* **Numerical Solver Core:** The structural engine uses the **Direct Stiffness Method** (a matrix-based numerical finite element formulation), assembling global stiffness matrices ($\mathbf{K}\mathbf{u} = \mathbf{F}$) from two-node Euler-Bernoulli Hermite beam elements for bending and uncoupled two-node bar elements for axial deformation. This enables rapid numerical solution of both statically determinate and indeterminate beams.
* **Closed-Form Analytical Reconstruction:** Once nodal displacements, rotations, and support reactions are solved numerically, the application integrates the governing differential equations across each discontinuity interval to output the exact **closed-form piecewise polynomial equations** for $V(x)$, $M(x)$, $\theta(x)$, $v(x)$, and $N(x)$.
* **Benchmark Validation:** Built-in verification cases validate numerical and symbolic outputs against classical closed-form textbook solutions.

## Future Work

* **3D Structural Analysis Version:** Extend the solver and interactive viewport into a full **3D version** supporting three-dimensional beams and space frames, six degrees of freedom per node ($U_x, U_y, U_z, R_x, R_y, R_z$), biaxial bending ($M_y, M_z$), and torsional shear ($T$).

## License

