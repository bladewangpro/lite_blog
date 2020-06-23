---
layout: default
name: home_page
use_math: true
heading1: THE BAND
heading2: we love music
motivation: Someday it will all make sense.
---

## Analog signal

Definition:
Signals continuous in time and amplitude can called analog signals.(Continuous on amplitude means it can take any real value in a certain range)

Manifestation:
Voltages or currents by being address via sensor or transducer in order to be processed electrically.

Operations:
Analog processing of electrical signals is typically based on electronic amplifier and which involves operations such as amplification, filtering, integration and differentiation as well as various form of nonlinear processing(squaring, rectification).

Drawbacks:
1. Accuracy limitation
2. Limited repeatability
3. Sensitivity to electrical noise
4. Limited dynamic range of voltage and currents
5. Limited processing speed due to physical delay
6. Lack of flexibility to sepcification changes in the processing function
7. Difficulty in implementing nonlinearand time-varying operation
8. High cost and accuracy limitation of storage and retrieval of analog information


## Digital signal

Definition:
Signals represented by numbers in a computer(or in specialized digital hardware)

Operations:
Digital Signal Processing is based on Digital signal and performing various numerial operations on these signals. Operations include, but are not limited to, addtions, multiplications, data transfers, and logical operations.

## DSP system

1. To convert analog signls into digital information, in the form of a sequence of binary numbers. (Sampling and analog-to-digital conversion.)
2. To perform numerical operations on the digital information, either by a computer or special-purpose digital hardware
3. To convert the digital information, after being processed, back to an analog signal. This again involves two operations: (D/A conversion and reconstruction).


### Basic DSP schemes

1. [General signal processing system]

    (Analog Signal)--sampling--(Digital Signal)--DSP--(Digital Signal)--Digital/analog conversion {Reconstruction}--(Analog Signal)
2. [Signal analysis system]

    (Analog Signal)--sampling--(Digital Signal)--DSP--(Digital information)
3. [Signal synthesis system]

    (Digital information)--DSP--(Digital Signal)--reconstruction--(Analog Signal)
4. [Purely digital DSP]

    (Digital signal)--DSP--(Digital Signal)

## Formular

$\mathbb{R}$ --> the real line
$\mathbb{C}$ --> the complex plane
$\mathbb{Z}$ --> the set of integers

### Convolution

The convolution of continuous-time signals is (whenever the right side exists)

$\{x*y\}(t) = \int_{-\infty}^{\infty}x(\tau)y(t-\tau)d\tau, t\in \mathbb{R}$

**The convolution is to detect the overlapped area of two figures, if these two figures is not overlapping with each other, then their multiplication will be zero**

### Transforms

1. Laplace transform of the continuous-time signal x(t) is 
$X^L(s) = \int_{-\infty}^{\infty}x(t)e^{-st}dt, s\in \mathbb{C}$, whenever the right side exists.

2. The Fourier transform of the continuous-time signal x(t) is
$X^F(\omega) = \int_{-\infty}^{\infty}x(t)e^{-j\omega t}dt, \omega\in\mathbb{R}$, whenever the right side exists.

3. The inverse Fourier transform is 
$x(t) = \frac{1}{2\pi}\int_{-\infty}^{\infty}X^F(\omega)e^{j\omega t}d\omega, t\in\mathbb{R}$

> When both Laplace and Fourier transform exist, $X^F(\omega) = X^L(j\omega)$

4. The Fourier transform of the continuous-time signal x(t) on the interval [0, T] (or of its periodic extension) is $X^S[k] = \frac{1}{T}\int_{0}^{T}x(t)exp(-\frac{j2\pi kt}{T})dt, k\in\mathbb{Z}$.

5. The inverse relationship is 
$x(t) = \sum_{k=-\infty}^{\infty}X^S[k]exp(\frac{j2\pi kt}{T}), 0\leq t \leq T$.

> $\omega == \frac{2\pi k}{T}$

6. The z-transform of the discrete-time signal x[n] is 
$X^z(z) = \sum^{\infty}_{n=-\infty}x[n]z^{-n}, z\in\mathbb{C}$, whenever the right side exists.

7. The Fourier transform of the discrete-time signal x[n] is 
$X^{f}(\theta) = \sum^{\infty}_{n = -\infty}x[n]e^{-j\theta n}, \theta\in\mathbb{R}$, whenever the right side eixsts.

8. The inverse Fourier transform of discreate-time signal x[n] is 
$x[n] = \frac{1}{2\pi}\int^{\pi}_{-\pi}X^{F}(\theta)e^{j\theta n}d\theta, n\in\mathbb{Z}$

9. When both z- and Fourier transform exist, 
$X^f(\theta) = X^z(e^{j\theta})$

10. The **discrete Fourier transform of the finite-duration, discrete-time signal ${x[n], 0\leq n \leq N-1}$** is 
$X^d[k] = \sum_{n=0}^{N-1}x[n]exp(-\frac{j2\pi kn}{N}), 0\leq k \leq N-1$

11. The **inverse discrete Fourier transform of the finite-duration, discrete-time signal ${x[n], 0\leq n \leq N-1}$** is 
$x[n] = \frac{1}{N}\sum_{k=0}^{N-1}X^d[k]exp(\frac{j2\pi kn}{N}), 0\leq n \leq N-1$


## Sufficient and necessary conditions

1. If p then q, then p is a sufficient condition of q;
2. If p, not q and if q then p, then p is a necessary condition of q;
3. if p, then q and if q then p, then p is a sufficient and necessary condition of q

## Frequency-Domain Analysis

### Fourier Series

#### Conventional Fourier Series (Complex)

#### Cosine and Sine Fourier Series (Real)

### Continuous-time signals and system

#### Defintion

Let x(t) be a continuous-time signal whose value can be **real or complex**. 

$X^{F}(\omega) = \int^{\infty}_{-\infty}x(t)e^{-j\omega t}dt, \omega\in\mathbb{R}$ and its sufficient condition is 
$\int^{\infty}_{-\infty}|x(t)|dt<\infty$

> The varible $\omega$ is **angular frequency** and is measured in radians per sec (rad/s). The variable $f=\omega/2\pi$ are frequency and is measured in hertz (Hz)

**And if the following conditions together are true, the IFT exists**

1. x(t) satisfy $\int^{\infty}_{-\infty}|x(t)|dt<\infty$
2. x(t) is continuous, except the function satisfying the following conditions together
    * discontinuity points whose number on any finite interval is finite;
    * the limits at both sides of each discontinuity point exist.
3. x(t) has a finite number of minima and maxima on any finite interval

#### Main properties of the Fourier Transform
1. Linearity

$z(t) = ax(t) + by(t) \leftrightarrow Z^F(\omega) = aX^F(\omega) + bY^F(\omega), a, b \in \mathbb{C}$

2. Time shift

$y(t) = x(t-\tau) \leftrightarrow Y^F(\omega) = e^{-j\omega\tau}X^F(\omega), \tau\in\mathbb{R}$

3. Frequency shift

$y(t) = e^{j\lambda t}x(t) \leftrightarrow Y^F(\omega) = X^F(\omega - \lambda), \lambda\in\mathbb{R}$

4. Time and frequency scale

$y(t) = x(at) \leftrightarrow Y^F(\omega) = \frac{1}{|a|}X^F(\frac{\omega}{a}), a\in\mathbb{R}, a\ne0$

5. Time-domain convolution

$z(t) = \{x*y\}(t) \leftrightarrow Z^F(\omega) = X^F(\omega)Y^F(\omega)$

6. Time-domain multiplication

$z(t) = x(t)y(t) \leftrightarrow Z^F(\omega) = \frac{1}{2\pi}\{X^F*Y^F\}(w)$

> Convolution on time zone is the multiplication on the frequency zone, and Multiplication on time zone is the convolution on the fequency zone

7. Parseval's theorem

> where the bar denotes complex conjugation and its special case

$\int^{\infty}_{-\infty}x(t)\overline{y}(t)dt = \frac{1}{2\pi}\int^{\infty}_{-\infty}X^F(\omega)\overline{Y}^F(\omega)d\omega$

$\int^{\infty}_{-\infty}|x(t)|^2dt = \frac{1}{2\pi}\int^{\infty}_{-\infty}|X^F(\omega)|^2d\omega$

8. Conjugation

$y(t) = \overline{x}(t)\leftrightarrow Y^F(\omega) = \overline{X}^F(-\omega)$

9. Symmetry If x(t) is real valued then

$X^F(-\omega) = \overline{X}^F(\omega)$

$\Re\{X^F(-\omega)\} = \Re\{X^F(\omega)\}$

$\Im\{X^F(-\omega)\} = -\Im\{X^F(\omega)\}$

$|X^F(-\omega)| = |X^F(\omega)|$

$\measuredangle X^F(-\omega) = -\measuredangle X^F(\omega)$

where $\Re$ denotes the real part, $\Im$ denotes the imaginary part, and the $\measuredangle$ denotes the angle of the corresponding complex number

10. Realness

$x(t) = \overline{x}(-t) \leftrightarrow X^F(\omega)$ is real

## Signal Concept

> The mathematical formula is an approximate of the real situations.

### A dynamic system (or simply a system) *mathematical operator*

An object that accepts signal, operates on them and yield other signals.

### Premise of all the book

a continuous-time, single input, single output (SISO) system is an operator that assign to a given input x(t) to a unique output y(t).

#### Linear Property

**If a SISO system is said to be linear if it satisfies Additivity and Homogeneity properties**

1. If $y_i(t)$ is the response to $x_i(t)$, then the response of $x_1(t) + x_2(t)$ is $y_1(t) + y_2(t)$
2. If $y(t)$ is the response to $x(t)$, then the response to $ax(t)$ is $ay(t)$ for all a

#### Time invariance

**Shifting the input signal in time by a fixed amount causes the same shift in time of the output signal**

1. If $y(t)$ is the response to $x(t)$, then the response to $x(t-t_0)$ is $y(t-t_0)$ for every fixed $t_0$

> If a system is both linear and time invariant is called linear time invariant or LTI.


### Impulse (or delta) function $\delta(t)$

**A countinuous-time signal of great importance**

$\int^{\infty}_{-\infty}f(t)\delta(t)dt = f(0)$ for any function f(t) is continuous at t = 0.

The Delta function $\delta (t)$ may or may not be the input family of the input family of a given LTI system. **If it is**, we denote by $h(t)$ the response to $\delta (t)$ and call it the impulse response of the system. 

If the impulse response of an LTI system exists, it completely characterizes the input-output relationship of the system..

Given an input signal x(t), the so-called zero-state output signal $y(t)$ is the convolution $y(t) = \{h*x\}(t)$. The signal is in the input family of the system if and only if the right side of this previous formula exists.

The frequency response of an LTI system is the Fourier transform $H^F(\omega)$ of the impulse response. The frequency-domain counterpart of the previous formula is $Y^F(\omega) = H^F(\omega)X^F(\omega)$

**Not every LTI system processing an impulse response necessarily has frequency response, since $H^F(\omega)$ may not exist, For example, the frequency response of a system whose impulse is $h(t) = e^t$ is not defined**

## Specific Signals and their Transform 

### Delta Function and DC Function

**Delta Function**

For any function $f(t)$ that is continuous at $t=0$, $\int_{-\infty}^{\infty}f(t)\delta(t)dt = f(0)$, The $\delta(t)$ is called the impulse (or delta) function.

**DC Function**

The function whose value is 1 for all t is called the DC function, and will be denoted by $1(t), DC stands for direct current.$

1. Fourier Transform 

For Delta Function: $\int^{\infty}_{-\infty}\delta(t)e^{-jwt}dt = 1$

For Direct Current Function: $2\pi\delta(\omega)$

For a constant A: $f(t)=A\leftrightarrow F(\omega) = A2\pi\delta(\omega)$

### Complex Exponentials and Sinusoids

The complex exponential function is $x(t)=e^{j\omega_0t}$

**The parameter $\omega_0$ is the angular frequency of the complex exponential; it is a real number, either positive or negative. When $\omega_0=0$ we get the DC function**

1. Fourier Transform

According to $y(t) = e^{j\lambda t}x(t) \leftrightarrow Y^F(\omega) = X^F(\omega-\lambda), \lambda\in\mathbb{R}$ and $1^F(w) = 2\pi\delta(\omega)$, we can get the FT of this complex exponiential function is $X^F(\omega) = 2\pi\delta(\omega-\omega_0)$

### Sinusoidal function has the general form $x(t) = Acos(\omega_0t+\phi_0)$

A -- The amplitude

$\omega_0$ -- The angular frequency

$\phi$ -- The initial phase

#### Two Eular formulas

$cos(\omega_0 t) = \frac{1}{2}(e^{j\omega_0 t} + e^{-j\omega_0 t})$

$sin(\omega_0 t) = \frac{1}{2}j(e^{-j\omega_0 t} - e^{j\omega_0 t})$


#### Super Important

<u>When a sinusoidal signal at frequency $\omega_0$ is fed to a real LTI system, The output is a sinusoidal signal at the same frequency. The retial of magnitudes of the output and input signals is the magnitude response of the system at $\omega_0$, and the difference in phases is the phase response of the system at $\omega_0$</u>

**Because of the special characteristics above, sinusoidal signals are said to be eigenfunctions of LTI system.**

#### The rect and sinc

**The rectangular function or rect (also known as box, boxcar, or pulse)**

$rect(t) = \begin{cases}1,&|t| < 0.5,\\ 0.5,&|t|=0.5,\\0,&|t|>0.5.\end{cases}$

$sinc(t) = \begin{cases}\frac{sin(\pi t)}{\pi t}, & t\ne0,\\1,&t=0.\end{cases}$

The FT of rect function is $rect^F(\omega) = sinc(\frac{\omega}{2\pi})$

The FT of sinc function is $sinc^F(\omega) = rect(\frac{\omega}{2\pi})$

#### Gausian Function $g(t) = e^{-0.5t^2}, t \in\mathbb{R}$

The Fourier transform of the Gaussian function is $G^F(\omega) = \sqrt{2\pi}e^{-0.5\omega ^ 2}$

**The Gaussian is a rare example of a signal and its Fourier transform being both real and positive valued for all t and $\omega$.**

### Continuous-Time Periodic Signals

#### Defintion

A continuous-time signal x(t) is said to be periodic if there exists T > 0 such that $x(t) = x(t + T), for all t\in\mathbb{R}$, The smallest T for which holds is called period. 


**When the input signal of an LTI system is periodic, the output (if exists) is also a periodic signal.**

The Fourier Transform is an LTI system

#### The Impulse Train

**Definition**

The impulse train $p_T(t)$ == $\sum_{n=-\infty}^{\infty}\delta(t-nT)$, where T is a positive constant, called period.

> an alternative expression for the impulse train is given by the **Poisson sum formula**, $p_T(t) = \sum_{k = -\infty}^{\infty}\delta(t-nT) = \frac{1}{T}\sum^{\infty}_{k = -\infty}exp(\frac{j2\pi kt}{T})$

## Formular

### Inverse Fourier Transform

$x[n] = \frac{1}{2\pi}\int_{-\pi}^{\pi}X^f(\theta)e^{j\theta n}d\theta,\; n \in \mathbb{Z}$                  (2.95)

## Definition

**Analog signal:** the signal continuous in time and amplitude.
    1. continuous on amplitude: the amplitude could take any real value in a certain range
    



```python

```
