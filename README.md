## Table of Contents
- [**Introduction**](https://github.com/ACM40960/project-Ellen_Bennett#introduction)
- [**Installation Instructions**](https://github.com/ACM40960/project-Ellen_Bennett#installation-instructions)
  - [Mathematica](https://github.com/ACM40960/project-Ellen_Bennett#mathematica)
  - [R](https://github.com/ACM40960/project-Ellen_Bennett#r)
- [**Running Code**](https://github.com/ACM40960/project-Ellen_Bennett#running-code)
  - [Mathematica Notebook](https://github.com/ACM40960/project-Ellen_Bennett#mathematica-notebook)
  - [R Script](https://github.com/ACM40960/project-Ellen_Bennett#r-script)
## Introduction

   The aim of this project is to estimate Pi using a variety of techniques with the ultimate goal of finding an optimal method. In total, nine different methods were trialed, eight of which involved Monte Carlo Simulation. Four of these methods were simulated using **Wolfram Mathematica 13.0**, while the rest were performed in **R**.
   
   One such method is demonstrated visually below. By dropping many random points on the square and counting the proportion landing inside the quarter circle, one can esimate Pi by multiplying this proportion by four. This is because the true proportion of the total area this region covers is Pi/4.
   
   This README file will detail how to run code to reproduce the results of each of the simulation techniques. First install annd download relevant softwares and scripts via "Installation Instructions" before reading the "Running Code" section.
  
   <img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/gif_of_quadrant_method.gif" width="300" height="275"/>

## Installation Instructions

### Mathematica

The notebook was created using **Wolfram Mathematica 13.0**, which can be installed by following these [**instructions**](https://reference.wolfram.com/language/tutorial/InstallingMathematica.html).

The ZIP file containing the notebook can be downloaded by clicking on the green ***Code*** button at the top of the project, and then selecting ***Download ZIP***.

<img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/download_code.png" width = "500"/>

Once the notebook has been downloaded it can be opened on your computer by running the *Wolfram Mathematica* program, and clicking the ***Open...*** icon. 

<img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/mathematica_menu.png" width = "500"/>

The notebook is divided into seven sections, each of which is split into various subsections. Sections can be expanded by clicking on the orange arrow icon at the right hand side of the section title. 

  <img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/notebook_layout.png" width = "500" />

The first four sections contain code pertaining to their relevant simulation method, and the last three contain code that was used to obtain plots included in the *LaTeX* document. 

It is advised not to run the entire notebook due to its run time, and instead to consult this [**guide**](https://github.com/ACM40960/project-Ellen_Bennett#mathematica-notebook).
  
  
  
### R

***"R is a programming language for statistical computing and graphics"***

It be installed freely via the following link: *https://cran.ma.imperial.ac.uk/*
R Studio is a great IDE that was used to write the code in and can be downloaded here: *https://www.rstudio.com/products/rstudio/download/*

Note that only base R functionality was used and no further packages need to be installed!

Again, The ZIP file containing all project items (including the R script) can be downloaded by clicking on the green ***Code*** button, and selecting ***Download ZIP***.

Once the script has been downloaded, it can be opened on your computer by right clicking the file, and clicking ***Open with > R Studio***. 

<img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/Open_R_Script.png" width = "500" />



## Running Code

**Note:** There is no external data sources required for this project. All data is generated using random number generators in Mathematica and R.

There is a single Mathematica notebook called *Estimating_Pi.nb* to run four of the methods. Five are then ran using the R script *Estimating_Pi.R*. An additional R script called *Convergence_Analysis.R* then runs code to determine the convergence of each method with the aim of finding an optimal few. A final R script called *Computation_Time_Analysis.R* is finally used to compare the computation time of the best method(s) from previous analysis.


### Mathematica Notebook

The Mathematica notebook *Estimating_Pi.nb* in folder *Mathematica Code* contains code to run the following four simulations methods:
1. Archimedes' Method
2. Quadrant Method
3. Gamma Function Integral
4. Gregory-Leibniz Series.

This is a guide to running this notebook. Certain subsections take up to 30 minutes to run, so it is **NOT** advised to run the entire notebook. Any section with a long running time includes a warning sign at the beginning of the code to inform the user. 

Sections 1 to 4 each feature a function that demonstrates the simulation method to the user. These have relatively very short running times and are recommended to use. 

The titles of the subsections containing these functions are:

- ***1.1. Archimedes' Method*** - *Illustrating the Approximation Method Using a Manipulate Function*
- ***2.2. Quadrant Method*** - *Demonstrate the Method Using a Manipulate Function*
- ***3.1. Gamma Function Integral Method*** - *Function to Demonstrate Method*
- ***4.1. Gregory-Leibniz Series Method*** - *Function to Demonstrate Method*

<img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/functions.png" width = "500" />

Sections 5 to 7 contain code that was used to create error plots, relative difference plots, and convergence plots for the project. By default the code is set to produce plots of the **Gamma Function Integral Method**, as its Monte Carlo Simulations take the shortest amount of time to run (5 minutes).

### R Script

#### Estimating_Pi.R

The R script *Estimating_Pi.R* in the folder *R Code* contains the code to run the following five different monte carlo simulation methods:

1. Buffon's Experiment
2. Quarter Circle Integral
3. Bernoulli Numbers Generating Function Integral
4. Standard Normal Distribution Integral
5. Coin Toss on Grid

This is a guide to running the R script which can simulate Pi using each of the 5 associated methods. 
Each method should be ran individually and has a runtime of no longer than 5 minutes.

To run a section, simply highlight all code from the top to the bottom of the section and run.
Note: The start and end of each section are clearly commented for convenience (See below):

After running each section, you will generate the convergence plots of the mean estimate of Pi and the associated confidence interval at specific time points as shown in the picture. You can then also retrieve the numeric estimates by running `N_pi_est_{insert question letter here}` for example `N_pi_est_b`.

<p float="left">
<img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/How_To_Run_R_Script_1.png" width = "450" height = "300" />
<img src="https://github.com/ACM40960/project-Ellen_Bennett/blob/main/images/How_To_Run_R_Script_2.png" width = "450" height = "300"/>
</p>

#### Convergence_Analysis.R

#### Computation_Time_Analysis.R

