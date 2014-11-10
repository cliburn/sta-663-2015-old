Expected background and pretest
----------------------------------------

### Miscellaneous basics

* Use LaTeX to generate the following

\\[
\begin{align}
\hat{y_1} &= \beta_0 + \beta_1 x_1 \\
\hat{y_2} &= \beta_0 + \beta_1 x_2
\end{align}
\\]

* Create a repository on GitHub. Add a README file to it with the text "Hello". Now clone it to your local filesystem and revise the text of READNE to "Goodbye".Commit and push your changes to GitHub.

* Open a console/terminal in your OS. Create a new directory, navigate to the new directory, creata a text file using `echo` and `>`, read the text file using `cat`, and count  the number of characters in the text file with `wc` without leaving the console/terminal

### Programming basics

Most of the programming will be in Python, with C towards the end of the course and occasional R and Julia excursions. You are expected to have *significant* programming experience in a high-level language commonly used for numerical computation such as R or Matlab - for example, by having completed  [STA 523 (Statistical Programming)](https://stat.duke.edu/~cr173/Sta523_Fa14/) or [BIOSTAT 721/722 (Introduction to Statistical Programming )](http://biostat.duke.edu/master-biostatistics-program/curriculum). Programming experience in Python and C is not necessary, but it is strongly recommended that you learn at least the basics of both languages from an online tutorial or introductory book before the course.

**In any language**

* What is the output of
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

* Explain what the quicksort function does when given the list of numbers [7,1,2,10,7,11].
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

* Understand series approximations to functions (for optimization algorithms). Explain the relationship between the Taylor series expansions for the exponential, sine and cosine functions.
* Understand concept of gradient of multi-dimensional surfaces and linearization (for optimization algorithms). What are the Jacobian and Hessian matrices for the following set of equations?

\\[
\begin{align}
y_1 &= x_2^2 \\
y_2 &= x_1^3x_2^2 - x_1
\end{align}
\\]

* Basic understanding of integration  (for Monte Carlo approximations, convolutions). A fair die (i.e. distribution is uniform over the numbers 1,2,3,4,5,6)  is rolled twice. What is the distribution of the sum?  Write a program to calculate the distribution of the sum after $n$ rolls.

**Linear algebra**

* Convert to matrix form by augmenting with a dummy variable $x_0 = 1$ to go with $\beta_0$.
\\[
\begin{align}
\hat{y_1} &= \beta_0 + \beta_1 x_1 \\
\hat{y_2} &= \beta_0 + \beta_1 x_2
\end{align}
\\]
Explain why $\beta = (X^TX)^{-1}X^T y$ is the least squares solution. 

* What are the properties of an inner product in a vector space? What is the inner product of real functions $f$ and $g$ over the closed interval [a, b]?

* Find eigenvalues and eigenvectors for the matrix
\\[
\begin{array}[cc]
0 1 & 2 \\
 3 & 4
\end{array}
\\]

* Are the following sets of basis functions linearly dependent?
(1, x, x^2, x^3), (1, x^2, x^4, x^6)

* For estimating $\beta$, can the following equations be treated as a linear system?
\\[
\begin{align}
\hat{y_1} &= \beta_0 + \beta_1 x_1 + \beta_2 x_1^2 \\
\hat{y_2} &= \beta_0 + \beta_1 x_2 + \beta_2 x_2^2
\end{align}
\\]

**Probability and statistics**

* In any programming language, draw and plot a histogram of 10,000 samples from a Poisson distribution with $\lambda=3$. What is the distribution of the *sum* of these 10,000 samples?
* Without using a computer or calculator, find the covariance of
\\[
\begin{array}[cc]
0 1 & 3 \\
 2 & 6
\end{array}
\\]

* What is the maximum likelihood loss function for simple logistic regression?

* In 10 coin flips, we got [H, H, T, H, H, T, H, H, H, T]. Is this a fair coin in the frequentist framework if we set the type 1 error as 0.05? How would you answer this question in the Bayesian framework?

* Write a short paragraph explaining the following concepts, ideally with a simple numerical and/or graphical example (we will be learning about their computational implementation, optimization and application , and will only provide a brief refresher of the relevant theory):
    * Law of large numbers and central limit theorem 
    * PCA
    * Linear and logistic regression
    * Overfitting, regularization and cross-validation
    * Resampling methods e.g. bootstrap and permutation resampling
    * Maximum likelihood
    * Expectation maximization
    * Markov chain Monte Carlo
