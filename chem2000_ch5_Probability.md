# Chapter 5 — Probability
## Continuous Distributions

So far, the events we have encountered have discrete outcomes, such as obtaining heads or tails when tossing a coin. However, some events correspond to continuous outcomes.

For example, imagine spinning an arrow. The resulting angle ϕ at which the arrow stops is not a discrete value; it can take any value in the continuous range **[0, 2π]**.

If there is no external influence that makes the arrow prefer one direction over another, then the probability of the arrow pointing at any given angle must be equal.

We introduce a function ρ(ϕ) to represent the probability density of the arrow pointing at angle ϕ.

The total probability over all directions must be:

![Eq1](https://latex.codecogs.com/svg.image?\int_{0}^{2\pi}\rho(\phi)\,d\phi=1)

Here,

![Eq2](https://latex.codecogs.com/svg.image?\rho(\phi)\,d\phi)

represents the probability that the arrow points within the infinitesimal range \(d\phi\).

For a uniform distribution:

![Eq3](https://latex.codecogs.com/svg.image?\rho(\phi)=\frac{1}{2\pi})

which satisfies:

![Eq4](https://latex.codecogs.com/svg.image?\int_{0}^{2\pi}\rho(\phi)\,d\phi=1)

---

## Another Example of Continuous Distribution

Consider a 1-D box of length \(L\). The distribution ρ(x) must satisfy:

![Eq5](https://latex.codecogs.com/svg.image?\int_{0}^{L}\rho(x)\,dx=1)

Probability of finding the sphere in \(a \le x \le b\):

![Eq6](https://latex.codecogs.com/svg.image?P(a\le%20x\le%20b)=\int_{a}^{b}\rho(x)\,dx)

Expectation values:

![Eq7](https://latex.codecogs.com/svg.image?\langle%20x\rangle=\int_{-\infty}^{\infty}x\rho(x)\,dx)

![Eq8](https://latex.codecogs.com/svg.image?\langle%20x^{2}\rangle=\int_{-\infty}^{\infty}x^{2}\rho(x)\,dx)

Variance:

![Eq9](https://latex.codecogs.com/svg.image?\sigma_{x}^{2}=\int_{-\infty}^{\infty}(x-\langle%20x\rangle)^{2}\rho(x)\,dx)

---

## Gaussian (Normal) Distribution

Definition:

![Eq10](https://latex.codecogs.com/svg.image?\rho(x)=\frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-x^{2}/(2\sigma^{2})})

Mean:

![Eq11](https://latex.codecogs.com/svg.image?\langle%20x\rangle=0)

Second moment:

![Eq12](https://latex.codecogs.com/svg.image?\langle%20x^{2}\rangle=\sigma^{2})

Variance identity:

![Eq13](https://latex.codecogs.com/svg.image?\langle%20x^{2}\rangle-\langle%20x\rangle^{2}=\sigma^{2}=\sigma_{x}^{2})


