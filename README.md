# ME-Portfolio
This portfolio showcases my engineering projects, simulations, and applications of MATLAB, ANSYS, and numerical methods .

# Custom 2D Finite Element Analysis Program 
[Matlab FEA Project](https://github.com/phaylent/ME522_MatlabFEAProject.git)

A MATLAB-based 2D structural finite element analysis (FEA) application developed by a team of three over five weeks. The program supports geometry creation, mesh generation, boundary condition assignment, and stress and deformation visualization, with an auto-convergence solver for mesh refinement.

My primary contributions focused on boundary condition assignment, post-processing, and solver convergence.

- **Boundary Conditions:** Implemented functionality for assigning boundary conditions and applying loads to the model.
- **Post-Processing:** Developed visualization tools for displaying structural deformation and stress results along with calculations.
- **Auto-Convergence Solver:** Implemented an iterative mesh refinement process that continues until the specified error tolerance is met.

<p align="center">
  <img src="images/fea-bc-loading-view.png" width="48%" alt="BC and loading tab showing DXF geometry, mesh, and a traction load">
  <img src="images/fea-postprocessing-contours.png" width="48%" alt="Post-processing tab showing deformation and stress contours">
</p>
<p align="center">
  <em>Left: boundary condition and load assignment. Right: post-processing of deformation and stress.</em>
</p>

## Finite-Difference CFD Solvers in MATLAB

[numerical-fluids-matlab](https://github.com/phaylent/numerical-fluids-matlab)

A set of MATLAB solvers developed individually to study numerical methods for fluid flow. The projects cover incompressible potential flow, advection schemes, and compressible duct flow, with results validated against exact or analytical solutions where available.

Focused on discretization, solver implementation, and verification:

- **Potential Flow Over a Cylinder:** Solved the 2D Laplace equation for the stream function on a stretched polar mesh using sparse finite differences, matching the analytical solution to within 5×10⁻⁴. Post-processed velocity and pressure fields and showed surface pressure coefficient converging toward the exact result (minimum Cp from -2.62 to -2.97 vs. exact -3) with mesh refinement.
- **Advection Schemes:** Compared Trapezoidal and RK4 time integration with second-order central and fourth-order compact spatial schemes, quantifying dispersion and dissipation errors across grid sizes and time steps.
- **Compressible Duct Flow:** Implemented a Newton-based solver with a numerical Jacobian for frictional duct flow, solving both the forward problem (prescribed inlet Mach number) and the inverse problem (prescribed exit pressure), plus a parametric study of inlet Mach number vs. exit pressure.

<p align="center">
  <img src="images/cfd_cylinder_results.png" width="48%" />
  <img src="images/cfd_duct_results.png" width="48%" />
</p>

*Left: stream function, velocity field, and surface Cp compared with the exact potential-flow solution. Right: Mach number, pressure, density, and temperature along the duct.*


## Steady-State Thermal Analysis of a Heated Sphere

**Tools:** ANSYS Mechanical, MATLAB  
**Methods:** Thermal FEA, Analytical Heat Transfer, Numerical Validation

### Project Overview

Investigated steady-state heat conduction in a solid sphere with internal volumetric heat generation and heat transfer at the outer surface. Developed an analytical solution in MATLAB, modeled the sphere using a one-eighth symmetry model in ANSYS Mechanical, and implemented an independent one-dimensional finite element solution for comparison.

### Methodology

- **Analytical Solution:** Derived the radial temperature distribution using the governing spherical heat conduction equation and appropriate boundary conditions.
- **ANSYS Thermal FEA:** Created a one-eighth solid model, applied thermal loads and boundary conditions, and extracted the temperature distribution along a radial path.
- **MATLAB 1D FEA:** Implemented a five-element, one-dimensional heat conduction model by assembling the global stiffness matrix and forcing vector.
- **Numerical Validation:** Compared the analytical solution, ANSYS results, and MATLAB finite element solution to evaluate agreement between the methods.

### Results

The ANSYS model produced the following temperatures:

| Location | Temperature |
|---|---:|
| Sphere center | 407.67 K |
| Outer surface | 392.06 K |
| Temperature difference | 15.61 K |

**Temperature Distribution Comparison**

![Temperature distribution comparison](images/temperature_comparison.png)

**ANSYS Temperature Contour**

![ANSYS temperature contour](images/temperature_contour.png)

### Engineering Relevance

This project demonstrates thermal modeling techniques relevant to aerospace structures and thermal protection analysis, including heat conduction, volumetric heat generation, surface heat transfer, and numerical validation.

The model represents a simplified heated sphere rather than a complete atmospheric re-entry simulation; it does not directly model aerodynamic heating or transient re-entry conditions.

### Skills Demonstrated

- ANSYS Mechanical thermal analysis
- MATLAB numerical modeling
- Analytical heat transfer
- One-dimensional and three-dimensional finite element analysis
- Thermal boundary conditions and symmetry modeling
- Numerical solution comparison and validation
