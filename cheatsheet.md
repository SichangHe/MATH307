<style>
* {
    line-height: 1 !important;
    margin-bottom: 0 !important;
    padding-top: 0 !important;
    padding-bottom: 0 !important;
}

h1, h2, h3, h4, h5, h6 {
    font-size: 1rem !important;
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
    font-size: 13px;
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

### de Moivre's formula

$$
(\cos\theta+i\sin\theta)^n=e^{in\theta}=\cos n\theta+i\sin n\theta
$$

## complex root

$$
z^n=z_0\\[12pt] ⇒
z_k=\sqrt[n]{r_0}e^{i \left(
    \frac{\theta_0+2\pi k}{n}
\right)},\qquad
k\in\{0,1,\cdots,n-1\}
$$

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

$u_x,u_y,v_x,v_y$ are continuous,
satisfy Cauchy-Riemann equations

### constancy from holomorphicity

$\bar f$ holomorphic in $D$ or
$|f|$ is constant

## Jordan curve theorem

simple closed contour separate $\mathbb C$ into
a bounded interior and
an unbounded exterior

### upper bound theorem for contour integral (ML theorem)

contour $C$ of length $L$,
$f(z)$ piecewise continuous on $C$,
$f(z)$ bounded by $M$

$$
⇒ \left|
    \int_Cf(z)\ dz
\right|≤ML
$$

- proof using lemma

    $$
    \left|\int_a^bz(t)\ dt\right|≤\int_a^b|z(t)|\ dt
    $$

    proof of lemma

    $$
    I:=∫_a^bw(t)\ dt=r_Ie^{i\theta_I}
    $$

    lemma hold for $I=0$.
    for $I≠0$

    $$
    r_I>0\\[12pt] ⇒
    r_I=\text{Re }\left(e^{-i\theta_I}∫_a^bw(t)\ dt\right)\\[12pt]=
    ∫_a^b\text{Re }\left(e^{-i\theta_I}w(t)\right)\ dt≤
    ∫_a^b\left|e^{-i\theta_I}w(t)\right|\ dt\\[12pt]=
    ∫_a^b|z(t)|\ dt
    $$

### path independence of contour integral

$f:D ⊆ \mathbb C → \mathbb C$ continuous in $D$

$∃$ antiderivative $F$ s.t. $∀\ C$ in $D$ from $z_1$ to $z_2$,
$\int_Cf(z)\ dz=F(z_2)-F(z_1)$

$⇔ ∀\ C$ closed,
$\oint_Cf(z)\ dz=0$

## Cauchy-Goursat theorem

on multiply connected domain $D ⊆ \mathbb C$,
positively oriented contour $C$,
negatively oriented contour $C_i$,
$C_i$ inside of and disjoint from $C$,
$f:D → \mathbb C$ holomorphic on $D$ and on the region between $C,C_i$

$$
⇒ ∫_Cf(z)\ dz+∫_{C_i}f(z)\ dz=0
$$

proof of Cauchy's theorem using Green's theorem and Cauchy-Riemann equations

$$
∫_Cf(z)\ dz=∫_C(u+iv)(dx+idy)=∫_C(u+iv)dx+(-v+iu)dy\\[12pt]=
\iint_D \left(
    \frac{∂}{∂x}(-v+iu)-\frac{∂}{∂y}(u+iv)
\right)dA\\[12pt]=
\iint_D(-v_x+iu_x-u_y+iv_y)dA=0
$$

## Cauchy's integral formula

$C$ positively oriented contour,
$f$ holomorphic inside and on $C$

$∀\ z_0$ inside $C$

$$
f(z_0)=\frac{1}{2\pi i}∫_C \frac{f(z)\ dz}{z-z_0},\quad
f'(z_0)=\frac{1}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^2}
$$

$$
f^{(n)}(z_0)=\frac{n!}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^{(n+1)}}
$$

$u,v$ have continuous partial derivative at all order

proof using upper bound theorem

$$
\left|∫_{C_R}\frac{f(z)-f(z_0)}{z-z_0}\ dz\right|=0
$$

### evaluating integral with Cauchy's integral formula

on positively oriented contour $C$,
evaluate integral
$I=∫_Cg(z)\ dz$

1. find $f(z),z_0$ s.t. $z_0$ inside $C$ and
    $g(z)=\frac{f(z)}{(z-z_0)^n}$

1. calculate $f^{(n-1)}(z_0)$
1. apply Cauchy's integral formula

    $$
    I=\frac{2\pi i}{(n-1)!}f^{(n-1)}(z_0)
    $$

## Morera's theorem

$f$ continuous on $D$,
$∀$ closed contour $C$,
$∫_Cf(z)\ dz=0$

$⇒ f$ holomorphic throughout $D$

## Liouville's theorem

bounded entire function is constant

## maximum modulus principle

non-constant holomorphic function $f$ on open $D$\
$⇒ |f|$ has no maximum on $D$

# Laurent series

annual domain $D$, $R_0<|z-z_0|<R_1$,
any closed contour $C$ in $D$,
function $f$ holomorphic in $D ⇒$

$$
f(z)=∑_{n=-∞}^∞ c_n(z-z_0)^n\\[12pt]
c_n=\frac{1}{2\pi i}∫_C \frac{f(z)\ dz}{(z-z_0)^{n+1}}
$$

## residue

$$
res\ f(z_0)=c_{-1}=\frac{1}{2\pi i}∫_Cf(z)\ dz
$$

### Cauchy residue theorem

positively oriented contour $C$,
$f$ analytic on and within $C$ *except* on finite number of singularities
$z_k,k\in\{1,2,\cdots,n\}$

$$
∫_Cf(z)\ dz=2\pi i∑_{k=1}^n res\ f(z_k)
$$

### residue at infinity

all singularity are inside negatively oriented contour $C$

$$
∫_Cf(z)\ dz=2\pi i\ res\ f(∞)
$$

- by replacing $z$ with $\frac{1}{z}$

    $$
    res \left(
        \frac{1}{z^2}f \left(
            \frac{1}{z}
        \right)
    \right)(0)=-res\ f(∞)
    $$

## isolated singularity

- $f$ has Laurent series about $z_0$

### pole

$∃\ m\in\N^+$ s.t. $∀\ n<-m,\ c_n=0$

- removable singularity $\Leftarrow m=0$,
    removed by setting $f(z_0)=c_0$

#### residue at pole

$$
m=1 ⇒ res\ f(z_0)=[(z-z_0)f(z)](z_0)
$$

$$
m=2 ⇒ res\ f(z_0)=\left\{
    \frac{d}{dz}[(z-z_0)^2f(z)]
\right\}(z_0)
$$

### zero of order $m$

$f$ analytic at $z_0$,
$∃\ m\in\N^+$ s.t.
$∀\ n<m,\quad f^{(n)}(z_0)=0$

#### zero and pole

$p,q$ analytic,
$q$ has zero of order $m$ at at $z_0$,
$p(z_0)≠0$

$⇒ \frac{p}{q}$ has pole of order $m$ at $z_0$

$$
m=1 ⇒ res\ \left[
    \frac{p}{q}
\right](z_0)=\frac{p(z_0)}{q'(z_0)}
$$

## Cauchy principal value $CPV$

$f$ is even $⇒$

$$
∫_{-∞}^∞ f(x)\ dx=CPV\ ∫_{-∞}^∞ f(x)\ dx=\lim_{R → ∞}∫_{-R}^R f(x)\ dx
$$

## Fourier integral

$$
∫_{-∞}^∞ f(x)\sin(kx)\ dx\quad\text{or}\quad
∫_{-∞}^∞ f(x)\cos(kx)\ dx,\quad
k>0
$$

consider instead
$f(z)e^{ikz}$

### Jordan's lemma

$f(z)$ analytic above the imaginary axis outside $|z|<R_0$,
semicircle contour $C_R:|z|=R>R_0,\ 0≤\theta≤\pi$

$$
|f(z)|(C_R)≤M_R,\quad \lim_{R → ∞}M_R=0\\[12pt]
⇒ ∀\ k>0,\ \lim_{R → ∞}∫_{C_R}f(z)e^{ikz}\ dz=0
$$

proof by parametric integral and Jordan's inequality

### lemma for indented path

$f$ analytic on $0<|z-x_i|<r$,\
clockwise upper semicircle $C_i:z=x_i+r_ie^{i\theta},\pi≥\theta≥0,r_i<r$,\
Laurent series of $f$ about $x_i$ contain *no even negative* power

proof by integrating Laurent series of parametric line integral term by term

$$
⇒ \lim_{r_i → 0}∫_{C_i}f(z)\ dz=-i\pi\ res\ f(x_i)
$$

- lemma hold at simple pole

## lemma for integral over branch point

circular segment of $C_r:z=re^{i\theta},0≤\theta≤\theta_1$,\
$f(z)$ continuous on $C_r ⇒$

$$
\lim_{z → 0}zf(z)=0\quad ⇒\quad \lim_{r → 0}∫_{C_r}f(z)\ dz=0
$$

proof by definition of limit and upper bound theorem

# trigonometric integral

$$
∫_{\theta_0}^{\theta_1}f(\sin\theta,\cos\theta)\ d\theta
$$

define $C:z=e^{i\theta},\theta_0≤\theta≤\theta_1$

$$
\sin\theta=\frac{z-z^{-1}}{2i},\quad
\cos\theta=\frac{z+z^{-1}}{2},\quad
d\theta=\frac{dz}{iz}\\[12pt] ⇒
∫_{\theta_0}^{\theta_1}f(\sin\theta,\cos\theta)\ d\theta=
∫_Cf \left(
    \frac{z-z^{-1}}{2i},
    \frac{z+z^{-1}}{2}
\right)\frac{dz}{iz}
$$

# Laplace transform

Laplace transform of $f:\R_0^+ → \R$

$$
\tilde f(s)=∫_0^∞ f(t)e^{-st}dt:\mathbb C → \mathbb C
$$

## Bromwich formula

inverse Laplace transform

$\gamma\in\R$ to the right of all sinularity of $\tilde f(s)$,
line contour $\Gamma_R$ from $\gamma-iR$ to $\gamma+iR$

$$
f(t)=\frac{1}{2\pi i}\lim_{R → ∞}∫_{\Gamma_R}\tilde f(s)e^{st}ds
$$

## theorem for meromorphic function

simple closed contour $C$,
$f$ non-zero and analytic on $C$, meromorphic within $C$

$$
\frac{1}{2\pi i}∫_C \frac{f'(z)}{f(z)} dz=Z-P
$$

## argument principle

$$
Z-P=\frac{1}{2\pi i}∫_C \frac{f'(z)}{f(z)} dz=
\frac{1}{2\pi}\Delta_C\arg f=\nu(\Gamma,0)
$$

## Rouché's theorem

$f,g$ analytic on and within $C$,
$|g|<|f|$ on $C$

$⇒f,f+g$ have the same number of zero counted with order inside $C$

## Brouwer's fixed point theorem

$D:|z|≤1,int\ D:|z|<1$,
$g:D → int\ D$ analytic

$⇒ ∃!\ z_0\in D$ s.t. $g(z_0)=z_0$ (fixed point)

- when changing $w$ continuously without crossing $\Gamma$,
    $\nu(\Gamma,w)$ is topological invariant

## Hopf's theorem

closed curve $\Gamma,\tilde\Gamma$,
one can be continuously deformed into another without crossing point $w$

$⇔ \nu(\Gamma,w)=\nu(\tilde\Gamma,w)$

## vector field index theorem

vector field $V:z\mapsto f(z)$,
simple closed contour $C$ enclose singularity $z_i, i=1,2,\cdots$ of $V$
with index $I_V(C_i) ⇒$

$$
I_V(C_i)=\nu(\Gamma,0)=Z-P=∑_iI_V(C_i)
$$

### vector field index

positively oriented contour $C_i$ enclose singularity $z_i$ of $V$

vector field index is integer number of rotation of $V$ traversing $C_i$

$$
I_V(C_i)=\nu(\Gamma_i,0)
$$

# Möbius transformation

$$
T(z)=\frac{az+b}{cz+d}:\bar{\mathbb C} → \bar{\mathbb C},\qquad
ad-bc≠0
$$

- only singularity is simple pole $-\frac{d}{c}$
- $$
    T^{-1}(w)=\frac{b-dw}{cw-a}
    $$

- $$
    T'(z)=\frac{ad-bc}{(cz+d)^2}≠0
    $$

- is composition of linear transformation and inversion

    $$
    f_1(z)=cz+d,\quad
    f_2(z)=\frac{1}{z},\quad
    f_3(z)=\frac{a}{c}-\frac{ad-bc}{c}z\\[6pt] ⇒
    T=f_1\circ f_2\circ f_3
    $$

## circle in Argand diagram

$$
Az\bar z+(B-iC)z+(B+iC)\bar z+D=0\\[12pt]
A,B,C,D\in\R
$$

## cross-ratio

$$
\frac{(w-w_1)(w_2-w_3)}{(w-w_3)(w_2-w_1)}=
\frac{(z-z_1)(z_2-z_3)}{(z-z_3)(z_2-z_1)}
$$

# conformal transformation

$f:D → \mathbb C$
analytic and
$∀\ z\in D,f'(z)≠0$

## inverse function theorem

analytic $f$ at $z_0$,
$f'(z_0)≠0$

$⇒ ∃\ U(z_0),∃!\ f^{-1}$ analytic

$$
(f^{-1})'(w)=\frac{1}{f'(z)}
$$

## conformal transformation preserve angle

proof by taking $f'(z_0)$ through $C_1$ and $C_2$ and their equality

## conformal transformation preserve harmonic

proof by constructing $f$ s.t. $\phi=Re\ f$

- $T(C)=k$ on smooth $C ⇒ \Phi(T(C))=k$

## maximum principle

simply connected $R$ bounded by simple closed $C$,
$\phi$ harmonic on $R$

$⇒ \phi$ attain extremum on boundary

proof by constructing $f$ s.t. $\phi=Re\ f$ and
using maximum modulus principle

## uniqueness of solution to Dirichlet problem

simply connected $R$ bounded by simple closed $C$

proof by assuming both $\phi_1,\phi_2$ are solutions and
arguing their difference is $0$ using maximum principle

# logarithm

$$
\log z=\ln r+i\theta\\[12pt]
$$

- $e^{\log z}=z$
- $\log e^z\not\equiv z$

$$
\frac{d}{dz}\log z=\frac{1}{z}
$$

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

- $\sin(iz)=i\sinh z,\quad\cos(iz)=\cosh z$

    $$
    ⇒ \sin z=\sin x\cosh y+i\cosh x\sin y\\[12pt]
    ⇒ |\sin z|^2=\sin^2x+\sinh^2y
    $$

# hyperbolic function

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

$$
\frac{d}{dz}\sin^{-1}z=\frac{1}{\sqrt{1-z^2}}\\[12pt]
\frac{d}{dz}\cos^{-1}z=-\frac{1}{\sqrt{1-z^2}}
$$

# Contour integral of power function on circle

$$
\int_{C_R}z^n\ dz=\begin{cases}
    0&n≠-1\\
    2\pi i&n=-1
\end{cases}
$$

## remainder

$$
\rho_N=S-S_N
$$

- $∑z_n$ converge $⇔ \lim_{N → ∞}\rho_N=0$

## power series

- $\sum_{n=0}^∞ c_n(z-z_0)^n$ converge to $S(z)$ for $z=z_1≠z_0$\
    $⇒$ absolutely convergent in circle $|z-z_0|<|z_1-z_0|$
- $S(z)$ is continuous function inside circle of convergence

### power series integration

$$
∫_Cg(z)S(z)\ dz=∑_{n=0}^∞ a_n ∫_Cg(z)(z-z_0)^ndz
$$
