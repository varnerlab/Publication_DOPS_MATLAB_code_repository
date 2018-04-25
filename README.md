## DOPS

### Background ###
Mathematical modeling is a powerful tool to analyze, and ultimately design biochemical networks. However, the estimation of the parameters that appear in biochemical models is a significant challenge. Parameter estimation typically involves expensive function evaluations and noisy data, making it difficult to quickly obtain optimal solutions. Further, biochemical models often have many local extrema which further complicates parameter estimation. Toward these challenges, we developed Dynamic Optimization with Particle Swarms (DOPS), a novel hybrid meta-heuristic that combined multi-swarm particle swarm optimization with dynamically dimensioned search (DDS). DOPS uses a multi-swarm particle swarm optimization technique to generate candidate solution vectors, the best of which is then greedily updated using dynamically dimensioned search. 

The DOPS code is described in the publication: 
 
[Sagar, LeCover, Shoemaker and Varner (2018) Dynamic Optimization with Particle Swarms(DOPS): A meta-heuristic for parameterestimation in biochemical models https://www.biorxiv.org/content/early/2017/12/28/240580](https://www.biorxiv.org/content/early/2017/12/28/240580)

# How do I run DOPS?
The code to run DOPS is in DOPS_core, runForTable1.m will run DOPS on a variety of test functions. 

# How do I run msDOPS?
The code to run DOPS is in msDOPS_core, runForTable1_ms.m will run DOPS on a variety of test functions. 
