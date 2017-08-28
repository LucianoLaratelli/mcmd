# MCMD
This is a Monte Carlo / Molecular Dynamics Simulation software used primarily for gas sorption in crystalline materials. 

# Quick start:
On HPC clusters, you may need to load a compiler module first:  <br />
&emsp;-> `module load compilers/gcc/6.2.0` (circe)  <br />
&emsp;-> `module load gcc/6.3.0` (bridges) <br />
1) Download: <br />
`git clone https://github.com/khavernathy/mcmd` <br />

2) Compile: <br />
`cd mcmd` <br />
`cd src` <br />
`bash compile.sh   [ options ]` <br />
`cd ..` <br />

3) Run: <br />
`./mcmd mcmd.inp`<br /><br />  
  
# Update
`cd mcmd` <br />
`git pull` <br />
`cd src` <br />
`bash compile.sh   [ options ]` <br />

# Advanced compilation
Take a look at mcmd/src/compile.sh for different options in compilation (OS-specific, CUDA implementation, OpenMP, optimization on different HPC systems, etc.)

<hr />

# Contact
Douglas Franz: dfranz@mail.usf.edu

# Features
&emsp;-> Monte Carlo simulation in NPT, NVT, NVE, and &mu;VT ensembles.  <br />
&emsp;-> Molecular Dynamics simulation in NVT, NVE, and &mu;VT ensembles.  <br />
&emsp;-> A crystal builder to create fully parameterized supercells from unit cells. <br />
&emsp;-> A fragment creator based around uniquely named atoms. <br /> 
&emsp;-> A LAMMPS input file exporter. <br />
&emsp;-> Trajectories and restart files in various formats. <br />
&emsp;-> Automatic radial distribution calculator<br />
&emsp;-> Hard-coded molecular models for easy input, including multi-sorbate support<br />
&emsp;-> Easy system basis parametrization via a, b, c, &alpha;, &beta;, &gamma; crystal values, or basis vectors<br />
&emsp;-> Quick routines for energy/force computation<br />
&emsp;-> Simulated annealing<br />
&emsp;-> Any periodic cell is supported for both MC and MD; non-periodic systems also supported.<br />
&emsp;-> Force-fields available are Lennard-Jones (12-6), Ewald electrostatics, and Thole-Applequist polarization.<br />
&emsp;-> Sample inputs are included. The program takes just one argument: the input file (which itself usually points to a file containing starting atoms).<br />

# What can be obtained from this software
The program outputs several quantities of interest:<br />
&emsp;->Uptake of sorbates in wt%, reduced wt%, cm^3/g, mmol/g and mg/g<br />
&emsp;->Excess adsorption ratio in mg/g<br />
&emsp;->Selectivities for multi-sorbate simulation<br />
&emsp;->Qst (heat of sorption) for sorbate<br />
&emsp;->Sorbate occupation about some site/atom (g(r))<br />
&emsp;->Diffusion coefficient and specific heat<br />
&emsp;->Trajectory and restart files to easily pickup a halted job and visualize simulation<br />
&emsp;->3D histogram data for visualization of sorbate occupation in a material (density visualization).<br />
&emsp;->Induced dipole strengths for polarization simulations<br />

# Operating System requirements
MCMD works out-of-the-box on <br />
&emsp;-> Linux (tested on Ubuntu 16.04)<br />
&emsp;-> Mac (tested on OS X El Capitan v10.11.6)<br />
&emsp;-> Windows (tested using Cygwin and Windows 7 with gcc 5.4.0 installed)<br />
&emsp;-> Raspberry Pi (3, using Raspian OS).<br /><br />
We recommend Visual Molecular Dynamics (VMD) for data visualization, but the output is compatible with most other software, e.g. Avogadro, Molden, Ovito, etc.<br />

<!--
# TODO
-->
