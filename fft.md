# 📘 Autocorrelation Function (ACF) & Fourier Transform (FFT)

## 1. Autocorrelation Function (ACF)

The **autocorrelation function** measures how a property \(A(t)\) correlates with itself after a time lag \(\tau\).

### Definition

![acf](https://latex.codecogs.com/svg.image?C_{AA}(\tau)=\langle%20A(t)A(t&plus;\tau)\rangle)

### Discrete Form for MD Trajectories

Given samples \(A_1, A_2, \dots, A_N\):

![disc_acf](https://latex.codecogs.com/svg.image?C_{AA}(k)=\frac{1}{N-k}\sum_{i=1}^{N-k}A_iA_{i&plus;k})

### Common Autocorrelation Functions in MD

| Application | Autocorrelation |
|------------|-----------------|
| IR Spectrum | ![muacf](https://latex.codecogs.com/svg.image?C_{\mu\mu}(\tau)=\langle\mu(t)\cdot\mu(t&plus;\tau)\rangle) |
| Vibrational DOS (VDOS) | ![vvacf](https://latex.codecogs.com/svg.image?C_{vv}(\tau)=\langle\mathbf{v}(t)\cdot\mathbf{v}(t&plus;\tau)\rangle) |
| Raman Spectrum | Polarizability ACF |
| Rotational Spectrum | Angular momentum ACF |

### Physical Meaning

- Slow decay → slow structural relaxation  
- Rapid decay → fast fluctuations  
- Oscillations → vibrational motion  

---

## 2. Fourier Transform (FFT) of ACF → Spectrum

Taking the **Fourier transform** of the autocorrelation function yields the **spectral density**.

### Continuous Fourier Transform

![fft](https://latex.codecogs.com/svg.image?I(\omega)=\int_{-\infty}^{\infty}C_{AA}(\tau)e^{-i\omega\tau}\,d\tau)

### Discrete FFT (used in MD)

![fft_disc](https://latex.codecogs.com/svg.image?I(\omega)=\text{FFT}[C_{AA}(\tau)])

### Convert Angular Frequency → Wavenumber

![wn](https://latex.codecogs.com/svg.image?\tilde{\nu}=\frac{\omega}{2\pi%20c})

where  
- \( \tilde{\nu} \) = wavenumber (cm⁻¹)  
- \( c \) = speed of light  

---

## 3. Steps to Compute Spectra from MD

### Step 1 — Extract a Time Series \(A(t)\)
Examples:
- Dipole moment → IR spectrum  
- Velocity → Vibrational DOS  
- Polarizability → Raman spectrum  
- Angular momentum → Rotational spectrum  

### Step 2 — Compute the Autocorrelation Function
From MD engine (e.g., GROMACS: `gmx analyze -ac`) or compute manually.

### Step 3 — Apply FFT to the ACF