# Ch 01 - 信号与系统

## 基本运算

- 加减运算（叠加）：$f_1(t)+f_2(t)$
- 乘法运算（信号互乘）：$f_1(t)f_2(t)$
- 标量乘法（数乘）：$af_1(t)$
- 平移变换：$x(t \pm t_0)$（左加右减）
- 对称反转：$x(-t)$（以$t=0$为轴）
- 水平尺度变换（连续信号）：$x(at)$，$a>1$缩窄，$a<1$展宽
- 水平尺度变换（离散信号）：缩窄：丢去信号；展宽：内插信号

## 常用特性

- 奇偶性：$x(t)=x(-t)$，$-x(t)=x(-t)$
- **奇偶分解**：$x_o(t)=\frac{1}{2}[x(t)-x(-t)]$，$x_e(t)=\frac{1}{2}[x(t)+x(-t)]$
- 周期性：$x(t)=x(t+mT),m=0,\pm 1,...$，最小正周期（基波周期）$T_0$

## 欧拉公式

$x(t)={\rm e}^{{\rm j}x}=\cos x+{\rm j}\sin x$

$\Rightarrow \sin \Omega t=\frac{1}{2{\rm j}}({\rm e}^{{\rm j}\Omega t} - {\rm e}^{-{\rm j}\Omega t}),\quad \cos\Omega t=\frac{1}{2}({\rm e}^{{\rm j}\Omega t} + {\rm e}^{-{\rm j}\Omega t}),$

## 谐波

一组周期性复指数信号

- 连续：$\Phi_k(t)=\{{\rm e}^{{\rm j}k\Omega_0 t}\}$，$\Omega_0$ 为基波周期
- 离散：$\Phi_k(n)=\{{\rm e}^{{\rm j}2\pi nk/N}\}$，$N$ 为基波周期

## 基本信号

- 单位冲激（Unit Impulse）

  - 连续：$\delta(t)$

    $\int_{-\infin}^{+\infin}\delta(t){\rm d}t=1$，$\delta(t)=0~(t\neq 0)$（狄利克雷函数）

    $\delta(t)=\delta(-t)$

    $\delta(at)=\frac{1}{|a|}\delta(t)$

    $\delta(t)=\frac{{\rm d}}{{\rm d}t}u(t)$（微分特性）

    冲击偶积分 $\int_{-\infin}^{+\infin}t\delta'(t){\rm d}t=-1$

  - 离散：$\delta(n)=1~(n=0), 0~(n\ne0)$

    $x(n)\delta(n)=x(0)\delta(n)$（取样特性）

    $x(n)\delta(n-m)=x(m)\delta(n-m)$（取样特性）

    $\delta(n)=u(n)-u(n-1)$

    $\sum_{k=0}^{\infin}\delta(n-k)=u(n)$

- 单位阶跃

  - 连续：$u(t)=1~(t>0),0~(t<0)$

    $x(t)u(t)=x(t)~(t>0),0~(t<0)$（单边化）

    $u(t)-u(t-\tau)$（脉冲分解）

  - 离散：$u(n)=1~(n\ge 0),0~(t<0)$

## 系统的基本单元

- 放大器：$y(t)=ax(t)$
- 积分器：$y(t)=\int_{-\infin}^tx(\tau){\rm d}\tau$
- 延迟器：$y(t)=x(t-T)$
- 加法器
- 乘法器
- 移序器：$y(n)=x(n-1)$

## 系统的性质

- 可逆性：$H \leftrightarrow H^{-1}$
- 因果性：某时刻的输出只取决于当前和以前的输入，而不取决于将来的输入
- 时不变：$x(t-t_0) \leftrightarrow y(t-t_0)$
- 线性：$ax_1+bx_2 \leftrightarrow ay_1+by_2$
- 稳定性：$|y(n)|$ 有界