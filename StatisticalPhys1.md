高统期末复习

### 第一章

$$
dQ = dE + dW = dE + PdV = \left(\frac{\partial E}{\partial V} \right)_T dV + \left(\frac{\partial E}{\partial T} \right)_V dT +PdV \\
dS = \frac{dQ}{T} = \frac1T[\left(\frac{\partial E}{\partial V} \right)_T + P ]dV + \frac1T \left(\frac{\partial E}{\partial T} \right)_V dT\\
\frac{\partial^2 S}{\partial T \partial V} = \frac{\partial^2 S}{\partial V \partial T}\\
\left(\frac{\partial E}{\partial V} \right)_T = T\left(\frac{\partial P}{\partial T} \right)_V -P\\
$$

一个容易忽略的操作：

For ideal gas
$$
E = \frac32 NRT\\
dE = \frac32 NRdT\\
PV = NRT\\
PdV + VdP = NRdT
$$
卡诺热机：四个过程  等温-绝热-等温-绝热

等温：no internal energy change, $d E=0$, $\delta Q = -\delta W$. $\Delta Q = \int PdV$

绝热：$\Delta Q = 0$, $\Delta E = -\int PdV$

用绝热方程：$PV^{\gamma}=const$

最后得到：$\eta = 1 - \frac{T_L}{T_H}$

Free energy: $F = E - TS$

If internal energy only depends on the temperature: 
$$
\left(\frac{\partial E}{\partial V} \right)_T = T\left(\frac{\partial P}{\partial T} \right)_V - P=0\\
P = Tf(V)
$$
In a reversible process, the total entropy doesn't change, and if the system is isolated, $\Delta Q = \sum_i C_{Vi}\Delta T_i$

### 第二章

对不同系综而言，描述它们的物理量无非包括：$\delta Q,\ \delta W,\ \delta N,\ \rho,\ S,\ F$

$\rho$是粒子的统计算符（在态表象下的矩阵形式即为密度矩阵），在微正则系综中是态数目的倒数，在其它系综中都需要借助配分函数描述

#### 微正则系综：

N个孤立系统组成，它们与外界没有物质和能量交换，能量在E到$E+\Delta E$之间变化。

计算粒子态在此能量区间的分布概率：$\Omega(E) = \frac{\partial  \left(\frac{1}{h^{3N}N!}\int_{H\leq E}dp_1 dp_2...dp_{3N}\right)}{\partial E}\Delta E $

上式的偏微分的函数内的积分是动量空间的一个态球的体积，除以一个$N!$是除以重复的排序，N个粒子对应N个态之间交换顺序不改变态总数。V是单个粒子在实空间（坐标空间）占据的体积，是在相空间全空间积分的坐标积分部分，得到实空间体积，而后面是单个粒子在态空间单位体积的态密度，单位空间就是一个动量代表的态占据了h的态空间，每个动量对应一个态，所以用占据的动量空间除以态空间就是态密度，$\pi^{3N/2}/\Gamma(3N/2 + 1)$是球体积积分得到的系数。
$$
\Omega(E) = \frac{\partial \frac{V^N \pi^{3N/2} p^{3N}}{h^{3N} N! \Gamma(3N/2 + 1)}}{\partial E} \Delta E = \frac{3N \Delta E}{2E}\frac{V^N \pi^{3N/2}p^{3N}}{h^{3N}N! \Gamma(3N/2 + 1)}\\
= \frac{3N\Delta E V^N \pi^{3N/2} (2mE)^{3N/2} }{2Eh^{3N}N! \Gamma(3N/2 + 1) }
$$
熵：
$$
S = k_B ln\Omega(E) \approx k_Bln(\frac{3N\Delta E}{2E}) + Nk_Bln\left[\frac{V}{h^3 N}\left(\frac{4\pi mE}{3N} \right)^{\frac32} \right] + \frac52 Nk_B
$$

这里用到的近似：斯特林近似，N为整数，$\Gamma$函数约为$(3N/2)!$（实际上$\Gamma(z) = \int_0^{\infin}x^{\mathcal{z}-1}e^x dx$，只有整数积分结果才是阶乘），故可用：$ln(N!(3N/2)!)\approx NlnN-N + \frac{3N}2ln(\frac{3N}2) - \frac{3N}2 $

对微正则系综而言，
$$
(\Delta E)^2 = \langle E^2\rangle - \langle E\rangle^2 = 0\\
(\Delta N)^2 = \langle N^2\rangle - \langle N\rangle^2 = 0\\
(\Delta S)^2 = \langle S^2\rangle - \langle S\rangle^2 = 0
$$

#### 正则系综

有能量交换，无粒子交换的系统

单粒子配分函数：$Z_1 = \sum_i exp(-\beta E_i)$，则该粒子处于某个态$\mid i\rangle \langle i\mid$上的概率幅为$P_i = \frac{exp(-\beta E_i)}{Z}$

对连续谱而言求和改积分（注意这里是在整个相空间对概率分布$exp(-\beta E)$进行积分）：

单粒子配分函数：$Z_1 = \frac{1}{h^{3}}\int d^3q_1 \int d^3p_1 exp(-\beta \bold{p}^2/2m) = \frac{V}{h^3}\left(\frac{2\pi m}{\beta} \right)^{\frac32} $

N粒子配分函数（这里的求和是e指数动量指标乘积的结果）：
$$
Z_N = \frac{1}{N! h^{3N}}\int d^3q_1 d^3q_2 ...d^3q_N \int d^3p_1 d^3p_2 ... d^3p_N exp(-\beta \sum_i p_i^2/2m )\\
= \frac{1}{N!}Z_1^N
$$
此时的密度矩阵（N个粒子在所有可能的态上的概率分布）：$\hat\rho =\frac{exp(-\beta \hat{H})}{Z_N} $，

于是有：$Z_N = \rho^{-1}exp(-\beta \hat H) = exp(-\beta \hat H)\rho = exp(-\beta \hat H)\sum_i p_i \mid i\rangle \langle i\mid = Tr(exp(-\beta H)) $
$$
E = \langle H\rangle  = Tr(\rho H) = -\frac{\partial}{\partial \beta}ln\mathcal{Z_N}\\
(\Delta E)^2 = \langle E^2\rangle - \langle E\rangle ^2 = \frac{\partial ^2}{\partial \beta^2}ln\mathcal{Z_N}\\
$$
求熵：$S = k_B ln \frac1\rho $
$$
S = k_B(\beta H + Z_N)\\
\Delta S = \langle S^2\rangle - \langle S\rangle^2 = (k_B\beta)^2 \left(Tr(\rho H^2) - (Tr(\rho H))^2\right) = \left(\frac{1}{T} \right)^2 \left(\frac{\partial^2}{\partial \beta^2}lnZ_N \right)
$$
N粒子总数不变

#### 巨正则系综

巨正则系综里就要考虑N的涨落问题，因为粒子数守恒，配分函数需要加上化学势项。微正则和正则都不需要粒子数守恒的条件，它们都是粒子数没有交换只有能量交换的。

巨正则配分函数：$\Xi = \sum_{i,N} exp(-\beta(E_i-\mu N))$，积分形式为：
$$
Z_G = \sum_{N=0}^{\infin}\frac{1}{h^{3N}N!}\int d^3q_1 d^3q_2 ...d^3q_N \int d^3 p_1 d^3p_2... d^3p_N exp(-\beta (H - \mu N)) \\
= \sum_{N=0}^{\infin}\frac{V^N exp(\beta\mu N)}{h^{3N}N!}\left(\frac{2\pi m}{\beta} \right)^{3N/2} = \sum_{N=0}^{\infin}\frac1{N!} \left(exp(\beta\mu) \frac{V(2\pi m)^{\frac32}}{h^3 \beta^{\frac32}} \right)^N = exp(e^{\beta\mu} \frac{V(2\pi m)^{\frac32}}{h^3 \beta^{\frac32}})
$$
密度算符：$\hat{\rho} = \frac{exp(-\beta(\hat H-\mu N ))}{Z_G} $

巨正则配分函数还可以写为：$Z_G = Tr(e^{-\beta(\hat H-\mu N)})$

下面求粒子数的均值：
$$
\langle N\rangle = Tr(\rho N) = Tr(\frac{exp(-\beta(\hat H-\mu N ))}{Z_G} N) = \frac1{Z_G}\frac{\partial }{\partial (\beta \mu)}Tr(e^{-\beta(H - \mu N)}) = \frac1{Z_G}\frac{\partial }{\partial (\beta \mu)}Z_G
$$

$$
(\Delta N)^2 = \langle N^2\rangle - \langle N\rangle ^2\\
= \frac1{Z_G} \frac{\partial^2 Z_G}{\partial (\beta\mu)^2} - \left(\frac1{Z_G}\frac{\partial Z_G}{\partial (\beta\mu)} \right)^2
$$

内能的均值：
$$
\langle E\rangle = Tr(\rho H) = - \frac{1}{Z_G} \frac{\partial }{\partial \beta} Tr(e^{-\beta(H-\mu N)}) = -\frac1{Z_G}\frac{\partial }{\partial \beta}Z_G
$$

$$
(\Delta E)^2 = \frac1{Z_G}\frac{\partial ^2}{\partial \beta^2} Z_G - \left(\frac1{Z_G} \frac{\partial}{\partial \beta}Z_G \right)^2
$$

熵可根据定义：
$$
S = -k_B ln\hat\rho = -k_B \left(-\beta(H - \mu N) - ln Z_G \right) = k_B(\beta(H - \mu N)+ lnZ_G)
$$

$$
\langle S\rangle = k_B\beta (\langle H\rangle - \mu \langle N\rangle) + k_BlnZ_G\\
(\Delta S)^2 = \langle S^2\rangle - \langle S\rangle^2 = Tr(\rho (k_B(\beta(H-\mu N)+lnZ_G))^2 ) - \langle S\rangle ^2
$$

#### 热力学基本方程

对微正则系综：
$$
dF(\beta,V) = \frac{S}{k_B\beta^2}d\beta - PdV = -\frac1\beta lnZ
$$


对正则系综：
$$
dF(\beta,V,N) = \frac{S}{k_B\beta^2} d\beta - PdV + \mu dN = -\frac1\beta lnZ
$$


对巨正则系综：
$$
d\Phi(\beta,V,\mu) = \frac{S}{k_B\beta^2} d\beta -PdV - Nd\mu = -\frac1\beta ln Z_G
$$


#### 量子化的谐振子问题

现有能级总数为$N = \sum N_n$，每个能级上粒子数为$n_i$，能级的能量为$n_i\hbar\omega$，态总数$M = \sum_i N_{n_i}n_i$
$$
E = \sum_i N_{n_i} (n_i+\frac12) \hbar \omega\\
\Omega(E) = C_{M + N-1 }^{N-1} = \frac{(M+N-1)!}{(N-1)!M!}\\
M = \frac{E}{\hbar \omega} - \frac12\sum_i N_{n_i} = \frac{E}{\hbar\omega} - \frac{N}{2}
$$
此时的配分函数(以正则系综为例)：
$$
Z_1 = \sum_{n=0}^{\infin} exp(-\beta (n+\frac12)\hbar\omega)\\
= \frac{exp(-\beta\hbar\omega/2) - exp(-\beta(n+\frac12)\hbar\omega)exp(-\beta\hbar\omega) }{1 - exp(-\beta\hbar\omega)} = \frac{exp(-\beta \hbar\omega/2)}{1 - exp(-\beta\hbar\omega)}\\
= \frac1{2sinh(\beta\hbar\omega/2)} \\
Z_N = \frac{Z_1^N}{N!}N! = (2sinh(\beta\hbar\omega/2))^{-N}
$$
这里N指的是N个不同的谐振子能级，每个能级具有的能量是$(n+\frac12)\hbar\omega$，因为每个能级对应的n不同，这N个都是可区分的，所以配分函数应该乘以$N!$
$$
\rho = \frac{exp(-\beta H)}{Z}\\
$$
写在能量本征态basis下，就是：
$$
\hat{\rho} = \frac1Z\sum_i e^{-\beta E_i}\mid i\rangle\langle i\mid
$$

### 第三章

#### 二次量子化、场的量子化

$$
\hat{\psi}^{\dagger}(x) = \sum_m \phi_m^*(x) b_m^{\dagger}\\
b_n^{\dagger} = \int dx \phi_n(x) \hat\psi^{\dagger}(x)\\
\{\hat\psi(x), \hat\psi^{\dagger}(x') \}= \delta(x-x')\\
\{b_m, b_n^{\dagger} \} = \int dx\int dx' \phi_m^*(x)\phi_n(x')\hat{\psi}(x)\hat{\psi}^{\dagger}(x') + \int dx\int dx' \phi_m^*(x)\phi_n(x')\hat{\psi}^{\dagger}(x')\hat{\psi}(x) \\
=  \int dx\int dx' \phi_m^*(x)\phi_n(x') \{\hat\psi(x), \hat\psi^{\dagger}(x') \}=\int dx\int dx' \phi_m^*(x)\phi_n(x')\delta(x-x')\\
= \int dx \phi_m^*(x)\phi_n(x) = \int dx \langle\phi_m\mid x\rangle\langle x\mid \phi_n\rangle = \langle \phi_m\mid \phi_n\rangle = \delta_{mn}
$$

Bosonic 系统
$$
[\hat{\psi}(x), \hat{\psi}(x') ] = [\hat{\psi}^{\dagger}(x), \hat{\psi}^{\dagger}(x') ] = 0\\
\hat{H} = \int d^3x \hat{\psi}^{\dagger}(x) \left(-\frac{\hbar^2 \bold\nabla^2}{2m} + V(x) \right)\hat{\psi}(x) + \frac U2 \int d^3x \hat\psi^{\dagger}(x)\hat{\psi}^{\dagger}(x)\hat{\psi}(x)\hat{\psi}(x)\\
$$
Heissenberg 运动方程
$$
\partial_t\rho = \frac1{i\hbar}[\rho,H]\\
\partial_t\hat{\psi}(x) = \frac{1}{i\hbar}[\hat{\psi}(x) , H ]
$$

#### 密度矩阵算符的计算：

下面以正则、微正则系综为例（不考虑粒子数守恒带来的化学势项）
$$
Z = Tr(e^{-\beta H})\\
= \sum_k \langle k\mid e^{-\beta H}\mid k\rangle = \sum_k \langle k\mid e^{-\beta E_k}\mid k\rangle = \int dr\sum_k \langle k\mid r\rangle e^{-\beta E_k}\langle r\mid k\rangle\\
= \int dr\sum_k \psi_k^*(r)\psi_k(r)e^{-\beta (\hbar^2 k^2/2m + V(k))}\\
\hat{\rho} = \frac1Z exp(-\beta \hat H) = \frac1Z \sum_k e^{-\beta E_k}\mid k\rangle\langle k\mid \\
\langle r\mid \hat\rho\mid r'\rangle = \frac1Z \sum_k e^{-\beta E_k}\psi_k(r)\psi^*_k(r')
$$
对自由粒子：
$$
Z = V\left(\frac{m}{2\pi \hbar^2\beta} \right)^{\frac32}\\
\langle r\mid \hat\rho\mid r'\rangle = \langle r'\mid \hat\rho\mid r\rangle = \frac1V exp\left(-\frac{m(r-r')^2}{2\hbar^2\beta} \right)
$$
一次量子化哈密顿量转换为二次量子化形式：
$$
H^{(1)} = \frac{\bold p^2}{2m} + V(x)\\
H^{(2)} = \sum_{i,j} \langle \phi_i\mid H^{(1)}\mid \phi_j\rangle \hat b_i^{\dagger} \hat b_j\\
= \sum_i \sum_j \int d^3x' d^3x'' \langle\phi_i\mid x'\rangle (-\frac{\hbar^2}{2m}\frac{\partial^2 }{\partial x'^2}\delta(x' - x'') + V(x')\delta(x' - x'')) \langle x''\mid\phi_j\rangle \\
= \int d^3x' d^3x'' \hat\psi^{\dagger}(x') (-\frac{\hbar^2}{2m}\frac{\partial^2 }{\partial x'^2}\delta(x' - x'') + V(x')\delta(x' - x'')) \hat\psi(x'')\\
\approx \int d^3 x' \hat{\psi}^{\dagger}(x')( - \frac{\hbar^2}{2m}\nabla^2 + V(x'))\hat{\psi}(x')\\
V^{(1)} = V^{(1)}(x',x'')\\
V^{(2)} = \frac12\int d^3x'd^3x''\hat{\psi}^{\dagger}(x')\hat{\psi}^{\dagger}(x'')V^{(1)}\hat{\psi}(x'') \hat{\psi}(x')
$$

#### Boson和Fermion的驻波束缚态

$$
Z_B = \sum_{\{k_1,k_2 \}} \langle k_1,k_2\mid exp(-\beta H)\mid k_1,k_2\rangle \\
=\sum_{k_1 <k_2 }(\frac1{\sqrt2})^2 (\langle k_1\mid\langle k_2\mid + \langle k_2\mid \langle k_1\mid )exp(-\beta (-\frac{\hbar^2}{2m}\nabla^2))(\mid k_1\rangle\mid k_2\rangle + \mid k_2\rangle \mid k_1\rangle ) \\
+ \sum_k \langle k\mid \langle k\mid exp(-\beta(\frac{\hbar^2}{2m}\bold{k}^2))\mid k\rangle\mid k\rangle\\
= \sum_{k_1 < k_2} exp(-\beta\frac{\hbar^2}{2m}(k_1^2 + k_2^2) ) + \sum_k exp(-\beta\frac{\hbar^2k^2}{m})\\
Z_F = \sum_{k_1<k_2} \frac12(\langle k_1\mid \langle k_2\mid - \langle k_2\mid \langle k_1\mid )exp^{-\beta H}(\mid k_1\rangle\mid k_2\rangle - \mid k_2\rangle\mid k_1 \rangle)\\
= \sum_{k_1 < k_2} exp(-\beta\frac{\hbar^2}{2m}(k_1^2 + k_2^2) ) 
$$

注意这里有个关系，
$$
\sum_{k_1,k_2} exp(-\beta\frac{\hbar^2}{2m}(k_1^2 + k_2^2)) = 2\sum_{k_1<k_2}exp(-\beta\frac{\hbar^2}{2m}(k_1^2 + k_2^2)) + \sum_{k_1 = k_2=k} exp(-\beta\frac{\hbar^2}{2m}(2k^2))\\ \Longrightarrow
\sum_{k_1<k_2}exp(-\beta\frac{\hbar^2}{2m}(k_1^2 + k_2^2)) = \frac12\left(\sum_{k_1,k_2} exp(-\beta\frac{\hbar^2}{2m}(k_1^2 + k_2^2)) - \sum_{k_1 = k_2=k} exp(-\beta\frac{\hbar^2}{2m}(2k^2)) \right)\\
= \frac12(Z_1^2(m) - Z_1(\frac{m}2) )\\
Z_F = \frac12(Z_1^2(m) - Z_1(\frac{m}2) )\\
Z_B = \frac12(Z_1^2(m) + Z_1(\frac{m}2) )
$$
经典的情形（配分函数就是k1，k2两个态相加）：
$$
Z_{classical} = \frac12 Z_1^2(m)
$$
计算经典和玻色/费米统计下的能量差：
$$
\Delta E_{\pm} = -\frac{\partial}{\partial\beta}\Delta lnZ_{\pm} 
$$
这里可以取近似：$Z_1(\frac{m}2)\ll Z_1^2(m)$

即：$ln(1+\frac{Z_1(\frac{m}2)}{Z_1^2(m)})\approx \frac{Z_1(\frac{m}2)}{Z_1^2(m)}$

热容差为：$\Delta C_V = \frac{\partial \Delta E_{\pm}}{\partial T}\bigg|_{V}$

巨正则势：$\Phi = -k_BT lnZ_G$

态密度：$n = \frac {\langle N\rangle} V = \frac{1}{Z_G V}\frac{\partial Z_G}{\partial (\beta\mu)}$

在一个盒子里，无相互作用费米子之间：$n = \frac{S_d}{(2\pi)^d}\frac{\beta^{-d/s}}{s}\Gamma(\frac ds)f_{\frac ds}(z)$

低温下的费米狄拉克分布：$\frac1{exp(\beta(\epsilon - \epsilon_F))+1}\rightarrow \Theta(\epsilon -\epsilon_F)$

K空间的球面积分：
$$
\frac{V}{(2\pi)^3}\int_{k<k_F} d^3\bold{k} = \frac{V}{(2\pi)^3}\int_{0}^{k_F}4\pi k^2dk 
$$

#### 自发磁化

磁化强度$\propto$态密度的涨落
$$
E_{\pm}/V = \frac{\hbar^2}{2m}\frac35 (6\pi^2)^{\frac23}(n_+^{\frac53} + n_-^{\frac53} )\\
n_+ = \frac n2 +\delta,\ \ n_- = \frac n2 -\delta\\
$$
对E进行$\delta$级数展开，得到E随$\delta$变化，存在一个cirtical $\alpha_C$，小于此值E随δ增大而增大，大于此值E随δ增大而减小
$$
\alpha_C = \frac{\hbar^2}{2m}\frac43(3\pi^2)^{\frac23}n^{-\frac13}\\
M\propto \pm\sqrt{\alpha - \alpha_C}
$$
常温下的费米狄拉克分布，$\mu = \epsilon_F$，此时n个粒子占据一个能量为$\epsilon$的态的概率为
$$
P(n(\epsilon) = 0,1 ) = \frac{exp(-\beta(\epsilon-\mu)n(\epsilon))}{exp(-\beta(\epsilon - \mu))+1}\\
\langle n(\epsilon)\rangle = P(1)\\
E(T,n) = \frac{V}{(2\pi)^3}\int d^3\bold{k} \langle n(\epsilon)\rangle \epsilon(k)
$$







