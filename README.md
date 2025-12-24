# MPC-Project
Optimal pacing in swimming competitions
Float Test Simulation — Optimal Pacing Project (Task 2) Overview This document describes the float test required in Project P1: Optimal Pacing in Swimming Competitions (Advanced Process Control). 
The float test validates the mechanical swimmer model by simulating passive motion under hydrodynamic drag without propulsion. 
Task Description The swimmer:- Starts with an initial velocity of 3 m/s- Has no fatigue-
Has a full alactacid energy system- 
Provides no propulsion force The goal is to: 
1. Simulate deceleration due to drag
2. 2. Compute floating distance until velocity reaches zero
   3.  Plot the velocity profile v(t) Model Description States: s(t) - distance v(t) - velocity Eal(t) - alactacid energy F(t) - fatigue Input: u(t) - propulsion force (set to zero) Dynamics: sdot = v vdot = -(1/2 * rho * cw * A * v^2) / m Ealdot = 0 Fdot = 0
Numerical Method The continuous-time system is simulated using a Runge–Kutta numerical integrator provided by CasADi with a fixed time step of 0.02 s.
Outputs- Floating time until v ≈ 0- Floating distance- Velocity decay plot Purpose
This test verifies the correctness of the drag model and numerical integration before applying MPC and orthogonal collocation.
