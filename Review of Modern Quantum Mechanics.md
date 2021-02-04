# Review of Modern Quantum Mechanics

## Chapter 1

### Stern-Gerlach Experiment

$$
\mid S_x,\pm\rangle=\pm\frac{1}{\sqrt{2}}{\mid S_z,+\rangle}+\frac{1}{\sqrt{2}}{\mid S_z,-\rangle}\\
{\mid S_y,\pm\rangle}=\frac{1}{\sqrt{2}}{\mid S_z,+\rangle}\pm\frac{i}{\sqrt{2}}{\mid S_z,-\rangle}\\
$$

When the magnetic field is applied on the z direction, the spin eigenstates of x and y direction (perform x or y filter) can be written as the equation (1) shown. 
$$
S_{x,y,z}{\mid S_{x,y,z},\pm\rangle}=\pm\frac{\hbar}{2}{\mid S_{x,y,z},\pm\rangle}
$$


### Kets and Bras

$$
{\langle a''\mid} {Z\mid a'\rangle}=\displaystyle{\sum_{a'''}}{\langle a''\mid}X{\mid a'''\rangle}{\langle a'''\mid}Y{\mid a'\rangle}\\
for\ Z=XY\\
\displaystyle{\sum_{a'''}}{\mid a'''\rangle}{\langle a'''\mid}=\mathbb{1}
$$

$$
{\langle a' \mid X^\dagger \mid a''\rangle}={\langle a'' \mid X \mid a' \rangle}^*
$$

### Spin-$\bold{\frac{1}{2}}$ System

$$
S_\pm\equiv\hbar{\mid\pm\rangle\langle\mp\mid}\\
S_\pm\equiv S_x \pm iS_y
$$

$$
S_x=\frac{\hbar}{2}({\mid +\rangle\langle-\mid}+{\mid -\rangle\langle+\mid})\\
S_y=\frac{\hbar}{2}({\mid-\rangle\langle+\mid}-i{\mid+\rangle\langle-\mid})\\
S_z=\frac{\hbar}{2}({\mid+\rangle\langle+\mid}-{\mid-\rangle\langle-\mid})
$$

Change the basis to the eigenstates of spin-x:
$$
\mid S_x,\pm\rangle=\frac{1}{\sqrt{2}}\mid+\rangle\pm\frac{1}{\sqrt{2}}e^{i\delta_1}\mid-\rangle\\
{\mid S_y,\pm\rangle}=\frac{1}{\sqrt{2}}\mid+\rangle\pm\frac{1}{\sqrt{2}}e^{i\delta_2}\mid-\rangle\\
$$

### Commutation Relation

$$
[S_i,S_j]=i\mathcal{\epsilon}_{ijk}\hbar S_k\\
\left\{ S_i,S_j \right\}=\frac{1}{2}\hbar^2\delta_{ij}\\
\left[ \bold{S}^2,S_i \right]=0\  (for\ \bold{S}^2=\frac{3}{4}\hbar^2) 
$$

### Compatible Observables

compatible: $[A,B]=0$, common eigenkets;

incompatible: $[A,B]\neq0$, no common eigenkets

### Uncertainty Relation

$$
\Delta A \equiv A-\langle A\rangle\\
$$

$$
\langle (\Delta A)^2\rangle=\langle(A^2-2A\langle A\rangle+\langle A\rangle^2)\rangle=\langle A^2\rangle-\langle A\rangle^2
$$

$$
\langle S_x^2\rangle-\langle S_x\rangle^2=\hbar^2/4\\
\langle (\Delta A)^2\rangle\langle(\Delta B)^2\rangle\geqslant\frac{1}{4}\mid\langle[A,B]\rangle\mid^2
$$

### Change of basis

$$
U = \sum_{k}\mid b^{(k)}\rangle\langle a^{(k)}\mid\\
U^{\dagger} = \sum_{k}\mid a^{(k)}\rangle\langle b^{(k)}\mid   \\
U_{ij}^{A} = \langle a^{(i)}\mid b^{(j)}\rangle\\
U_{ij}^{\dagger A} = \langle b^{(i)}\mid a^{(j)}\rangle  \\
\langle b^{(i)}\mid \alpha\rangle = \sum_j\langle b^{(i)}\mid a^{(j)}\rangle\langle a^{(j)}\mid\alpha\rangle = \sum_j U_{ij}^{\dagger A} \langle a^{(j)}\mid\alpha\rangle
$$

The representation change on an operator can be expressed as:
$$
X^{(B)} = U^{\dagger}X^{(A)}U
$$

### Diagonalization:

If the matrix elements of B under one basis (marked as a) is given, how to solve the eigenvalues under another basis (marked as b)? 

The matrix in basis b is wanted to be diagonalized, namely: $B = U^{\dagger}\Lambda U$
$$
B_{ij} = \sum_k\sum_m U_{mi}^*\Lambda_{mk} U_{kj}\\
B_{ij} = \sum_k U_{ki}^*\Lambda_{kk}U_{kj}\\
$$
Or we can write the same thing in another form:
$$
B\mid b^{(l)}\rangle = b^{(l)}\mid b^{(l)}\rangle\\
\langle a^{(i)}\mid B\sum_j\mid a^{(j)}\rangle\langle a^{(j)}\mid b^{(l)}\rangle = b^{(l)}\langle a^{(i)}\mid b^{(l)}\rangle\\
\sum_j B_{ij} C_j^{(l)} = b^{(l)}C_i^{(l)}
$$

###  The conservation of inner product in continuous spectrum

$\{\mid x'\rangle\}$ is a set of complete basis, and $\mid\alpha\rangle$ is some normalized eigenket. 
$$
\int dx'\mid x'\rangle\langle x'\mid = 1\\
\int dx' \mid \langle x'\mid\alpha\rangle\mid^2 = 1=\int dx' P(\alpha\rightarrow x')
$$


### Translation

infinitesimal\ translation
$$
\bold{\mathscr{T}}(d\bold{x'})\mid\bold{x'}\rangle=\mid\bold{x'}+d\bold{x'}\rangle\\
\langle x''\mid \mathscr{T(\epsilon)}\mid\alpha\rangle = \langle x''\mid \mathscr{T(\epsilon)}\int dx' \mid x'\rangle\langle x'\mid\alpha\rangle = \int dx' \langle x''\mid x'+\epsilon\rangle \psi(x') = \psi(x''-\epsilon)\\
\mathscr{T}(d\bold{x'})=1-i\bold{K}\cdot d\bold{x'}\\
$$

The operator commutative relation:
$$
[\bold{x},\mathscr{T}(d\bold{x'})]=d\bold{x'}\\
[\mathbf{x},\mathbf{K}]\cdot d\mathbf{x'} =  d\mathbf{x'} \\
[x_i,K_j]=i\delta_{ij}
$$



### Momentum as a Generator of Translation

$$
\bold{K}=\frac{\bold{p}}{universal\ constant\ with\ the\ dimension\ of\ action}
$$

$$
[\bold{p},\mathscr{T}(d\bold{x'})]=0
$$

### The Canonical Commutation Relations

The canonical transformation generating function:
$$
F(\mathbf{x},\mathbf{P}) = \mathbf{x}\cdot\mathbf{P} + \mathbf{p}\cdot d\mathbf{x}\\
\mathbf{K} = \mathbf{p}/\hbar
$$

$$

\left\{A,B\right\}_{Poisson}\rightarrow\frac{[A,B]}{i\hbar}
$$

### Position-Space Wave Function

$$
\mid\alpha\rangle=\int dx'\mid x'\rangle\langle x'\mid\alpha\rangle\\
the\ expanded\ representation\ of\ a\ physical\ state
$$

$$
\psi_{\alpha}(x')=\langle x'\mid\alpha\rangle
$$

The completeness condition in the discrete case: $\displaystyle{\sum_{x'}}\mid x'\rangle\langle x'\mid=\mathscr{1}$ now changes to the continuous case:
$$
\int dx' \mid x'\rangle\langle x'\mid=\mathscr{1}
$$

$$
\langle\beta\mid A\mid\alpha\rangle=\int dx'\int dx''\langle\beta\mid x'\rangle\langle x'\mid A\mid x''\rangle\langle x''\mid\alpha\rangle\\
=\int dx'\int dx''\psi_{\beta}^*(x')\langle x'\mid A\mid x''\rangle\psi_{\alpha}(x'')
$$

For example:
$$
\langle x'\mid x^2\mid x''\rangle=(\langle x'\mid)\cdot(x''^2\mid x''\rangle)=x'^2\delta(x'-x'')\\
\langle\beta\mid f(x)\mid\alpha\rangle=\int dx'\psi_\beta^*(x')f(x')\psi_\alpha(x')
$$

### Momentum Operator in the Position Basis

$$
\mathscr{T}(\Delta x'\bold{\hat{x}})\mid\bold{\hat{x}}\rangle=\mid \bold{x'}+\Delta x'\bold{\hat{x}}\rangle\\
\mathscr{T}(\Delta x'\bold{\hat{x}})=\lim\limits_{N\rightarrow\infty}\left (1-\frac{ip_x\Delta x'}{N\hbar} \right)^N=exp\left(-\frac{ip_x\Delta x'}{\hbar} \right)
$$

$$
\left(1-\frac{ip\Delta x'}{\hbar} \right)\mid\alpha\rangle=\int dx'\mathscr{T}(\Delta x')\mid x'\rangle\langle x'\mid\alpha\rangle=\int dx'\mid x'+\Delta x'\rangle\langle x'\mid\alpha\rangle=\int dx'\mid x'\rangle\langle x'-\Delta x'\mid\alpha\rangle\\
=\int dx'\mid x'\rangle\left (\langle x'\mid\alpha\rangle-\frac{\partial}{\partial x''}\int dx''\Delta x'\mid x''\rangle\langle x''\mid\alpha\rangle \right )\\
=\int dx'\mid x'\rangle\left (\langle x'\mid\alpha\rangle-\int dx''\Delta x'\frac{\partial}{\partial x''}\mid x''\rangle\langle x''\mid\alpha\rangle\right)\\
=\int dx'\mid x'\rangle\left (\langle x'\mid\alpha\rangle-\int dx''f(x'')\delta(x''-x')\frac{\partial}{\partial x''}\langle x''\mid\alpha\rangle\right)\\
=\int dx'\mid x'\rangle\left(\langle x'\mid\alpha\rangle-f(x')\frac{\partial}{\partial x'}\langle x'\mid\alpha\rangle \right)\\=\int dx'\mid x'\rangle\left(\langle x'\mid\alpha\rangle-\Delta x'\frac{\partial}{\partial x'}\langle x'\mid\alpha\rangle \right)\\
(Here\ f(x')=\Delta x')\\
\mid\alpha\rangle = \int dx'\mid x'\rangle\langle x'\mid\alpha\rangle\\
p\mid\alpha\rangle = (-i\hbar)\int dx'\mid x'\rangle \frac{\partial }{\partial x'}\langle x'\mid\alpha\rangle = (-i\hbar\frac{\partial }{\partial x'}) \int dx'\mid x'\rangle\langle x'\mid\alpha\rangle
$$

$$
\langle\beta\mid p\mid\alpha\rangle=\int dx'\langle\beta\mid x'\rangle\left(-i\hbar\frac{\partial}{\partial x'}\langle x'\mid\alpha\rangle \right)=\int dx'\psi_\beta^*(x')\left(-i\hbar\frac{\partial}{\partial x'} \right)\psi_\alpha(x')\\
\langle\beta\mid p^n\mid\alpha\rangle=\int dx'\psi_\beta^*(x')(-i\hbar)^n\frac{\partial^n}{\partial x'^{n}}\psi_\alpha(x')
$$

Actually, we can prove that $\frac{\partial }{\partial x}$ has no effect on $\mid x\rangle$:
$$
\langle x'\mid \hat{p}\mid x''\rangle = \int dp'\langle x'\mid p'\mid p'\rangle\langle p'\mid x''\rangle = \frac{1}{2\pi\hbar} \int dp' p' e^{ix'p'/\hbar}e^{-ix''p'/\hbar} \\
= \frac{1}{2\pi\hbar} \int dp'  \frac{d}{dp'}(2\pi\hbar p')\delta(x'-x'') = p'\delta(x'-x'')\\
or\ use\ the\ result\ above:\\
\langle x'\mid \hat{p}\mid x''\rangle = -i\hbar \frac{\partial}{\partial x'}\delta(x'-x'')  
$$
And also the other inference:
$$
\langle x'\mid \hat x\mid x''\rangle = x'\delta(x'-x'')\\
\langle p'\mid \hat x\mid p''\rangle = i\hbar\frac{\partial}{\partial p'}\delta(p'-p'')\\
\langle p'\mid \hat p\mid p''\rangle = p'\delta(p'-p'')
$$


### Momentum-Space Wave Function

$$
\phi_\alpha(p')=\langle p'\mid\alpha\rangle
$$

$$
\langle \bold{x'}\mid \bold{p'}\rangle=\left[\frac{1}{\sqrt{2\pi\hbar}}\right]^3exp\left(\frac{i\bold{p'}\cdot\bold{x'}}{\hbar} \right)
$$

The Transformation between the position-space wave function and the momentum-space wave function
$$
\psi_\alpha(\bold{x'})=\left[\frac{1}{\sqrt{2\pi\hbar}} \right]^3 \int d^3p'exp\left(\frac{i\bold{p'}\cdot\bold{x'}}{\hbar} \right)\phi_\alpha(\bold{p'})\\
\phi_\alpha(\bold{p'})=\left[\frac{1}{\sqrt{2\pi\hbar}} \right]^3 \int d^3x'exp\left(\frac{-i\bold{p'}\cdot\bold{x'}}{\hbar}\right)\psi_\alpha(\bold{x'})
$$

### Gaussian Wave Packets

$$
\langle x'\mid\alpha\rangle=\left[\frac{1}{\pi^{\frac{1}{4}}\sqrt{d}} \right]exp\left[ikx'-\frac{x'^2}{2d^2} \right]\\
\langle p'\mid\alpha\rangle=\sqrt{\frac{d}{\hbar\sqrt{\pi}}}exp\left[\frac{-(p'-\hbar k)^2d^2}{2\hbar^2} \right]
$$

$$
\langle A\rangle = \langle\alpha\mid A\mid\alpha\rangle = \int dx' \int dx'' \phi_{\alpha}^*(x') \langle x'\mid A\mid x''\rangle \phi_{\alpha}(x'')  \\
\langle x\rangle=0\\
\langle x^2\rangle=\frac{d^2}{2}\\
\langle p\rangle=\hbar k\\
\langle p^2\rangle=\frac{\hbar^2}{2d^2}+\hbar^2k^2\\
\langle(\Delta x)^2\rangle\langle(\Delta p)^2\rangle=\frac{\hbar^2}{4}
$$

## Chapter 2

$$
F(q,P) = \mathbf{q}\cdot\mathbf{P} + \epsilon G(q,P)\\
Q_i = \frac{\partial F}{\partial P_i} = q_i + \epsilon \frac{\partial G}{\partial p_i}\\
p_i = \frac{\partial F}{\partial q_i} = P_i + \epsilon \frac{\partial G}{\partial q_i}\\
\delta q_i = Q_i - q_i = \epsilon \frac{\partial G}{\partial p_i}\\
\delta p_i = P_i - p_i = -\epsilon \frac{\partial G}{\partial q_i}
$$



### Time-evolution operator in Schrodinger picture

$$
\mid\alpha,t_0;t_0+dt\rangle=\mathscr{U}(t_0+dt,t_0)\mid\alpha,t_0\rangle\\
\mathscr{U}(t_0+dt,t_0)\approx1-i\Omega dt\\
\Omega^\dagger=\Omega=\frac{H}{\hbar}
$$

$$
H\mathscr{U}(t,t_0)=i\hbar\frac{\partial}{\partial t}\mathscr{U}(t,t_0)
$$

Case 1: (Hamiltonian independent of time)
$$
\mathscr{U}(t,t_0)=exp\left[\frac{-iH(t-t_0)}{\hbar} \right]
$$
Case 2: (Hamiltonian time-independent but H's at different times commute)
$$
\mathscr{U}(t,t_0)=exp\left[-\frac{i}{\hbar}\int_{t_0}^tdt'H(t') \right]
$$
Case 3: (Hamiltonian at different do not commute)
$$
\mathscr{U}(t,t_0)=1+\displaystyle{\sum_{n=1}^{\infin}}\left(\frac{-i}{\hbar} \right)^n\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\cdot\cdot\cdot\int_{t_0}^{t_2}dt_nH(t_1)H(t_2) {\cdot\cdot\cdot}H(t_n)
$$
It is called the $\bold{Dyson\ Series}$

### Time Dependence of Expectation Values

#### stationary state:

$$
\langle B\rangle=(\langle a'\mid\mathscr{U}^\dagger(t,0))\cdot B\cdot(\mathscr{U}(t,0)\mid a'\rangle)=\langle a'\mid B\mid a'\rangle
$$

#### non-stationary state

$$
\langle B\rangle=\left[\displaystyle{\sum_{a'}}c_a^*{\langle a'\mid} exp\left(\frac{iE_{a'}t}{\hbar}\right) \right]{\cdot B\cdot}\left[\displaystyle{\sum_{a''}}c_{a''}exp\left(\frac{-iE_{a''}t}{\hbar} \right){\mid a''\rangle} \right]\\
=\displaystyle{\sum_{a'}\sum_{a''}}c_{a'}^*c_{a''}{\langle a'\mid} B{\mid a''\rangle}exp\left[\frac{-i(E_{a''}-E_{a'})t}{\hbar} \right]
$$

### Spin-Precession

$$
H=-\left(\frac{e}{m_ec} \right)\bold{S}\cdot\bold{B}\\
H=-\frac{eB}{m_ec}S_z=\omega S_z \\
E_\pm=\mp\frac{e\hbar B}{2m_e c}=\pm\frac{\hbar}{2}\omega
$$

time-evolution under stationary magnetic field
$$
\mid\alpha,t_0=0;t\rangle=c_+exp(-i\omega t/2){\mid+\rangle}+c_-exp(i\omega t/2){\mid-\rangle}
$$
If $c_+=1,c_-=0$, $\alpha$ is in the spin-up eigenstate of $S_z$;

If $c_+=0,c_-=1$, $\alpha$ is in the spin-down eigenstate of $S_z$;

If $c+=\frac{1}{\sqrt{2}},c_-=\frac{1}{\sqrt{2}}$, $\alpha$ is in the $\mid S_x,+\rangle$ eigenstate;

If $c+=\frac{1}{\sqrt{2}},c_-=-\frac{1}{\sqrt{2}}$, $\alpha$ is in the $\mid S_x,-\rangle$ eigenstate;
$$
\langle S_x\rangle=\frac{\hbar}{2}\frac{1}{\sqrt{2}}(\langle+\mid exp(i\omega t/2)+\langle-\mid exp(-i\omega t/2))\frac{1}{\sqrt{2}}(\langle+\mid+\langle-\mid)(\mid+\rangle\langle-\mid\\
+\mid-\rangle\langle+\mid)\frac{1}{\sqrt{2}}(\mid+\rangle+\mid-\rangle)\frac{1}{\sqrt{2}}(exp(-i\omega t/2)\mid+\rangle+exp(i\omega t/2)\mid-\rangle)\\
+\frac{\hbar}{2}\frac{1}{\sqrt{2}}(\langle+\mid exp(i\omega t/2)-\langle-\mid exp(-i\omega t/2))\frac{1}{\sqrt{2}}(\langle+\mid-\langle-\mid)(\mid+\rangle\langle-\mid\\
+\mid-\rangle\langle+\mid)\frac{1}{\sqrt{2}}(\mid+\rangle-\mid-\rangle)\frac{1}{\sqrt{2}}(exp(-i\omega t/2)\mid+\rangle-exp(i\omega t/2)\mid-\rangle)\\
=\frac{\hbar}{2}\frac{1}4\left[(exp(i\omega t/2)+exp(-i\omega t/2))^2+(exp(i\omega t/2)-exp(-i\omega t/2))^2) \right]\\
=\frac{\hbar}{2}cos\omega t\\
$$
Similarly,
$$
\langle S_y\rangle=\frac{\hbar}{2}sin\omega t\\
\langle S_z\rangle=0
$$

### Neutrino Oscillations

$$
\mid\nu_e\rangle=cos\theta\mid\nu_1\rangle-sin\theta\mid\nu_2\rangle\\
{\mid\nu_\mu\rangle}=sin\theta\mid\nu_1\rangle+cos\theta\mid\nu_2\rangle
$$

$$
E=\left[p^2c^2+m^2c^4 \right]^{\frac{1}{2}}\approx pc\left(1+\frac{m^2c^2}{2p^2} \right)
$$

### Correlation Amplitude and the Energy-Time Uncertainty Relation

$$
C(t)=\langle\alpha\mid\mathscr{U(t_0,t)}\mid\alpha\rangle\\
=\displaystyle{\sum_{a'}}|c_{a'}|^2exp\left(\frac{-iE_{a'}t}{\hbar} \right)\\
Knowm\ as\ the\ \bold{Correlation\ Amplitude}
$$

$$
\displaystyle{\sum_{a'}}\rightarrow\int dE\rho(E),\ c_{a'}\rightarrow g(E)\Bigg|_{E\simeq E_{a'}}
$$

$$
C(t)=\int dE|g(E)|^2\rho(E)exp\left(\frac{-iEt}{\hbar} \right)=
exp(\frac{-iE_0t}{\hbar})\int dE|g(E)|^2\rho(E)exp\left[\frac{-i(E-E_0)t}{\hbar} \right]
$$

If $|E-E_0|\simeq\hbar/t$, the $|g(E)|^2\rho(E)$ term get no contribution to $C(t)$ because of the strong cancellations. 

### Heisenberg Picture 

$$
A^H(t,t_0)=\mathscr{U}^\dagger(t) A^S(t_0)\mathscr{U}(t)\\
\frac{d}{dt}A^H=\frac{1}{i\hbar}[A^H,\mathscr{U}^\dagger H\mathscr{U}]
$$

### Free Particles; Ehrenfest's Theorem

$$
[x_i,F(\bold{p})]=i\hbar\frac{\partial F}{\partial p_i}\\ 
[p_i,G(\bold{x})]=-i\hbar\frac{\partial G}{\partial x_i}\\
This\ is\ easy\ to\ prove\ if\ we\ use\ the\ Taylor\ series\ to\ expand\ F\ and\ G
$$

Quantum-Mechanical analogue of Newton's second law:
$$
m\frac{d^2}{dt^2}\bold{x}=-\nabla\bold{V(x)}\\
in\ the\ expectation\ form,\ the\ \bold{Ehrenfest\ Theorem}:
m\frac{d^2}{dt^2}\bold{\langle x\rangle}=\frac{d\bold{p}}{dt}=-\nabla\bold{\langle V(x)\rangle}
$$

### Harmonic Oscillator

$$
a=\sqrt{\frac{m\omega}{2\hbar}}\left(x+\frac{ip}{m\omega} \right)\\
a^\dagger=\sqrt{\frac{m\omega}{2\hbar}}\left(x-\frac{ip}{m\omega} \right)
$$

$$
\mid n\rangle=\frac{(a^\dagger)^n}{\sqrt{n!}}{\mid0\rangle}
$$

### Time-Dependent Wave Equation

$$
\psi(\bold{x'},t)=\langle\bold{x'}\mid\alpha,t_0;t\rangle\\
i\hbar\frac{\partial}{\partial t}\psi(\bold{x'},t)=-\frac{\hbar^2}{2m}\nabla'^2\psi(\bold{x'},t)+V(\bold{x'})\psi(\bold{x'},t)
$$

### Time-Independent Wave Equation

$$
\psi(\bold{x'},t)=\langle\bold{x'}\mid\alpha,t_0\rangle exp\left(\frac{-iE_\alpha t}{\hbar} \right)
$$

### Interpretation of the Wave Function

$$
\rho(\bold{x'},t)={\mid\psi(\bold{x'},t)\mid}^2\\
\bold{j}=-\frac{\hbar}{m}Im(\psi^*\nabla\psi)\ (the\ imaginary\ part)\\
\frac{\partial}{\partial t}\rho+\nabla\cdot\bold{j}=0\ (the\ convention\ of\ probability\ current)  
$$

### Elementary Solutions To Schrodinger Wave Equation

Introduce a periodic boundary condition with a period length $L$, for the position-space wave function:
$$
\psi(\bold{x},t)=\frac{1}{L^{\frac{3}{2}}}exp\left(\frac{i\bold{p}\cdot\bold{x}}{\hbar}-\frac{iEt}{\hbar}\right)\\
\bold{j}=\frac{\hbar\bold{k}}{mL^3}
$$
Note: How to solve the differential equation in the following form:
$$
\frac{d^2}{dy^2}h-2y\frac{d}{dy}h+(\varepsilon-1)h=0\\
The\ Hermite\ polynomial:\\
H''_n(y)=2xH'_n(y)-2nH_n(y)
$$
The solution of harmonic oscillator:
$$
u_n(x)=c_nH_n(x\sqrt{\frac{m\omega}{\hbar}})e^{-\frac{m\omega x^2}{2\hbar}}
$$

### Propagators and Feynman Path Integrals

For a Free Particle (with zero potential energy)
$$
K(\bold{x''},t;\bold{x'},t_0)={\langle\bold{x''}\mid} exp\left(\frac{-iH(t-t_0)}{\hbar} \right){\mid \bold{x'}\rangle}\\
=\int d^3p'\langle\bold{x''}\mid\bold{p'}\rangle\langle\bold{p'}\mid\bold{x'}\rangle exp\left(\frac{-ip'^2(t-t_0)}{2m\hbar} \right)\\
=(\frac{1}{2\pi\hbar})^3\int d^3p'exp\left(\frac{ip'x''}{\hbar} \right) exp\left(\frac{-ip'x'}{\hbar} \right)exp\left(\frac{-ip'^2(t-t_0)}{2m\hbar} \right)\\
=(\frac{1}{2\pi\hbar})^3\int_{-\infin}^{\infin}d^3p'exp\left[\frac{-ip'^2(t-t_0)}{2m\hbar}+\frac{ip'(x''-x')}{\hbar} \right]\ (for\ 3D\ case)\\ 
K(x'',t;x',t_0)=\sqrt{\frac{m}{2\pi i\hbar(t-t_0)}}exp\left[\frac{im(x''-x')^2}{2\hbar(t-t_0)} \right]\ (for\ 1D\ case)
$$

For a harmonic oscillator:
$$
K(x'',t;x',t_0)=\sqrt{\frac{m\omega}{2\pi i\hbar sin(\omega(t-t_0))}}exp\left\{ \left[\frac{im\omega}{2\hbar sin(\omega(t-t_0))} \right]\left[(x''^2+x'^2)cos(\omega(t-t_0))-2x''x' \right]\right\}
$$

The integral of K in all space:
$$
G(t)=\int d^3x'K(\bold{x''},t;\bold{x'},t_0)\\
=\displaystyle{\sum_{a'}}exp\left(\frac{-iE_{a'}t}{\hbar}\right)\\
The\ Laplace-Fourier\ transformation\ of\ G(t):\\
\tilde{G}(t)=-i\int_0^\infin dtG(t)exp(iEt/\hbar)/\hbar=\displaystyle{\sum_{a'}}\frac{1}{E-E_{a'}}
$$

Propagator as Transition Amplitude:
$$
K(x'',t;x',t_0)=\langle x'',t\mid x',t_0\rangle\\
K(x''',t_2;x',t_0)=\int d^3x''\langle x''',t_2\mid x'',t_1\rangle\langle x'',t_1\mid x',t_0\rangle\\
......\\
Here\ t_2>t_1>t_0
$$

### Feynman's Formulation

$$
\langle x_n,t_n;x_{n-1},t_{n-1}\rangle=\frac{1}{\omega(\Delta t)}exp\left(\frac{i\int^{t_n}_{t_{n-1}}dt\mathcal{L}(x,\dot{x})}{\hbar} \right)\\
\langle x_n,t_n;x_{n-1},t_{n-1}\rangle=\sqrt{\frac{m}{2\pi i\hbar\Delta t}}exp\left(\frac{iS_{n,n-1}}{\hbar} \right)\\
S(n,n-1)=\int^{t_n}_{t_{n-1}}dt \left[\frac{m\dot{x}^2}{2}-V(x) \right]=\Delta t\left[\frac{m(x_{n}-x_{n-1})^2}{2\Delta t^2}-V(\frac{x_{n}+x_{n-1}}{2}) \right]\\
(Use\ the\ Lagarange\ mean\ value\ theorem\ to\ obtain\ the\ integral\ of\ the\ V\ term)\\
For\ a\ fress\ particle:\ V=0\ always\ holds\\
The\ normalization\ factor\ \sqrt{\frac{m}{2\pi i\hbar\Delta t}}\ is\ obtained\ from\ the\ integral\ of\ S:\\
\int^{t_n}_{t_{n-1}}dt \left[\frac{m\dot{x}^2}{2\hbar} \right]=\Delta t\left[\frac{m(x_{n}-x_{n-1})^2}{2\hbar\Delta t^2} \right]\\
The\ normalization\ relation\ requires:\\
N\int d(x_{n}-x_{n-1})\Delta t\left[\frac{m(x_{n}-x_{n-1})^2}{2\hbar\Delta t^2} \right]=1\\
Thus\ we\ have\ N=\sqrt{\frac{m}{2\pi i\hbar\Delta t}}\\
We\ can\ check\ \langle x_n,t_n;x_{n-1},t_{n-1}\rangle\Bigg{|}_{t_n=t_{n-1}}=\delta(x_n-x_{n-1}),\\
namely\ \lim\limits_{\Delta\rightarrow0}\sqrt{\frac{m}{2i\pi\hbar\Delta t}}exp\left(\frac{im(x_n-x_{n-1})^2}{2\hbar\Delta t}\right)=\delta(x_n-x_{n-1})
$$

$$
\langle x_n,t_n;x_{n-1},t_{n-1}\rangle=\sqrt{\frac{m}{2\pi i\hbar\Delta t}}exp\left(\frac{iS(n,n-1)}{\hbar} \right)\\
\langle x_N,t_N;x_1,t_1\rangle=\lim\limits_{N\rightarrow\infin}\left(\frac{m}{2\pi i\hbar\Delta t} \right)^{(N-1)/2}\int x_{N-1}\int x_{N-2}......\int x_{2}\prod_{n=2}^{N}exp
\left[\frac{iS(n,n-1)}{\hbar} \right]\\
=\int_{x_1}^{x_N}\mathscr{D}[x(t)]exp\left[i\int_{t_1}^{t_N}dt\frac{\mathcal{L}(x,\dot{x})}{\hbar} \right]
$$

Solve the $\langle x_N,t_N\mid x_1,t_1\rangle$:
$$
\langle x_N,t_N\mid x_1,t_1\rangle=\langle x,t+\Delta t\mid x_1,t_1\rangle=-\int d\xi\langle x,t+\Delta t\mid x-\xi,t\rangle\langle x-\xi,t\mid x_1,t_1\rangle\\
=\sqrt{\frac{m}{2i\pi\hbar\Delta t}}\int d\xi exp\left(\frac{im\xi^2}{2\hbar\Delta t}-\frac{iV\Delta t}{\hbar} \right)\langle x-\xi,t\mid x_1,t_1\rangle\\
$$
Expand $\langle x,t+\Delta t\mid x_1,t_1\rangle$ in t with Taylor series, at the beginning we remain the 1st term, then expand the exponential potential term and remain the second order:
$$
\langle x,t+\Delta t\mid x_1,t_1\rangle\simeq\langle x,t\mid x_1,t_1\rangle+\Delta t\frac{\partial}{\partial t}\langle x,t\mid x_1,t_1\rangle\\
=\sqrt{\frac{m}{2i\pi\hbar\Delta t}}\int d\xi exp\left(\frac{im\xi^2}{2\hbar\Delta t}\right)\left(1-\frac{iV\Delta t}{\hbar}+...... \right)\times\left[\langle x,t\mid x_1,t_1\rangle+\frac{\xi^2}{2}\frac{\partial^2}{\partial x^2}\langle x,t\mid x_1,t_1\rangle+...... \right]\\
=\sqrt{\frac{m}{2i\pi\hbar\Delta t}}\sqrt{2\pi}\left(\frac{i\hbar\Delta t}{m} \right)^{\frac{3}{2}}\frac{1}{2}\frac{\partial^2}{\partial x^2}\langle x,t\mid x_1,t_1\rangle-\frac{i}{\hbar}\Delta tV\langle x,t\mid x_1,t_1\rangle+\left(1-\frac{iV\Delta t}{\hbar} \right)\langle x,t\mid x_1,t_1\rangle
$$

### Gauge Transformation

For spatial uniform and time-dependent potential, 
$$
Gauge: V(\bold{x})\rightarrow V(\bold{x})+V_0(t)  \\
exp\left(-i\int_{t_0}^{t_n} dt'\frac{V_0(t')}{\hbar}\right)\mid\alpha,t_0;t\rangle\\
\phi_1-\phi_2=\frac{1}{\hbar}\int_{t_0}^{t_n}dt'(V_2(t')-V_1(t'))
$$
Gravity-Induced Quantum Interference
$$
\ddot{\bold{x}}=-\nabla\Phi_{grav}=-g\hat{\bold{z}}\\
\Phi_{grav}=mgz\\
\phi_{ABD}-\phi_{ACD}=-\frac{m_n^2gl_1l_2\lambda sin\delta}{\hbar^2}\\
m_n\ is\ the\ mass\ of\ the\ neutron,\ l_1\ and\ l_2\ are\ the\ length\ of\ two\ paths,\ \lambda\ is\ the\ de\ Broglie\ wavelength,\\ \delta\ is\ the\ angle\ that\ the\ plane\ of\ two\ paths\ is\ rotated\ from\ the\ direction\ of\ the\ gravity.
$$
AB effect: 
$$
H=\frac{\left(\bold{p}-\frac{e\bold{A}}{c}\right)^2}{2m}+e\phi\\
\phi\rightarrow\phi+\lambda,\ \bold{A}\rightarrow\bold{A};\\
or,\ \phi\rightarrow\phi-\frac{\partial\Lambda}{c\partial t},\ \bold{A}\rightarrow\bold{A}+\nabla\Lambda\\
\bold{E}=-\nabla\phi-\frac{\partial\bold{A}}{c\partial t},\ \bold{B}=\nabla\times\bold{A}
$$

$$
\bold{A}=\frac{B\rho_a^2}{2\rho}\hat{\bold{\phi}}\\
\mathcal{L}=\frac{m}{2}(\frac{d\bold{x}}{dt})^2+\frac{e}{c}\frac{d\bold{x}}{dt}\cdot\bold{A}\\
K(x_1,t_1;x_2,t_2)=Nexp\left(\frac{im(x_1-x_2)^2}{2\hbar\Delta t} \right) exp\left(i\int\frac{e}{\hbar c}dt\frac{d\bold{x}}{dt}\cdot\bold{A} \right)\\
The\ AB\ effect\ will\ change\ the\ path\ integral\ to :\\
\left\{\prod exp\left[\frac{iS^0(n,n-1)}{\hbar} \right] \right\}exp\left(\frac{ie}{\hbar c}\int_{x_1}^{x_N}\bold{A}\cdot d\bold{s} \right)\\
$$

The AB phase difference between the two paths is:
$$
\left[\frac{e}{\hbar c}\int_{x_1}^{x_N}\bold{A}\cdot d\bold{s}\right]_{\Gamma_1}-\left[\frac{e}{\hbar c}\int_{x_1}^{x_N}\bold{A}\cdot d\bold{s}\right]_{\Gamma_2}=\frac{e}{\hbar c}\oint_{\Gamma_1+\Gamma_2}\bold{A}\cdot d\bold{s}=\iint \bold{B}\cdot d\bold{a}=\frac{e}{\hbar c}\Phi_B\\
Here\ \Phi_B=\frac{\hbar}{|e|}m\ \ \ \ \ \ \ \ (m\ is\ an\ integer)
$$

## Chapter 3 

### Rotation Matrix

$$
R_z(\epsilon)=\begin{pmatrix}
1-\frac{\epsilon^2}{2}&-\epsilon&0\\
\epsilon&1-\frac{\epsilon^2}{2}&0\\
0&0&1
\end{pmatrix}\\
R_x(\epsilon)=\begin{pmatrix}
1&0&0\\
0&1-\frac{\epsilon^2}{2}&-\epsilon\\
0&\epsilon&1-\frac{\epsilon^2}{2}
\end{pmatrix}\\
R_y(\epsilon)=\begin{pmatrix}
1-\frac{\epsilon^2}{2}&0&\epsilon\\
0&1&0\\
-\epsilon&0&1-\frac{\epsilon^2}{2}
\end{pmatrix}\\
$$

$$
[R_x(\epsilon),R_y(\epsilon)]=R_z(\epsilon^2)-R_{x,y,z}(0)=R_z(\epsilon^2)-1
$$

### Infinitesimal Rotation

$$
\mid\alpha_R\rangle=\mathcal{D}(R)\mid\alpha\rangle\\
U_\epsilon=1-iG\epsilon\\
G=\frac{J_k}{\hbar}\\
\mathcal{D}(\hat{\bold{n}},d\phi)=1-i\frac{\bold{J}\cdot\hat{\bold{n}}d\phi}{\hbar}
$$

$$
From\ the\ closure: \mathcal{D}(R_1)\mathcal{D}(R_2)=\mathcal{D}(R_1R_2),\ and\ [R_x(\epsilon),R_y(\epsilon)]=R_z(\epsilon^2)-1,\\ we\ can\ derive\ the\ commutation\ relation:[J_i,J_j]=i\hbar\epsilon_{ijk}J_k
$$

### Rotation of Spin-$\frac{1}{2}$

$$
\mathcal{D}(\hat{\bold{n}},\phi)=exp\left(\frac{-i\bold{S}\cdot\hat{\bold{n}}\phi}{\hbar} \right)\\
\mathcal{D}_z^\dagger(\phi)S_x\mathcal{D}_z(\phi)=S_xcos\phi-S_ysin\phi\\
\mathcal{D}_z^\dagger(\phi)S_y\mathcal{D}_z(\phi)=S_ycos\phi+S_xsin\phi
$$

### Spin Precession Revisited

$$
H=-\frac{e}{m_e c}\bold{S}\cdot\bold{B}=\omega S_z\\
\mathscr{U}(t,t_0)=exp\left(\frac{-i\omega S_z(t-t_0)}{\hbar} \right)\\
\mid\alpha,t_0=0;t\rangle=e^{-i\omega t/2}{\mid+\rangle}{\langle+\mid}{\alpha\rangle}+e^{i\omega t/2}{\mid-\rangle}{\langle-\mid}{\alpha\rangle}\\
If\ it\ is\ rotated\ by\ a\ 2\pi\ phase,\ the\ state\ will\ have\ a\ minus\ sign,\ if\ it\ is\ rotated\ by\ a\ 4\pi\ phase,\\ the\ state\ will\ get\ back\ to\ the\ original.
$$

### Neutron Interferometry Experiment to Study 2$\pi$ Rotations

$$
\omega=\frac{g_neB}{m_pc}\\
\Delta B=\frac{4\pi\hbar c}{eg_n\lambda l}
$$

### Pauli Two-Component Formalism

$$
\left\{\sigma_i,\sigma_j\right\}=2\delta_{ij}\\ 
[\sigma_i,\sigma_j]=2i\epsilon_{ijk}\sigma_k
$$

$$
(\bold{\sigma}\cdot\bold{a})(\bold{\sigma}\cdot\bold{b})=\bold{a}\cdot\bold{b}+i\bold{\sigma}\cdot(\bold{a}\times\bold{b})\\
If\ \bold{a}\ is\ real,\ then\ (\bold{\sigma}\cdot\bold{a})^2=|\bold{a}|^2
$$

Rotation in Pauli's Formalism:
$$
(\bold{\sigma}\cdot\hat{\bold{n}})^n=\begin{cases} 
1,  & \mbox{if }n\mbox{ is even} \\
\bold{\sigma}\cdot\hat{\bold{n}}, & \mbox{if }n\mbox{ is odd}
\end{cases}\\
exp\left(\frac{-i\hbar\bold{\sigma}\cdot\hat{\bold{n}}\phi/2}{\hbar} \right)=\bold{1}cos(\phi/2)-i\bold{\sigma}\cdot\hat{\bold{n}}sin(\phi/2)
$$

### Orthogonal Group

$$
RR^T=1
$$

### Unitary Unimodular Group

$$
U(a,b)=\begin{pmatrix}
a&b\\
-b^*&a^*\\
\end{pmatrix}\\
U^{-1}(a,b)=U(a^*,-b) \ \ \ \ (SU(2)\ group,\ a\ subgroup\ of\ U(2).)
$$

### Euler Rotation

$$
R_{z'}(\gamma)=R_{y'}(\beta)R_{z}(\gamma)R_{y'}^{-1}(\beta)\\
R_{y'}(\beta)=R_{z'}(\alpha)R_{y}(\beta)R_{z'}^{-1}(\alpha)\\
R(\alpha,\beta,\gamma)=R_{z'}(\gamma)R_{y'}(\beta)R_{z}(\alpha)=R_z(\alpha)R_y(\beta)R_z(\gamma)\\
$$

### Density Operator

$$
Ensemble\ Average:\\
\langle\langle A\rangle\rangle=\displaystyle{\sum_i}\omega_i\langle\alpha^{(i)}\mid A\mid\alpha^{(i)}\rangle=tr(\rho A)\\
Density\ Operator:\\
\rho=\displaystyle{\sum_i}\omega_i\mid\alpha_i\rangle\langle\alpha_i\mid\\
tr(\rho)=1\\
\rho^2=1\ \ \ only\ for\ pure\ ensembles
$$

### Quantum Statistical Mechanics

$$
S=-kTr(\rho (ln\rho))
$$



