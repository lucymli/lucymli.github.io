---
layout: page
title: Projects
permalink: /projects/
---

## R package: EpiGenR

This R package allows users to process phylogenetic data and interface with the [EpiGenMCMC](https://github.com/lucymli/EpiGenMCMC) (discussed in the next section).

Some functions include:

- coal.intervals.in.discrete.time(), which converts phylogenetic trees into time-series data (needed for statistical inference using PMCMC)
- generate_cpp_input_files() produces the files needed to run the EpiGenMCMC program
- generate.MrBayes.input(), which creates the input file used in MrBayes, a phylogenetic tree reconstruction program
- Phylos2Skyline() generates an 'average skyline' plot based on a posterior distribution of phylogenetic trees inferred from genetic data

Link to code on [Github](https://github.com/lucymli/EpiGenR). 

## Particle Markov chain Monte Carlo (PMCMC)

Parameters important for summarizing infectious disease spread in the population are not usually directly observation, e.g. rates of transmission. Fitting to time-series data where the case reports are aggregated at the daily/weekly/monthly level provides an indirect way to infer the values of these parameters. Particle Markov chain Monte Carlo enables this type of inference, while accounting for the inherently stochastic nature of infection spread. 

In this project, I developed a statistic inference framework that uses both genetic data (in the form of phylogenetic trees) and time-series (number of confirmed cases on each day). The framework was implemented in C++ (available as the 'EpiGenMCMC' program on [Github](https://github.com/lucymli/EpiGenMCMC)).

This [paper](https://academic.oup.com/mbe/article/doi/10.1093/molbev/msx195/3952784/Quantifying-transmission-heterogeneity-using-both?guestAccessKey=1853723e-23a7-4a02-be30-f6710e1d177a) written by me, Prof Grassly, and Prof Fraser details the theory behind PMCMC and application to both simulated and real data.



## Poliovirus surveillance


