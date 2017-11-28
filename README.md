# FinalCode
Final Code for Numerics Corse Work
This folder contains the code for the 29th of November deadline of the Numerics assignment .

In file main_LinearAdvection.py there is the main code for the Linear Advection equation problem. The main calls all the numerical schemes and the numerical tests I have implemented. I have selected some choice of the parameters (grid, steps,Courant number, type of initial condition) to show how my code behaves. In the final report I will probably include more plots for different choice of the parameters.  
Firstly, the main calls four numerical methods (FTBS, CTCS, CNCS and Lax Wendroff) for 
for two different initial conditions (cosBell and square wave functions), two different grid meshes and time steps, and plots the results.
Secondly, after defining a new set up for the grid , time steps and Courant number, the main calls the functions to calculate the Mass and Variance of the numerical solutions  each time step, and plots the result for M and V respectively. 
Thirdly, the main calls a function that compute the l-2 norm error for the schemes, for different number of grid points, keeping C constant. 

Grid.py sets up the 1-d space grid, provided number of grid points and total light.

InitialConditions.py sets up a profile on a grid, you can choose a cosBell function or a square wave function.

Analytical.py computes the anlytical solution of the linear advection, given an initial condition type, the Courant number and the time steps.

AdvectionSchemes.py contains all the implemented schemes: FTBS, CTCS, CNCS and LaxWendroff. They advect a given initial profile using a proided C and timesteps. It also include a function that runs all the schemes together.

Errors.py contains functions that computes the l_2 norm and the l_infinity norm errors given a numerical solution and the analytical; also contains a function that computes the error for all schemes and different grid resolutions.

MassVariance.py computes mass and variance of a profile defined on a grid of space step dx. Contains also a function that computes the mass and variance as function of time for all schemes.

Plot.py contains three functions: plot of schemes and analytical solution after tsteps; plot of errors vs grid mesh; plot of Mass or Variance in time .