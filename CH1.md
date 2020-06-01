# 1 #

## 1.2 ##

判断下列信号是否是周期信号，如果是周期信号，求出它的基波周期。

### 1 ###

$$ x(t) = 2\cos(3t + \dfrac{\pi}{4}) $$

---

$$ T = \dfrac{2\pi }{3} $$

---

### 3 ###

$$ x(t) = \mathrm{e}^{\jmath (\pi t-1)} $$

---

$$ T = \dfrac{2\jmath\pi }{\jmath\pi } = 2 $$

---

### 5 ###

$$ x(n) = \sum_{m = 0}^{\infty} \left (\delta[n - 3m] - \delta[n - 1 - 3m]\right ) $$

---

$$ n < 0, m > 0 \rightarrow n \neq m \rightarrow x = 0 $$
$$ n > 0 \rightarrow x \neq 0 $$
$$ T\notin \mathbb{R} $$

---

### 7 ###

$$ x(n) = \cos\dfrac{n}{4}\cos\dfrac{n\pi }{4} $$

---

$$ x(n) = \dfrac{1}{2}\left (\cos\dfrac{n + n\pi }{4} + \cos\dfrac{n - n\pi }{4}\right ) $$
$$ T_1 = \dfrac{2\pi }{(1 + \pi )/4} $$
$$ T_2 = \dfrac{2\pi }{(1 - \pi )/4} $$
$$ T = lcm(T_1, T_2) \notin \mathbb{R} $$

---

## 1.3 ##

试判断下列信号是能量信号？还是功率信号？

### 1 ###

$$ x_1(t) = A \mathrm{e}^{-t}, t\geqslant 0 $$

---

$$ W = \lim_{T\rightarrow \infty }\int\nolimits_{-T}^{T} x_1^2(t)\mathrm{d} t = \int\nolimits_0^TA^2\mathrm{e}^{-2t}\mathrm{d}t = \dfrac{A^2}{2} $$
$$ P = \lim_{T\rightarrow \infty }\dfrac{1}{2T}\int\nolimits_{-T}^{T} x_1^2(t)\mathrm{d}t = 0 $$

---

### 2 ###

$$ x_2(t) = A\cos(\omega_0 t + \theta) $$

---

$$ P = \lim_{T\rightarrow \infty }\dfrac{1}{2T}\int\nolimits_{-T}^{T} x_1^2(t)\mathrm{d}t =  \lim_{T\rightarrow \infty }\dfrac{1}{2T}\int\nolimits_{-T}^{T} A^2\cos^2(\omega_0 t + \theta )\mathrm{d}t = \dfrac{A^2}{2} $$
$$ W = \lim_{T\rightarrow \infty }\int\nolimits_{-T}^{T} x_1^2(t)\mathrm{d}t = \infty $$

---

## 1.4 ##

判断下列论点正确与否：

### 1 ###

两个周期信号之和总是周期信号；

---

✗

当且仅当两个周期信号的最小公倍数存在，两个周期信号之和是周期信号。

---

### 2 ###

所有非周期信号都是能量信号；

---

✗

当且仅当非周期信号绝对平方可积时，非周期信号是能量信号。

---

### 3 ###

所有能量信号都是非周期信号；

---

✓

$$ s(t)是能量信号 \rightarrow \int\nolimits_{-\infty }^{\infty }s^2(t)\mathrm{d}t < \infty $$
$$ s(t)是周期信号 \rightarrow \int\nolimits_{-\dfrac{T}{2} }^{\dfrac{T}{2} }s^2(t)\mathrm{d}t = 0 $$
$$ \int\nolimits_{-\dfrac{T}{2} }^{\dfrac{T}{2} }s^2(t)\mathrm{d}t > 0 \rightarrow 矛盾 $$

---

### 4 ###

所有随机信号都是非周期信号；

---

✗

信号分为随机信号和确知信号，确知信号分为非周期信号和周期信号。

---

### 5 ###

两个功率信号之积总是一个功率信号；

---

✗

$$ \sin(t)u(t)是功率信号，\sin(t)u(-t)是功率信号, 0不是功率信号 $$

---

### 6 ###

两个功率信号之和总是一个功率信号；

---

✗

$$ \sin(t)u(t)是功率信号，-\sin(t)u(t)是功率信号, 0不是功率信号 $$

---

### 7 ###

一个功率信号和一个能量信号之积总是一个能量信号。

---

✗

$$ \sin(t)u(t)是功率信号，u(t + 1)-u(t)是能量信号, 0不是能量信号 $$

---

## 1.6 ##

离散随机变量X由0, 1, 2, 3四个样本组成，相当于四元通信中的四个电平，四个样本的取
值概率顺序为1/2, 1/4, 1/8, 1/16 。求随机变量的数学期望和方差。

---

$$ EX = \sum_{n = 0}^3 nP(X = n) = 0.6875 $$
$$ EX^2 = \sum_{n = 0}^3 n_2P(X = n) = 1.5273 $$
$$ DX = EX^2 - \left (EX\right )^2 = 0.8398 $$

---

## 1.9 ##

随机变量X在[α, β]上均匀分布，求它的数学期望和方差。

---

$$ EX = \int\nolimits_{-\infty }^\infty tP(X = t)\mathrm{d}t = \dfrac{\alpha + \beta }{2} $$
$$ EX^2 = \int\nolimits_{-\infty }^\infty t_2P(X = t)\mathrm{d}t = \dfrac{\alpha^2 + \beta^2 + \alpha \times \beta }{3} $$
$$ DX = EX^2 - \left (EX\right )^2 = \dfrac{\left (\alpha - \beta\right )^2}{12} $$

---

## 1.10 ##

设随机变量X的概率密度为

$$ f(x) = \left\{
\begin{matrix}
1, 0\leqslant x\leqslant 1\\
0, 其他
\end{matrix}
\right.
$$
求Y ＝ 5X + 1的概率密度。

---

$$ x(y) = \dfrac{y - 1}{5} $$

$$ f_Y(y) = f\big(x(y)\big) \left | \dfrac{\mathrm{d}}{\mathrm{d}y}x(y) \right | = \dfrac{u(y - 1) - u(y - 6)}{5}$$

---

## 1.13 ##

已知二维随机变量(X, Y)的二阶混合原点矩 m_1, 及数学期望 m_x 和m_y，求随机变量 X，
Y 的二阶混合中心矩。

---

$$ cov(X, Y) = E(XY) - E(X)E(Y) = m_1 - m_Xm_Y $$

---

## 1.16 ##

随机变量 X、Y 的联合概率密度为
$$ f_{XY}(x, y) = A\sin(x + y), 0\leqslant x, y\leqslant \dfrac{\pi }{2} $$
求：

### 1 ###

系数A ；

---

$$ \int\nolimits_{-\infty }^\infty f_{XY}(x, y) = 1 \rightarrow A = \dfrac{1}{2} $$

---

### 2 ###

数学期望 m_X，m_Y；

---

$$ f_X(x) = \int\nolimits_{-\infty }^\infty f_{XY}(x, y)\mathrm{d}y =
\dfrac{\sqrt{2}}{2}\sin(x + \dfrac{\pi }{4}) $$

$$ m_X = EX = \int\nolimits_{-\infty }^\infty xf_X(x)\mathrm{d}x = \dfrac{\pi }{4} $$

$$ X, Y对称 \rightarrow m_Y = m_X = \dfrac{\pi }{4} $$

---

### 3 ###

方差 σ_x^2和σ_y^2；

---

$$ EX^2 = \int\nolimits_{-\infty }^\infty t^2P(X = t)\mathrm{d}t = \dfrac{\pi^2 + 4\pi - 16}{8} $$
$$ \sigma_x^2 = DX = EX^2 - \left (EX\right )^2 = \dfrac{\pi^2 + 8\pi - 32}{16} $$
$$ X, Y对称 \rightarrow \sigma_Y^2 = \sigma_X^2 = \dfrac{\pi^2 + 8\pi - 32}{16} $$

---

### 4 ###

相关矩 R_{XY}及相关系数r_{XY} 。

---

$$ R_{XY} = E(XY) = \int\nolimits_{-\infty}^\infty
\int\nolimits_{-\infty}^\infty xyf_{XY}(x, y)\mathrm{d}x\mathrm{d}y = \dfrac{\pi - 2}{2} $$
$$ cov(X, Y) = E(XY) - EXEY = \dfrac{8\pi - \pi^2 - 16}{16} $$
$$ r_{XY} = \dfrac{cov(X, Y)}{\sqrt{DX}\sqrt{DY}} = \dfrac{8\pi - \pi^2 - 8}{8\pi + \pi^2 - 32} $$

---

## 1.17 ##

求随机变量 X 的特征函数，已知随机变量 X 的概率密度
$$ f_X(x) = 2\mathrm{e}^{-\alpha x}, x\geqslant 0 $$

---

$$ \int\nolimits_{-\infty}^\infty f_X(x)\mathrm{d}x = 1 \rightarrow \alpha = 2 \rightarrow f_X(x) = 2\mathrm{e}^{-2x}u(x) $$

$$ \hat{f}_X(\omega ) = \int\nolimits_{-\infty}^\infty f_X(x)\mathrm{e}^{\jmath \omega x}\mathrm{d}x =
\dfrac{2}{2 - \jmath \omega } $$

---

## 1.20 ##

已知互相独立随机变量 X_1 ,X_2 ,…,X_n 的特征函数，求 X_1 ,X_2 ,…,X_n 的线性组合
$$ Y = \sum_{i = 1}^n a_iX_i + c $$
的特征函数。a_i 和c 是常数。

---

$$ \hat{f}(\omega ) = E\mathrm{e}^{\jmath \omega Y} = \mathrm{e}^{\jmath \omega c}E\mathrm{e}^{\jmath \omega
\sum_{i = 1}^n a_iX_i} = \mathrm{e}^{\jmath \omega c}\prod_{i = 1}^n E\mathrm{e}^{\jmath \omega a_iX_i}  $$

---

## 1.22 ##

已知随机变量 X 的数学期望为零，方差为 1的高斯变量，求
$$ Y = aX^2 $$
的概率密度。

---

$$ x_{1, 2}(y) = \pm \sqrt{\dfrac{y}{a}} $$

$$ f(y) = \sum_{i = 1}^2 f_X\big(x_i(y)\big) \left | \dfrac{\mathrm{d}}{\mathrm{d}y}x_i(y) \right | = \dfrac{\mathrm{e}^{-\dfrac{y}{2a}}}{\sqrt{2\pi ay}} $$

---

## 1.24 ##

如果随机变量X服从 [0, 1] 区间的均匀分布，随机变量 Y 的概率密度为
$$ f_Y(y) = \left\{
\begin{matrix}
y, 0\leqslant y \leqslant 1\\
2 - y, 1\leqslant y \leqslant 2\\
0, 其他
\end{matrix}
\right.$$
X和Y互相独立。求X与Y之和的概率密度。

---

$$ f_X(x) = u(x) - u(x - 1) $$

$$ f(z) = f_X(x) * f_Y(y) = \dfrac{z^2}{2}\big(u(z) - u(z - 1)\big) + \dfrac{6z - 2z^2 - 3}{2}\big(u(z - 1) - u(z - 2)\big) + \dfrac{9 - 6z - z^2}{2}\big(u(z - 2) - u(z - 3)\big) $$

---

## 1.25 ##

若X为在 [0, 1] 区间上均匀分布的随机变量，求 X 的特征函数及所有原点矩。

---

$$ f_X(x) = u(x) - u(x - 1) $$

$$ \hat{f}(\omega ) = \int\nolimits_{-\infty}^\infty \mathrm{e}^{\jmath \omega x}f(x)\mathrm{d}x = \dfrac{\mathrm{e}^{\jmath \omega} - 1}{\jmath \omega } $$

$$ EX^n = \int\nolimits_{-\infty}^\infty x^nf(x)\mathrm{d}x = \dfrac{1}{n + 1} $$

---

