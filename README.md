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

A set of MATLAB solvers I developed individually to study numerical methods for fluid flow, covering incompressible potential flow, advection schemes, and compressible duct flow. Each solver is validated against an exact or analytical solution, with grid-convergence studies.

- **Potential Flow Over a Cylinder:** Solved the 2D Laplace equation for the stream function on a stretched polar mesh using sparse finite differences, demonstrating second-order convergence (max ψ error 9.9×10⁻³ → 1.6×10⁻⁴ over four mesh levels). Separated discretization error from domain-truncation error by deriving the finite-domain exact solution, and verified that full-cylinder pressure forces vanish to roundoff (d'Alembert's paradox).
- **Advection Schemes:** Implemented Trapezoidal and RK4 time integration with second-order central and fourth-order compact spatial schemes for 1D linear advection. Verified observed convergence orders of 2 for three pairings and 4 for RK4 + compact, and used Fourier analysis to show the errors are dispersion-dominated.
- **Compressible Duct Flow:** Built a Newton solver (finite-difference Jacobian) for adiabatic flow with wall friction, solving the forward problem (prescribed inlet Mach number) and the inverse problem (prescribed exit pressure). Validated against the analytic Fanno-flow solution (max error ~3×10⁻⁶ at 200 grid points), showed second-order grid convergence, and computed the choking limit (M₁ ≈ 0.509 for fL/D = 1).

<p align="center">
  <img src="images/cfd_cylinder_results.png" width="32%" />
  <img src="images/cfd_advection_convergence.png" width="32%" />
  <img src="images/cfd_duct_results.png" width="32%" />
</p>

*Left: stream function, velocity, and surface pressure coefficient for flow over a cylinder. Center: convergence of the four time/space scheme pairings (second- and fourth-order). Right: numerical duct-flow profiles against the analytic Fanno solution.*
