## 混合高斯模型

### 1. 高斯分布

如果连续标量随机变量$x$概率密度函数为：
$$
p(x)=\frac{1}{(2\pi)^{1/2}\sigma}\exp[-\frac{1}{2}(\frac{x-\mu}{\sigma})^2],\\
(-\inf<x<\inf;\sigma>0)
$$
则称$x$服从高斯分布（或正态分布），记为：
$$
x\sim \mathcal{N}(\mu,\sigma^2)
$$
高斯分布的随机变量均值为$\mu$，方差为$\sigma^2$。

如果D维随机变量$\bold{x}=(x_1,x_2,\cdots,x_D)^T$的联合概率密度函数为：
$$
p(\bold{x})=\frac{1}{(2\pi)^{D/2}|\bold{\Sigma}|^{1/2}}\exp[-\frac{1}{2}(\bold{x}-\bold{\mu})^T\bold{\Sigma}^{-1}(\bold{x}-\bold{\mu})],\\
(\bold{\mu}\in\mathcal{R}^D,\bold{\Sigma}\in\mathcal{R}^{D\times D})
$$
则称$\bold{x}$服从D元高斯分布（或正态分布），记为：
$$
x\sim \mathcal{N}(\bold{\mu},\bold{\Sigma})
$$
均值为$\bold{\mu}$，$\bold{\Sigma}$称为协方差矩阵。

由于大数定理的存在，很多实际问题中很多变量都可近似为高斯分布。

假设一个随机变量是从多个高斯分布中采样的，即：
$$
\begin{aligned}
p(x)&=\sum\limits_{m=1}^{M}\frac{c_m}{(2\pi)^{1/2}\sigma_m}\exp[-\frac{1}{2}(\frac{x-\mu_m}{\sigma_m})^2]\\
&=\sum\limits_{m=1}^{M}c_m\mathcal{N}(x;\mu_m,\sigma_m^2)
\end{aligned}
$$
