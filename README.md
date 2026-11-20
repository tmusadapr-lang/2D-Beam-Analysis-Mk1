# 2D Beam Analysis

**2D Beam Analysis** is an interactive, browser-based structural engineering application for analyzing two-dimensional linear-elastic beams. Built around the direct stiffness method, it combines two-node Euler-Bernoulli Hermite beam elements for bending with uncoupled two-node bar elements for axial loading to deliver rapid, verifiable structural calculations and visual diagnostics directly in the browser.

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
  - [Beam, Material & Unit Controls](#beam-material--unit-controls)
  - [Cross-Section Library](#cross-section-library)
  - [Supports & Loading Conditions](#supports--loading-conditions)
  - [Interactive Schematic & Internal Force Diagrams](#interactive-schematic--internal-force-diagrams)
  - [Stress & Failure Analysis](#stress--failure-analysis)
  - [Verification, Reporting & UI Themes](#verification-reporting--ui-themes)
- [Workflow](#workflow)
- [Verification & Accuracy](#verification--accuracy)
- [License](#license)

---

## Overview

Evaluating beam behavior often requires switching between hand calculations, spreadsheets, and heavyweight finite element packages. **2D Beam Analysis** streamlines structural modeling, internal force evaluation, cross-sectional stress analysis, failure criteria checks, and report generation into a single self-contained web workspace.

---

## Key Features

### Beam, Material & Unit Controls
- **Geometry & Material Properties:** Configure total beam length, elastic modulus ($E$), yield and ultimate strengths ($S_y$, $S_{ut}$, $S_{uc}$), and material density ($\rho$).
- **Built-In Material Presets:** Quickly select from standard engineering materials—including structural steels, stainless steel 304, aluminium 6061-T6, and cast iron—or define custom material properties.
- **Per-Field Unit Conversion:** Switch seamlessly between metric and imperial units on an individual per-field basis.
- **Preloaded Examples:** Explore and modify 8 built-in example beams covering common structural configurations.

### Cross-Section Library
- **Standard & Custom Profiles:** Model I-sections, C-sections, solid rectangles, rectangular hollow sections (RHS), solid rounds, round tubes, or enter custom geometric properties directly.
- **Live Dimensioned Preview:** View an automatically updated, dimensioned cross-section drawing as dimensions change.
- **Automated Section Properties:** Automatically computes cross-sectional area ($A$), second moment of area ($I$), section modulus ($Z$), and flexural rigidity ($EI$).

### Supports & Loading Conditions
- **Flexible Boundary Conditions:** Place standard **Pin**, **Roller**, and **Fixed** supports, or configure custom degree-of-freedom restraints ($U_x$, $U_y$, $R_z$).
- **Comprehensive Load Types:** Apply inclined point forces, uniform or trapezoidal distributed loads, and concentrated bending moments anywhere along the span.
- **Automatic Self-Weight:** Toggle automatic gravitational self-weight loading ($\rho g A$) derived from section area and material density.

### Interactive Schematic & Internal Force Diagrams
- **Interactive Beam Canvas:** Inspect the structural model with smooth zoom and pan controls, hover value readouts, and an optional scaled deflected-shape overlay.
- **Diagrams & Piecewise Equations:** Generate high-precision plots alongside exact piecewise analytical equations for:
  - Shear Force ($V$)
  - Bending Moment ($M$)
  - Slope ($\theta$)
  - Deflection ($v$)
  - Axial Force ($N$)
  - Static self-weight deflection

### Stress & Failure Analysis
- **Through-Depth Stress Profiles:** Inspect normal bending/axial stress ($\sigma_x$) and transverse shear stress ($\tau_{xy}$) distributions across the cross-section depth.
- **2D & 3D Stress Visualization:** Examine 2D stress elements (standard orientation, principal stresses, and maximum in-plane shear) alongside an interactive 3D stress cube.
- **Multi-Theory Safety Factor Checks:** Evaluate structural safety factors across five classical failure theories:
  1. von Mises (Distortion Energy)
  2. Tresca (Maximum Shear Stress)
  3. Maximum Normal Stress
  4. Coulomb-Mohr
  5. Modified Mohr

### Verification, Reporting & UI Themes
- **Benchmark Verification:** Compare numerical solver outputs directly against closed-form textbook solutions.
- **Multi-Format Export:** Export individual plots and schematics as **SVG**, **PNG**, or **JPEG** files.
- **Automated Word Reports:** Generate a formatted Microsoft Word (`.docx`) engineering report complete with embedded diagrams, calculation summaries, and technical appendices.
- **Customizable Interface:** Choose from **21 visual UI themes** to suit your workspace preferences.

---

## Workflow

1. **Define Geometry & Material:** Set the beam span, choose a material preset (or enter custom $E$, $S_y$, $S_{ut}$, $S_{uc}$, and $\rho$ values), and select preferred units.
2. **Select Cross-Section:** Pick a profile from the cross-section library and verify $A$, $I$, $Z$, and $EI$ in the live dimensioned preview.
3. **Apply Supports & Loads:** Add boundary restraints ($U_x$, $U_y$, $R_z$) and external loads (point forces, distributed loads, moments, and optional self-weight).
4. **Analyze Diagrams & Stresses:** Inspect $V$, $M$, $\theta$, $v$, and $N$ diagrams, evaluate $\sigma_x$ and $\tau_{xy}$ profiles, and review safety factors across all five failure theories.
5. **Verify & Export:** Cross-check results against built-in analytical benchmarks and export figures or a complete `.docx` engineering report.

---

## Verification & Accuracy

The solver implements the direct stiffness method using two-node Euler-Bernoulli Hermite elements for transverse bending and uncoupled two-node bar elements for axial deformation. Built-in verification cases allow users to validate solver accuracy against closed-form analytical solutions for standard statically determinate and indeterminate beam problems.

---

## License

