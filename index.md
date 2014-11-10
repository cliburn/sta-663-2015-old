STA 663: Statistical Computing and Computation
===========================

### Pretest

Try the [pretest](pretest.html) - if you are not familiar with at least 75-100% of the material, you may not be ready for this class.

### Overview

Most of science, including statistics, revolves around the design of models to represent data of some sort. In statistics, these models are typically probability distributions with parameters to estimate. The typical stages of analysis goes something like this:

1. Data management 
    1. Receive possibly messy and bad data
    2. Clean and filter the data 
2. Exploratory data analysis
    1. Describe and visualize the data to come up with possible models
3. Statistical inference
    1. Estimate model parameters given data (Model estimation and selection)
    2. Make predictions with model (Model prediction)
4. Reporting

In today's context, statisticians will be doing all three stages in front of a computer. We believe that modern analysis of massive data sets is best achieved using a combination of complementary software tools, and the course will cover what we consider to be an essential toolkit comprising `bash`, `git`, `make`, `sqlite3`, `python`, `R`, `C` and `LaTeX`. We use Python as the computational "glue" that integrates these collection of tools, and also in its capacity as an efficient high-level language for scientific and statistical computing.

To deal with the massive data sets that you will encounter in your career, the course will emphasize reproducible analysis, code optimization, high-performance computing and cloud computing. Examples will be drawn from the core topics in computational statistics of optimization (e.g. smoothing, interpolation, maximum likelihood, constrained and unconstrained methods) and simulation (e.g. jackknife, bootstrap, permutation, Monte Carlo integrals, MCMC).

At the end of the course, these are the practical skills (Units 1-6) every student should learn:

1. How to set up a reproducible analysis pipeline using bash, git, make and LaTeX
2. How to clean, manage and manipulate huge data sets using text processing, relational databases
3. How to explore data sets interactively using the IPython notebook and visualization packages
4. How to code statistical routines efficiently in high level languages 
5. How to optimize statistical routines by compiling to native code
6. How to compute in parallel on multi-core machines, clusters and GPUs

In particular, students should be able to write readable, well-documented, efficient (and if necessary parallel) code to implement a statistical method described in a textbook or paper, and apply it to real-world, possibly messy, data sets.

### Unit 1: Python bootcamp and setting up a reproducible analysis pipeline (10%)
* Setting up workspace and introduction to bash
* Version control with git
* Document generation with LaTeX
* Automating the pipeline with make
* Introduction to Python and the IPython notebook
* Testing and debugging

**Sample Exercise**: Create a git repository on Github for this project. Write a makefile to automate generation of a LaTeX report with embedded R and Python results. Ensure that git commits are performed regularly and well-documented.

**Sample Exercise**: You are given a Python program that has errors. Fix it.

**Sample Exercise**: Write functions to calculate the mean, median and variance of a set of numbers using test-driven development.

### Unit 2: Data manipulation and munging (10%)
* Reading and writing data
* Text processing and regular expressions
* Querying a relational database with SQL
* Database design for statisticians

**Sample Exercise**: You are given a data set that needs to be cleaned and reformatted into a data frame.

**Sample Exercise**: Given an SQLite3 database, use SQL to answer some questions and extract data subsets.

**Sample Exercise**: Given a spreadsheet, design a normalized database to manage the data. Transfer the data from the spreadsheet into the database.

### Unit 3: Exploratory data analysis and visualization (10%)
* Manipulating data in a DataFrame
* Visualizing data with matplotlib
* Grammar of graphics with ggplot and bokeh
* Animation - Metropolis, Gibbs and Hamiltonian sampling

**Sample Exercise**: Load a dataset into a DataFrame and use joins and the split-apply-combine pattern to answer some quesiotns.

**Sample Exercise**: Plot and annotate the given dataset to illustrate its key features.

### Unit 4: Efficient statistical routines (50%)
* Program complexity and Big $\mathcal{O}$ notation
* Classic data structures (arrays, dictionaries, disjoint sets, trees, priority queues)
* Classic algorithms (divide-and-conquer, hashing, recursion, search, sort, graph algorithms)
* Broadcasting and vectorization in numpy and pandas
* Functional programming (motivation, apply, map, filter, reduce, comprehensions, recursion, partial application)
* Representation of numbers and linear algebra
* Decompositional approach to matrix computations (LR, QR, SVD, Cholesky)
* Introducing BLAS and LAPACK
* Quadrature (Numerical integration)
* Optimization (Newton's method, gradient and conjugate gradient descent, EM algorithm)
* Resampling methods (bootstrap, jackknife, permutation, boosting and bagging)
* Dynamic programming and Viterbi algorithm
* Monte Carlo simulations
* Markov chain Monte Carlo

**Sample Exercise**: You are given a slow and buggy simulation script. Fix the errors and speed it up using vectorization.

**Sample Exercise**: Write an efficient function to calculate Cook's distance for the influence of data points on a regression.

**Sample Exercise**: Use a gradient descent method to fit a logistic regression model (aka Iterative reweighed least squares).

**Sample Exercise**: Implement the non-parametric and parametric bootstrap for phylogenetic trees described in <http://www.pnas.org/content/93/23/13429.full.pdf>

**Sample Exercise**: Use permutation resampling to find the FWER given experimental data.

**Samepl Exercsie**: Use symbolic integration, numerical integration and Monte Carlo integration to evaluate a definite double integral

**Sample Exercise**: Use regular Python, PyMC3 and PyStan to find the posterior distribution for a two-level model.

### Unit 5: Code optimization and native code (10%)

* Complexity and performance of algorithms and data structures
* C crash course for statisticians
* Using numexpr, numba and cython
* Using functions from C/C++ libraries
* Writing functions in C/C++ and wrapping for Python/R
* Introduction to the Julia programming language

**Sample Exercise**: You are given some slow code. Speed it up by using a better algoithm or data structure.

**Sample Exercise**: Write the Newton-Raphson method in C - it should take the following arguments - a function pointer f, a function pointer fprime, an initial point x0, and a tolerance.

**Sample Exercise**: You are given some slow code in Python. Speed it up using Cython.

### Unit 6: High-performance computing (10%)
* Common parallel programing patterns
* Multiprocessing and IPython.Parallel
* Introduction to processing big data with MapReduce
* Introduction to Multi-CPU computing with MPI
* Introduction to GPU computing with CUDA

**Sample Exercise**: Rewrite the function to calculate Cook's distance using multiprocessing.

**Sample Exercise**: Use Elastic MapReduce to do some massive genomic data manipulation.

**Sample Exercise**: Use MPI to run an MCMC with parallel tempering (aka $MC^3$) for a long time with some defined swap interval between chains.

**Sample Exercise**: Write a matrix multiplication kernel with and without use of shared memory using CUDA. Test it out using square matrices initialized with random numbers from CURAND. 
