# TEST
A test repository

# Dirac Delta Function

## Introduction
The **Dirac delta function**, often denoted as δ(x), is a mathematical construct that is not a conventional function but a *generalized function* or *distribution*. It is widely used in physics, engineering, and signal processing to model idealized impulses, point events, or instantaneous phenomena.

## Definition
The Dirac delta function satisfies the following key properties:

### 1. Zero Everywhere Except at Zero
δ(x) = 0 for all x ≠ 0


![Equation](https://latex.codecogs.com/svg.image?\int_{-\infty}^{\infty}\delta(x)\,dx=1)
Integral from -inf to +inf of δ(x) dx = 1
### 2. Integral Equals One
\[
\int_{-\infty}^{\infty} \delta(x)\,dx = 1
\]

### 3. Sifting (Sampling) Property
For any smooth function \(f(x)\):
\[
\int_{-\infty}^{\infty} f(x)\,\delta(x - a)\,dx = f(a)
\]

## Interpretation
The delta function represents an infinitely narrow, infinitely tall spike at x = 0, with a total area of 1. It is not a real function but behaves like one under integration. It is used to represent:

- Point masses  
- Point charges  
- Impulses in signals  
- Instantaneous changes in systems  

## Common Representations

### Limit of a Narrow Gaussian
\[
\delta(x) = \lim_{\sigma \to 0} \frac{1}{\sigma\sqrt{2\pi}} e^{-x^2/(2\sigma^2)}
\]

### Limit of a Sinc Function
\[
\delta(x) = \lim_{L \to \infty} \frac{1}{\pi} \frac{\sin(Lx)}{x}
\]

## Applications
- **Signal processing:** ideal impulse signals  
- **Physics:** point charges, point masses  
- **Differential equations:** Green’s functions  
- **Systems engineering:** impulse response of systems  

## Conclusion
The Dirac delta function is an essential mathematical tool for representing idealized or instantaneous phenomena. Although it is not a true function, its well-defined properties under integration make it indispensable in theoretical and applied mathematics.