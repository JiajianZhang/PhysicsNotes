第四章

### BEC

计算巨正则系综下的玻色子配分函数
$$
Z_G = \sum_{N = 0}^{\infin}\sum_{\{n_i \}} e^{-\beta(\sum_i n_i\epsilon_i - \mu N )}
= \prod_i \frac1{-exp(-\beta(\epsilon_i -\mu))+1} = \prod_i \frac{exp(\beta(\epsilon_i - \mu))}{exp(\beta(\epsilon_i -\mu))-1}
$$
这个也可用占据数表象求解：
$$
Z_G = Tr(e^{-\beta(\hat H-\mu N)}) = \sum_{\{n_q \}}\langle n_{q_1},n_{q_2}...\mid e^{\beta(\hat H-\mu N)}\mid n_{q_1}, n_{q_2}...\rangle = \prod_i \frac{exp(\beta(\epsilon_i -\mu))}{exp(\beta(\epsilon_i -\mu))-1}
$$
这里面矩阵元：$\langle n_{q_1}...\mid exp(-\beta(\hat H-\mu N))\mid n_{q_1}...\rangle = \prod_{\{q_i \}} exp(-\beta(\epsilon_{q_i}n_{q_i} -\mu n_{q_i})) $

特征函数可以求解均值：
$$
\langle e^{ik\hat n_q}\rangle = Tr(\rho e^{ik\hat n_q}) = \sum_{\{n_q \}}\langle n_{q_1}...\mid \frac1{Z_G}e^{-\beta(\hat H-\mu \hat N)}e^{ik\hat n_q} \mid n_{q_1}...\rangle\\
= \frac{1-exp(-\beta(\epsilon_{q} - \mu))}{1 - exp(-\beta(\epsilon_q - \mu + ik))}\\
\lang n_q\rangle = -i\frac{\partial}{\partial k}\langle e^{ikn_q}\rangle\bigg|_{k=0}\\
\langle n_q^2\rangle = -\frac{\partial^2}{\partial k^2}\langle e^{ikn_q}\rangle\bigg|_{k=0}
$$
熵
$$
S = k_Bln\frac1{\rho} = -k_Bln(\frac1{Z_G}e^{-\beta(H-\mu N)}) = k_B\beta(H-\mu N) + k_BlnZ_G\\
= -k_B \sum_i p_ilnp_i\\
p_i = \frac{exp(-\beta(n(q)\epsilon_i - \mu n_{q}))}{Z_G}\\
S = k_B\sum_{\{n_{q_i} \}}\left( ln(1+ \langle n_{q_i} \rangle) - \langle n_{q_i} \rangle ln\frac{\langle n_{q_i}\rangle}{1+ \langle n_{q_i}\rangle} \right)
$$
玻色/费米分布的配分函数：$Z_{B/F} = \frac1{1 \mp exp(-\beta H)}$，n个粒子占据一个能量为$\epsilon$的态的概率为：$P = Z_{B/F} exp(-\beta(\epsilon - \mu)n(\epsilon))$，则平均粒子数为：$\langle n\rangle = \sum_i P_i n_i = \int d\epsilon P(\epsilon)n(\epsilon) = \frac{V}{(2\pi)^3}\int d^3k P(k)n(k)$

常常用到的d微球体积积分：$S_d = \frac{2\pi^{\frac d2}}{\Gamma(\frac d2)}$
$$
lnZ_G = \sum_i ln\left(\frac{exp(\beta(\epsilon_i - \mu))}{exp(\beta(\epsilon_i -\mu))-1} \right) = \frac{V}{(2\pi)^d} \int d^d \bold{k} ln\left(\frac{exp(\beta(\epsilon_i - \mu))}{exp(\beta(\epsilon_i -\mu))-1} \right) \\
= \frac{V S_d}{(2\pi)^d}\int k^{d-1}dk ln\left(\frac{exp(\beta(\epsilon_i - \mu))}{exp(\beta(\epsilon_i -\mu))-1} \right)\\
= \frac{V}{\lambda^d}g_{\frac d2+1}(z)\\
\lambda = \frac{h}{\sqrt{2\pi mk_BT}}\\
\langle N\rangle = \frac{\partial lnZ_G}{\partial(\beta\mu)} = \frac{V}{\lambda^d}g_{\frac d2}(z)\\
\langle E\rangle = -\frac{\partial }{\partial \beta} ln Z_G = \frac{d}{2\beta} \frac{V}{\lambda^d} g_{\frac d2+1}(z)\\
PV = \frac1\beta lnZ_G = -\Phi
$$

#### BEC临界温度

对应的是化学势为0，$z = e^{\beta\mu}=1$，
$$
n = \frac1{\lambda^d(T_C)} g_{\frac d2}(z)
$$
在临界温度左右的相变可以用热容的变化刻画：
$$
C_V/(Nk_B) = \frac d2(\frac d2+1) \frac{g_{\frac d2+1}(1)}{g_{\frac d2}(z)} \ \ (T<T_C)\\
C_V/(NK_B) = \frac {d(d+1)z}{2^{\frac d2+1}} + \frac d2 + \mathcal{O}(z^2) \ \ (T>T_C)
$$
重要积分/求导
$$
\Gamma(z) = \int_0^{\infin} x^{z-1} e^{-x} dx\\
\int_{-\infin}^{\infin} e^{-Ax^2} dx = \sqrt{\frac{\pi}{A}}\\
\int_{-\infin}^{\infin} \mid x\mid e^{-Ax^2}dx = \frac1A \\
\int_{-\infin}^{\infin} x^2 e^{-Ax^2}dx = \frac12\sqrt{\frac{\pi}{\lambda^3}} \\
\frac{\partial g_{v}(z)}{\partial z} = \frac1v g_{v-1}(z)\\
g_v(z) = \sum_{n=1}^{\infin} \frac{z^n}{n^v}\\
$$
有固定磁场（z方向）作用下的系统的平均粒子数，s 为自旋磁量子数，如果是spin-1玻色子系统，s可以取0，-1，1三种值。
$$
\langle N_s\rangle = \frac{V}{\lambda^3}g_{\frac32}(ze^{\beta\mu_0sB})
$$
磁化率：
$$
M(T,\mu) = \mu_0(\langle N_+\rangle - \langle N_-\rangle ) \approx 2\beta \mu_0^2 B g_{\frac12}(z)
$$
susceptibility: $\chi(T,\mu) = \frac{\partial M}{\partial B} $

### 集团展开、维里展开

已知n，求z用n的展开
$$
n = \frac1V\sum_{s}\langle N_s\rangle = \frac1{\lambda^3} \sum_s g_{\frac32}(ze^{\beta\mu_0sB} ) = \frac1{\lambda^3} \sum_s \sum_i^{\infin} A_n \frac{z^i}{i^{\frac32}}\\
$$
假设$z = \sum_j^{\infin} a_j n^j$
$$
n = \frac1{\lambda^3} \sum_s \sum_i^{\infin} A_n \frac{(\sum_j^{\infin}a_j n^j)^i}{i^{\frac32}}
$$
集团展开：

<img src="C:\Users\apple\AppData\Roaming\Typora\typora-user-images\image-20201228111139604.png" alt="image-20201228111139604" style="zoom:50%;" />

求解热容差：
$$
C_P - C_V = T(\frac{\partial S}{\partial V})_T (\frac{\partial V}{\partial t})_P = T(\frac{\partial p}{\partial T})_V(\frac{\partial V}{\partial T})_P
$$


### 黑体辐射

$$
E = \frac{V}{(2\pi)^3} \int d^3k \frac{2\hbar \omega(k)}{e^{\beta\hbar\omega(k)}-1} = \int u(\omega)d\omega\\
\langle N\rangle = \frac{V}{(2\pi)^3}\int 4\pi k^2 dk  \frac1{exp(\beta\hbar ck)-1} 
$$

