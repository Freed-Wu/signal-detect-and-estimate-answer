# 3 #

## 3.2 ##

根据一次观测，用极大极小化检验来对下面两个假设做出判断。
$$
\begin{aligned}
H_1: & z(t) = n(t)\\
H_0: & z(t) = 1 + n(t)
\end{aligned}
$$
假定 $n(t)$ 为具有零均值和功率 $\sigma^2$ 的高斯过程，以及 $C_{00} = C_{11} =
0, C_{10} = C_{01} = 1$ 根据观测结果定出的门限是什么？
每一个假设的先验概率是多少？
$$
\begin{dcases}
p(z|H_1) & = \frac{1}{\sqrt{2\pi}\sigma}\exp\frac{-z^2}{2\sigma^2}\\
p(z|H_0) & = \frac{1}{\sqrt{2\pi}\sigma}\exp\frac{-(z - 1)^2}{2\sigma^2}
\end{dcases}
$$
$$
\begin{aligned}
	\lambda(z) = \frac{p(z|H_0)}{p(z|H_1)}
	= \exp\frac{2z - 1}{2\sigma^2} & \mathop{\gtrless}\limits_{H_1}^{H_0}
	\lambda_0\\
	z & \mathop{\gtrless}\limits_{H_1}^{H_0} \sigma^2\ln\lambda_0 +
	\frac{1}{2} = \lambda'_0
\end{aligned}
$$
$$
\begin{dcases}
	P_\mathrm{F} = \int\nolimits_{\lambda'_0}^\infty p(l|H_1)dl =
\int\nolimits_{\lambda'_0}^\infty
\frac{1}{\sqrt{2\pi}\sigma}\exp\frac{-l^2}{2\sigma^2}dl\\
	P_\mathrm{M} = \int\nolimits_{-\infty}^{\lambda'_0} p(l|H_0)dl =
\int\nolimits_{\lambda'_0}^\infty
\frac{1}{\sqrt{2\pi}\sigma}\exp\frac{-(l - 1)^2}{2\sigma^2}dl
\end{dcases}
$$
$$
\begin{aligned}
	P_\mathrm{M} & = P_\mathrm{F}\\
	1 - \mathrm{erfc}\frac{\lambda'_0 - 1}{\sigma}
	& = \mathrm{erfc}\frac{\lambda'_0}{\sigma}\\
	\lambda'_0 & = \frac{1}{2}
\end{aligned}
$$
$$
\begin{aligned}
	\lambda_0 = \frac{p(z_\mathrm{T}^*|H_0)}{p(z_\mathrm{T}^*|H_1)} =
\frac{P^*(H_1)}{P^*(H_0)}\frac{C_{01} - C_{11}}{C_{10} - C_{00}} = 1
\end{aligned}
$$
$$
又 P^*(H_1) + P^*(H_0) = 1 \Rightarrow P^*(H_1) = P^*(H_0) = \frac{1}{2}
$$

## 3.3 ##

若上题假定 $C_{10} = 3, C_{01} = 6$ 。

#### 1 ####

每个假设的先验概率为何值时达到最大的可能代价；

#### 2 ####

根据一次观测的判决区域如何?
$$
\begin{dcases}
	P_\mathrm{F} = \int\nolimits_{\lambda'_0}^\infty p(l|H_1)dl =
\int\nolimits_{\lambda'_0}^\infty
\frac{1}{\sqrt{2\pi}\sigma}\exp\frac{-l^2}{2\sigma^2}dl\\
	P_\mathrm{M} = \int\nolimits_{-\infty}^{\lambda'_0} p(l|H_0)dl =
\int\nolimits_{\lambda'_0}^\infty
\frac{1}{\sqrt{2\pi}\sigma}\exp\frac{-(l - 1)^2}{2\sigma^2}dl
\end{dcases}
$$
$$
\begin{aligned}
	P_\mathrm{M} & = P_\mathrm{F}\\
	\lambda_0' & = \exp\frac{\lambda'_0 - 1/2}{\sigma^2}
\end{aligned}
$$

## 3.5 ##

若假设 $H_1$ 下和假设 $H_0$ 下，观测信号 $z$ 都是零均值，但方差分别是
$\sigma_1^2$ 和 $\sigma_0^2$ 的高斯随机变量，设似然比检测门限为 $\lambda_0$ 。

#### 1 ####

两个假设作出选择的判决形式如何;

$$
\begin{dcases}
	p(z|H_0) & =
	\frac{1}{\sqrt{2\pi}\sigma_0}\exp\frac{-z^2}{2\sigma_0^2}\\
	p(z|H_1) & =
	\frac{1}{\sqrt{2\pi}\sigma_1}\exp\frac{-z^2}{2\sigma_1^2}
\end{dcases}
$$
$$
\begin{aligned}
	\lambda(z) = \frac{p(z|H_0)}{p(z|H_1)}
	= \frac{\sigma_0}{\sigma_1}\exp\frac{\sigma_1^2 -
	\sigma_0^2}{2\sigma_0^2\sigma_1^2}z^2 &
	\mathop{\gtrless}\limits_{H_0}^{H_1} \lambda_0\\
	|z| & \mathop{\gtrless}\limits_{H_0}^{H_1} \lambda'_0,
	\sigma_1 > \sigma_0\\
	|z| & \mathop{\gtrless}\limits_{H_1}^{H_0} \lambda'_0,
	\sigma_1 < \sigma_0\\
	\lambda'_0 & = \sqrt{\frac{2}{\sigma_1^2 -
	\sigma_0^2}\ln(\frac{\sigma_1}{\sigma_0}\lambda_0)}\sigma_0\sigma_1
\end{aligned}
$$

#### 2 ####

判决域是如何划分的;

#### 3 ####

求两类错误概率 $P(H_1|H_0)$ 和 $P(H_0|H_1)$ 。
$$
\sigma_1 > \sigma_0\rightarrow
\\
\begin{aligned}
	P(H_1|H_0) & = 2\int\nolimits_{-\infty}^{-\lambda'_0} p(l|H_0)dl\\
	& = 2\int\nolimits_{\frac{\lambda'_0}{\sigma_0^2}}^\infty
	\frac{1}{\sqrt{2\pi}}\exp\frac{-t^2}{2}dt\\
	& = 2Q(\sqrt{\frac{2}{\sigma_1^2 -
	\sigma_0^2}\ln(\frac{\sigma_1}{\sigma_0}\lambda_0)}\sigma_1)\\
	P(H_0|H_1) & = \int\nolimits_{-\lambda'_0}^{\lambda'_0} p(l|H_0)dl\\
	& = 1 - 2Q(\sqrt{\frac{2}{\sigma_1^2 -
	\sigma_0^2}\ln(\frac{\sigma_1}{\sigma_0}\lambda_0)}\sigma_0)
\end{aligned}
$$
$$
\sigma_1 < \sigma_0\rightarrow
\\
\begin{aligned}
	P(H_0|H_1) & = 2Q(\sqrt{\frac{2}{\sigma_0^2 -
	\sigma_1^2}\ln(\frac{\sigma_0}{\sigma_1}\lambda_1)}\sigma_0)\\
	P(H_1|H_0) & = 1 - 2Q(\sqrt{\frac{2}{\sigma_0^2 -
	\sigma_1^2}\ln(\frac{\sigma_0}{\sigma_1}\lambda_1)}\sigma_1)
\end{aligned}
$$
## 3.8 ##

试推导如下情况的似然比。在假设 $H_1$ 下和假设 $H_0$ 下,观测信号 $z$
是高斯随机变量，均值和方差分别为 $m_1, \sigma_1^2$ 和 $m_0, \sigma_0^2$
，似然比检测门限为 $\lambda_0$ ，并求判决域和错误概率。

$$
\begin{dcases}
	p(z|H_1) & = \frac{1}{\sqrt{2\pi}\sigma_1}\exp\frac{-(z -
	m_1)^2}{2\sigma_1^2}\\
	p(z|H_0) & = \frac{1}{\sqrt{2\pi}\sigma_0}\exp\frac{-(z -
	m_0)^2}{2\sigma_0^2}
\end{dcases}
$$
$$
\begin{aligned}
	\lambda(z) = \frac{p(z|H_0)}{p(z|H_1)}
	= \frac{\sigma_0}{\sigma_1}\exp\left(\frac{(z -
	m_0^2)}{2\sigma_0^2}-\frac{(z - m_1)^2}{2\sigma_0^2}\right)
	& \mathop{\gtrless}\limits_{H_0}^{H_1}
	\lambda_0\\
	\left(\frac{1}{\sigma_0^2} - \frac{1}{\sigma_1^2}\right)z^2 -
	2\left(\frac{m_0}{\sigma_0^2} - \frac{m_1}{\sigma_1^2}\right)z +
	\frac{m_0^2}{\sigma_0^2} - \frac{m_1^2}{\sigma_1^2}
	& \mathop{\gtrless}\limits_{H_0}^{H_1}
	2\ln\frac{\lambda_0\sigma_1}{\sigma_0}
\end{aligned}
$$
$$
z_{1, 2} = \left.
\left(\left(\frac{m_0}{\sigma_0^2} - \frac{m_1}{\sigma_1^2}\right) \pm
\sqrt{\frac{(m_0 - m_1)^2}{\sigma_0^2\sigma_1^2} +
2\left(\frac{1}{\sigma_0^2} -
\frac{1}{\sigma_1^2}\right)}\ln\frac{\lambda_0\sigma_1}{\sigma_0}\right)
\middle/
\left(\frac{1}{\sigma_0^2} - \frac{1}{\sigma_1^2}\right)
\right.
$$
$$
\sigma_0 < \sigma_0\Rightarrow
\\
\begin{aligned}
	H_1 & : (-\infty, z_1) \cup (z_2,  + \infty)\\
	H_0 & : (z_1, z_2)
\end{aligned}
$$
$$
\sigma_0 > \sigma_0\Rightarrow
\\
\begin{aligned}
	H_0 & : (-\infty, z_0) \cup (z_1,  + \infty)\\
	H_1 & : (z_0, z_1)
\end{aligned}
$$

## 3.10 ##

考虑二元假设检验问题，已知
$$
\begin{aligned}
	p(z|H_1) & = (\frac{1}{2\pi})^{1/2} \exp(-\frac{z^2}{2})\\
	p(z|H_0) & = \frac{1}{2}\exp(-|z|)
\end{aligned}
$$

#### 1 ####

建立似然比检验，并求判决域；

$$
\begin{aligned}
	\lambda(z) = \frac{p(z|H_0)}{p(z|H_1)}
	= \sqrt{\frac{2}{\pi}}\exp\left(|z|-\frac{z^2}{2}\right) &
	\mathop{\gtrless}\limits_{H_1}^{H_0}
	\lambda_0\\
	|z|-\frac{z^2}{2} & \mathop{\gtrless}\limits_{H_1}^{H_0}
	\ln\lambda_0 - \frac{1}{2}\ln\frac{2}{\pi}
\end{aligned}
$$
$$
z_{1, 2} = 1 \pm \sqrt{1 - 2\left(\ln\lambda_0 - \frac{1}{2}\frac{2}{\pi}\right)}
$$
$$
\begin{aligned}
	H_0: & |z| \in (z_1, z_2)\\
	H_1: & |z| \in (-\infty, z_1) \cup (z_2, \infty)
\end{aligned}

$$

#### 2 ####

设 $C_{00} = C_{11} = 0$ ， $C_{01} = C_{10} = 1$ ，若 $P(H_1) = \frac{3}{4}$
，试求贝叶斯检验的 $P(H_1|H_0)$ 和 $P(H_0|H_1)$ 。

$$
\lambda_0 = \frac{P(H_0)}{P(H_1)}\frac{C_{10} - C_{00}}{C_{01} - C_{11}} =
\frac{1}{3}
$$

## 3.11 ##

数字通信系统中，两假设下的接收信号分别为
$$ H_1: z_k = A + n_k, k = 1, 2, \ldots, N $$
$$ H_0: z_k = n_k, k = 1, 2, \ldots, N $$
若 $N$ 个样本 $z$ 相互统计独立，噪声 $n_k \sim N(0, 1)$ ， 先验概率 $P(H_1) =
P(H_0) = \frac{1}{2}$ , 代价因于 $C_{00} = C_{11} = 0$ ， $C_{01} = C_{10} = 1$
。

#### 1 ####

求最小总错误概率的判决规则；

$$
\begin{aligned}
	H_1: & p(z_1, z_2, \ldots, z_N|H_1) = \frac{1}{(2\pi)^{N/2}\sigma_n^N}
	\exp\frac{-\sum\limits_{i = 1}^N (z_k - A)^2}{2\sigma_n^2}\\
	H_0: & p(z_1, z_2, \ldots, z_N|H_0) = \frac{1}{(2\pi)^{N/2}\sigma_n^N}
	\exp\frac{-\sum\limits_{i = 1}^N z_k^2}{2\sigma_n^2}
\end{aligned}
$$
$$
\begin{aligned}
	\lambda(z) = \frac{p(z_1, z_2, \ldots, z_N|H_1)}{p(z_1, z_2, \ldots,
	z_N|H_0)} = \exp\frac{\sum\limits_{i = 1}^N A(2z_k - A)}{2\sigma_\mathrm{n}^2} &
	\mathop{\gtrless}\limits_{H_0}^{H_1} \lambda_0 = 1\\
	\bar{z} &
	\mathop{\gtrless}\limits_{H_0}^{H_1} \frac{A}{2}
\end{aligned}
$$

#### 2 ####

求最小总错误概率 $P_\mathrm{e}$ 。
$$
\begin{dcases}
	p(l|H_1) & = \frac{1}{\sqrt{2\pi/N}\sigma_\mathrm{n}}\exp\frac{-(l -
	A)^2}{2\sigma_\mathrm{n}^2/N}\\
	p(l|H_1) & =
	\frac{1}{\sqrt{2\pi/N}\sigma_\mathrm{n}}\exp\frac{-l^2}{2\sigma_\mathrm{n}^2/N}
\end{dcases}
$$
$$
\begin{aligned}
	P_\mathrm{e} & = P(H_0)P(H_1|H_0) + P(H_1)P(H_0|H_1)\\
	& = \frac{1}{2}\left(\int\nolimits_{\frac{A}{2}}^\infty p(l|H_0)dl +
\int\nolimits_{-\infty}^\frac{A}{2} p(l|H_1)dl\right)\\
	& =
	\frac{1}{2}\mathrm{erfc}\frac{A\sqrt{N}}{2\sqrt{2}\sigma_\mathrm{n}}
\end{aligned}
$$

