# Ch 09 - $z$ 变换

## $z$ 变换

$$
X(z)=\sum_{n=-\infty}^{+\infty}x(n)z^{-n}\\
x(n)=\frac{1}{2\pi {\rm j}}\oint_C X(z)z^{n-1}{\rm d}z
$$

围线积分在 $X(z)$ 的 ROC 内绕逆时针。

### 收敛域

存在的前提是 $X(z)$ 绝对可和。收敛域内不含极点。

- 有限长序列

  $X(z)=\sum_{n=n_1}^{n_2}$