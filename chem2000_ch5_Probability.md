## Continuous Distributions

So far, the events we have encountered have discrete outcomes, such as obtaining heads or tails when tossing a coin.
However, some events correspond to continuous outcomes.

For example, imagine spinning an arrow (see figure on the left). The resulting angle, ϕ, at which the arrow stops is not a discrete value; it can take any value in the continuous range 
[0,2π].

If there is no external influence that makes the arrow prefer one direction over another, then the probability of the arrow pointing at any given angle must be equal.

We introduce a function ρ(ϕ) to represent the probability density, or propensity, of the arrow pointing at angle ϕ.
A higher value of ρ(ϕ) indicates a greater likelihood of the arrow pointing near that angle.

The total probability over all possible directions must be 1:

![Integral](https://latex.codecogs.com/svg.image?\int_{-\infty}^{\infty}\delta(x)\{dx}=1)

Here, ρ(ϕ)dϕ represents the probability that the arrow points within the infinitesimal range dϕ around φ.

For a uniform distribution (equal likelihood in all directions),

![Integral](https://latex.codecogs.com/svg.image?\int_{-\infty}^{\infty}\delta(x)\{dx}=1)

which is independent of φ, and indeed satisfies

![Integral](https://latex.codecogs.com/svg.image?\int_{-\infty}^{\infty}\delta(x)\{dx}=1)

## Another Example of Continuous Distribution

Consider a one-dimensional box of length L into which we randomly drop a small sphere. The probability of the sphere landing at a position x follows a continuous distribution ρ(x)dx, which must also be normalized to 1:

The probability of finding the sphere within a certain range 
𝑎
≤
𝑥
≤
𝑏
a≤x≤b is given by

𝑃
(
𝑎
≤
𝑥
≤
𝑏
)
=
∫
𝑎
𝑏
𝜌
(
𝑥
)
 
𝑑
𝑥
P(a≤x≤b)=∫
a
b
	​

ρ(x)dx
