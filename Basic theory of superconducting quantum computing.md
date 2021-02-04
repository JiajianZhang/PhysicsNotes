# Basic theory of superconducting quantum computing

### Heisenberg model

$$
H = A_x \sigma_x\sigma_x + A_y \sigma_y\sigma_y + A_z \sigma_z\sigma_z
$$

How do we act the evolution with this Hamiltonian on a two-qubit system? (how to decompose the time-evolution to a set of unitary transformations (quantum gates))

Set all constants to 1.
$$
H_1 = \frac12 (\sigma_x\sigma_x + \sigma_y\sigma_y)\\
H_2 = \frac12 (\sigma_y\sigma_y + \sigma_z\sigma_z)\\
H_3 = \frac12 (\sigma_x\sigma_x + \sigma_z\sigma_z)\\
$$

In a infinitesimal time scale t, we have approximation: $e^{\hat{A}+\hat{B}} \approx e^{\hat{A}}e^{\hat{B}}$, so:
$$
e^{-iHt}\approx e^{-i H_1t}e^{-i H_2t}e^{-i H_3t}\\
$$
Define: $U_1\equiv exp(-iH_1t)$

Now we can add rotating operations to this $U_1$ to obtain the other two time-evolution operators corresponding to $H_2,H_3$
$$
e^{-i H_2t} = e^{i\sigma_y \frac{\theta}{2}\sigma_y \frac{\theta}2} U_1 e^{-i\sigma_y \frac{\theta}2 \sigma_y \frac{\theta}2}\\
e^{-i H_3t} = e^{i\sigma_x \frac{\theta}2\sigma_x \frac{\theta}2} U_1 e^{-i\sigma_x\frac{\theta}2 \sigma_x \frac{\theta}2}\\
$$
 Here $\theta = \frac{\pi}2$, means that the axes are rotated along certain axes by $\frac{\pi}2$, which will lead to a permutation of x, y, z. 

The quantum circuit of this process can be expressed as:

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210119154145492.png" alt="image-20210119154145492" style="zoom:40%;" />

## Random process

### Classical case

The expectation is defined by: $E[X] \equiv \int dx p(x)X(x) = \mu$

The variance can be defined by: $\Delta X \equiv E[x^2] - (E[x])^2$

The co-variance can be defined by: $E[XY] \equiv \int dxdy X(x)Y(y) p(x,y) $

Define a time line: $t_1,t_2,t_3...t_n$,  and variables: $X_1, X_2, X_3...X_m$

#### Stationary process

Two requirements: (1) variance: $E[X_i(t_j)] = E[X_i(t_k)]$;  (2) co-variance: $E[X_i(t_j),X_i(t_k)] = E[X_i(t_j+h),X_i(t_k+h)]$

Self-correlation function: (the fluctuation between two time points)
$$
C(t_1,t_2) = E[X(0),X(t_2-t_1)]-\mu^2\\
$$
Based on this correlation function, we can define the power spectrum density (PSD) , as the Fourier transformation:
$$
S(\omega) = \int C(\Delta t)e^{-i\omega t}d\Delta t
$$
In this stationary process, the PSD can be approximately written as: (take $\Delta t$ as $t$)
$$
S(\omega) = \int_{-\infin}^{\infin} C( t)e^{-i\omega t}dt \approx \frac{\mid X(\omega)\mid^2 }{T}\\
X(\omega) = \int_{-\infin}^{\infin} X(t) e^{-i\omega t}dt
$$

##### Example: telegram noise

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210120154117530.png" alt="image-20210120154117530" style="zoom:33%;" />

The noise happens like square wave, only flip between 0 and 1.

The self correlation function and PSD are:
$$
C(t) = e^{-\mid t/\tau\mid}\\
S(\omega) = \frac{1}{1+(\omega\tau)^2}
$$
$\tau$ is certain characteristic coherent correlation time, and the PSD here is in a Lorentz form.

Question: the Fourier transformation of $C(t)$ may be a complex function, should we take the real part or modular? Notice that $C(t)$ is a function symmetric along the y-axis. Therefore, if we do the integral from $-\infin$ to $\infin$, the imaginary part of the integrated function will cancel. 

##### Example: Bernoulli distribution

Only two possible value, 0 and 1, with probability $\frac12$ each. 

$\sigma = p(1-p)$, for instance, we sample the system 400 times, then the variance will be $\sigma^2/400$, the standard deviation is $\sigma/\sqrt{400} = 0.025$

### Quantum case

Define the correlation function as: $C(t) = \langle \hat{X}(0),\hat{X}(t)\rangle$

Consider the simplest case, a mixed state, $\mid0\rangle\langle 0\mid$ with probability $p_0$, $\mid1\rangle\langle1\mid$ with probability $p_1$. 

The PSD: $S(\omega)\equiv \int_{-\infin}^{\infin}\langle \hat{X}(o),\hat{X}(\tau)\rangle e^{-i\omega\tau}d\tau $

Given a simple example, Hamiltonian is $H = \frac12\omega_0\sigma_z$

And choose $\sigma_x$ to take the correlation function, use $\sigma_x(\tau) = e^{i\omega_0 \tau}\sigma_x(0)e^{-i\omega_0 \tau} $ , then we obtain $\langle\hat\sigma_x(0),\hat\sigma_x(\tau)\rangle = \langle(\sigma_++\sigma_-)(\sigma_+e^{i\omega_0 t} + \sigma_-e^{-i\omega_0 t})\rangle = p_0 e^{i\omega_0 \tau} + p_1 e^{-i\omega_0\tau}$

Turn out to be: 
$$
S(\omega) = \int_{-\infin}^{\infin}(p_0 e^{i\omega_0 \tau} + p_1 e^{-i\omega_0\tau})e^{-i\omega\tau}d\tau\\
= p_0\delta(\omega - \omega_0) + p_1\delta(\omega+\omega_0)
$$

## Open quantum system

#### Interpret open-system dissipation as quantum channel

$\varepsilon(\rho) = (1-2p)\gamma_x\sigma_x + (1-2p)\gamma_y\sigma_y + \sigma_z$

$\varepsilon^N(\rho) = (1-2p)^N\gamma_x + (1-2p)^N\gamma_y  $

The probability and transition rate have the relation: $2p = \Gamma \Delta t$

The evolution of density matrix can be written as the equation of motion. The first term is the evolution in a closed system (energy conserving). The ellipsis is the dissipation 

$\dot{\rho}(t) = \mathcal{L}(t) = i[\rho,H]+...$

The dissipation is covered in the Liouvillion 

#### Bloch equation

(It's a simple example...)
$$
\dot{r}_x = -\omega_0 r_y - \Gamma_2 r_x\\
\dot{r}_y = \omega_0 r_x - \Gamma_2 r_y\\
\dot{r}_z = 0 - \Gamma_1(r_z - \bar{r}_2)\\
(\bar{r}_2 = r_2(\infin))
$$
Pure dephasing: only diagonal elements of the density matrix have dissipation factors.

Pure decoherence: only non-diagonal elements have dissipation factors (impossible). If there is no dephasing process, only state decaying from $\mid1\rangle$ to $\mid0\rangle$, then the routine of the decaying will be a straight line, this is not allowed. Another relation is $\Gamma_1 = \Gamma_2/2$

### Redfield theory and Lindblad equation

Firstly, we can introduce the interaction picture of state evolution. The effective Hamiltonian of is: 
$$
H_I = U^\dagger V U = U^\dagger H_S U - H_0= V_I
$$
So the density matrix is $\frac{d\rho}{dt} = -i[V_I,\rho_I]$ (It's a generalized form of ratating frame in multi-level systems)

However, the measurement is finally done in the lab frame, the equation of motion (with on dissipation) is:
$$
\frac{d\rho_S(t)}{dt} = -\int_0^t dt' Tr_E\{V_I(t),[V_I(t),\rho_S(t)\otimes\rho_E]] \}\\
=- \sum_{k,n}\int_0^t dt'\{\langle \tilde{B}_k(t)\tilde{B}_n(t') \rangle_E [\hat{A}_k(t), \hat{A}_n(t')\rho_S(t)] - \langle\hat{B}_n(t')\hat{B}_k(t)_E [\hat{A}_k(t),\rho_S(t)\hat{A}_n(t')] \}\\
$$
If we define the initial state as: $\rho_S = \left[\begin{matrix}\rho_{uu} & \rho_{ud}\\ \rho_{du} & \rho_{dd} \end{matrix}\right]$

u means spin up state, d means spin down state.

For a simple example, 
$$
[\sigma_x(t), \sigma_x(t')\rho_S(t) ]\\
=e^{i\omega_0\tau} 
\left[ 
\begin{matrix}
\rho_{uu} & \rho_{ud}\\ 0 & -\rho_{uu}
\end{matrix}
\right] + 
e^{-i\omega\tau}
\left[
\begin{matrix}
-\rho_{dd} & 0 \\ \rho_{du} &\rho_{dd}
\end{matrix}
\right][{1}]\\
+ e^{i\omega\tau} 
\left[
\begin{matrix}
\rho_{dd} & -\rho_{ud}\\ 0 & -\rho_{dd}
\end{matrix}
\right]+
e^{-i\omega_0\tau}
\left[
\begin{matrix}
-\rho_{uu} & 0 \\ -\rho_{du} &\rho_{uu}
\end{matrix}
\right][2]
$$
Consider the total Hamiltonian of the system is $H_{tot} = H_E + H_S = \frac12\omega_0\sigma_z + \sum_{\omega_a} \omega_a a^{\dagger}_{\omega} a_{\omega}$, where the potential is: $\hat{V} = g\sigma_x \sum_{\omega} (a^{\dagger}_{\omega}+ a_{\omega}) $
$$
\frac{d\rho_S(t)}{dt} = -\int_0^t d\tau \int_{-\infin}^{\infin} d\omega \{S(\omega) e^{-i\omega\tau} [1] - S(\omega)e^{i\omega\tau}[2] \}
$$

## Noise introduced in what direction and frequency contribute to the decaying of  Rabi oscillation?

###  Noise in the rotating frame

The driving part of the Hamiltonian in $\sigma_x$ direction results in the Rabi oscillation, with Rabi frequency $\Omega$

A simple way to this problem is to treat the driving Hamiltonian as a qubit in x direction with qubit frequency $\Omega$, the decay can be interpreted as a $T_1$ and $T_2$ relaxation. 

With the first order Born approximation and Markovian approximation, we have the  relaxation rate:
$$
\frac1{T_{Rabi}} = \frac1{2T_{1R}} + \frac1{T_{\varphi R}}\\
$$
The first term is contributed by the "energy relaxation" process, in the rotating frame, it's along $x'$ direction. the corresponding noise term in the Hamiltonian should be the "non-diagonal elements", namely the directions perpendicular to the $x'$ direction ( $y',z'$ plane). The noise frequency contributes to this is $\Omega$, thus the PSD can be written as: $S_{\perp x'}(\Omega)$. The second term is the "dephasing" process, the noise frequency contributing to this is 0, and the diagonal elements of the Hamiltonian, thus the PSD can be written as: $S_{x'}(0)$

### Noise in the lab frame

The noise above can be expressed in the lab frame. In the weak driving limit ($\omega_0 \gg \Omega$), we have:
$$
S_{\perp x'}(\Omega) \rightarrow S_{x,y}(\omega_o \pm\Omega) + S_z(\Omega)
$$

## Pure dephasing

The pure $T_2$ decay curve is exponentially under Born approximation and Markovian approximation according to the deduction above. However, in most situations, the decay curve is Gaussian, what is the difference?

In a Ramsey experiment, we can find the $T_2$ by cycles. Firstly we act a $\pi/2$ pulse to rotate the $\mid0\rangle$ state to $\frac1{\sqrt2}(\mid0\rangle + \mid1\rangle)$, on the equator plane, and wait for time $\tau$, the pure dephasing will make the state spray out, the averaged length of the state vector will shrink. After this, act another $\pi/2$ pulse to rotate the state to $\mid1\rangle$, then immediately do the measurement, find the population of the state, it will display how much the state has decayed. Then we wait for about 100 $\mu s$, the qubit will relax to the ground state, one cycle ends. We can repeat the cycles to obtain the 

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210201171532508.png" alt="image-20210201171532508" style="zoom:33%;" />

Suppose the correlation time of the noise is $\tau_C$, namely in this time, the noise can be considered as a constant. If $\tau\ll \tau_C$, we call it is quasi-static, the noise measured in $\tau$ is almost static. 

### How to obtain the average $T_2$? 

Assume that the qubit frequency fluctuation is $\delta\omega_0^{(i)}$ in the $i$th Ramsey experiment. According to the central limit theorem, the distribution of $\delta\omega_0$ is Gaussian. The phase accumulated in time $\tau$ is $\delta\omega_o\tau$, after the second $\pi/2$ pulse, the length of the state will be $cos(\delta\omega_0^{(i)}\tau)$ the original length. The average of N times experiment should be:
$$
\frac1N\sum_{i=1}^N cos(\delta\omega_0^{(i)}\tau)\Longrightarrow \int cos(\delta\omega_0\tau)p(\delta\omega_0)d\delta\omega_0\\
p(\delta\omega_0) = \frac1{\sqrt{2\pi\sigma^2}} e^{-\frac{\delta\omega_0^2}{2\sigma^2}}\\
\int cos(\delta\omega_0\tau)p(\delta\omega_0)d\delta\omega_0 = Ae^{-\frac{\sigma^2\tau^2}{2}}
$$
Remember that here the Gaussian distribution is from the central limit theorem, the simplest case for phase accumulation $\delta\omega_0\tau$, the quasi-static approximation. The real calculation should be $cos\int_0^{\tau}\delta\omega_0(\tau')d\tau'$.

## Circuit quantization

### Single transmon case

The Hamiltonian must be deduced from the Lagrangian since the generalized momentum must be defined by $\frac{\partial \mathcal L}{\partial \dot p}$. 

Now review the process from the Lagrangian to the second-quantization Hamiltonian:
$$
\mathcal{L}=\frac12 C\dot{\Phi}^2 - \frac1{2L}{\Phi}^2\\
Q = \frac{\partial \mathcal{L}}{\partial \dot\Phi} = C\dot\Phi\\
Legendre\ \ transformation:\ H = Q\dot\Phi - \mathcal{L} = \frac{Q^2}{2C} + \frac{\Phi^2}{2L}\\
It's\ \ a\ \ typical\ \ SHO\ \ form,\ thus:\\
[\hat{\Phi},\hat{Q}]=i\hbar\\
\hat{H} = \hbar\Omega(\hat{a}^{\dagger}\hat{a} + \frac12 ),\ \Omega = \frac{1}{\sqrt{LC}}\\
$$
Now add a persistent current as a drive to this system. 

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210202201136783.png" alt="image-20210202201136783" style="zoom:33%;" />

When analyzing this circuit, we treat the current source as the ground, and choose the three-wire-cross as the node,   the Lagrangian is the kinetic energy subscribing the potential energy, the contribution of the drive to the potential is $\Phi I_b$, thus:
$$
\mathcal{L} = \frac12C\dot{\Phi}^2-\frac1{2L}\Phi^2 - \Phi I_b\\
H = Q\dot{\Phi}-\mathcal{L}\\
H = \frac{Q^2}{2C} + \frac{\Phi^2}{2L} + \Phi I_b
$$
The left two terms contribute to the $a^{\dagger}a$ term in the second-quantization Hamiltonian, it is diagonal. $I_b$ is a number, $\Phi$ is some constant times $(a^{\dagger}+a)$, so in the matrix form, it is non-diagonal. The SHO is definitely Bosonic, but when we do a truncation and take only 2 levels, it becomes Fermion, that's how we define a qubit. It's not difficult to imagine that the diagonal part then will be reduced to the $\sigma_z$ part of the qubit Hamiltonian, and the drive is the $\sigma_x$ part. Actually, only when the drive is weak we can write the Hamiltonian as $H = \frac12\Delta\sigma_z + \frac12\Omega\sigma_x$ and the two terms are in the same Hilbert space, because only when the drive is a perturbation, we can still use the SHO quantization in a non-SHO Hamiltonian. 

### Double capacitively coupled transmons case

$$
\hat{\Phi} = (\Phi_1, \Phi_2)^T,\ \hat{C} = \left(\begin{matrix}C_1+C_2 & -C_g\\ -C_g & C_1 + C_2 \end{matrix} \right)\\
\hat H = \frac12\hat{Q}^T\hat{C}^{-1}\hat{Q} + \frac12\hat{\Phi}^T \hat{L}^{-1}\hat{\Phi}\\
\mathcal{L} = \frac12C_1\dot{\Phi}_1^2 - \frac{\Phi_1^2}{2L_1} + \frac12C_2\dot{\Phi}_2^2 - \frac{\Phi_2^2}{2L_2} + \frac12C_g(\dot{\Phi}_2 - \dot{\Phi}_1)^2\\
\hat H = \frac{\hat{Q}_1^2}{2C_1'} + \frac{\hat{\Phi}_1^2}{2L_1} + \frac{\hat{Q}_2^2}{2C_2'}+ \frac{\hat{\Phi}_2^2}{2L_2} + \beta \frac{\hat{Q}_1\hat{Q}_2}{\sqrt{C_1'C_2'}}\\
C_1'\approx C_1 + C_g,\ \ C_2'\approx C_2 + C_g,\ \beta\approx \frac{C_g}{\sqrt{C_1'C_2'}}
$$

### Cooper-pair-box 

$$
H = 4E_C(\hat{n}-n_g)^2 - E_J cos\hat{\varphi}\\
\hat{n} = -i\frac{\partial}{\partial\varphi}\\
matrix\ \ form: \hat{n} = diag
\left( 
-\infin,...,-2,-1,0,1,2,...,\infin
\right)\\
cut\ \ off: \hat n = diag(n_{min},...,0,1,2,...,n_{max})\\
\hat n = \sum n\mid n\rangle\langle n\mid\\
cos\hat\varphi = \frac12(e^{i\hat\varphi}+e^{-i\hat\varphi}) = \frac12\sum(\mid n+1\rangle\langle n\mid + \mid n\rangle\langle n+1\mid)\\
$$

$\omega_{01} = \sqrt{8E_CE_J}-E_J, \Delta\omega_{01} = -E_C$



