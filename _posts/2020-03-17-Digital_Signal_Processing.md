---
name: Digital Signal Processing
use_math: false
heading1: Digital Signal Processing
motivation: Someday it will all make sense.
about: SP
---

Digital Signal Processing

## Digital Signal Processing

### What is Digital Signal Processing

#### Concept

##### Formal concept

> That discipline which has allowed us to replace a circuit previously composed of a capacitor and resistor with two antialiasing filters, an A-to-D and a D-to-A converter, and a general purpose computer (or array processor) so long as the signal we are interested in does not vary too quickly.   ~ Tomas P.Barnwell, 1974

##### Concise concept

We could describe the Digital signal processing is a process which is capable to turn a circuit into a signal where <u>the interesting part does not vary too much</u>. Besides it is based on representing signals by numbers. Operation in DSP include, but are not limited to, additions, multiplications, data transfers and logical operations.


### Why we need Digital Signal Processing

#### Analog data processing

##### Concept of Analog

A signal which is both continuous in <u>time domain and amplitude domain</u>. 

###### Continuous in amplitude domain

The amplitude of signal can take any real value in a certain range.

##### Concept of ASP

In this process, the analog signal are converted to voltage or currents by sensor and it will involve operation such as <u>amplification, filtering, integration, and differentiation, as well as forms of nonlinear processing (squaring, rectification)</u>

##### The drawback of ASP

* Accuracy limitation
* Limited repeatability
* Sensitive to electronic noise
* Limited dynamic range of valtage and currents
* Limited processing speeds due to physical delays
* Lack of flexibility to specification changes in the processing function
* Difficulty in implementing nonlinear and time-varying operations
* High cost and accuracy limitations of storage and retrieval of analog information

**DSP is designed to solve the drawbacks of ASP**

### Digital Signal Processing System

#### Prerequistes

1. Capability to convert analog signals into digital informations (a sequence of binary numbers)
    * it would include sampling and analog-to-digital (A/D) conversation
2. To perform numerical operations on the digital informations.
3. Capability to convert digital infromation, after being processed, back to analog signal.
    * it would include digital-to-analog conversation (D/A) conversation and reconstruction.

#### What does it looks like

![BasicDSP](/images/posts/DSP/Basic_DSP_Schemes.png)

##### General DSP system

It is the first DSP shown in the graph above. This system accepts analog input signal, converts it to a digital signal, processes it digitally and converts it back to analog signals. Its operations involves tasks such as filtering, mixing, and reverberation control. (**Pre-processing**)

##### Signal analysis system

It is the second DSP shown in the graph above. This systems are used for applications that require us to extract only certain information from the analog signal.(**Information Extraction**)

##### Signal synthesis system

It is the third DSP shown in the graph above. This systems are used when we need to generate an analog signal from digital information. (**Such as in Text-to-Speech system**)

##### Degenerate version of DSP system

It is purely digital, accepting and yielding digital information.

#### Drawbacks

* Sampling inevitably leads to loss of information, which cannot be completely avoided.
* A/D and D/A hardware maybe expensive
* programming bottleneck
* unable to meet speed requirement of certain application, such as Radio frequency signal (RF)


### History

* Fourier Transform -> Jean Baptisted Joseph Fourier, 1807, a paper in Institut de France
* Major theoretical -> Nyquist and Shannon, 1930 ~ 1940
* Fast Fourier Transform -> mid 1960 **The history of Applied digital signal processing began**
* The advent of microprocessors -> 1970s


### Citation

[1] “Introduction.” A Course in Digital Signal Processing: Solutions Manual to Accompany, by Boaz Porat, John Wiley &amp; Sons, 1997.

