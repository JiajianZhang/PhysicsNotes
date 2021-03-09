# Solid state theory

## Chap 0 second quantization

### Fock states: creation & annihilation operators

1. Why do we need Fock states?

Mathematically: better to describe many-particle, identical particle, statistical features

Physically: In a system without particle-number conservation, first quantization is not enough

First quantization: $i \hbar \frac{\partial \Phi}{\partial t} = H\Phi$, it holds for particle-number-conserving Hamiltonian. while in superfluid, superconductivity, vacuum fluctuation, particle-number conservation is broken. 

2. Why second quantization is used in statistical physics?

In a grand canonical ensemble, the chemical potential is introduced to count the particle number for non-conserving case. 

### For a mono-body problem:

$i\hbar \frac{\partial \Psi(z,t)}{\partial t} = H\Psi(z,t)$, $H\varphi(z) = E\varphi(z)$, $\psi(t) = e^{-iHt/\hbar}\psi(t=0)$, here $\psi $ is the state, then we find a certain complete set of othonormal basis, the wavefunction can be expressed as: $\langle \psi_{\vec{k}}(z,t)\mid z\rangle$

The wavefunction expansion: 
$$
\varphi(z) = \sum_k \psi_k \varphi_{\vec{k}}(q)\\
H_{kk'} = \int dz \varphi_k^* (z) H \varphi_k(z)\\
\sum_{k'} H_{kk'}\psi_{k'} = E_k \psi_{k}
$$

### For a many-particle system

We use a complete set of othonormal basis, and try to do the following decomposition:
$$
\psi(q_1, q_2, q_3..., q_N; t) = \sum_{\alpha,\beta\,\gamma...} C_{\alpha,\beta\,\gamma...} \varphi_{\alpha}(q_1)\varphi_{\beta}(q_2)\varphi_{\gamma}(q_3)...
$$
This decomposition doesn't hold for many-body system. 

The state-determined particles are distinguishable, however, the identical particles have extra limitation for the system.

The cases, $p_1$ is at $q_1$, $p_2$ is at $q_2$ and $p_2$ is at $q_1$, $p_1$ is at $q_2$ are equivalent. This many-to-one mapping causes a incomplete set of basis. Now try to change it to one-to-one mapping.

Consider the wavefunction: $\psi(q_1,q_2,q_3,...q_N)$

Define a particle position exchanging operation by two steps: first rotate one of the particle around another one by half a circle; translate the positions of two particles by the same vector. (Since rotation by a full circle is an identical operation in 3-dim, the one-circle rotation operations in 3-dim is random)

After each exchanging operation, we have a phase: $\phi_{ij}$, ($\psi(...q_i,...q_j,...) =e^{i\phi_{ij}} \psi(...q_j,...q_i...)$)

Define the Fermion and Boson by: $\phi_{ij}^F=\pi, \phi_{ij}^B = 0$
$$
\varphi_{alpha,\beta,\gamma...}^S(q_1,...q_N) = \sqrt{\frac{\prod_i n_i!}{N!}}\sum_p p[\varphi_{k_1}(q_1)\varphi_{k_1}(q_2)... \varphi_{k_2}(q_1)\varphi_{k_2}(q_2)...]\\
(for\ each\ k_m,\ the\ position\ go\ over\ q_{i_1}\ to\ q_{i_{n_m}})\\
\varphi_{\alpha,\beta,\gamma...}^A(q_1,...q_N) = \frac1{\sqrt{N!} }\sum_p \delta_p p [\varphi_{\alpha}(q_1) \varphi_{\beta}(q_2)...]\\
$$
S is symmetric for Boson, A is anti-symmetric for Fermion, the Fermion basis can be rewritten as the determinant form. 
$$
\left|
\begin{matrix}
\varphi_{\alpha}(q_1) & \varphi_{\beta}(q_1) & ...\\
.\\.\\.\\
\varphi_{\alpha}(q_n) & \varphi_{\beta}(q_N) & ...
\end{matrix}
\right|
$$
The feature of determinant, any two same rows or columns will make the determinant 0, this is consistent with the Pauli's exclusion principle, proving that this basis is a good physical basis.
$$
H_{\{\alpha\},\{\alpha'\}} = \int \varphi_{\{\alpha\}}^{A*}(q_1,q_2,...)H(q_1,q_2,...)\varphi_{\{\alpha'\}}^{A}(q_1,q_2,...)
$$

Here the wavefunction is the expression in equation(3)

What is wavefunction?

For an arbitrary quantum state, choose a set of basis under certain representation to expand the state, the coefficients are the wavefunctions. 

For example, a point in the coordinate space, $\mid q\rangle$, as the basis to expand state $\mid\psi\rangle$, it would be: $\mid\psi\rangle = \sum_k \mid q_k\rangle\langle q_k\mid \psi\rangle = \sum_k \psi_k(q)\mid q_k\rangle $ or $\int dq \langle q\mid\psi\rangle \mid q\rangle$

Why the description of a quantum state is so complicated? 

Because we get used to use wavefunctions to describe quantum states. If we directly give the state a label, it would be simple. This method is the $\bold{Fock\ State}$

For Bosons: 
$$
\varphi^A = p(\varphi_{k_1},...\varphi_{k_{n_1}},\varphi_{k_2},...\varphi_{k_{n_2}},...)\\
\mid n_{k_1},n_{k_2},...\rangle \Longrightarrow \mid n_1,n_2,...\rangle
$$
p is the permutation operator, $n_1$ particles are on $k_1$ state, $n_2$ particles occupy $k_2$ state.

Whereas, for identical particles, symmetric or anti-symmetric might be not a problem at all, because we only consider how many particles are on state 1, the position is unnecessary to know since we don't need wavefunctions to describe the states.

For Fermions:

$n_i\rightarrow i_{\{\alpha,\beta,\gamma...\}}\rightarrow \{\alpha,\beta,\gamma...\}$, $n_i = 0,1,2,...$

Fock state is powerful because it's simple.

### The formalism of operators under Fock states

Single-body operator: $F= \sum_i f(q_i)$

$\hat{F} = \sum_i f_{\alpha,\beta}a_{\alpha}^{\dagger}a_{\beta} $,  ex: $-\frac{\hbar^2}{2m}\nabla_{q_i}^2$, $V(q_i)$

Two-body operator: $G = \sum_{ij} \frac12(q_i,q_j)$

ex: Coulomb potential $1/{|q_i-q_j|}$
$$
\hat{G} = \frac12\sum_{\alpha',\beta',\alpha,\beta}g_{\alpha',\beta',\alpha,\beta}a^{\dagger}_{\alpha'}a^{\dagger}_{\beta'}a_{\alpha}a_{\beta}
$$
Prove the equation above:

### Creation/annihilation operator

A short review of 1d SHO, why is it important?

The study of condensed matter physics usually acts perturbation around the equilibrium state, where the first-order term is zero, the second-order term is the SHO at the equilibrium.  

The algebraic understanding of SHO:

$H = Ap^2 + Bx^2$ , in order to obtain the square formula, we quantize it to SHO.

 Now if only the commutative relation $[a,a^{\dagger}]=1$ is known, and the Hamiltonian $H = \hbar\omega(a^{\dagger}a+\frac12)$, the eigenstate of $\hat{n}\mid n\rangle = n\mid n\rangle$, therefore, $[a,\hat{n}]=a\Longrightarrow \hat{n}a = a\hat{n}-a$, $\hat{n}a\mid n\rangle = a\hat{n}\mid n\rangle-a\mid n\rangle = (n-1)a\mid n\rangle$, so $\{a\mid n\rangle\}$ is the eigenstate of $\hat{n}$. Moreover, if we act $\hat{n}$ on $a\mid n\rangle$, the eigenvalue will decrease since n will -1 after each $\hat{n}$. Will n be negative infinite?

In Hilbert space, $n = \langle n\mid \hat{n}\mid n\rangle = \langle n\mid a^{\dagger}\hat{n}a\mid n\rangle\geq0$, so $n = 0,1,2,...$

(When we choose the basis, the map from Hilbert space to the physical space is not dependent on the phase factor $e^{i\phi}$.)

 An alternative point of review:

The Fock state representation describes this type of particles: the energy of a single particle is $E = \hbar\omega$, on this energy state, there could be n particles occupied, and no particle-particle interactions are considered. This indicates that SHO is exactly Boson.

### Generalization of creation & annihilation operators

Bosonic:

$a\rightarrow a_i$, $a^{\dagger}\rightarrow a_j^{\dagger}$, $[a_i, a_j^{\dagger}] = \delta_{ij}$
$$
\mid n_1,n_2,...\rangle = \frac1{\sqrt{n_1!n_2!...}}(a_1^{\dagger})^{n_1}(a_2^{\dagger})^{n_2}...\mid 0\rangle\\
\hat{F} \rightarrow F_{\{m_i\}\{n_i\}} = \langle\{m_i\}\mid \hat{F}\mid \{n_i\}\rangle\\
\hat{F} = \sum_{\{m_i\}\{n_i\}}F_{\{m_i\}\{n_i\}}\mid \{m_i\}\rangle\langle\{n_i\}\}\mid\\
$$
Fermionic:

classical $\rightarrow $ Boson $\rightarrow$ SHO, this is a standard idea of QFT

For fermion, if T is low enough, lower than the fermion temperature, we can see the statistical features (ex: forming a Fermi sphere)

Single mode: $\mid0\rangle,\ \mid1\rangle$

$c^{\dagger}\mid0\rangle= \mid1\rangle$  $c^{\dagger}\mid1\rangle=0$, no length, not a physical state

$\{c,c^{\dagger} \}=1$,  $c^2 = \{c,c \} = 0$,  $(c^\dagger)^2 = \{c^\dagger,c^{\dagger} \}=0$

General case for Fermion
$$
c_\alpha, c_\beta, c_\gamma,...\\
c_{\alpha}^{\dagger}, c_{\beta}^{\dagger}, c_{\gamma}^{\dagger},...\\
\{c_{\alpha},c_{\beta}^{\dagger} \} = \delta_{\alpha,\beta}\\
\{c_{\alpha}, c_{\beta} \} = \{c_{\alpha}^{\dagger}, c_{\beta}^{\dagger} \}=0\\
\hat{n_{\alpha}} = c_{\alpha}^{\dagger}c_\alpha
$$
If $\alpha \neq \beta$, the anti-commutative relation can be changed to commutative relation, it doesn't affect the Pauli exclusion principle.

Eigenstate of $\{n_{\alpha} \}$: $\mid n_\alpha,n_\beta,n_{\gamma},...\rangle (n_i = 0,1,...)$
$$
\mid n_{\alpha}, n_{\beta}, n_{\gamma},...\rangle = (c_{\alpha}^\dagger)^{n_\alpha}(c_{\beta}^{\dagger})^{\dagger}...\mid0\rangle\\
\Longrightarrow (another\ notation)\\
\mid \alpha,\beta,\gamma,...\rangle = (c_{\alpha}^{\dagger})(c_\beta^{\dagger})(c_{\gamma}^{\dagger})...\mid0\rangle
$$
Notice that here the order of $\alpha,\beta,\gamma,...$ should be defined, otherwise the permutation will lead in minus signs.:

$\mid\beta,\alpha,\gamma,...\rangle = -\mid \alpha,\beta,\gamma,...\rangle$
$$
c_\alpha^{\dagger}\mid ...n_{\alpha}...\rangle = \delta_{n_\alpha,0}(-1)^{\sum_{v=1}^{\alpha-1}n_v}\mid ...1_\alpha...\rangle\\
c_{\alpha}\mid ...n_\alpha...\rangle = \delta_{n_\alpha,1}(-1)^{\sum_{v=1}^{\alpha-1}n_v}\mid...0_{\alpha}...\rangle\\
$$
The sum of $n_v$ represents the population 

Why single/double-body operators can be written as the formalism above?

Consider: 

Bosonic case: a single-body operator:
$$
\hat{F_1} = \sum_i \hat{f}(q_i)\\
\hat{F_2} = \sum_{ij} f_{ij} a_i^{\dagger}a_j\\
(f_{ij} = \int dq\psi_i^*(q) \hat{f} \psi_j(q))\\
$$
Are the two expressions above equivalent? Following is the proof.

We calculate the matrix elements: $\langle\{n_i' \}\mid \hat{F_2}\mid \{n_i \}\rangle = \int dq_1dq_2...\psi_{\{n_i' \}}^{S*}(q_1,...q_N) \hat{F_2}\psi_{\{n_i \}}^S(q_1,...q_n) $
$$
a_i^{\dagger}a_j\mid ...n_i...n_j\rangle = \mid...n_i+1,...n_j-1,...\rangle \ (i\neq j)\\
elsewise\ \ \mid...n_i...\rangle\ \ (i=j)\\
\int dq_1...dq_N \psi_{\{n_i'\}}^{*S}\hat{F_1} \psi_{\{n_i \}}^S = N\int dq_1...dq_N \psi^{*S}\hat{f}(q)\psi^S\ (here\ \hat{F_1} = \sum_i \hat{f}(q_i))
$$

## Chap 2 Phonon

### Einstein Model

Classical approach of studying phonon is the considering it as lattice wave, this is common in classical field theory. 

Our thought will be as following: quantizing the lattice wave, and what is obtained is the quantum field theory.

The properties should be noticed here are: DOS, $C_V$, Von-Home singularity, etc.

ex: atomic crystal Ar, it's FCC solid, now assume it's simple cubic, consider merely the Van Der Waals force dominates, set the origin at the equilibrium center, the potential atoms feel is $\Phi(\vec{r})$, with the small displacement approximation, the vibration is SHO, after quantization, $E = (n+\frac12)\hbar\omega_E$.

A natural idea: each atom vibrates independently and could be considered as a SHO with frequency $\omega_E$, "E" marks Einstein since this idea is conjectured by him. Einstein's model works in normal temperature, whereas, at low temperature, correlated vibrating modes become more important than normal, those modes will lead to lower ground state energy.

The advantages of Einstein model: 

1. Justified at high T
2. Effective as a brutal estimation of thermal vibration
3. The optical phonon can be considered as SHO in some cases.

Ex: simple lattice, N unit cells, atom with mass M, lattice vector $\vec{R_L}=\sum_il_i\vec{a}_i, (l_i\in \mathbb{Z})$, 

Following the classical field theory, the first step is to describe the states as: 
$$
\{\vec{r}_i, \dot{\vec{r}}_i \},\ i = 1,...,N\\
\Longrightarrow
\{\vec{u}_i, \dot{\vec{u}}_i \},\ \vec{u}_i = \vec{r}_i - \vec{R}_i
$$
 Then find the potential in small-displacement approximation:
$$
E = H(\vec{u}_i,\vec{p}_i)\longrightarrow equation\ of\ motion\\
E = T+V\\
T = \frac12\sum_l M\dot{\vec{u}}_l^2 = \frac12\sum_{l,\alpha}M(\dot{\vec{u^\alpha_l}} )^2,\ \alpha=x,y,z\\
V = V(\{\vec{u}_l \})\\
V = V\big|_{n_l = 0} + \frac12 \sum_{l,l',\alpha,\beta} \frac{\partial^2 V}{\partial u_l^\alpha \partial u_{l'}^{\beta} } u_{l}^{\alpha}u_{l'}^\beta+...\\
V\big|_{n_l = 0}\equiv V_0,\ \ \frac{\partial^2 V}{\partial u_l^\alpha \partial u_{l'}^{\beta}} \equiv \Phi_{\alpha,\beta}(l,l')
$$
Remark: 

1. $\Phi_{\alpha,\beta}(l,l')$ is real
2. $\Phi_{\alpha,\beta}(l,l')=\Phi_{\beta,\alpha}(l',l)$, it's symmetric ($\Phi_{\alpha l,\beta l'}$ is a matrix element)
3. $\Phi$ matrix is positive definite. 
4. Translational invariant: $\Phi_{\alpha,\beta}(l,l') = \Phi_{\alpha\beta}(l-l')-\Phi_{\beta\alpha}(l'-l)$,  ($l-l' = \mid\vec{R}_l - \vec{R}_{l'}\mid$)
5. $\sum_{l'}\Phi_{\alpha,\beta}(l,l')=0$ This is not difficult to understand since the translation of the total lattice is equivalent to doing nothing. 

Using the SHO approximation:
$$
H = \frac12M\sum_{l,\alpha}(\dot{u}_l^\alpha)^2 + \frac12\sum_{l\alpha}\sum_{l'\beta} \Phi_{\alpha,\beta}(l,l')u_{l}^\alpha u_{l'}^\beta\\
P_l^\alpha = M\dot{u}_l^\alpha \ (conjugate\ momentum\ of\ u_l^\alpha)
$$
When the parameter $l,l',\alpha,\beta$ are taken extremely dense, the sum becomes integral, we go back to classical field theory.

In Hamilton mechanics:

Equation of motion can be written as:
$$
\dot{P}_l^\alpha = -\frac{\partial H}{\partial u_l^\alpha} \Longrightarrow M\ddot{u}_l^\alpha = -\sum_{l',\beta}\Phi_{\alpha\beta}(l-l')u_{l'}^\beta\\.\\.\\.\\(3N\ eqns)
$$
Take the Bloch theorem $u_l^\alpha = e^{i\vec{k}\vec{R}_l}U_l^\alpha$ into the eqn above, since it has translational invariance, the result is equivalent to do a $\bold{Fourier\ Transformation}$ to $\Phi_{\alpha\beta}(l-l')$

$\bold{N}\times3$
$$
\dot{U}_k^\alpha = -\sum_{\beta}D_{\alpha\beta}(\vec{k})U_k^{\beta}\\
D_{\alpha\beta}(\vec{k}) = \frac1M \sum_l\Phi_{\alpha\beta}(l)e^{-i\vec{k}\cdot\vec{R}_l}\\
De = \omega^2 e
$$
Why the last eqn above holds? (Why D is positive definite?)
$$
D^*_{\beta\alpha}(\vec{k}) = \frac1M\sum_{l}\Phi_{\beta\alpha}(l)e^{i\vec{k}\cdot\vec{R}_l}\\
(\Phi_{\beta\alpha}(l) = \Phi_{\alpha\beta}(l)) \\
\frac1M \sum_{l} \Phi_{\alpha\beta} (l) e^{-i\vec{k}\cdot\vec{R}_l}\\
=D_{\alpha\beta}(\vec{k})\\
so\ D^{\dagger}(\vec{k}) = D(\vec{k}),\ it's\ Hermitian
$$
eigenvalues: $\omega_\sigma(\vec{k})\ \ (\sigma=1,2,3...) $

eigenvectors: $\vec{e}_{\vec{k},\sigma}$

$\vec{e}_{k,\sigma}\cdot\vec{e}_{k,\sigma'}=\delta_{\sigma,\sigma'}$, $\sum_\sigma e_{k\sigma}^\alpha e_{k\sigma'}^{\beta}=\delta_{\alpha\beta} $, the special solution: $U_k^\alpha \propto e^{-i\omega_{k\sigma}t}e_{k\sigma}^\alpha\ (\sigma = 1,2,3...) $

$u_l^\alpha \propto \frac1{\sqrt{N}}\vec{e}_{k\sigma}^\alpha e^{i(\vec{k}\vec{R}_l - \omega_{k\sigma}t)} $

$\vec{e}_{k\sigma}^\alpha$ is similar to the polarization vector of EM wave, here it is denoted as "lattice wave". $e^{i(\vec{k}\vec{R}_l - \omega_{k\sigma}t)}$ is similar to propagating plane wave, and $l$ is discrete, the real plane wave $u(x)$ has continuous $x$.

General solution:
$$
\vec{u}_l(t) = \frac1{\sqrt{NM}}\sum_{k\sigma}\vec{e}_{k\sigma}Q_{k\sigma}(t) e^{i\vec{k}\cdot\vec{R}_l}\\
(Q_{k\sigma}\ denotes\ the\ normal\ coordinates)\\
normal\ mode:
\vec{u}_l = A\frac1{\sqrt{N}}\vec{e}_{k\sigma} e^{i(\vec{k}\cdot\vec{R}_l-\omega_{k\sigma}t)}
$$
$Q_{k\sigma}(t)$ is determined by initial conditions. The total $\vec{u}_l(t)$ is a sum of all normal modes, or saying a superposition of lattice wave. (All above is the single atom per unit cell case) Now consider each unit cell with $r$ atoms inside.

EoM: 
$$
M_S \ddot{u}_l^\alpha(s) = -\sum_{l's'\beta}\Phi_{\alpha\beta}\left(\begin{matrix}l,-l'\\s,s'  \end{matrix}\right)\vec{u}_{l'}^\beta(s'),\ (s,s' = 1,...r)\\
M_S \ddot{u}_k^\alpha(s) = -\sum_{\beta,s'} D_{\alpha\beta}\left(\begin{matrix}\vec{k}\\s,s' \end{matrix}\right) U_k^\beta(s')\\
\omega^2(\sqrt{M_S}\tilde{U}_k^\alpha(s)) = \sum_s \frac1{\sqrt{M_S M_{S'}}} D_{\alpha\beta}\left(\begin{matrix}k\\s,s' \end{matrix} \right)\tilde{U}_k^\beta (s')\sqrt{M_{s'}}\\
\tilde{D}_{\alpha\beta}\left(\begin{matrix}k\\s,s' \end{matrix} \right) \equiv \frac1{\sqrt{M_S M_{S'}}} D_{\alpha\beta}\left(\begin{matrix}k\\s,s' \end{matrix} \right)
$$
$3r\times3r$ matrix $\tilde{D}$ ($\alpha,\beta,\gamma$ denotes the xyz axes, 3-dim; $s,s'$ take values from 1 to r, r-dim)

$\tilde{D}e_k^\beta(s') = \omega^2 e^\alpha_k(s)\rightarrow \omega_{k\sigma},\vec{e}_{k\sigma}(s),\ (\sigma=1,2,...3r)$,  D has 3r eigenvalues.

The general solution: $\sum_s \vec{e}_{kr}^*(s)\cdot \vec{e}_{kr'}(s) = \delta_{\sigma\sigma'}$

$\vec{u}_l(s)=\frac1{\sqrt{NM_s}}\sum_{k,\sigma}\vec{e}_{k\sigma}(s) Q_{k\sigma} e^{i\vec{k}\cdot\vec{R}_l} $,  $\frac1{\sqrt{B}}A\frac1{\sqrt{B}}\sqrt{B}u = e\sqrt{B}u$

### SHO lattice model

Consider the following lattice: ${\Large\varepsilon}\times 1$, lattice constant $a$, spring constant $f$

$\Phi_{\alpha\beta}(l)=?$, may be $\frac12f(u_1-u_2)^2$

The force acting on the direction of the spring: $\vec{F} = - f\Delta u \hat{R}_l$; the force acting on the perpendicular direction of the spring: $\vec{F_\perp} = -f(\sqrt{R_l^2 + \Delta u^2}-R_l)\hat{R}_{\perp}$, this term can be expanded by Taylor series and take the first order under SHO approximation, while the first order term is zero, so this term doesn't exist if the displacement is small.

The potential (which generate the force above) can be written as: 
$$
\Phi_{\alpha\beta}(l) = -f_l(\hat{R}_l\cdot\hat{\beta})(\hat{R}_l\cdot\hat{\alpha})\\
\Phi(\hat{x}) = \Phi(-\hat{x}) = -f_1\begin{matrix}\hat{x}\ \ \ \hat{y} & \\ \left(\begin{matrix} 1 & 0\\ 0 & 0 \end{matrix}\right) \end{matrix}\\
\Phi(\hat{y}) = \Phi(-\hat{y}) = -f_1\left(\begin{matrix}0 & 0\\ 0 & 1\end{matrix} \right)
$$
$l=0$,  $\sum_l \Phi_{\alpha\beta}(l)=0$

$\Phi_{\alpha\beta}(0) = -\sum_{l\neq0}\Phi_{\alpha\beta}(l) = f_1\left(\begin{matrix}2 & 0\\0 &2 \end{matrix}\right) $

Apply the same trick in previous section in CH2: Fourier transformation, then
$$
D(k) = \frac1M\sum_l \Phi(l) e^{-i\vec{k}\cdot\vec{l}}\\
=\frac2M\left(\begin{matrix} \hbar(1-cosk_xl)& 0\\ 0 & \hbar(1-cosk_yl) \end{matrix} \right)
$$
Eigenvalue: $\omega_1^2(k)$ (suppose this one is smaller), $\omega_2^2(k)$
$$
\omega_1(k) = min\left(2\sqrt{\frac{f_1}{M}}\mid sin{\frac{k_x}{2}}a\mid, 2\sqrt{\frac{f_1}{M}}\mid sin{\frac{k_y}{2}a}\mid \right)\\
\omega_2(k) = min\left(2\sqrt{\frac{f_2}{M}}\mid sin{\frac{k_x}{2}}a\mid, 2\sqrt{\frac{f_2}{M}}\mid sin{\frac{k_y}{2}a}\mid \right)
$$

#### High symmetry points/lines

figure1 figure2



#### Properties of $\omega_{\sigma}(\vec{k})$

1. $\vec{k}$-reciprocal lattice vector, $\omega_{\sigma}(\vec{k}+\vec{\kappa}) = \omega_{\sigma}(\vec{k})$. $D_{\alpha\beta}(\vec{k}+\vec{\kappa}) = \frac1M\sum...e^{i\vec{k}\cdot\vec{R}_l} = D_{\alpha\beta}(\vec{k})$, $e^{i\vec{k}\cdot\vec{R}_l}=1$
2. $\omega_{\sigma}(\vec{k})$ respects point group symmetry. General case: $\omega_{\sigma}(\vec{k}),\omega_{\sigma}(g\cdot\vec{k}),g\in G$. $D_{\alpha\beta}(g\cdot\vec{k}) = \frac1M\sum_l \Phi(l) e^{-i(g\cdot\vec{k})\vec{R}_l} = \frac1M \sum_l\Phi(g^{-1}\cdot l)e^{-i\vec{k}\cdot\vec{R}_l}=D_{\alpha\beta}(g^{-1}\cdot\vec{l}) $, $e^{-i(\vec{g}\cdot\vec{k})\vec{R}_l}= e^{-i\vec{k}\cdot(g^{-1}\cdot\vec{R}_l)}$

3. $\omega_{\sigma}(\vec{k})=\omega_{\sigma}(-\vec{k})\Longleftarrow  $ if it's T-symmetric. $D(-\vec{k}) = \{\frac1M \sum\Phi^*(l)e^{-i\vec{k}\cdot\vec{R}_l} \}^*=\{\frac1M \sum\Phi(l)e^{-i\vec{k}\cdot\vec{R}_l} \}^*=D^*(k) $. $D^*(k)\vec{e}^* = \omega^2\vec{e}^*$. This indicates that D is unnecessary to be space-symmetric, this property (3) still holds when it's T-symmetric, too.

4. $\omega_{\sigma}(\vec{k}=0)=0$, $D(\vec{k}=0)=\frac1M\sum\Phi(l)=0$, for simple cubic lattice, lattice with basis: $D_{\alpha\beta}\left(\begin{matrix}k=0\\s,s' \end{matrix} \right) =\frac1{\sqrt{M_sM_{s'}}}\sum_l \Phi_{\alpha\beta}\left(\begin{matrix}l\\s,s' \end{matrix} \right) $.  Special solution: $\frac{e^{\alpha}_T(s)}{\sqrt{M_s}}=\frac{e^{\alpha}_T(s')}{\sqrt{M_{s'}}}\rightarrow \omega_{\sigma}^2(T)=0 $. $\omega_{\sigma}^2(T)e_T^{\alpha}(s) = \sum_{s'}D_{\alpha\beta}\left(\begin{matrix}T\\ s,s' \end{matrix} \right)e_T^{\beta}(s')=\frac1{\sqrt{M_s}}\sum_{s'}\frac{e_T^\beta(s')}{\sqrt{M_s}}\Phi_{\alpha\beta}\left(\begin{matrix}l\\ s,s' \end{matrix} \right) $. If the last term, the $\Phi$ is 0, then $\omega_{\sigma}^2(T)$ must be 0 since the eigenvectors cannot be 0.  In d-dim, there are only d independent $\frac{\vec{e}_T(s)}{\sqrt{M_s}}$ vectors. Therefore, ther are only d branches $\omega_r(\vec{k})$ (acoustic modes), $r = 1,...d$ with $\omega_r(T)=0$.

    

   ### Example: Diatomic chain

   Two types of atoms lay in series alternatively. One mass M, another mass m, r denotes r types of atoms, d denotes the dimension. If M=m, how to return to the mono-atomic chain?

   Note: d-dim $\rightarrow$ d acoustic modes is not occasional, $\vec{u}_l(\vec{s})=const$, it's related to spontaneous symmetry breaking. 
   $$
   D(\vec{k}) = \frac2M\left[\begin{matrix}f_1(1-cosk_xa) & 1-f_2(1-cos(k_xa)cos(k_ya))\\
   f_2sin(k_xa)sin(k_ya) & f_1(1-cos(k_ya))+f_2(1-cos(k_xa)cos(k_ya)) \end{matrix}\right]
   $$

   1. From $\Gamma$ to M, $\vec{k} = (\frac{k}{\sqrt{2}}, \frac{k}{\sqrt{2}} )$

   $\omega^2(\vec{k}) = \frac2M\left[f_1(1-cos^2(ka/{\sqrt{2}}))+f_2(1-cos^2(ka/\sqrt{a}))\pm f_2sin^2(ka/{\sqrt{a}}) \right] $

   ​       Longitudinal:  $\omega_L(\vec{k})\rightarrow $ eigenvector: $\vec{e}_L(\vec{k}) = (\frac1{\sqrt{2}},\frac1{\sqrt{2}})^T$;  Transverse:  $\omega_T(\vec{k}) \rightarrow$ eigenvector: $\vec{e}_T(\vec{k}) = (-\frac1{\sqrt{2}}, \frac1{\sqrt{2}})$. $\vec{e_1}//\vec{k}$, $\vec{e}_2\perp \vec{k}$.  Usually, $\omega_L(\vec{k})>\omega_{T}(\vec{k})$

   <img src="C:\Users\ZJJ-quantum\AppData\Roaming\Typora\typora-user-images\image-20210308154645478.png" alt="image-20210308154645478" style="zoom:50%;" />

   $4f_2>f_1$

   2. From $\Gamma$ to $X$   $\vec{k} = (k,0)$

   $\omega_L^2:$  $\vec{e}_L = (1,0)$,  $\omega_T^2$:  $\vec{e}_k = (0,1)$,  $\omega_L(\vec{k})\geq \omega_k(\vec{k})$

   

   3. From $X$ to $M$  $\vec{k} = (\frac{\pi}a,k')$

   $\omega_1^2$:  $\vec{e}_1 = (0,1)$,  $\omega_2^2$:  $\vec{e}_2 = (1,0)$

   Longitudinal wave and transverse wave are not always able to define. With small k, they're defined, but large k, lattice is not ignorable, they cannot be defined.

   Remark:

   The lattice waves are longitudinal or transverse only when they propagate along some high-symmetry lines. (maybe there exist exceptions. )

Tips:

Normal coordinate:
$$
\vec{U}_l(t) = \frac1{\sqrt{NM}}\sum_{k,\sigma}Q_{k\sigma}(t)\vec{e}_{k\sigma}e^{i\vec{k}\cdot\vec{R}_l}\\
=\frac1{\sqrt{NM}} \sum_{k,\sigma} Q^*_{k\sigma}(t) \vec{e}^*_{k\sigma}e^{-i\vec{k}\cdot\vec{R}_l}\\
$$
$k $ has $n$ possible values to choose, $\sigma$ has $d$ possible values, there are $6n$ values in total.

$Q_{k\sigma}\vec{e}_{-k\sigma} = Q^*_{k\sigma}\vec{e}_{k\sigma}^*$

Since $D(-k) = D^*(k)$,  $\vec{e}_{-k\sigma} = \vec{e}_{k\sigma}^*\Longrightarrow Q_{-k\sigma} = Q_{k\sigma}^*$
$$
H = \frac12\sum_{k\sigma}\left\{\dot{Q}_{k\sigma}^*\dot{Q}_{k\sigma} + \omega_{\sigma}^2(\vec{k})Q^*_{k\sigma}Q_{k\sigma} \right\}\\
\ddot{Q}_{k\sigma} + \omega^2_{k\sigma}Q_{k\sigma} = 0\\
Q_{k\sigma} = \sqrt{M/N} \sum_l (\vec{e}_{k\sigma}\cdot\vec{u}_l)e^{-i\vec{k}\vec{R}_l}
$$
$Q_{k\sigma}$ here describes the collective motions, corresponding to some collective coordinates. 