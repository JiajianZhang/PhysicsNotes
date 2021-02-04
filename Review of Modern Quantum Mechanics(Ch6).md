# Chapter 6 Scattering

## Scattering: Time-Dependent Perturbation

### Interaction Picture

$$
The\ state\ vector\ in\ Schrodinger\ picture:\\
\mid\alpha,t,t_0\rangle_S=U(t,t_0)\mid\alpha,t_0\rangle\\
Define\ the\ state\ vector\ in\ the\ interaction\ picture:\\
\mid\alpha,t,t_0\rangle_I\equiv e^{iH_0t/\hbar}\mid\alpha,t,t_0\rangle_S\\
V_I\equiv e^{iH_0t/\hbar}V_Se^{-iH_0t\hbar}\\
i\hbar\frac{\partial}{\partial t}\mid\alpha,t,t_0\rangle_I=i\hbar(\frac i{\hbar}H_0)\mid\alpha,t,t_0\rangle_S+i\hbar e^{iH_0t\hbar}(-\frac{i(H_0+V)}{\hbar})\mid\alpha,t,t_0\rangle_S\\
=e^{iH_0t/\hbar}V_Se^{-iH_0t/\hbar}e^{iH_0t/\hbar}\mid\alpha,t,t_0\rangle_S=V_I\mid\alpha,t,t_0\rangle_I\\
The\ interaction\ picture\ has\ an\ equation\ like\ the\ Heisenberg\ equation:\\
\frac{\partial}{\partial t}A_I=\frac{1}{i\hbar}[A_I,H_0]\\
and\ the\ time-evolution\ operator\ can\ be\ defined\ as:\\
i\hbar\frac{\partial}{\partial t}U_I(t,t_0)=V_I(t)U_I(t,t_0)\\
The\ solution\ is:\\
U_I(t,t_0)=Te^{-\frac{i}{\hbar}\int_{t_0}^tV_I(\tau)d\tau}\\
(T\ is\ the\ time-order\ operator)\\
U_I(t+\delta t,t)=-\frac{i}{\hbar}V_I(t)\delta t\\
U_I(t,t_0)=1-\frac{i}{\hbar}\int_{t_0}^tV_I(t')U_I(t',t_0)dt'\\
$$

$$
\langle n\mid U_I(t,t_0)=\delta_{ni}-\frac{i}{\hbar}\sum_m\langle n\mid V\mid m\rangle\int_{t_0}^t e^{i\omega_{nm}t'}\langle m\mid U_I(t',t_0)\mid i\rangle dt'\\
\langle n\mid i\rangle=\delta_{ni};\ \hbar\omega_{nm}=E_n-E_m\\
\langle\bold{x}\mid\bold{k}\rangle=\frac{1}{L^{3/2}}e^{i\bold{k\cdot x}}
$$

### Transition Rates and Cross Section

$$
Transition\ Rate:\\
\omega(i\rightarrow n)\equiv\frac{\partial}{\partial t}\mid\langle n\mid U_I(t,-\infin)\mid i\rangle\mid^2\\
\langle n\mid U_I(t,-\infin)\mid i\rangle=-\frac{i}{\hbar}T_{ni}\int_{-\infin}^t e^{i\omega_{ni}t'+0^+t'}dt'\\
\omega(i\rightarrow n)=\frac{1}{\hbar^2}\mid T_{ni}\mid^2\frac{20^+e^{20^+t}}{\omega_{ni}^2+{0^+}^2}
$$

Calculate the rates:
$$
\int_{-\infin}^{\infin}\frac{1}{\omega^2+{0^+}^2}d\omega=\pi/0^+\\
\omega(i\rightarrow n)=\frac{2\pi}{\hbar}\mid T_{ni}\mid^2\delta(E_n-E_i)\\
\omega(i\rightarrow n)=\frac{mkL^3}{(2\pi)^2\hbar^3}\mid T_{ni}\mid^2d\Omega\\
\frac{d\sigma}{d\Omega}=\left( \frac{mL^3}{2\pi\hbar^2} \right)^2\mid T_{ni}\mid^2\\
$$
Solving T-matrix
$$
T_{ni}=V_{ni}+\frac{1}{\hbar}\sum_{m}V_{nm}\frac{T_{mi}}{-\omega_{mi}+i0^+}=V_{ni}+\sum_mV_{nm}\frac{T_{mi}}{E_i-E_m+i\hbar\epsilon} \\
T_{ni}=\sum_j\langle n\mid V\mid j\rangle\langle j\mid\psi^{(+)}\rangle=\langle n\mid V\mid\psi^{(+)}\rangle\\
$$

### Lippmann-Schwinger equation

$$
\mid\psi^{(+)}\rangle=\mid i\rangle+\frac{1}{E_i-H_0+i\hbar\epsilon}V\mid\psi^{(+)}\rangle\\
$$

Rewrite the differential scattering area and expand transition operator T when scattering potential V is considered as perturbation:
$$
\frac{d\sigma}{d\Omega}=\left( \frac{mL^3}{2\pi\hbar^2} \right)^2\mid T_{ni}\mid^2=\left( \frac{mL^3}{2\pi\hbar^2} \right)^2\mid\langle n\mid V\mid\psi^{(+)}\rangle\mid^2\\
T=V+V\frac{1}{E_i-H_0+i\hbar\epsilon}V+V\frac{1}{E_i-H_0+i\hbar\epsilon}V\frac{1}{E_i-H_0+i\hbar\epsilon}V+\cdot\cdot\cdot
$$

## Scattering Amplitude


$$
\langle \bold{x}\mid\psi(\pm)\rangle=\langle\bold{x}\mid i\rangle+\int d^3x'\langle\bold{x\mid}\frac{1}{E_i-H_0\pm i\hbar\epsilon}\mid\bold{x'}\rangle\langle\bold{x'\mid}V\mid\psi^{(\pm)}\rangle\\
G_{\pm}(\bold{x,x'})\equiv\frac{\hbar^2}{2m}\langle\bold{x}\mid \frac{1}{E_i-H_0\pm i\hbar\epsilon}\mid\bold{x'}\rangle=\frac{\hbar^2}{2m}\sum_{k'}\sum_{k''}\langle\bold{x}\mid\bold{k'}\rangle\frac{\delta_{k'k''}}{E_i-\hbar^2k'^2/2m\pm i\hbar\epsilon}\langle\bold{k''}\mid \bold{x'}\rangle\\
=\frac{1}{L^3}\sum_{\bold{k'}}\frac{e^{i\bold{k'\cdot(x-x')}}}{k^2-k'^2\pm i\epsilon}=\frac{1}{8\pi^2}\frac{1}{i\mid \bold{x-x'}\mid}\int_{-\infin}^{\infin}k'dk'\left[ \frac{e^{-ik'\mid\bold{x-x'}\mid}-e^{ik'\mid\bold{x-x'}\mid}}{k^2-k'^2\pm i\epsilon}\right]\\
=-\frac{2\pi i(e^{\pm ik'\mid\bold{x-x'}\mid})}{8\pi^2i\mid\bold{x-x'\mid}}=-\frac{e^{\pm ik'\mid\bold{x-x'}\mid}}{4\pi \mid\bold{x-x'\mid}}
$$
The Green function:
$$
(\nabla^2+k^2)G_{\pm}(\bold{x,x'})=\delta^3(\bold{x-x'})\\
\langle \bold{x}\mid\psi(\pm)\rangle=\langle\bold{x}\mid i\rangle+\frac{2m}{\hbar^2}\int d^3x'G_{\pm}(\bold{x,x'})\langle\bold{x'\mid}V\mid\psi^{(\pm)}\rangle\\
=\langle\bold{x}\mid i\rangle-\frac{2m}{\hbar^2}\int d^3x' \frac{e^{\pm ik'\mid\bold{x-x'}\mid}}{4\pi \mid\bold{x-x'\mid}}\langle\bold{x'\mid}V\mid\psi^{(\pm)}\rangle\\
=\langle\bold{x}\mid i\rangle-\frac{2m}{\hbar^2} \int d^3x' \frac{e^{\pm ik'\mid\bold{x-x'}\mid}}{4\pi \mid\bold{x-x'\mid}}V(\bold{x'})\langle\bold{x'}\mid\psi^{(\pm)}\rangle\\
take\ \mid \bold{x-x'}\mid\approx r-\bold{\hat{r}\cdot x'}\\
\lim\limits_{r\rightarrow\infin}\langle \bold{x}\mid\psi(\pm)\rangle=\langle\bold{x'\mid k'}\rangle-\frac{1}{4\pi}\frac{2m}{\hbar^2}\frac{e^{ikr}}{r}\int d^3x'e^{-i\bold{k'\cdot x'}}V(\bold{x'})\langle \bold{x'}\mid\psi^{(+)}\rangle\\
=\frac{1}{L^{3/2}}\left[e^{i\bold{kx}}+\frac{e^{ikr}}{r}f(\bold{k',k}) \right]\\
$$
Scattering Amplitude is defined as:
$$
f(\bold{k',k})=-\frac{mL^3}{2\pi\hbar^2}\langle\bold{k'}\mid V\mid\psi^{(+)}\rangle\\
\frac{d\sigma}{d\Omega}=\mid f(\bold{k',k})\mid^2
$$

### Optical Theorem

$$
Im(f(\theta=0))=\frac{k\sigma_{tot}}{4\pi}
$$

Prove this theorem:
$$
f(\theta=0)=f(\bold{k',k})=-\frac{mL^3}{2\pi\hbar^2}\langle\bold{k'}\mid V\mid\psi^{(+)}\rangle\\
\langle\bold{k}\mid V\mid\psi^{(+)}\rangle=\left[\langle\psi^{(+)}\mid-\langle\psi^{(+)}\mid V\frac{1}{E-H_0-i\epsilon}\right] V\mid\psi^{(+)}\rangle\\
=\langle\psi^{(+)}\mid V\mid\psi^{(+)}\rangle-\langle\psi^{(+)}\mid V \frac{1}{E-H_0-i\epsilon}V\mid\psi^{(+)}\rangle\\
Im\langle\bold{k}\mid V\mid\psi^{(+)}\rangle=-\pi\langle\bold{k}\mid T^{\dagger}\delta(E-H_0)T\mid \bold{k}\rangle\\
Imf(\bold{k,k})=-\frac{mL^3}{2\pi\hbar^2}Im\langle\bold{k}\mid V\mid\psi^{(+)}\rangle=-\frac{mL^3}{2\hbar^2}\sum_{\bold{k'}}\mid\langle\bold{k'}\mid T\mid\bold{k}\rangle\mid^2\delta_{E,E'}\\
=\frac{mL^3}{2\hbar^2}\left(\frac{2\pi\hbar^2}{mL^3} \right)^2\sum_{\bold{k'}}\mid f(\bold{k',k})\mid^2\delta_{E,E'}=\frac{k}{4\pi}\sigma_{tot}
$$

## Born Approximation

To calculate the cross section easier:
$$
T=T=V+V\frac{1}{E_i-H_0+i\hbar\epsilon}V+V\frac{1}{E_i-H_0+i\hbar\epsilon}V\frac{1}{E_i-H_0+i\hbar\epsilon}V+\cdot\cdot\cdot\\
take\ the\ first\ order\ Born\ Approximation,\\
f^{(1)}(\bold{k',k})=-\frac{mL^3}{2\pi\hbar^2}\langle\bold{k'}\mid V\mid\bold{k}\rangle\\
=-\frac{mL^3}{2\pi\hbar^2}\int d^3x'e^{i\bold{(k-k')x}}V(\bold{x'})\\
Or\ in\ the\ angular\ integral\ form:\\
q=\mid\bold{k-k'}\mid=2ksin(\theta/2)\\
f^{(1)}(\theta)=-\frac{2m}{\hbar^2}\frac{1}{q}\int_0^{\infin}rV(r)sin(qr)dr\\
$$

#### Ex: Spherical Potential Well

$$
f^{(1)}(\theta)=-\frac{2m}{\hbar^2}\frac{1}{q}\int_0^{\infin}rV_0sin(qr)dr\\
V_r=V_0\ (r\leq a);\ 0\ (r>a)\\
$$

#### Ex: Yukawa Potential

$$
V(r)=\frac{V_0e^{-\mu r}}{\mu r}\\
f^{(1)}(\theta)=-\frac{2m}{\hbar^2}\frac{1}{q}\int_0^{\infin} rV(r)sin(qr)dr=-\frac{2m}{\hbar^2}\frac{V_0}{\mu(q^2+\mu^2)}\\
\frac{d\sigma}{d\Omega}=\mid f^{(1)}(\theta)\mid^2=\left(\frac{2mV_0}{\mu\hbar^2} \right)^2\frac{1}{(4k^2sin^2(\theta/2)+\mu^2)^2}\\
\approx\frac1{16}\left(\frac{ZZ'e^2}{E_0} \right)^2\frac1{sin^4(\theta/2)}
$$

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20210104080350180.png" alt="image-20210104080350180" style="zoom:33%;" />

For any spherical Bessel:

$f_l'(x) = \frac{l}{x}f_l(x) - f_{l+1}(x)$

$\beta_l \approx 1-(\kappa R) \frac{j_{l+1}(\kappa R)}{j_{l}(\kappa R)}$

$j_l(x) = \frac{x^l}{(2l+1)!!}$,  $n_l(x) = -\frac{(2l-1)!!}{x^{l+1}}$

$tan\delta_l = \frac{(kR)^{2l+3}}{(2l+3)!!(2l+1)!!}\left(\frac{\kappa^2}{k^2}-1 \right)$

$tan\delta_0\approx sin\delta_0$

$tan\delta_1\approx sin\delta_1$

$\sigma_{tot} = \frac{4\pi}{k^2}\sum_l (2l+1)sin^2\delta_l$

Take $l=0$,  $\sigma_{tot} = \frac{4\pi}{k^2}sin^2\delta_0 $

$\frac{d\sigma}{d\Omega} = \frac1{k^2}\left(\mid e^{i\delta_0}sin\delta_0 + 3e^{i\delta_1}sin\delta_1cos\theta \mid\right)^2$

$\frac{B}{A} = \frac25(kR)^2$













