<style>
* {
    line-height: 1 !important;
    margin-bottom: 0 !important;
    padding-top: 0 !important;
    padding-bottom: 0 !important;
    font-size: 12.2px;
}

:not(.newline) {
    margin-top: 0 !important;
}

main, div, section {
    margin: 0 !important;
    padding: 0 !important;
}

:not(span, code, pre) {
    font-family: Arial !important;
}

main {
    display: block !important;
}

a.anchor {
    display: none;
}

section.markdown-body {
    column-count: 3;
    column-gap: 0;
}
</style>

- $x=\frac{z+\bar z}{2},\quad y=\frac{z-\bar z}{2i}$
- $|z|^2=z\bar z$
- $\bar z=re^{-i\theta}$

### de Moivre's formula

$$
(\cos\theta+i\sin\theta)^n=e^{in\theta}=\cos n\theta+i\sin n\theta
$$

## complex root

$z_0=r_0e^{i\theta_0}$

$n$th root of $z_0$

$$
z^n=z_0\\[12pt] ⇒
z_k=\sqrt[n]{r_0}e^{i \left(
    \frac{\theta_0+2\pi k}{n}
\right)},\qquad
k\in\{0,1,\cdots,n-1\}
$$

# differentiation

- $f(z)$ depend on $\bar z ⇒ f$ not differentiable
- $u,v$ differentiable $\not ⇒ f$ differentiable

## Cauchy-Riemann equations

$$
u_x=v_y,\quad
u_y=-v_x,\quad
f'=u_x+iv_x
$$

$$
ru_r=v_\theta,\quad
u_\theta=-rv_r,\quad
f'=e^{-i\theta}(u_r+iv_r)
$$

### differentiability from Cauchy-Riemann equations

1. $u_x,u_y,v_x,v_y$ are continuous
1. satisfy Cauchy-Riemann equations

$$
⇒ f'=u_x+iv_x
$$

### constancy from holomorphicity

$f$ holomorphic, in $D$

$f$ is constant

$⇔ f'=0$

$⇔ \bar f$ holomorphic in $D$

$⇔ |f|$ is constant

# harmonic function

$h:D ⊆ \R^2 → \R$ with continuous second partial derivative

$$
h_{xx}+h_{yy}=0
$$

## parametric derivative

$x'(t),y'(t)$ continuous

$⇒ C$ differentiable,

$$
z'(t)=x'(t)+iy'(t)
$$

## parametric integral

- both real part and imaginary part commute
- mean value theorem of integral fail

### parametric curve length

$$
L(C)=∫_a^b\sqrt{x'(t)^2+y'(t)^2}\ dt=∫_a^b|z'(t)|\ dt
$$

# contour

piecewise smooth curve $C$ joined from finite smooth parametric curve

- $z$ continuous
- $z'$ piecewise continuous

## Jordan curve theorem

simple closed contour separate $\mathbb C$ into

1. a bounded interior
1. an unbounded exterior

## contour integral

$$
\int_Cf(z)\ dz=\int_a^bf(z(t))\ z'(t)\ dt
$$

- independent of parametrization

### upper bound theorem (ML theorem)

contour $C$ of length $L$,\
$f(z)$ piecewise continuous on $C$,\
$f(z)$ bounded by $M$

$$
⇒ \left|
    \int_Cf(z)\ dz
\right|≤ML
$$

### path independence of contour integral

$f:D ⊆ \mathbb C → \mathbb C$ continuous in $D$

$∃$ antiderivative $F$ s.t. $∀\ C$ in $D$ from $z_1$ to $z_2$

$$
\int_Cf(z)\ dz=F(z_2)-F(z_1)
$$

$⇔ ∀\ C$ closed,

$$
\oint_Cf(z)\ dz=0
$$

## Cauchy-Goursat theorem

on $D ⊆ \mathbb C$,\
simple closed contour $C$ in $D$,\
$f:D → \mathbb C$ holomorphic on and within $C$

$$
⇒ \int_Cf(z)\ dz=0
$$

- on simply connected domain, $C$ need not be simple

### path deformation principle

positively oriented simple closed contour $C_1,C_2$,\
$f$ holomorphic between $C_1,C_2$

$$
⇒ ∫_{C_1}f(z)\ dz=∫_{C_2}f(z)\ dz
$$

## Cauchy's integral formula

$C$ positively oriented simple closed contour,\
$f$ holomorphic inside and on $C$

$∀\ z_0$ inside $C$

$$
f^{(n)}(z_0)=\frac{n!}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^{(n+1)}}
$$

- $f$ holomorphic $⇒ u,v$ have continuous partial derivative at all order

proof:
show using upper bound theorem

$$
\left|∫_{C_R}\frac{f(z)-f(z_0)}{z-z_0}\ dz\right|=0
$$

### evaluating integral with Cauchy's integral formula

on positively oriented simple closed contour $C$,
evaluate integral

$$
I=∫_Cg(z)\ dz
$$

1. find $f(z),z_0$ s.t. $z_0$ inside $C$ and

    $$
    g(z)=\frac{f(z)}{(z-z_0)^n}
    $$

1. calculate $f^{(n-1)}(z_0)$
1. apply Cauchy's integral formula

    $$
    I=\frac{2\pi i}{(n-1)!}f^{(n-1)}(z_0)
    $$

## Morera's theorem

$f$ continuous on $D$

$∀$ closed contour $C$

$$
∫_Cf(z)\ dz=0
$$

$⇒ f$ holomorphic throughout $D$

## Liouville's theorem

bounded entire function is constant

## fundamental theorem of algebra

non-constant polynomial of degree $n$ has $n$ root

## maximum modulus principle

non-constant holomorphic function $f$ on open $D$\
$⇒ |f|$ has no maximum on $D$

- for $f$ on $D\cup ∂D$,
    $|f|$ reach maximum always on $∂D$,
    never on interior

<div style="break-after: page;"></div>

# logarithm

$$
\text{Log }z=\ln r+i\Theta
$$

- $e^{\log z}=z,\log e^z\not\equiv z$
- $\log z_1z_2=\log z_1+\log z_2,
    \text{Log }z_1z_2\not\equiv\text{Log }z_1+\text{Log }z_2$

# exponential

$$
e^z=e^xe^{iy}=e^x\cos y+ie^x\sin y
$$

- periodic, $e^{z+i2\pi k}=e^z$
- $(z_1z_2)^c\not\equiv z_1^cz_2^c$

$$
\frac{d}{dz}c^z=c^z\text{Log }c
$$

# trigonometric function

$$
\sin z=\frac{e^{iz}-e^{-iz}}{2i},\quad
\cos z=\frac{e^{iz}+e^{-iz}}{2}
$$

- $\sin(iz)=i\sinh z,\quad\cos(iz)=\cosh z$

    $$
    ⇒ \sin z=\sin x\cosh y+i\cos x\sinh\\[12pt]
    ⇒ |\sin z|^2=\sin^2x+\sinh^2y\\[12pt]
    ⇒ \sin z=0 ⇔ z=\pi k,k\in\Z
    $$

# hyperbolic function

$$
\sinh z=\frac{e^z-e^{-z}}{2},\quad
\cosh z=\frac{e^z+e^{-z}}{2}
$$

- $\sinh(iz)=i\sin z$

    $$
    ⇒ |\sinh z|^2=|i\sin(y-ix)|=\sinh^2x+\sin^2y\\[12pt]
    ⇒ \sinh z=0 ⇔ z=i\pi k,k\in\Z
    $$

# inverse trigonometric function

$$
\sin^{-1}z=-i\log \left(
    iz+\sqrt{1-z^2}
\right)\\
\cos^{-1}z=-i\log \left(
    z+i\sqrt{1-z^2}
\right)
$$

- $\log,\sqrt{}$ are multi-valued
- holomorphic in branch

## derivative of inverse trigonometric function

$$
\frac{d}{dz}\sin^{-1}z=\frac{1}{\sqrt{1-z^2}}\\[12pt]
\frac{d}{dz}\cos^{-1}z=-\frac{1}{\sqrt{1-z^2}}
$$

# Contour integral of power function on circle

$$
\int_{C_R}z^n=\begin{cases}
    0&n≠-1\\
    2\pi i&n=-1
\end{cases}
$$
