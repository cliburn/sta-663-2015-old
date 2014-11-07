Expected background and pretest
----------------------------------------

### Miscellaneous basics

* LaTeX

> Use LaTeX to generate the following

\\[
\begin{align}
\hat{y_1} &= \beta_0 + \beta_1 x_1 \\
\hat{y_2} &= \beta_0 + \beta_1 x_2
\end{align}
\\]

* Can use a version control system

> Create a repository on GitHub. Add a README file to it with the text "Hello". Now clone it to your local filesystem and revise the text of READNE to "Goodbye".Commit and push your changes to GitHub.

* Comfortable working in command line

> Create a new directory, read a text file, run a script without leaving the console/terminal

### Programming basics

**In any language**

* Understand what a nested loop does and why we first optimize the inner loop
> What is the output of
```c
#include "stdio.h"

int main()
{
  for (int i=0; i< 3; i++)
    for (int j=0; j<4; j++)
      printf("%d, %d\n", i, j);
}
```

* Write a function to calculate the n$^\text{th}$ Fibonacci number. If $F_1 = 1$ and $F_2 = 1$, what is $F_{23}$?

* Write code to find the column means of

\\[
\begin{array}[ccc]
01 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\\]

* Explain what the quicksort function does
```python
def quicksort(xs):
    if xs == []:
        return []
    else:
        smaller = [x for x in xs[1:] if x <= xs[0]]
        larger = [x for x in xs[1:] if x > xs[0]]
        return quicksort(smaller ) + [xs[0]] + quicksort(larger)
```

**In C**

> Write, compile and execute a "Hello world" program in C
> Write a makefile to compile a "Hello world" program in C

### Data management basics

* Can read input from a CSV file into a data structure (e.g. data frame)
* Convert the following data into linked tables in a relational databases (e.g. SQLite)

| Student | Subject | Grade |
|---|---|---|
| Ali | Math | 90 |
| Baba | Science | 89 |
| Ali | Science | 75 |
| Baba | Math | 65 |

* Write an SQL statement to find out Ali's average grade over all his subjects.

### Math basics

**Calculus**

* Understand series approximations to functions (for optimization algorithms)
* Understand concept of gradient of multi-dimensional surfaces and linearization (for optimization algorithms)
* Basic understanding of integration  (for Monte Carlo approximations, convolutions)

**Linear algebra**

* Solving systems of linear equations (for regression)

> Convert to matrix form by augmenting with a dummy variable $x_0 = 1$ to go with $\beta_0$.
\\[
\begin{align}
\hat{y_1} &= \beta_0 + \beta_1 x_1 \\
\hat{y_2} &= \beta_0 + \beta_1 x_2
\end{align}
\\]
Explain why $\beta = (X^TX)^{-1}X^T y$ is the least squares solution. 

* Properties of vector spaces (e.g. scalars, vectors, matrices, functions)
* Spectral decomposition of a matrix (for PCA, SVD, other matrix decompositions)

> Find eigenvalues and eigenvectors for the matrix
\\[
\begin{array}[cc]
0 1 & 2 \\
 3 & 4
\end{array}
\\]

* Linear dependence, basis vectors and spanning (for FFT)

> Are the following sets of basis functions linearly dependent?
(1, x, x^2, x^3), (1, x^2, x^4, x^6)

> For estimating $\beta$, can the following equations be treated as a linear system?
\\[
\begin{align}
\hat{y_1} &= \beta_0 + \beta_1 x_1 + \beta_2 x_1^2 \\
\hat{y_2} &= \beta_0 + \beta_1 x_2 + \beta_2 x_2^2
\end{align}
\\]

**Probability and statistics**

* Familiarity with common univariate distributions (uniform, Gaussian, exponential, Poisson, binomial etc) and the multivariate normal distribution
> In any programming language, draw and plot a histogram of 10,000 samples from a Poisson distribution with $\lambda=3$.
* Can calculate expectation, variance and covariance
> Without using a computer or calculator, find the covariance of
\\[
\begin{array}[cc]
0 1 & 3 \\
 2 & 6
\end{array}
\\]

* Some experience using classification and regression methods (e.g. linear, logistic)
> What is the maximum likelihood loss function for simple logistic regression?

* Some exposure to statistical inference in both Bayesian and frequentist frameworks
> In 10 coin flips, we got [H, H, T, H, H, T, H, H, H, T]. Is this a fair coin in the frequentist framework if we set the type 1 error as 0.05? How would you answer this question in the Bayesian framework?
