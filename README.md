# Group Knockoff Reproducibility

This repo contains scripts to reproduce the simulated and real data experiments of the group knockoff paper. All scripts are provided as individual jupyter notebooks, which can be viewed directly in the web browser. To execute the scripts, one can do so directly within jupyter notebooks, or copy the code into the Julia REPL. 

## Software versions

We developed a number of softwares to enable group knockoff simulation and analysis. Installing these Julia packages will automatically install the relevant Julia dependencies.

+ `Knockoffs.jl` (v1.1.1): https://github.com/biona001/Knockoffs.jl
+ `EasyLD.jl` (pre-release): https://github.com/biona001/EasyLD.jl
+ `GhostKnockoffGWAS.jl` (pre-release): https://github.com/biona001/GhostKnockoffGWAS

For the real-data analysis, we also used 

+ `ghostbasil` (v0.1.3, currently NOT publicaly available): https://github.com/JamesYang007/ghostbasil
+ `liftOver` (v1.14.0): https://bioconductor.org/packages/release/workflows/html/liftOver.html

We used `Julia` v1.8.4 and `R` v4.0.2 for all analyses. 

## Simulated experiments

All scripts (including scripts to make figures) are available in jupyter notebooks starting with `compare`. Note, figure 1 is a combination of 5 simulations, where the simulations are provided in standalone notebooks (e.g. `compare_group_knockoff_AR1.ipynb`), while the figure is generated in `compare_group_knockoff_figure1.ipynb`. 

## Albuminuria GWAS

The analysis is conducted in several steps

+ `ghostknockoff-part0.ipynb`: Downloads the Pan-UKB LD matrices 
+ `ghostknockoff-part1.ipynb`: Reads the downloaded LD matrices and solves the knockoff optimization problem across 1703 genomic regions 
+ `ghostknockoff-part2.ipynb`: Reads Albuminuria Z-scores, generates knockoff Z-scores, and performs knockoff filter
+ `ghostknockoff-manhattan.ipynb`: Creates the Manhattan plot as featured in our paper

## Questions?

If anything is unclear, or you cannot reproduce our results, please file an issue on GitHub and I will take a look at it asap. You can also reach me at `bbchu@stanford.edu`.

