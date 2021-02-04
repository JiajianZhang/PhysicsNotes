### Angular Momentum addition

$J_{\pm} = J_x\pm iJ_y$

$[J^2,J_{\pm}]=0$

$[J_z,J_{\pm}] = \hbar J_{\pm}$

$[J_+,J_-]=2\hbar J_z$

$J^2\mid j,m\rangle = \hbar^2j(j+1)\mid j,m\rangle $

$J_z\mid j,m\rangle = m\hbar\mid j,m\rangle $

$J_{\pm}\mid j,m\rangle = \hbar\sqrt{(j\mp m)(j\pm m+1)}\mid j,m\pm1\rangle $

$D_{m'm}^{(j)}(R) = \langle j,m'\mid D(R)\mid j,m\rangle$

$D_{m'm}^{(j)}(\alpha,\beta,\gamma) = \langle j,m'\mid exp(-\frac{iJ_z\alpha}{\hbar})exp(-\frac{iJ_y\beta}{\hbar})exp(-\frac{iJ_z\gamma}{\hbar})\mid j,m\rangle = e^{-i(m'\alpha+m\gamma)}d_{m'm}^{(j)}(\beta) $

### Orbital angular momentum

$\langle \vec{x}'\mid L_x\mid \alpha\rangle = -i\hbar(-sin\phi\frac{\partial }{\partial \theta}- cot\theta cos\phi\frac{\partial}{\partial\phi})\langle\vec{x}'\mid \alpha\rangle$

$\langle\vec{x}'\mid L_y\mid\alpha\rangle = -i\hbar(cos\phi\frac{\partial}{\partial\theta} - cot\theta sin\phi\frac{\partial}{\partial\phi})\langle \vec{x}'\mid\alpha\rangle$

$\langle\vec{x}'\mid L_z\mid \alpha\rangle = -i\hbar\frac{\partial}{\partial\phi}\langle\vec{x}'\mid\alpha\rangle$

$\langle\vec{x}'\mid L^2\mid\alpha\rangle = -\hbar^2(\frac1{sin^2\theta}\frac{\partial^2}{\partial\phi^2}+\frac1{sin\theta}\frac{\partial}{\partial\theta}(sin\theta\frac{\partial}{\partial\theta}))\langle\vec{x}'\mid\alpha\rangle $

The transformation from Levi tensor to Dirac's delta notation: $\epsilon_{ijk}\epsilon_{lmk} = \delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}$

#### Addition 

$J = L\otimes I_S + I_L\otimes S$

$R(\vec{n}) =exp(-i\vec{L}\cdot\hat{n}/\hbar)\otimes exp(-i\vec{S}\cdot\hat{n}/\hbar) $

spin state $\mid+\rangle \mid-\rangle$

New four basis of a spin-spin coupling system, with both parts spin-1/2

$\mid s=0,m=0\rangle = \frac1{\sqrt2}(\mid-+\rangle - \mid+-\rangle)$

$\mid s=1,m=-1\rangle = \mid--\rangle$

$\mid s=1,m=0\rangle = \frac1{\sqrt2}(\mid-+\rangle+\mid+-\rangle)$

$\mid s=1,m=1\rangle = \mid++\rangle$

### Spherical Harmonic function as Rotation matrices

$\langle \bold{x}'\mid n,l,m\rangle = R_{nl}(r)Y_{l}^{m}(\theta,\phi) $

$\langle \bold{n}\mid l,m\rangle = Y_l^m(\theta,\phi)$
$$
\mid \bold{\hat{n}}\rangle=\mathscr{D}(R)\mid \bold{\hat{z}}\rangle=\sum_{l}\sum_{m}\mathscr{D}(R)\mid l,m\rangle\langle l,m\mid\bold{\hat{z}}\rangle\\
\langle l,m\mid\bold{\hat{n}}\rangle=\sum_m\mathscr{D}_{m'm}^{(l)}(\alpha=\phi,\beta=\theta,\gamma=0)\langle l,m\mid\bold{\hat{z}}\rangle\\
\langle l,m\mid\bold{\hat{z}}\rangle=\sqrt{\frac{2l+1}{4\pi}}\delta_{m'0}
$$

### Schrodinger equation for central potentials

$$
[\bold{L,x^2}]=[\bold{L,p^2}]=0\\
 [\bold{L},H]=[\bold{L^2},H]=0\\
u_{El}(\rho)=\rho^{l+1}e^{-\rho}\omega(\rho)\\
E_{l=0}=\frac{\hbar^2}{2ma^2}[\pi^2,(2\pi)^2,(3\pi)^2{\cdot\cdot\cdot}]
$$

### Isotropic Harmonic Oscillator

$$
u(\rho)=\rho^{l+1}e^{-\rho^2/2}f(\rho)\\
E_N=(N+\frac32)\hbar\omega\\
$$

### CG coefficient

CG is the transformation matrix element of the two bases

$\mid j_1,j_2,m_1,m_2\rangle \Longrightarrow \mid j_1,j_2,j,m\rangle$

$\langle j_1,j_2,m_1,m_2\mid j_1,j_2,jm\rangle$ is the CG coefficient

$J_1^2\mid j_1,j_2,m_1,m_2\rangle = j_1(j_1+1)\hbar^2\mid j_1,j_2,m_1,m_2\rangle$

$J_{1z}\mid j_1,j_2,m_1,m_2\rangle = m_1\hbar\mid j_1,j_2,m_1,m_2\rangle$

$J_1^2\mid j_1,j_2,jm\rangle = j_1(j_1+1)\hbar^2\mid j_1,j_2,jm\rangle$

$J^2\mid j_1,j_2,jm\rangle = j(j+1)\hbar^2\mid j_1,j_2,jm\rangle $

$J_z\mid j_1,j_2,jm\rangle = m\hbar\mid j_1,j_2,jm\rangle$

The selection rule of CG coefficient: 

$m = m_1+m_2$, otherwise CG is 0. Proof, use $J_z-J_{1z}-J_{2z} $ to obtain it. And we should have $\mid j_1-j_2\mid\leq j\leq j_1+j_2 $

The CG coefficient form a unitary matrix. So the rows and columns are orthogonal. 

#### How to obtain CG?

Use $J_-,J_+$ to act on a known state $\mid j_1,j_2,jm\rangle$, only $m$ will change on the resulting state. 

$\langle j_1,j_2,m_1,m_2\mid J_{\pm}\mid j_1,j_2,jm\rangle = \langle j_1,j_2,m_1,m_2\mid (J_{1\pm} + J_{2\pm})\sum_{m_1'}\sum_{m_2'}\mid j_1,j_2,m_1',m_2'\rangle\langle j_1,j_2,m_1',m_2'\mid j_1,j_2,jm\rangle $

And significantly, we should have the total normalization:

$\sum_{m_1}\sum_{m_2}\mid \langle j_1,j_2,m_1,m_2\mid j_1,j_2,jm\rangle\mid^2 = 1$

An example: a orbit $l$ couple with a spin $\frac12$, 
$$
\langle m+\frac12,\frac12\mid l+\frac12,m+1\rangle=\sqrt{\frac{l+m+3/2}{l+m+1/2}}\langle m-\frac12,\frac12\mid l+\frac12,m\rangle\\
\langle m-\frac12,\frac12\mid l+\frac12,m\rangle=\sqrt{\frac{l+m+1/2}{2l+1}}
$$

CG matrix changing basis from $\mid j_1,j_2,m_l,m_s\rangle$ to $\mid j_1,j_2,jm\rangle$

is in the form: $\left(\begin{array}{cc}\cos \alpha & \sin \alpha \\ -\sin \alpha & \cos \alpha\end{array}\right)$

$cos\alpha = \sqrt{\frac{l+m+1/2}{2l+1}}$

#### Wigner 3-j notation

$\left\langle j_{1} j_{2} ; m_{1} m_{2} \mid j_{1} j_{2} ; j m\right\rangle=(-1)^{j_{1}-j_{2}+m} \sqrt{2 j+1}\left(\begin{array}{ccc}j_{1} & j_{2} & j \\ m_{1} & m_{2} & -m\end{array}\right)$

#### Schwinger's Notation

$$
J_+=\hbar a^{\dagger}_+a_-;\ J_-=\hbar a^{\dagger}_-a_+\\
N_+=a_+^{\dagger}a_+;\ N_-=a_-^{\dagger}a_-\\
N=N_++N_-\\
J^2=\frac{\hbar^2}{2}N(\frac N2+1)\\
\mid j,m\rangle = \frac{(a_+^{\dagger})^{j+m}(a_-^{\dagger})^{j-m}}{\sqrt{(j+m)!(j-m)!}}\mid0\rangle
$$


### Tensor Operator

In classical physics, rotation (in 3D) has the following representation:
$$
V_m\rightarrow\displaystyle{\sum_{m=1,2,3}}R_{mn}V_n
$$
In quantum mechanics, rotation  (in 3D) should be able to be represented by:
$$
V_m\rightarrow\mathscr{D}^\dagger(R)V_m\mathscr{D}(R)
$$
If we want it has the same form as $(1)$, namely:
$$
\displaystyle{\sum_{m=1,2,3}}R_{mn}V_n=\mathscr{D}^\dagger(R)V_m\mathscr{D}(R)
$$
When making this analogy in quantum mechanics, we should take the expectation as the classical world can be considered as the statistical average of the quantum world.
$$
\mid\alpha\rangle\rightarrow\mathscr{D}(R)\mid\alpha\rangle\\
\langle\alpha\mid V_m\mid\alpha\rangle\rightarrow\langle\alpha\mid\mathscr{D}^\dagger(R)V_m\mathscr{D}(R)\mid\alpha\rangle=\displaystyle{\sum_{n=1,2,3}}R_{mn}\langle \alpha\mid V_n\mid\alpha\rangle
$$
For infinitesimal rotation, 
$$
\mathscr{D}(R)=\mathscr{1}-\frac{i\epsilon\bold{J}\cdot\hat{n}}{\hbar}\\
V_m+\frac{\epsilon}{i\hbar}[V_m,\bold{J}\cdot\hat{n}]=\displaystyle{\sum_n}R_{mn}V_n\\
R(\hat{z},\epsilon)=\begin{pmatrix}
1&-\epsilon&0\\
\epsilon&1&0\\
0&0&1
\end{pmatrix}
$$
We can conclude the Lie algebra for 3D rotation in quantum mechanics:
$$
[V_i,V_j]=i\hbar\epsilon_{ijk}V_k
$$

### Cartesian Tensors  vs Irreducible Tensors

The classical tensor is defined by generalizing $V_i\rightarrow\sum_j R_{ij}V_j$
$$
T_{ijk...}\rightarrow\sum_{ii'}\sum_{jj'}\sum_{kk'}\cdot\cdot\cdot R_{ii'}R_{jj'}\cdot\cdot\cdot T_{i'j'k'}\\
$$
The $T_{ijk...}$ is the $\bold{Cartesian\ Tensor}$ with the rank equal to the number of the indexes. 

The simplest rank-2 Cartesian Tensor is the dyadic formed out of vectors $\bold{U}$ and $\bold{V}$, take their Cartesian components, we will have the tensor:
$$
T_{ij}=U_i V_j
$$
This is reducible, the decomposed objects transform differently under rotations, for example:
$$
U_{i}V_{j}=\frac{\bold{U\cdot V}}{3}\delta_{ij}+\frac{U_i V_j-U_j V_i}{2}+(\frac{U_iV_j+U_j V_i}{2}-\frac{\bold{U\cdot V}}{3}\delta_{ij})\\
=\frac{\bold{U\cdot V}}{3}\delta_{ij}+\frac{\epsilon_{ijk}(\bold{U\cdot V})_k}{2}+(\frac{U_iV_j+U_j V_i}{2}-\frac{\bold{U\cdot V}}{3}\delta_{ij})
$$
The first term is scalar, thus invariant under rotation, the second term is a sum of 3 components (i,j,k), the third term is traceless with $3\times 3-3-1=5$ independent components.

The three terms have the number of independent components exactly as the values of the spin magnetic quantum number for angular momentum $l=0,\ 1,\ 2$, and $(9)$ is the simplest nontrivial $\bold{irreducible\ spherical\ tensor}$ representation of the rank-2 Cartesian Tensor.

### Spherical  Tensor

Since if the angular momentum is set $l$, the magnetic quantum number can be taken {$-l,-l+1...,l-1,l$}, $2l+1$ values in total, the angular momentum can be considered as the rank of the spherical tensor, and the number of values of the magnetic quantum number can be considered as the number of independent components of the tensor. 

A simple example of the spherical tensor is taking it as the spherical harmonic function $T_k^q=Y_{l=k}^{m=q}(\bold{V})$. k is the rank, q is the magnetic quantum number, to differ from m, vector V is to replace the direction vector $\hat{\bold{n}}$, which is determined by the angle $\theta$ and $\phi$.  

#### Transformation of spherical harmonic function under rotation

$$
Y_l^m(\bold{\hat{n}'})=\langle \bold{\hat{n}'}\mid l,m\rangle\\
\mathscr{D}(R^{-1})\mid l,m\rangle=\sum_{m'}\mid l,m'\rangle\langle l,m'\mid\mathscr{D}(R^{-1})\mid l,m\rangle=\sum_{m'}\mid l,m'\rangle \mathscr{D}_{mm'}^{(l)}(R^{-1})\\
\langle \bold{\hat{n}}\mid\mathscr{D}(R^{-1})\mid l,m\rangle=\langle \bold{\hat{n}}\mid\mathscr{D}(R^{T})\mid l,m\rangle=\langle \bold{\hat{n}}\mid\mathscr{D}^{\dagger}(R)\mid l,m\rangle=\langle \bold{\hat{n}'}\mid l,m\rangle=Y_l^m(\bold{\hat{n}'})\\
 -------------------------------------- \\
Therefore,\\
  --------------------------------------\\
Y_l^m(\bold{\hat{n}'})=\sum_{m'} \langle\bold{\hat{n}}\mid l,m'\rangle \mathscr{D}_{mm'}^{(l)}(R^{-1})=\sum_{m'} Y_{l}^{m'} \mathscr{D}_{mm'}^{(l)}(\bold{\hat{n}})(R^{-1})\\
$$

Now rewrite the spherical harmonic function and see how the spherical tensor comes out.
$$
\mathscr{D}^{\dagger}(R)Y_l^m(\bold{V})\mathscr{D}(R)=\sum_{m'} Y_{l}^{m'} \mathscr{D}_{mm'}^{(l)*}(\bold{\hat{n}})(R^{-1})\\
-------------------------------\\
Replace\ the\ spherical\ harmonic\ function\ by\ the\ tensor\ operator\\
-------------------------------\\
\mathscr{D}^{\dagger}(R)T_q^k\mathscr{D}(R)=\displaystyle{\sum_{q'=-k}^{k}}\mathscr{D}_{qq'}^{(k)*}(R)T_{q'}^{(k)}\\
$$
This is the definition of $Spherical\ Tensor$, and this definition holds for all tensors, not only spherical-harmonic-function-like ones.

Ex: (For a infinitesimal rotation)
$$
(1+\frac{i\epsilon\bold{J\cdot\hat{n}}}{\hbar})T_q^{(k)}(1-\frac{i\epsilon\bold{J\cdot\hat{n}}}{\hbar})=\displaystyle{\sum_{q'=-k}^{k}}T_{q'}^{(k)}\langle kq'\mid(1+\frac{i\epsilon\bold{J\cdot\hat{n}}}{\hbar})\mid kq\rangle\\
 [\bold{J\cdot\hat{n}},T_q^{(k)}]=\sum_{q'}T_{q'}^{(k)}\langle kq'\mid\bold{J\cdot\hat{n}}\mid kq\rangle\\
 [J_z,T_q^{(k)}]=\hbar q\ T_q^{(k)}\\
 [J_{\pm},T_q^{(k)}]=\hbar \sqrt{(k\mp q)(k\pm q+1)}\ T_{q\pm 1}^{(k)}
$$

### Products of  Tensors

#### The language of spherical tensor

$$
T_0^{(0)}=\frac{-\bold{U\cdot V}}{3}=\frac{U_{+1}V_{-1}+U_{-1}V_{+1}-U_0V_0}{3}\\
T_q^{(1)}=\frac{(\bold{U\times V})_q}{i\sqrt2}\\
T_{\pm2}^{(2)}=U_{\pm1}V_{\pm1}\\
T_{\pm1}^{(2)}=\frac{U_{\pm1}V_0+U_0V_{\pm1}}{\sqrt2}\\
T_{0}^{(2)}=\frac{U_{+1}V_{-1}+2U_0V_0+U_{-1}V_{+1}}{\sqrt6}\\
$$

A special case:
$$
if\ \ \bold{U}=\bold{V}=\bold{r}\\
T_0^{(2)}=Y_2^0=\sqrt{\frac{5}{16\pi}}\frac{3z^2-r^2}{r^2}
$$
An example, under rotation, transform T to spherical tensor, its irreducible representation:
$$
T_q^{(k)}=\sum_{q1}\sum_{q2} \langle{k1k2;q1q2}\mid{k1k2;kq}\rangle X_{q1}^{(k_1)}Z_{q2}^{(k2)}\\
$$
The coefficient in front of the decomposition of a tensor operator into irreducible 
$$
\sum_{q1}\sum_{q2}\sum_{q1'}\sum_{q2'}\langle k1k2;q1q2\mid k1k2;kq\rangle\times X_{q1'}^{(k1)}\mathscr{D}_{q1'q1}^{(k1)}(R^{-1})Z_{q2'}^{(k2)}\mathscr{D}_{q2'q2}^{(k2)}(R^{-1})\\
=\sum_{k''}\sum_{q1}\sum_{q2}\sum_{q1'}\sum_{q2'}\sum_{q''}\sum_{q'} \langle k1k2;q1q2\mid k1k2;kq\rangle \langle k1k2;q1'q2'\mid k1k2;k''q'\rangle \langle k1k2;q1q2\mid k1k2;k''q''\rangle \\
\times \mathscr{D}_{q'q''}^{(k'')}(R^{-1})\ X_{q1'}^{(k1)}\ Z_{q2'}^{(k2)}\\
=\sum_{k''}\sum_{q1'}\sum_{q2'}\sum_{q''}\sum_{q'}\delta_{kk''}\delta_{qq''} \langle k1k2;q1'q2'\mid k1k2;k''q'\rangle \mathscr{D}_{q'q''}^{(k'')}(R^{-1})\ X_{q1'}^{(k1)}\ Z_{q2'}^{(k2)}\\
=\sum_{q'} \left(\sum_{q1'}\sum_{q2'} \langle k1k2;q1'q2'\mid k1k2;k''q'\rangle X_{q1'}^{(k1)}\ Z_{q2'}^{(k2)}\right) \mathscr{D}_{q'q''}^{(k'')}(R^{-1})\\
=\sum_{q'}T_{q'}^{(k)}\mathscr{D}_{qq'}^{(k)*}(R^{-1})\\
---------------------------\\
Where\ we\ use\ the\ following\ formula\\
---------------------------\\
\mathscr{D}_{q1'q1}^{(k1)}(R^{-1})\mathscr{D}_{q2'q2}^{(k2)}(R^{-1})=\sum_{k''}\sum_{q''}\sum_{q'}\langle k1k2;q1q2\mid k1k2;k''q''\rangle \langle k1k2;q1'q2'\mid k1k2;k''q'\rangle\\ \times \mathscr{D}_{q'q''}^{(k'')}(R^{-1})\ X_{q1'}^{(k1)}\ Z_{q2'}^{(k2)}
$$

### the Wigner-Eckart Theorem

$$
\langle\alpha',j'm'\mid T_q^{(k)}\mid \alpha,jm\rangle=\langle jk,mq\mid jk,j'm'\rangle \frac{\langle \alpha'j'\mid\mid T^{(k)}\mid\mid \alpha j\rangle}{\sqrt{2j+1}}
$$

First we prove the selection rules of magnetic quantum number:
$$
Use\ [J_z,T_q^{(k)}]=\hbar q\ T_q^{(k)}\\
\langle \alpha',j'm'\mid [J_z,T_q^{(k)}]-\hbar q\ T_q^{(k)}\mid \alpha,jm\rangle=0\\
expand\ the\ commutator\ and\ we\ have:
q=m'-m
$$
Then we proceed the prove of W-E theorem:
$$
\mathscr{D}(R)\ T_q^{(k)}\mid \alpha,jm\rangle=\mathscr{D}(R)\ T_q^{(k)}\mathscr{D}^{\dagger}(R)\mathscr{D}(R)\mid\alpha,jm\rangle\\
\mid kj,qm\rangle=\sum_{q'm'}\mathscr{D}_{q'q}^{(k)}(R)\mathscr{D}_{m'm}^{(j)}(R)T_{q'}^{(k)}\mid \alpha,j'm'\rangle\rightarrow\mid kq'\rangle\otimes\mid jm'\rangle\\
D^{(k)}\otimes D^{(j)}=\oplus_{\mid k-j\mid \leq j'\leq k+j}D^{(j')}\times CGseries\\
reducible\ representation\rightarrow irreducible\ representation
$$
Compare:
$$
\langle\alpha',j'm'\mid[J_{\pm},T_q^{(k)}]\mid\alpha,jm\rangle=\hbar\sqrt{(k\mp q)(k\pm q+1)}\langle\alpha',j'm'\mid T_{q\pm1}^{(k)}\mid\alpha,jm\rangle\\
namely,                        \\
\sqrt{(j'\pm m')(j'\mp m'+1)}\langle\alpha',j'm'\mp1\mid T_q^{(k)}\mid\alpha,jm\rangle-\sqrt{(j\mp m)(j\pm m+1)}\langle\alpha',j'm'\mid T_q^{(k)}\mid\alpha,jm\pm1\rangle\\
=\sqrt{(k\mp q)(k\pm q+1)}\langle\alpha',j'm'\mid T_{q\pm1}^{(k)}\mid\alpha,jm\rangle\\
$$
With the recurrence relation of the CG coefficient:
$$
\sqrt{(j\mp m)(j\pm m+1)}\langle j1,j2;m1,m2\mid j1,j2,j,m\pm1\rangle\\
=\sqrt{(j1\mp m1)(j1\pm m1+1)}\langle j1,j2;m1\mp1,m2\mid j1,j2,j,m\rangle\\
=\sqrt{(j1\mp m1)(j1\pm m1+1)}\langle j1,j2;m1,m2\mp1\mid j1,j2,j,m\rangle
$$
We know:
$$
\langle\alpha',j'm'\mid T_{q\pm1}^{(k)}\mid\alpha,jm\rangle=C(\alpha,j,\alpha',j')\langle jk,mq\pm1\mid jk,j'm'\rangle\\
C(\alpha,j,\alpha',j')=\frac{\langle \alpha'j'\mid\mid T^{(k)}\mid\mid \alpha j\rangle}{\sqrt{2j+1}}
$$
For rank-0 (scalar) tensor S
$$
\langle\alpha',j'm'\mid S\mid\alpha,jm\rangle=\delta_{jj'}\delta_{mm'}C
$$
For rank-1 (vector operator in spherical tensor language) $V_{q=\pm1,0}^{(k=1)}$, the selection rules:
$$
\Delta m=m'-m=\pm1,0\\
\Delta j=j'-j=\pm1,0
$$

### the Projection Theorem

$$
\langle \alpha',jm'\mid V_q\mid\alpha,jm\rangle=\frac{\langle\alpha',jm\mid\bold{J\cdot V}\mid\alpha,jm\rangle}{\hbar^2j(j+1)}\langle jm'\mid J_q\mid jm\rangle
$$

The proof:
$$
\langle\alpha',jm\mid\bold{J\cdot V}\mid\alpha,jm\rangle=\langle\alpha',jm\mid J_0V_0-J_+V_--J_-V_+\mid\alpha,jm\rangle=m\hbar\langle\alpha',jm\mid V_0\mid\alpha,jm\rangle\\
\mp\frac{\hbar}{\sqrt2}\sqrt{(j\pm m)(j\mp m+1)}\langle\alpha',jm\mp1\mid V_{\mp1}\mid\alpha,jm\rangle\\
\langle\alpha',jm\mp1\mid V_{\mp1}\mid\alpha,jm\rangle=\langle j,1;m\mp1,1\mid j,1;j,m\mp1\rangle C\\
\langle\alpha',jm\mid\bold{J\cdot V}\mid\alpha,jm\rangle=c_{jm}\langle\alpha',j\mid\mid V\mid\mid\alpha,j\rangle\\
Now\ take\ \bold{V}\ as\ \bold{J},\\
\langle\alpha,jm\mid\bold{J^2}\mid\alpha,jm\rangle=c_{jm}\langle\alpha,j\mid\mid \bold{J}\mid\mid\alpha,j\rangle\\
Use\ twice\ W-E\ theorem,\ one\ on\ V_q,\ the\ other\ one\ on\ J_q\\
\frac{\langle\alpha',jm'\mid V_q\mid\alpha,jm\rangle}{\langle\alpha,jm'\mid J_q\mid\alpha,jm\rangle}=\frac{\langle\alpha'j\mid\mid\bold{V}\mid\mid\alpha j\rangle}{\langle\alpha j\mid\mid\bold{J}\mid\mid\alpha j\rangle}=\frac{\langle\alpha',jm\mid\bold{J\cdot V}\mid\alpha,jm\rangle/c_{jm}}{\langle\alpha,jm\mid\bold{J^2}\mid\alpha,jm\rangle/c_{jm}}=\frac{\langle\alpha',jm\mid\bold{J\cdot V}\mid\alpha,jm\rangle}{\hbar^2j(j+1)}
$$

## Chapter4 Symmetries in Quantum Mechanics

### Symmetries in classical physics

#### SO(4) Symmetry in Coulomb Potential

The $\bold{Lenz\ vector}$:
$$
\bold{M}=\frac{\bold{p\times L-L\times p}}{2m}-\frac{Ze^2}{r}\bold{r}\\
the\ Hamiltonian:\ H=\frac{\bold{p^2}}{2m}-\frac{Ze^2}{r}
$$
They satisfy:
$$
[\bold{M},H]=0\\
\bold{L\cdot M}=0\\
\bold{M^2}=\frac{2}{m}H(\bold{L^2}+\hbar^2)+Z^2e^4\\
\frac{d\bold{M}}{dt}=\left\{\bold{M},H \right\}_{Poisson}=0\\
\frac{d\bold{M}}{dt}=[\bold{M},H]=0\\
 [M_i,L_j]=i\hbar\epsilon_{ijk}M_k\\
 [M_i,M_j]=-i\hbar\epsilon_{ijk}\frac{2}{m}HL_{k}
$$
To make the M commutators share the same Lie algbra with the angular momentum, we replace M by operator N (E<0 bound state) :
$$
\bold{N}=\sqrt{-\frac{m}{2E}}\bold{M}\\
 [N_i,N_j]=i\hbar\epsilon_{ijk} L_k=[L_i,L_j]\\
 [N_i,L_j]=i\hbar\epsilon_{ijk} N_k
$$
The above commutative relationship generates the symmetry of rotation in four spatial dimensions, namely SO(4).

### Symmetries in quantum Mechanics

G denotes the transformation, if G conserves, G commutes with the Hamiltonian. If the system Hamiltonian is invariant under translation, then G is the momentum, if invariant under rotation, G is the anuglar momentum. 

#### Degeneracy

If the Hamiltonian is invariant under rotation, namely $[\mathscr{D}(R),H]=0$, we know the rotation is corresponding to the total angular momentum J, so $[\bold{J},H]=0$, the eigenkets of J, $J^2$, $J_z$, D(R): $\mid n;jm\rangle$ can generate degeneracy by the combination of 2j+1 independent states: 
$$
\mathscr{D}(R)\mid n,jm\rangle=\sum_{m'}\mid n,jm'\rangle\mathscr{D}_{m'm}^{(j)}(R)
$$

#### Rotation in four spatial space

The rotations in n-dimension space can be characterized by mixed operations around two axises, this is the generator, so they have $C_n^2$ generators. Here are 6 generators, 3 L-components, 3 N-components, we can infer it is a rotation in 4-dimnesion. 

To formally do this, we imagine a dimnesion $x_4, p_4$, 
$$
\tilde{L}_{14}\equiv x_1p_4-x_4p_1\equiv N_1\\
\tilde{L}_{24}\equiv x_2p_4-x_4p_2\equiv N_2\\
\tilde{L}_{34}\equiv x_3p_4-x_4p_3\equiv N_3\\
 [L_i,N_j]=i\hbar\epsilon_{ijk}N_k
$$

#### Energy levels and degeneracy

We now use the commutative relation to derive the form of eigen-energy.
$$
\bold{I}\equiv \frac{\bold{L+N}}{2}\\
\bold{K}\equiv \frac{\bold{L-N}}{2}\\
 [I_i,I_j]=i\hbar\epsilon_{ijk}I_k\\
 [K_i,K_j]=i\hbar\epsilon_{ijk}K_k\\
 [I_i,K_j]=0\\
 [\bold{I},H]=0=[\bold{K},H]
$$
We have the equation:
$$
\langle\bold{I^2+K^2}\rangle=\frac12\langle\bold{L^2+N^2}\rangle=\frac12\langle\bold{L^2}-\frac{m}{2E}\bold{M^2}\rangle\\
\hbar^2 \left\{i(i+1)+k(k+1)\right\}=\frac12\hbar^2\left\{l(l+1)-\frac{m}{2E}\frac{2}{m}E\ l(l+1)-1       \right\}-\frac{m}{2E}Z^2e^4\\
with\ \  \bold{I^2-K^2=L\cdot N}=0,\ i=k\\
2k(k+1)\hbar^2=\frac12(-\hbar^2-\frac{m}{2E}Z^2e^4)\\
E=-\frac{mZ^2e^4}{2\hbar^2(2k+1)^2}
$$


### Parity (Space Inversion), Discrete Symmetries

Define parity operator in the expectation of space position operator 
$$
\langle \alpha\mid \pi^{\dagger}\bold{x}\pi\mid\alpha\rangle=-\langle\alpha\mid\bold{x}\mid\alpha\rangle\\
\pi^{\dagger}\bold{x}\pi=-\bold{x}\\
\pi\mid \bold{x'}\rangle=e^{i\delta}\mid-\bold{x'\rangle}\\
\pi^{-1}=\pi^{\dagger}=\pi\ \ (Hermitian\ and\ Unitary)
$$
Some more properties of parity transformation
$$
R^{(parity)}=\begin{pmatrix}
-1&0&0\\
0&-1&0\\
0&0&-1
\end{pmatrix}\\
 [R^{(parity)},R^{rotation}]=0\\
  [\pi,\mathscr{D}(R)]=0\\
  [\pi,\bold{J}]=0
$$

#### Polar vectors and Axial vectors (or Pseudovectors)

Odd under parity transformation: Polar; $\bold{x,p}$

Even under parity transformation: Axial;$\bold{L,S}$

Scalar, but odd under parity transformation: psudoscalar. $\bold{S\cdot x,\ L\cdot S}$

#### Wavefunctions under Parity

In position space:
$$
\psi(\bold{-x})=\langle\bold{-x}\mid\alpha\rangle=\langle\bold{x}\mid\pi\mid\alpha\rangle\\
\pi\mid\alpha\rangle=\pm\mid\alpha\rangle\\
thus\ \psi(-\bold{x})=\pm\psi(\bold{x}) (+\ for\ even,\ -\ for\ odd)
$$
In spherical position
$$
\langle\bold{x}\mid\alpha,lm\rangle=R_{\alpha}(r)Y_l^m(\theta,\phi)\\
r\rightarrow r\\
\theta\rightarrow\pi-\theta\\
\phi\rightarrow\phi+\pi\\
Y_m^l\rightarrow(-1)^lY_m^l\\
\pi\mid\alpha,lm\rangle=(-1)^l\mid\alpha,lm\rangle
$$

#### Theorem 4.1

$$
if\ [H,\pi]=0, H\mid n\rangle=E_n\mid n\rangle,\ and\ \mid n\rangle\ is\ nondegenerate\\
then\ \pi\mid n\rangle=\pm\mid n\rangle\\
proof:\\
\pi\left\{\frac12(1\pm\pi)\mid n\rangle \right\}=\frac12(\pi\pm1)\mid n\rangle,\\
namely\ \frac12(1\pm\pi)\mid n\rangle\ is\ a\ parity\ eigenket\\
H\frac12(1\pm\pi)\mid n\rangle=\frac12E_n(1\pm \pi)\mid n\rangle\\
it's\ also\ an\ energy\ eigenket,\ and\ because\ \mid n\rangle\ is\ nondegenrate,\\ \frac12(1\pm\pi)\mid\ n\rangle\ must\ represent\ the\ same\ state\ as\ \mid n\rangle
$$

#### Symmetrical Double-Well Potential

Symmetrical state $\mid S\rangle$, antisymmetrical state $\mid A\rangle$
$$
E_A>E_S\\
\mid R\rangle=\frac1{\sqrt2}(\mid S\rangle+\mid A\rangle)\\
\mid L\rangle=\frac1{\sqrt2}(\mid S\rangle-\mid A\rangle)\\
\mid R,t_0;t\rangle=\frac1{\sqrt2}(e^{-iE_At/\hbar}\mid S\rangle+e^{-iE_St/\hbar}\mid A\rangle)\\
\omega=\frac{(E_A-E_S)}{\hbar}\\
the\ states\ oscillate\ between\ \mid R\rangle\ and\ \mid L\rangle\ in\ anuglar\ frequency\ \omega
$$

#### Parity selection rule

$\bold{Laporte's\ Rule}$: consequence of parity-selection rule
$$
\langle \alpha\mid \bold{x}\mid\beta\rangle=0\\
unless:\ \ \epsilon_{\alpha}=-\epsilon_{\beta}\\
where:\ \pi\mid\alpha\rangle=\epsilon_{\alpha}\mid\alpha\rangle;\ \pi\mid\beta\rangle=\epsilon_{\beta}\mid\beta\rangle\\
the Laporte's rule:\ \int\psi_{\beta}^*\bold{x}\psi_{\alpha}d\tau=0
$$

### Lattice Translation as a Discrete Symmetry

$$
T(l)^{\dagger}\bold{x}T(l)=\bold{x+l}\\
T(l)\mid\bold{x}\rangle=\mid\bold{x+l}\rangle\\
T^{\dagger}(a)V(x)T(a)=V(x+a)=V(x)\\
T^{\dagger}(a)pT(a)=p\\
therefore\ [T^{\dagger}(a),H]=0
$$

$$
H\mid n\rangle=E_n \mid n\rangle\\
T(a)\mid n\rangle=\mid n+1\rangle\\
\mid\theta\rangle\equiv\sum_{n=-\infin}^{\infin}e^{in\theta}\mid n\rangle\\
T(a)\mid\theta\rangle=\sum_{n=-\infin}^{\infin}e^{in\theta}\mid n+1\rangle=\sum_{n=-\infin}^{\infin}e^{i(n-1)\theta}\mid n\rangle=e^{-i\theta}\mid\theta\rangle
$$

#### Tight Binding Model

$$
\langle n\pm1\mid H\mid n\rangle=-\Delta\\
\langle n\mid H\mid n\rangle=E_0\ (translation\ invariance)
$$

#### Bloch's Theorem

$$
\langle x\mid T(a)\mid\theta\rangle=\langle x-a\mid\theta\rangle=\langle x\mid\theta\rangle e^{-i\theta}\\
The\ general\ solution\ is\ the\ Bloch\ wavefunction:\ \langle x\mid\theta\rangle=u_k(x)e^{-ika}
$$

#### First Brillouin Zone

$$
E(k)=E_0-2\Delta coska\\
energy\ changes\ from\ E_0-2\Delta\ to\ E_0+2\Delta,\ k\ changes\ from\ -\pi/a\ to\ \pi/a.
$$

### The Time-Reversal Discrete Symmetry

#### Antiunitary Operator

$$
\mid\tilde{\alpha}\rangle=\theta\mid\alpha\rangle\\
\mid\tilde{\beta}\rangle=\theta\mid\beta\rangle\\
\langle\tilde{\alpha}\mid\tilde{\beta}\rangle=\langle\alpha\mid\beta\rangle^*\\
\theta(c_1\mid\alpha\rangle+c_2\mid\beta\rangle)=c_1^*\theta\mid\alpha\rangle+c_2^*\theta\mid\beta\rangle
$$

If an operator is antiunitary, it has to be antilinear at first. The last equation in $(46)$ define an antilinear operator. 

$\theta$ is the time reversal operator, now check $(46)$ 
$$
\mid\tilde{\bold{\alpha}}\rangle= UK\mid\alpha\rangle=\sum_{a}\mid a\rangle\langle a\mid UK\mid\alpha\rangle=\sum_{a}\mid a\rangle\langle\alpha\mid UK\mid a\rangle^*=\sum_{a}\langle\alpha\mid a\rangle\ U\mid a\rangle\\
\mid\tilde{\bold{\beta}}\rangle= UK\mid \beta\rangle=\sum_{a'}\langle\beta\mid a'\rangle U\mid a'\rangle\\
$$

#### Time-Reversal Operator

$$
-iH\Theta\mid\rangle=\Theta iH\mid\rangle\\
if\ \Theta\ is\ unitary,\ the\ eigenenergy\ will\ be\ negative,\ which\ is\ unacceptable\\
so,\ \Theta\ is\ antiunitary,\\
H\Theta=\Theta H\\
we\ must\ avoid\ to\ make\ \Theta\ operate\ on\ bra
$$

Prove the identity of time reversal
$$
\langle\beta\mid\otimes\mid\alpha\rangle=\langle\gamma\mid\alpha\rangle=\langle\alpha\mid\gamma\rangle^*=\langle\tilde{\alpha}\mid\tilde{\gamma}\rangle=\langle\tilde{\alpha}\mid\Theta\ \otimes^{\dagger}\mid\beta\rangle=\langle\tilde{\alpha}\mid\Theta\ \otimes^{\dagger}\Theta^{-1}\Theta\mid\beta\rangle=\langle\tilde{\alpha}\mid\Theta\ \otimes^{\dagger}\Theta^{-1}\mid\tilde{\beta}\rangle\\
where\ \otimes\ is\ a\ linear\ operator,\ and\ \mid\gamma\rangle\equiv\otimes^{\dagger}\mid\beta\rangle
$$
We now have the expectation:
$$
\langle\alpha\mid A\mid\alpha\rangle=\langle\tilde{\alpha}\mid\Theta A^{\dagger}\Theta^{-1}\mid\tilde{\alpha}\rangle\\
examples:\\
\Theta\bold{p}\Theta^{-1}=-\bold{p}\\
\Theta\bold{x}\Theta^{-1}=\bold{x}\\
\Theta\mid\bold{p}\rangle=\mid-\bold{p}\rangle\\
\Theta\mid\bold{x}\rangle=\mid\bold{x}\rangle\\
\Theta\bold{J}\Theta^{-1}=-\bold{J}
$$

#### Wave function under time-reversal

$$
For a abstrct particle state \mid\alpha\rangle\\
\Theta\mid\alpha\rangle=\int d^3x\ (\Theta\mid x\rangle)\ \langle x\mid\alpha\rangle^*=\int d^3x\ \mid x\rangle\langle x\mid\alpha\rangle^*\\
\psi(\bold{x})\rightarrow\psi(\bold{x})^*\\
Y_l^m(\theta,\phi)\rightarrow Y_l^m(\theta,\phi)^*=(-1)^mY_l^{-m}(\theta,\phi)\\
\Theta\mid j,m\rangle=(-1)^m\mid j,-m\rangle
$$



#### Theorem 4.1 Real eigenfunction for time-reversal invariant Hamiltonian

$$
H\Theta\mid n\rangle=\Theta H\mid n\rangle=E_n\Theta\mid n\rangle\\
\langle\bold{x}\mid n\rangle=\langle\bold{x}\mid \Theta^{-1}\Theta\mid n\rangle=\langle\bold{x}\mid n\rangle^*\\
$$

For wavefunction in momentum representation:
$$
\Theta\mid\alpha\rangle=\int d^3p\mid -p\rangle\langle p\mid\alpha\rangle^*=\int d^3p\mid p\rangle\langle -p\mid\alpha\rangle^*\\
\phi(\bold{p})\rightarrow\phi^{*}(-\bold{p})
$$

### Time-Reversal for Spin-1/2 System

$$
\mid \hat{\bold{n}},+\rangle=e^{-iS_z\alpha/\hbar}e^{-iS_y\beta/\hbar}\mid+\rangle\\
\Theta\ operates\ on\ S\ will\ generate\ a\ -1,\ and\ i\ will\ change\ to\ -i,\ so\ it\ does\ nothing\ in\ total\\
\Theta\mid\hat{\bold{n}},+\rangle=\eta\mid\hat{\bold{n}},-\rangle\\
\mid\hat{\bold{n}},-\rangle=e^{-iS_z\alpha/\hbar}e^{-iS_y(\beta+\pi)\hbar}\mid+\rangle\\
thus\ \Theta=\eta e^{-i\pi S_y/\hbar} K=-i\eta\left( \frac{2S_y}{\hbar}\right)K \ (multiply\ K\ to\ make\ it\ antiunitary)\\
e^{-iS_z\pi/\hbar}\mid+\rangle=+\mid-\rangle;\\ e^{-iS_y\pi/\hbar}\mid-\rangle=-\mid+\rangle\\
\Theta(c_+\mid+\rangle+c_-\mid-\rangle)=\eta c_+^*\mid-\rangle-\eta c_-^*\mid+\rangle\\
$$


$$
\Theta^2\mid j\ is\ half-odd\rangle=-\mid j\ is\ half-odd\rangle\\
\Theta^2\mid j\ is\ integer\rangle=\mid j\ is\ integer\rangle\\
or\ we\ can\ write:\\
e^{-2i\pi J_y/\hbar}\mid j,m\rangle=(-1)^{2j}\mid j,m\rangle\\
\Theta\mid j,m\rangle=i^{2m}\mid j,-m\rangle
$$

### Interactions with EM fields; Kramers Degeneracy

$$
For\ odd-angular-momentum-quantum-number\ system,\\ every\ energy\ level\ has\ at\ least\ two-fold\ degeneracy\ in\ an\ external\ E\ field. \\
B\ field\ is\ treated\ extrenal,\ so\ B\ field\ doesn't\ change\ in\ the\ closed\ quantum\ mechanics\ we\ discuss.
$$




$$

$$

$$

$$




