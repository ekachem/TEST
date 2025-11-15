# Chapter 5 — Probability
## Continuous Distributions

So far, the events we have encountered have discrete outcomes, such as obtaining heads or tails when tossing a coin. However, some events correspond to continuous outcomes.

For example, imagine spinning an arrow. The resulting angle ϕ at which the arrow stops is not a discrete value; it can take any value in the continuous range **[0, 2π]**.

If there is no external influence that makes the arrow prefer one direction over another, then the probability of the arrow pointing at any given angle must be equal.

We introduce a function ρ(ϕ) to represent the probability density, or propensity, of the arrow pointing at angle ϕ. A higher value of ρ(ϕ) indicates a greater likelihood of the arrow pointing near that angle.

The total probability over all possible directions must be:

![Eq1](https://latex.codecogs.com/svg.image?\int_{0}^{2\pi}\rho(\phi)\,d\phi=1)

Here,

![Eq2](https://latex.codecogs.com/svg.image?\rho(\phi)\,d\phi)

represents the probability that the arrow points within the infinitesimal range \(d\phi\).

For a uniform distribution (equal likelihood in all directions):

![Eq3](https://latex.codecogs.com/svg.image?\rho(\phi)=\frac{1}{2\pi})

which is independent of ϕ, and indeed satisfies:

![Eq4](https://latex.codecogs.com/svg.image?\int_{0}^{2\pi}\rho(\phi)\,d\phi=1)

---

## Another Example of Continuous Distribution

Consider a one-dimensional box of length \(L\) into which we randomly drop a small sphere. The probability of the sphere landing at a position \(x\) follows a continuous distribution ρ(x)dx, which must also be normalized to 1:

![Eq5](https://latex.codecogs.com/svg.image?\int_{0}^{L}\rho(x)\,dx=1)

The probability of finding the sphere within a certain range \(a \le x \le b\) is given by:

![Eq6](https://latex.codecogs.com/svg.image?P(a\le%20x\le%20b)=\int_{a}^{b}\rho(x)\,dx)

All the concepts developed for discrete distributions can be extended to continuous distributions. For example:

![Eq7](https://latex.codecogs.com/svg.image?\langle%20x\rangle=\int_{-\infty}^{\infty}x\rho(x)\,dx)

![Eq8](https://latex.codecogs.com/svg.image?\langle%20x^{2}\rangle=\int_{-\infty}^{\infty}x^{2}\rho(x)\,dx)

and the variance is defined as:

![Eq9](https://latex.codecogs.com/svg.image?\sigma_{x}^{2}=\int_{-\infty}^{\infty}(x-\langle%20x\rangle)^{2}\rho(x)\,dx)

---

## The Gaussian (Normal) Distribution

The most important continuous probability distribution is the Gaussian (Normal) distribution, defined as:

![Eq10](https://latex.codecogs.com/svg.image?\rho(x)=\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-x^{2}/(2\sigma^{2})})

For this distribution:

![Eq11](https://latex.codecogs.com/svg.image?\langle%20x\rangle=0)

![Eq12](https://latex.codecogs.com/svg.image?\langle%20x^{2}\rangle=\sigma^{2})

Therefore:

![Eq13](https://latex.codecogs.com/svg.image?\langle%20x^{2}\rangle-\langle%20x\rangle^{2}=\sigma^{2}=\sigma_{x}^{2})

Thus, \( \sigma^{2} \) is the variance of the Gaussian distribution.

# Gaussian Distribution and Its Properties

See Slide 4 for Gaussian distributions with different values of σ².  

![Standard Deviation Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Standard_deviation_diagram.svg/512px-Standard_deviation_diagram.svg.png)

A larger σ corresponds to a broader distribution.

See Slide 5 for the probability of finding a value within 1 σ, 2 σ, and 3 σ of the center of a Gaussian distribution:

![Standard Deviation Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Standard_deviation_diagram.svg/512px-Standard_deviation_diagram.svg.png)

[ https://en.wikipedia.org/wiki/Normal_distribution ]

![Eq1](https://latex.codecogs.com/svg.image?\int_{-\sigma}^{\sigma}\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-x^{2}/(2\sigma^{2})}\,dx=0.6827)

![Eq2](https://latex.codecogs.com/svg.image?\int_{-2\sigma}^{2\sigma}\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-x^{2}/(2\sigma^{2})}\,dx=0.9545)

![Eq3](https://latex.codecogs.com/svg.image?\int_{-3\sigma}^{3\sigma}\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-x^{2}/(2\sigma^{2})}\,dx=0.9973)

Thus, approximately **68.3%**, **95.5%**, and **99.7%** of the total probability lie within **1 σ**, **2 σ**, and **3 σ** of the mean, respectively.

---

## Gaussian Centered at a Non-Zero Mean

A Gaussian distribution need not be centered at \(x = 0\).  
A more general form is:

![Eq4](https://latex.codecogs.com/svg.image?\rho(x)=\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-(x-\langle%20x\rangle)^{2}/(2\sigma^{2})})

which is centered at the mean value ⟨x⟩.

As σ → 0, the Gaussian becomes sharper and narrower, eventually approaching the Dirac delta function:

![Eq5](https://latex.codecogs.com/svg.image?\delta(x-a)=\lim_{\sigma\to0}\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-(x-a)^{2}/(2\sigma^{2})})

The delta function satisfies:

![Eq6](https://latex.codecogs.com/svg.image?\delta(x-a)=\begin{cases}\infty,&x=a\\0,&x\neq%20a\end{cases})

and

![Eq7](https://latex.codecogs.com/svg.image?\int_{-\infty}^{\infty}\delta(x-a)\,dx=1)

---

# The Normal (Gaussian) Distribution and the Central Limit Theorem

The Gaussian distribution is also called the **Normal Distribution**.  
It is of fundamental importance because of a major result in statistics — the **Central Limit Theorem**.

The theorem states that if \(x_1, x_2, \dots, x_n\) are independent random variables with the same underlying distribution, then their average

![Eq8](https://latex.codecogs.com/svg.image?\bar{x}=\frac{x_{1}+x_{2}+\cdots+x_{n}}{n})

tends toward a normal distribution, and the approximation becomes increasingly accurate as \(n\) increases.

---

## Example — Rolling Dice

Consider rolling \(n\) dice.  
Let \(X_1, X_2, X_3, \dots, X_n\) represent the face-up values of each die.

Slide 6 shows the probability distribution of the sum

![Eq9](https://latex.codecogs.com/svg.image?S=X_{1}+X_{2}+\cdots+X_{n})

![Central Limit Theory](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Dice_sum_central_limit_theorem.svg/800px-Dice_sum_central_limit_theorem.svg.png)

[ https://en.wikipedia.org/wiki/Normal_distribution ]

which can take values from **n** to **6n**.

With one die, all six outcomes are equally probable.

With two dice, the central value \(S=7\) becomes the most probable, since more combinations of dice values yield 7 than any other sum.


## Convergence Toward the Gaussian Distribution

For two dice, many different combinations yield the same total.  
For example, a sum of 7 can result from:

(1,6), (6,1), (2,5), (5,2), (3,4), (4,3)

whereas only one combination, (1,1), gives a sum of 2.

As the number of dice \(n\) increases, the probability distribution of the sum becomes smoother and approaches the bell-shaped Gaussian (normal) curve.

If we divide the total by \(n\), i.e., consider the mean value

![Eq1](https://latex.codecogs.com/svg.image?\bar{x}=\frac{x_{1}+x_{2}+\cdots+x_{n}}{n})

the results range from 1 to 6.

In the series of plots (see the figure in the lecture slides), all five distributions share the same **range**, but differ in **shape** — and as \(n\) increases, the curves converge to the Gaussian form.

---

## Example — Distribution of H₂ Bond Lengths

Consider one mole of hydrogen molecules (H₂).  
If we could instantaneously measure the bond length of each molecule, we would find that the values are not identical — some bonds are slightly longer, some shorter, with an average value around **0.74 Å**.

These variations in bond length are analogous to the different face-up values of dice in the previous example.  
All H₂ molecules are identical, just as all dice have the same probability distribution of outcomes.

Suppose we take a “snapshot” of all \(N_A\) molecules and record their instantaneous bond lengths  
\(x_1, x_2, \dots, x_{N_A}\).  
We can then compute their average bond length:

![Eq2](https://latex.codecogs.com/svg.image?\bar{x}=\frac{x_{1}+x_{2}+\cdots+x_{N_A}}{N_A})

where

![Eq3](https://latex.codecogs.com/svg.image?N_{A}=6.022\times10^{23})

is Avogadro’s number.

If we repeat this process—taking many such snapshots and recording the corresponding average bond length each time—we will find that these averaged values follow a **normal (Gaussian) distribution**.

Because \(N_A\) is extremely large, the **Central Limit Theorem** guarantees that the measured averages of microscopic quantities (such as bond length, velocity, or energy) are normally distributed.

---

## Implication for Experiments

Nearly all experimental measurements can be viewed as observing the **average of a very large number of microscopic events or particles**.  
Consequently, the results of most physical and chemical experiments **follow the normal (Gaussian) distribution**.

## Importance of the Normal Distribution

This is why the normal (Gaussian) distribution finds such extensive use in analytical chemistry.  
Many experimental measurements—such as absorbance, concentration, or instrumental noise—naturally follow normal distributions because they are averages of numerous microscopic events.

---

## Joint Probability Distributions

An event can depend on more than one random variable.

Example:  
If a die is thrown into a box, both the face-up value and the landing position are random quantities.  
Let these be represented by two continuous random variables, x and y.

The joint probability density function ρ(x,y) describes the combined probability of both variables.

The quantity:

![Eq1](https://latex.codecogs.com/svg.image?\rho(x,y)\,dx\,dy)

gives the probability that:

- \(X\) lies within the infinitesimal range \(x \le X \le x+dx\), and  
- \(Y\) lies within \(y \le Y \le y+dy\).

The normalization condition must hold:

![Eq2](https://latex.codecogs.com/svg.image?\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}\rho(x,y)\,dx\,dy=1)

---

## Marginal Probability Densities

If we integrate over one variable, we obtain the marginal distribution of the other:

![Eq3](https://latex.codecogs.com/svg.image?\rho(x)=\int_{-\infty}^{\infty}\rho(x,y)\,dy)

This gives the probability distribution of \(x\) after averaging over all values of \(y\).

---

## Expectation of a Function

The expected (mean) value of any function \(f(x,y)\) is:

![Eq4](https://latex.codecogs.com/svg.image?\langle%20f(x,y)\rangle=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(x,y)\rho(x,y)\,dx\,dy)

---

## Independent Variables

If \(X\) and \(Y\) are independent:

![Eq5](https://latex.codecogs.com/svg.image?\rho(x,y)=\rho(x)\rho(y))

Example:  
Throwing two dice.  
The probability of obtaining (1,1) is:

![Eq6](https://latex.codecogs.com/svg.image?P(1,1)=\frac{1}{6}\times\frac{1}{6}=\frac{1}{36})

since the outcomes are independent.

---

## Mean and Variance of Sums of Variables

For two random variables \(X\) and \(Y\):

![Eq7](https://latex.codecogs.com/svg.image?\langle%20X+Y\rangle=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}(X+Y)\rho(x,y)\,dx\,dy)

This separates as:

![Eq8](https://latex.codecogs.com/svg.image?\langle%20X+Y\rangle=\langle%20X\rangle+\langle%20Y\rangle)

---

## Variance of the Sum

The variance of the sum is:

![Eq9](https://latex.codecogs.com/svg.image?\sigma_{x+y}^{2}=\langle(X+Y-\langle%20X+Y\rangle)^{2}\rangle)

Expanding:

![Eq10](https://latex.codecogs.com/svg.image?\sigma_{x+y}^{2}=\langle(X-\langle%20X\rangle)^{2}\rangle+\langle(Y-\langle%20Y\rangle)^{2}\rangle+2(\langle%20XY\rangle-\langle%20X\rangle\langle%20Y\rangle))

Thus:

![Eq11](https://latex.codecogs.com/svg.image?\sigma_{x+y}^{2}=\sigma_{x}^{2}+\sigma_{y}^{2}+2(\langle%20XY\rangle-\langle%20X\rangle\langle%20Y\rangle))

For independent variables, \( \langle XY\rangle = \langle X\rangle\langle Y\rangle \), so:

![Eq12](https://latex.codecogs.com/svg.image?\sigma_{x+y}^{2}=\sigma_{x}^{2}+\sigma_{y}^{2})

## Covariance and Correlation

If \(X\) and \(Y\) are independent, then:

![Eq1](https://latex.codecogs.com/svg.image?\langle%20XY\rangle=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}XY\rho(x)\rho(y)\,dx\,dy=(\int_{-\infty}^{\infty}x\rho(x)\,dx)(\int_{-\infty}^{\infty}y\rho(y)\,dy)=\langle%20X\rangle\langle%20Y\rangle)

Substituting this into the variance relation gives:

![Eq2](https://latex.codecogs.com/svg.image?\sigma_{x+y}^{2}=\sigma_{x}^{2}+\sigma_{y}^{2})

Thus, the term:

![Eq3](https://latex.codecogs.com/svg.image?\langle%20XY\rangle-\langle%20X\rangle\langle%20Y\rangle)

provides a measure of how dependent the two variables are.

---

## Covariance

This quantity is called the **covariance** of \(X\) and \(Y\), defined as:

![Eq4](https://latex.codecogs.com/svg.image?\mathrm{Cov}(X,Y)=\langle%20XY\rangle-\langle%20X\rangle\langle%20Y\rangle)

An equivalent form is:

![Eq5](https://latex.codecogs.com/svg.image?\mathrm{Cov}(X,Y)=\langle(X-\langle%20X\rangle)(Y-\langle%20Y\rangle)\rangle)

This is consistent with the definitions of variance:

![Eq6](https://latex.codecogs.com/svg.image?\sigma_{x}^{2}=\langle(X-\langle%20X\rangle)^{2}\rangle)

![Eq7](https://latex.codecogs.com/svg.image?\sigma_{y}^{2}=\langle(Y-\langle%20Y\rangle)^{2}\rangle)

---

## Correlation Coefficient

It is often useful to normalize the covariance by the product of the standard deviations of \(X\) and \(Y\).  
This normalized quantity is the **correlation coefficient** \(\rho_{xy}\):

![Eq8](https://latex.codecogs.com/svg.image?\rho_{xy}=\frac{\langle(X-\langle%20X\rangle)(Y-\langle%20Y\rangle)\rangle}{\sigma_{x}\sigma_{y}})

Another equivalent form:

![Eq9](https://latex.codecogs.com/svg.image?\rho_{xy}=\frac{\langle(X-\langle%20X\rangle)(Y-\langle%20Y\rangle)\rangle}{\sqrt{\langle(X-\langle%20X\rangle)^{2}\rangle\langle(Y-\langle%20Y\rangle)^{2}\rangle}})

By construction:

![Eq10](https://latex.codecogs.com/svg.image?-1\le\rho_{xy}\le1)

- If \(\rho_{xy}=0\): X and Y are uncorrelated (independent).  
- If \(\rho_{xy}>0\): X and Y are positively correlated (when \(X>\langle X\rangle\), \(Y>\langle Y\rangle\)).  
- If \(\rho_{xy}<0\): X and Y are negatively correlated (when \(X>\langle X\rangle\), \(Y<\langle Y\rangle\), or vice versa).

---

## Interpreting Correlations

The correlation coefficient allows us to compare the degree of statistical dependence between different pairs of variables, even when their units or magnitudes differ.

For example:

Are **wealth and health** more strongly correlated than  
**temperature and humidity** in a city?

Such comparisons are meaningful because \(\rho_{xy}\) is **dimensionless and normalized**.

