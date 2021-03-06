## DOPS

### Background ###
Mathematical modeling is a powerful tool to analyze, and ultimately design biochemical networks. However, the estimation of the parameters that appear in biochemical models is a significant challenge. Parameter estimation typically involves expensive function evaluations and noisy data, making it difficult to quickly obtain optimal solutions. Further, biochemical models often have many local extrema which further complicates parameter estimation. Toward these challenges, we developed Dynamic Optimization with Particle Swarms (DOPS), a novel hybrid meta-heuristic that combined multi-swarm particle swarm optimization with dynamically dimensioned search (DDS). DOPS uses a multi-swarm particle swarm optimization technique to generate candidate solution vectors, the best of which is then greedily updated using dynamically dimensioned search. 

The DOPS code is described in the publication: 
 
[Sagar, LeCover, Shoemaker and Varner (2018) Dynamic Optimization with Particle Swarms(DOPS): A meta-heuristic for parameter estimation in biochemical models https://www.biorxiv.org/content/early/2017/12/28/240580](https://www.biorxiv.org/content/early/2017/12/28/240580)

### Installation and Requirements ###
You can download this repository as a zip file, or `clone`/`pull` it by using the command (from the command-line):

	$ git pull https://github.com/varnerlab/Publication_DOPS_MATLAB_code_repository.git

or

	$ git clone https://github.com/varnerlab/Publication_DOPS_MATLAB_code_repository.git

This code is written in Matlab, and requires Matlab or an equivalent (Octave) to run.

# How do I run DOPS? #
First, you need to ensure that the files in DOPS_core have been added to Matlab's path. Then, you will need to create output directories-results will be written to ../DOPS_Results/my_function, which you need to create. 

The code to run DOPS is in DOPS_core, runForTable1.m will run DOPS on a variety of test functions. To run DOPS on your own function, call run_DOPS(@my_function, lower_bounds, upper_bounds, lowerIter, upperIter), where my_function takes in a vector of parameters and returns a floating point number. Lower_bounds and upper_bounds must have the same dimensions, and lowerIter and upperIter are integers describing how many iterations of DOPS will be run. 

# How do I run msDOPS? #
Then, you will need to create output directories-results will be written to ../DOPS_Results/ms/my_function, which you need to create. 

First, you need to ensure that the files in msDOPS_core have been added to Matlab's path. 
The code to run DOPS is in msDOPS_core, runForTable1_ms.m will run DOPS on a variety of test functions. To run msDOPS on your own function, call run_msDOPS(@my_function, lower_bounds, upper_bounds, lowerIter, upperIter), where my_function takes in a vector of parameters and returns a floating point number. Lower_bounds and upper_bounds must have the same dimensions, and lowerIter and upperIter are integers describing how many iterations of msDOPS will be run. 

# How do I view my results? #
j = interation number  
DOPS_solution_iterj.mat contains the best solution vector from swarm search.  
DOPS_particlej.mat contains the particle matrix - contains particle states for every iteration within the trial.  
DOPS_fitnessj.mat contains the fitness matrix - contains fitness states for the corresponding particle matrix.  
DOPS_time_iterj.txt - contains the run time.  
DDSPSO_strategy1_5_swarms_results_DDSPSO_strategy1_errordds_iterj.mat - contains the best fitness value from DDS search.  
DDSPSO_strategy1_5_swarms_results_DDSPSO_strategy1_particledds_iterj.mat - contains the best solution vector from DDS search.  
