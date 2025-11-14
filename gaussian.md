# 📘 Gaussian (Normal) Distribution — Variance, Covariance, Correlation, CLT

## 1. Gaussian (Normal) Distribution

A random variable \(X\) is **normally distributed** with mean \(\mu\) and variance \(\&sigma^2\) if its probability density function is:

![gauss](https://latex.codecogs.com/svg.image?f(x)=\frac{1}{\sqrt{2\pi\sigma^{2}}}\exp\left(-\frac{(x-\mu)^{2}}{2\sigma^{2}}\right))

### Key Properties

- Symmetric about the mean  
- Fully determined by **mean** and **variance**  
- Mean = median = mode  

---

## 2. Mean (Expectation Value)

The mean (expected value) is:

![mean](https://latex.codecogs.com/svg.image?\mu=\mathbb{E}[X]=\int_{-\infty}^{\infty}x\{f(x)}\{dx})

---

## 3. Variance

Variance measures the spread around the mean:

![var](https://latex.codecogs.com/svg.image?\sigma^{2}=\mathbb{E}[(X-\mu)^{2}])

Equivalent computational form:

![var2](https://latex.codecogs.com/svg.image?\sigma^{2}=\mathbb{E}[X^{2}]-\mu^{2})

---

## 4. Covariance

For two random variables \(X\) and \(Y\):

![cov](https://latex.codecogs.com/svg.image?\mathrm{Cov}(X,Y)=\mathbb{E}[(X-\mu_{X})(Y-\mu_{Y})])

If  
- Cov(X,Y) > 0 → variables move together  
- Cov(X,Y) < 0 → variables move oppositely  
- Cov(X,Y) = 0 → no linear relationship  

---

## 5. Correlation Coefficient

Correlation is the **normalized covariance**:

![corr](https://latex.codecogs.com/svg.image?\rho_{XY}=\frac{\mathrm{Cov}(X,Y)}{\sigma_X\sigma_Y})

Properties:

- \( -1 \le \rho_{XY} \le 1 \)  
- \( \rho = 1 \): perfect positive correlation  
- \( \rho = -1 \): perfect negative correlation  
- \( \rho = 0 \): uncorrelated  

---

## 6. Multivariate Gaussian Distribution

For a vector \( \mathbf{x} \in \mathbb{R}^n \) with mean vector \( \boldsymbol{\mu} \) and covariance matrix \( \Sigma \):

![mv_gauss](https://latex.codecogs.com/svg.image?f(\mathbf{x})=\frac{1}{\sqrt{(2\pi)^{n}\det(\Sigma)}}\exp\left[-\frac{1}{2}(\mathbf{x}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{x}-\boldsymbol{\mu})\right])

The covariance matrix is:

![covmat](https://latex.codecogs.com/svg.image?\Sigma_{ij}=\mathrm{Cov}(X_{i},X_{j}))

---

## 7. Central Limit Theorem (CLT)

The **Central Limit Theorem** states that the sum (or average) of independent random variables tends toward a Gaussian distribution, regardless of the original distribution.

Let \(X_1, X_2, \dots, X_n\) be independent with mean \(\mu\) and variance \(\sigma^2\). Then:

![clt](https://latex.codecogs.com/svg.image?\frac{\sum_{i=1}^{n}X_i-n\mu}{\sigma\sqrt{n}}\xrightarrow[n\to\infty]{d}\mathcal{N}(0,1))

Meaning:  
- Averages become normally distributed  
- Uncertainty decreases as \(1/\sqrt{n}\)  

---

## 8. Standard Normal Distribution

A Gaussian with mean 0 and variance 1:

![stdnorm](https://latex.codecogs.com/svg.image?Z=\frac{X-\mu}{\sigma}\sim\mathcal{N}(0,1))

---

## 9. Useful Identities

### Sum of Independent Gaussians

If \(X \sim \mathcal{N}(\mu_1,\sigma_1^2)\) and \(Y \sim \mathcal{N}(\mu_2,\sigma_2^2)\):

![sum_gauss](https://latex.codecogs.com/svg.image?X&plus;Y\sim\mathcal{N}(\mu_1&plus;\mu_2,\sigma_1^{2}&plus;\sigma_2^{2}))

### Linear Transformation

For \(Y = aX + b\):

![lintrans](https://latex.codecogs.com/svg.image?Y\sim\mathcal{N}(a\mu&plus;b,a^{2}\sigma^{2}))

---

## 10. Visual Interpretation

- Variance → width of the bell curve  
- Covariance → how variables fluctuate together  
- Correlation → strength of linear relationship  
- CLT → explains why Gaussian models appear everywhere  

---