### 量子输运note

张家健 2021

## Chapter 0: Introduction

This note is based on the lecture of quantum transport in mesoscopic system 2020 given by Prof Haizhou Lu. 

### Ohm's law

The conductance: 
$$
G = \sigma \frac{W}{L},\ \ J = \sigma E
$$
Where $W$ is the width of the bulk material, $L$ is the length of the bulk, $\sigma$ is the conductivity (it's material-dependent and dimension-independent), $J$ is the current density.

Ohm's law is an experimental law to describe the resistance/conductance of 3-dimension homogeneous bulk materials. In principle, it's a comprehensive effect of all the scattering in the bulk, but not a fundemental law. The motivation of this course is initially "how small $L$ or $W$ will Ohm's law break down?" Apparently it'll beak down in a microscopic system since current cannot be considered as a macroscopic phenomenon, but electrons scattering in lattice and atoms. However, experiments had shown that Ohm's law breaks down on the way of shriking up to that size, which means the changes happen in mesoscopic scale. This is what this course interested in. 

A conductor is usually Ohmic if it is larger than:

1. De Broglie length: $l\sim $ kinetic energy, since $\frac{2\pi}{k_F} = \lambda_F$
2. Mean free path: the distance that an electron travels before its momentum is changed.
3. Phase relaxation length (coherent length): the distance that an electron travels before its phase is destroyed.

A landmark experiment is the A-B ring (Washburn and Webb, 1986, Adv.Phys):

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210115111149133.png" alt="image-20210115111149133" style="zoom:33%;" />

with phase relaxation length $\sim$ several $\mu m$ to hundreds of $nm$.

This course will cover the following main contents:

1. Preliminary concepts
2. Well-known experiments
3. Several theoretical methods including:

1) Tight-binding model (in real space) + Green's functions

2) Linear-response theory: Kubo formula + Feymann diagrams (in momentum space)

## Chapter 1: Preliminary concepts

### Chapter 1.1      2DEG

A 2DEG can be trapped at the interface between two semi-conductors

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210115112955509.png" alt="image-20210115112955509" style="zoom:33%;" />

The energy band of certain semi-conductor. We can define Fermi-level as the highest position that electrons occupy. If the Fermi level is at (1), this is a N-type semi-conductor, because there are movable electrons acting as carriers. Filled up to (4), it is a P-type semi-conductor, holes act as carriers. In this course, up to (3) will be called an intrinsic semi-conductor, since the density of movable electrons and holes are equal. The Fermi level is at the top of valence band. Howver, Fermi level sometimes is defined on the center of the gap, (2). This definition is in two cases: 1. consider the average electron occupation distribution. $n_0 = N_Cexp(-\frac{E_C-E_F}{k_BT})$, $p_0 = N_Vexp(-\frac{E_F-E_V}{k_BT})$, when $n_0=p_0, N_C=N_V$, $E_F = \frac12(E_C+E_V)$. 2. consider the topological materials, the band can cross on the center.

The top of valence band and the bottom of conducting band are called the band edges. 

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210115125153329.png" alt="image-20210115125153329" style="zoom:33%;" />

The carrier concentration of 2DEG

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210115155749979.png" alt="image-20210115155749979" style="zoom:33%;" />

MODEF modulation doped field effect transistor

Gate: negative votage to deplete electrons below. Up is the intrinsic semi-conductor GaAs, down is the N-type AlGaAs. The thickness of the junction is about 100$nm$

#### Mobility

An electric field $E$ gives electrons a drift velocity $v_d$. The mobility is defined as the ratio $\frac{v_d}{E}$
$$
\left[\frac{d\vec{p}}{dt} \right]_{field} = \left[\frac{d\vec{p}}{dt} \right]_{scattering}
$$
The $\vec{p}$ on the left side is the momentum received for electric field. The right is the lost momentum due to scattering.

Define the momentum relaxation time $\tau_m$  by:
$$
\left[\frac{d\vec{p}}{dt}\right]_{scattering} = \ = e\frac{m\vec{v_d}}{\tau_m}\\
\left[\frac{d\vec{p}}{dt}\right]_{field}=e\vec{E}\\
\Longrightarrow\ \ \frac{m\vec{v_d}}{\tau_m} = e\vec{E}\\
$$
Therefore, the mobility is defined as $\mu \equiv \mid \frac{\vec{v_d}}{\vec{E}} \mid$

In massy system, it reduces to $\mu = \frac{\mid e\mid\tau_m}{m}$

In massless system, the definition $\mu \equiv \mid \frac{\vec{v_d}}{\vec{E}} \mid$ still holds. 

A table of several mobility:

| Topological semimetal                              | 2DEG GaAs-AlGaAs      | Graphene                                                     | Topological insulator                               |
| -------------------------------------------------- | --------------------- | ------------------------------------------------------------ | --------------------------------------------------- |
| $10^6cm^2/(v\cdot s)$(under liquid-He temperature) | $10^6cm^2/(v\cdot s)$ | $1.5\times10^4cm^2/(v\cdot s)$ (300K); $2\times10^5cm^2/(v\cdot s)$ (<10K) | $\propto10^2$ ($Bi_2Se_3$ at liquid He temperature) |

$v_x = \frac1\hbar\frac{\partial E}{\partial k_x}$,  $E=\frac{p^2}{2m}$,  $v=\frac1\hbar \frac{\hbar^2}{2m}2k = \frac{\hbar k}{m}=\frac{p}m$

### Chapter 1.2   Effective mass, DOS

#### Effective mass: 

To describe the electrons in the conduction band of a semi-conductor.
$$
[E_C + \frac{(i\hbar\vec{\nabla}+e\vec{A})^2}{2m} + U(\vec{r}) ]\psi(\vec{r}) = E\psi(\vec{r})
$$
The effective mass takes into account the effects of the lattice potential, spatial constant.

(1) "Free" electron

$U(\vec{r})=0,\ \ \vec{A}=0,\ \ E_C = constant$

wave function $\psi(\vec{r}) \sim e^{i\vec{k}\cdot\vec{r}}$

It's not Bloch wave because of the effective mass approximation: $\psi(\vec{r})=u_{\vec{k}}(\vec{r})e^{-i\vec{k}\cdot{\vec{r}}}$

(2) Subbands

Suppose there is a quantum well along the z direction, x-y is free

The wave function: $\psi(\vec{r}) = \phi_n(z)e^{ik_xx}e^{ik_yy}$

Energy spectrum: $E = \epsilon_n + \frac{\hbar^2 }{2m}(k_x^2+k_y^2)$

The quantum well in z direction quantize the spectreum along z direction. (symmetry breaking in z, the group representation split to the direct sum of some non-equivalent irreducible representation)

Some simple examples:

(1) Infinite square well

$\epsilon_n = \frac{\hbar^2}{2m}(\frac{n\pi}{a})^2$,  now $k_z$ is no more a good quantum number, it is quantized to $n\pi/a$,  a is the well width

(2) Harmonic oscillator

$\epsilon_n = (n+\frac12)\hbar\omega$

The wave function in x-y is still plane wave, but z-direction splits to levels, so the 3-dim spectrum (in K space) becomes a stacking of "bows", since the quadratic-form harmonic oscillator spectrum is like a bow, a confinement in z direction makes it splitting bows in total.

#### DOS

Consider the state sphere in K space. Divide the space to unit plaquettes, each plaquette is occupied by one state.

The area of an individual state in te $k_x-k_y$ plane is $(\frac{2\pi}{L})^2$, $L$ is the sample length width in real space

For given $E_F$, we can find $k_F$, the Fermi-wavevector

The number of electrons
$$
N_T(E_F) = 2\times \frac{\pi k_F^2}{(\frac{2\pi}{L})^2}=\frac1{2\pi}\frac{2mE_F}{\hbar^2}L^2
$$
2  is the spin degenracy.

DOS (per unit area in real space):
$$
N(E) = \frac1{L^2}\frac{d}{dE}N_T(E)=\frac{2\pi}{(2\pi)^2}\frac{2m}{\hbar^2}=\frac{m}{\pi\hbar^2}
$$
Conclusion: **For conventional electrons, width dispersion $p^2/2m$ in 2-dim, DOS is a constant independent of energy**

Problem: For Dirac Fermions in 2-dim, $H = \gamma(k_x\sigma_x + k_y\sigma_y )+\frac{m}2\sigma_z$

Find its DOS?

| DOS           | 1-dim                                 | 2-dim                           | 3-dim                                     |
| ------------- | ------------------------------------- | ------------------------------- | ----------------------------------------- |
| $p^2/2m$      | $\propto \frac1{\sqrt{E}}$            | $\propto \frac{m}{\pi\hbar^2}$  | $\propto\sqrt{E}$                         |
| Dirac Fermion | $\propto \frac{1}{2\sqrt{\pi}\gamma}$ | $\propto \frac{E}{\gamma^2\pi}$ | $\propto \frac{E^2}{2\sqrt{\pi}\gamma^3}$ |

 Von-Hove singularity: $\frac1{\sqrt{E}}\rightarrow0$ as $E\rightarrow0$

##### Degenerate & Non-degenerate Conductors

Fermi-Dirac Distribution: $f_0(E) = \frac{1}{1+exp((E-E_F)/(k_BT))}$

##### Two limits

(1) High Temperature (Non-degenrate limit)

$exp[(E_S-E_F)/(k_BT)]\gg 1$

$f_0(E)\approx exp[-(E_S-E_F)/(k_BT)]$

It's a Boltzman distribution

(2) Low temperature (Degenerate limit)

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210116110137277.png" alt="image-20210116110137277" style="zoom:43%;" />

For quantum transport, we focus on the degenerate limit.

Equilibruim electron density $n_S$ (also called the concentration $N_T(E)$)

$N_T(E)=n_S = \int_{-\infin}^{\infin} N(E)f_0(E)dE$

For degenerate conductors: (ex in 2-dim)
$$
n_S = \int_{-\infin}^{\infin}N(E)\theta(E_F-E)dE = \int_{E_S}^{E_F}N(E)dE = \frac{m}{\pi\hbar^2}(E_F-E_S)
$$
$E_s$ is the band bottom.

### Chapter 1.3  Characteristic Lengths

(1) Fermi wavelength $\lambda_F = \frac{2\pi}{k_F}$
$$
n_S = \frac{m}{\pi\hbar^2}\frac{\hbar^2}{2m}k_F^2\Longrightarrow k_F = \sqrt{2\pi n_S}\\
\lambda_F\approx 35nm
$$
(If $n_S=5\times10^{11}/cm^2$)

(2) Mean free path $L_m$

Average distance before momentum is changed
$$
L_m = v_F\tau_m 
$$
$v_F$: Fermion velocity,  $\tau_m$: momentum relaxation time (should be transport time)

Dirac Fermion: intrinsic anisotropic scattering

Conventional electron: isotropic

##### The transport time

relaxation

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210116214011918.png" alt="image-20210116214011918" style="zoom:39%;" />
$$
\tilde{v}_k=v + \sum_{k'}\tilde{v}_k G_{k'}^R G_{k'}^A\langle U_{kk'}U_{k'k}\rangle
$$
The Feynmann diagram of a scattering (dash line), the velocity after it can be expressed as above. The second term is an iteration equation.
$$
\frac{\tilde{v}}{v} = \frac{\tau_{tr}}{\tau_m}\\
L_m = v_F\tau_{tr} = \tilde{v}v_m\\
$$
For $\frac{p^2}{2m}$ and isotropic scattering, $\tau_m = \tau_{tr}$

For anisotropic scattering, $\tau_m\neq \tau_{tr}$

For 2DEG, $n_S = 5\times10^{11}/cm^2$
$$
v_F = \frac{\hbar k_F}{m} = \frac{\hbar^2}{m}\sqrt{2\pi n_S} = 3\times10^{7}/cm^2\\
L_m\approx30\mu m
$$
If $\tau_m\approx 100ps$, it is very long. This is in a very pure sample. In normal samples, the disorder will make it $1ps$

In topological insulators, $L_m\approx 10nm$, In Graphene, $L_m\approx 26\mu m$

(3) Phase relaxation (coherent) length (PCL)

If scattering is elastic, there is no energy relaxation, if scattering is unelastic, threre is relaxation.

##### How to measure the Phase coherent time (PCT) or PCL?

(1) One method: A-B ring

Consider a thought experiment:

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210117012816563.png" alt="image-20210117012816563" style="zoom:33%;" />

The A-B phase amplitude will oscillate with the change of magnetic field $B$. 

Amplitude$\propto exp[-\frac{\tau_t}{\tau_\varphi}]$, $\tau_t$ is the time spent travelling in the ring.

(2) Weak localization

(3) Universal conductance fluctuation

These three methods are all used to measure $\tau_\varphi$ ($\tau_\varphi$ changes from $\infin$ to finite)

#### Mechanism leading to decoherence

##### Elastic scattering: does not

Static impurities, defects (disorders)

##### Inelastic scattering: does (Dynamical Scatters)

1）Phonons-electron interaction

2)  Electron-electron interaction

3)  Magnetic inpurities (spin, angular momentum) (internal degrees of freedom)

If the phase relaxation time is in the same order as the momentum relaxation time, or shorter, often in high-mobility semi-conductors, namely $\tau_{\varphi}\sim \tau_m, \tau_{\varphi}<\tau_m$, we have similarly $L_{\varphi} = v_F\tau_{\varphi}$

Howver, this is wrong if $\tau_{\varphi}\gg \tau_m$, often in low-mobility semi-conductors. In this case, the phase coherent length can be defined by:
$$
L_{\varphi} = \sqrt{D\tau_{\varphi}}\\
D = \frac12 v_F^2\tau_m
$$
Here is the 2-dim case. 

How to calculate $\tau_{\varphi}$, $l_{\varphi}$  as a function of temperature for different mechanisms of decoherence is a long story.

### Chapter 1.4  Low-field magnetoresistance

##### Magnetoresistance:

Defined as the change of eleresistance with magnetic field

#### Drude model

Electrons under influence of $\vec{E},\vec{B}$, impurities scattering, disorder

For electric field parallel to the 2-dim material (in the plane), and magnetic field perpendicular to the plane, we have
$$
\frac{m\vec{v_d}}{\tau_m} = e[\vec{E}+\vec{v_d}\times\vec{B}]\\
\vec{E} = (E_x, E_y, 0)\\
\vec{B} = (0,0,B)\\
\vec{v_d} = (v_x, v_y, 0)\\
\vec{v_d}\times\vec{B} = \hat{i}v_y B + \hat{j}(-v_x B)\\
\frac{m}{\tau_m}(V_x, V_y)^T = e(E_x,E_y)^T + e(V_y B, -V_x B)^T\\
\Longrightarrow
\left[
\begin{matrix}
\frac{m}{e\tau_m} & -B\\
B & \frac{m}{e\tau_m}
\end{matrix}
\right]
\left[
\begin{matrix}
V_x \\ V_y
\end{matrix}
\right]=\left[
\begin{matrix}
E_x \\ E_y
\end{matrix}
\right]
$$
Define the current density $\vec{J}$ per unit width:
$$
\vec{J}\equiv e\vec{v_d}n_s = en_s\left(\begin{matrix}V_x\\V_y \end{matrix} \right)
\Longrightarrow
\left(
\begin{matrix}
V_x\\V_y
\end{matrix}
\right)=
\left(
\begin{matrix}
J_x/(en_s)\\ J_y/(en_s)
\end{matrix}
\right)\\
\left[
\begin{matrix}
\frac{m}{e\tau_m} & -B\\
B & \frac{m}{e\tau_m}
\end{matrix}
\right]
\left[
\begin{matrix}
J_x \\ J_y
\end{matrix}
\right]\frac{1}{\mid e\mid n_s}
=\left[
\begin{matrix}
E_x \\ E_y
\end{matrix}
\right]
$$
Define the mobility as: $\mu \equiv \frac{\mid e\mid \tau_m}{m}$,  zero-field conductivity as: $\sigma\equiv \mid e\mid n_s\mu$
$$
\left[
\begin{matrix}
1 & -\mu B\\
\mu B & 1
\end{matrix}
\right]
\left[
\begin{matrix}
J_x \\ J_y
\end{matrix}
\right]\frac{1}{\mid e\mid\mu n_s}
=\left[
\begin{matrix}
E_x \\ E_y
\end{matrix}
\right]\\
\left[\mu\right] = cm^2/(v\cdot s) = \left[\frac1B \right] (Dimension)
$$
$v$ is in the unit of Volt, s is in the unit of second.  

Define $\rho_{xx}\equiv E_x/J_x$, $\rho_{xy} \equiv E_x/J_y$, $\rho_{yx} \equiv E_y/J_x$, $\rho_{yy} \equiv E_y/J_y $, the resistivity tensor: $\left(\begin{matrix}\rho_{xx} & \rho_{xy}\\ \rho_{yx} & \rho_{yy}  \end{matrix} \right)$

$\rho_{xx} = \rho_{yy} = \frac1\sigma$, where $\sigma$ is the zero-field conductivity. $\rho_{yx} =- \rho_{xy}= \frac{\mu B}{\sigma} = \frac{B}{\mid e\mid n_s}$

The conductivity tensor can be defined as: $\left(\begin{matrix}\sigma_{xx} & \sigma_{xy}\\ \sigma_{yx} & \sigma_{yy} \end{matrix} \right) = \left(\begin{matrix}\rho_{xx} & \rho_{xy}\\ \rho_{yx} & \rho_{yy}  \end{matrix} \right)^{-1} $

$\sigma_{xx} = \frac{\rho_{xx}}{\rho_{xx}^2 + \rho_{xy}^2} = \frac{\sigma}{1+(\mu B)^2}$,  $\rho_{xy} = \frac{\rho_{xy}}{\rho_{xx}^2+\rho_{xy}^2} = \frac{\sigma\mu B}{1+(\mu B)^2}$

#### Problem: two-current model

For two types of carriers:

$\sigma_{xx}^{(1)} = \frac{\sigma_1}{1+(\mu_1 B)^2}$,  $\sigma_{xy}^{(1)} = \frac{\sigma_1\mu_1 B}{1+(\mu_1 B)^2}$,  $\sigma_{xx}^{(2)} = \frac{\sigma_2}{1+(\mu_2 B)^2}$,  $\sigma_{xy}^{(2)} = \frac{\sigma_2\mu_2 B}{1+(\mu_2 B)^2}$,  where $$









