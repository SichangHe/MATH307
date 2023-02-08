<style>
.markdown-preview.markdown-preview :not(span, code, pre) {
    font-family: Times New Roman;
}
.reveal.slide {
    font-size: 32px !important;
}
.reveal.slide p {
    text-align: left;
}
.reveal.slide ul {
    list-style: none;
    padding-inline-start: 0px;
    margin-left: 0px;
}
.reveal.slide li > p {
    padding-top: 0px;
    padding-bottom: 0px;
}
.proof-end:after {
    content: "□";
    font-size: 48px;
    float: right;
}
</style>

<!-- slide -->
# Proof for Cauchy-Riemann Equations and a Sufficient Condition for Differentiability

Group 2

Sichang He, Yidan Mao, Yue Wu

<!-- slide -->
# Credits

Sichang He:
write-up proof for the second theorem,
typeset and presentation of the middle part of the second theorem,
and edit for the slides.

Yidan Mao:
write-up proof for the first theorem,
and typeset and presentation of the first and last part of the second theorem.

Yue Wu:
typeset and presentation of the first theorem.

Reference:
Complex Variables and Applications, Ninth Edition,
by James Ward Brown and Ruel V. Churchill.

Slides made with Reveal.js in VSCode Markdown Preview Enhanced.

<!-- slide -->
# Cauchy-Riemann Equations

- <!-- .fragment -->
    Suppose $f^{\prime}(z)$ exists at $z_0=\left(x_0, y_0\right)$. Then, the first partial derivatives of $u$ and $v$ satisfy
- <!-- .fragment -->
    $$
    \frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}, \quad \frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}
    $$
- <!-- .fragment -->
    and $f^{\prime}\left(z_0\right)=\frac{\partial u}{\partial x}+\mathrm{i} \frac{\partial v}{\partial x}$, all evaluated at $\left(x_0, y_0\right)$.

<!-- slide -->
# Proof for Cauchy-Riemann Equations

- <!-- .fragment -->
    Suppose $z_0=x_0+iy_0$, $\Delta z=\Delta x+i\Delta y$, $f(z)=u(x,y)+iv(x,y)$,
    By the definition of complex differentiation,

- <!-- .fragment -->
    $$
    \begin{align*}
    f'(z_0)&=\lim\limits_{\Delta z\to\ 0} \frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}\\[18pt]
    &= \lim\limits_{(\Delta x, \Delta y)\to\ (0,0)} \frac{\begin{align*}
        &u(x_0+\Delta x, y_0+\Delta y)-u(x_0,y_0)\\
        &+i[v(x_0+\Delta x, y_0+\Delta y)-v(x_0,y_0)]
    \end{align*}}{\Delta x+i\Delta y}
    \end{align*}
    $$

- <!-- .fragment -->
    Since the limit exists at $z_0=(x_0,y_0)$, we can approach the limit from different directions and get the same result.

<!-- slide -->
- If we approach the limit horizontally, that is, let $\Delta y=0$,
    $$
    \begin{align*}
    f'(z_0)&=
    \lim\limits_{(\Delta x, \Delta y)\to\ (0,0)} \frac{\begin{align*}
        &u(x_0+\Delta x, y_0+\Delta y)-u(x_0,y_0)\\
        &+i[v(x_0+\Delta x, y_0+\Delta y)-v(x_0,y_0)]
    \end{align*} }{\Delta x+i\Delta y}\\[24pt]
    &=\lim\limits_{\Delta x\to\ 0}\frac{\begin{align*}
        &u(x_0+\Delta x,y_0)-u(x_0,y_0)\\
        &+i[v(x_0+\Delta x, y_0+\Delta y)-v(x_0,y_0)]
    \end{align*}}{\Delta x}
    \end{align*}
    $$

- <!-- .fragment -->
    Since the limit exists at $z_0=(x_0,y_0)$, we can take the limits of the real and imaginary parts to evaluate the limit.

<!-- slide -->
## Review

- <!-- .fragment -->
    Suppose that $f(z)=u(x,y)+iv(x,y), z=x+iy$ and
    $$
    z_0=x_0+iy_0, w_0=u_0+iv_0.
    $$
    Then,
- <!-- .fragment -->
    $$\lim_{z\to\ z_0}f(z)=w_0$$
    if and only if
    $$\lim_{(x,y)\to\ (x_0,y_0)}u(x,y)=u_0$$
    and
    $$ \lim_{(x,y)\to\ (x_0,y_0)} v(x,y)=v_0$$

<!-- slide -->
- Since the real part of the limit equals to the limit of the real part and the imaginary part of the limit equals to the limit of the imaginary part,

- <!-- .fragment -->
    $$
    \begin{align*}
    f'(z_0)&=
    \lim\limits_{\Delta x\to\ 0}\frac{\begin{align*}
        &u(x_0+\Delta x,y_0)-u(x_0,y_0)\\
        &+i[v(x_0+\Delta x, y_0+\Delta y)-v(x_0,y_0)]
    \end{align*}}{\Delta x}\\[18pt]
    &=\lim\limits_{\Delta x\to\ 0} \frac{u(x_0+\Delta x, y_0)-u(x_0,y_0)}{\Delta x}\\
    &\quad+ i\lim\limits_{\Delta x\to\ 0} \frac{v(x_0+\Delta x,y_0)-v(x_0,y_0)}{\Delta x}\\[12pt]
    &=u_x(x_0,y_0)+iv_x(x_0,y_0)
    \end{align*}
    $$
    (By the definition of partial derivatives)

<!-- slide -->
- Similarly, if we approach the limit vertically, that is, let $\Delta x=0$,
- <!-- .fragment -->
    $$
    \begin{align*}
    f'(z_0)&=\lim\limits_{(\Delta x, \Delta y)\to\ (0,0)} \frac{\begin{align*}
        &u(x_0+\Delta x, y_0+\Delta y)-u(x_0,y_0)\\
        &+i[v(x_0+\Delta x, y_0+\Delta y)-v(x_0,y_0)]
    \end{align*}}{\Delta x+i\Delta y}\\[18pt]
    &=\lim\limits_{\Delta y\to\ 0}\frac{\begin{align*}
        &u(x_0,y_0+\Delta y)-u(x_0,y_0)\\
        &+i[v(x_0, y_0+\Delta y)-v(x_0,y_0)]
    \end{align*}}{i\Delta y}
    \end{align*}
    $$
- <!-- .fragment -->
    Since the limit exists at $z_0=(x_0,y_0)$, we can take the limits of the real and imaginary parts to evaluate the limit.

<!-- slide -->
$$
\begin{align*}
f'(z_0)&=\lim\limits_{\Delta y\to\ 0}\frac{\begin{align*}
    &u(x_0+,y_0+\Delta y)-u(x_0,y_0)\\
    &+i[v(x_0, y_0+\Delta y)-v(x_0,y_0)]
\end{align*}}{i\Delta y}\\[18pt]
&=\lim\limits_{\Delta y\to\ 0} \frac{u(x_0, y_0+\Delta y)-u(x_0,y_0)}{i\Delta y}\\&\quad+i\lim\limits_{\Delta y\to\ 0} \frac{v(x_0,y_0+\Delta y)-v(x_0,y_0)}{i\Delta y}\\[12pt]
&=v_y(x_0 , y_0)-iu_y(x_0,y_0)
\end{align*}
$$
(By the definition of partial derivatives)

<!-- slide -->
Since
$$
f'(z_0)=u_x(x_0,y_0)+iv_x(x_0,y_0)
$$
and
$$
f'(z_0)=v_y(x_0,y_0)-iu_y(x_0,y_0),
$$

- <!-- .fragment .proof-end -->
    $$
    u_x(x_0,y_0)=v_y(x_0,y_0), v_x(x_0,y_0)=-u_y(x_0,y_0),
    $$

    which is a necessary condition for the existence of $f'(z_0)$.

<!-- slide -->
# Proof for a sufficient condition for differentiability

<!-- slide -->
## Conditions given

- $f(z)=u(x, y)+\mathrm{i} v(x, y)$ is defined.
- <!-- .fragment data-fragment-index="1" -->
    $∀\ z\in U_\varepsilon\left(z_0\right)$,
    $u_x,u_y,v_x,v_y$ exist and are continuous.
- <!-- .fragment data-fragment-index="2" -->
    Cauchy-Riemann equations are satisfied:

    $$
    u_x=v_y,\quad
    u_y=-v_x.
    $$

<div class="fragment" data-fragment-index="3">

## Want to prove

$f'(z_0)$ exists and

$$
f'(z_0)=u_x(x_0,y_0)+iv_x(x_0,y_0).
$$
</div>

<!-- slide -->
## Analyzing the problem

- <!-- .fragment -->
    Continuity of partial derivatives implies
    $$\lim\limits_{(x, y) \to (x_0, y_0)} {u_x(x, y)} = u_x(x_0, y_0)$$
    $$\lim\limits_{(x, y) \to (x_0, y_0)} {u_y(x, y)} = u_y(x_0, y_0)$$
    $$\lim\limits_{(x, y) \to (x_0, y_0)} {v_x(x, y)} = v_x(x_0, y_0)$$
    $$\lim\limits_{(x, y) \to (x_0, y_0)} {v_y(x, y)} = v_y(x_0, y_0)$$

<!-- slide -->
- By the definition of limit of a function of two variables, this is to say,

- <!-- .fragment -->
    $\forall\ \varepsilon > 0$, $\exists$ $\delta > 0$, such that
    $$
    |u_x(x, y)-u_x(x_0, y_0)|< \varepsilon
    $$
    whenever $|(x-x_0)^2+(y-y_0)^2|<\delta$.

- <!-- .fragment -->
    Similar definition applies to other three limits as well.

<!-- slide -->
- To prove $f'(z_0) = u_x(x_0, y_0) + i v_x(x_0, y_0)$, by the definition of derivative of complex-valued functions, is equivalent to prove
- <!-- .fragment -->
    $$
    \lim\limits_{\Delta z \to 0} {\frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}} = u_x(x_0, y_0) + i v_x(x_0, y_0)
    $$
- <!-- .fragment -->
    is equivalent to prove
    $\forall\ \varepsilon > 0$, $\exists$ $\delta > 0$, such that
    $$
    \left|
        \frac{f(z_0+\Delta z)-f(z_0)}{\Delta z} - (u_x(x_0, y_0) + i v_x(x_0, y_0))
    \right|< \varepsilon
    $$
    whenever $|z-z_0|<\delta$.

<!-- slide -->
## Proof

- <!-- .fragment -->
    Let $\varepsilon>0$ be given.

    $$
    A:=u_x(x_0,y_0),\quad
    B:=v_x(x_0,y_0),\quad
    \Delta z:=\Delta x+i\Delta y
    $$

- <!-- .fragment -->
    $$
    \begin{align*}
    \Delta w&:=f(z_0+\Delta z)-f(z_0)\\[6pt]&=
    u(x_0+\Delta x,y_0+\Delta y)+iv(x_0+\Delta x,y_0+\Delta y)\\&\qquad-
    (u(x_0,y_0)+iv(x_0,y_0))\\[6pt]&=
    \underbrace{(u(x_0+\Delta x,y_0+\Delta y)-u(x_0,y_0))}_{\Delta u}\\&\qquad+
    i\underbrace{(v(x_0+\Delta x,y_0+\Delta y)-v(x_0,y_0))} _{\Delta v}\\[6pt]&=:
    \Delta u+i\Delta v
    \end{align*}
    $$

<!-- slide -->
$$
\begin{align*}
\Delta u&=\underbrace{
    u(x_0+\Delta x,y_0+\Delta y)-u(x_0+\Delta x,y_0)
}_{\Delta\theta}\\&\qquad+
\underbrace{
    u(x_0+\Delta x,y_0)-u(x_0,y_0)
} _{\Delta\phi}
\end{align*}
$$

- <!-- .fragment -->
    $$
    \begin{align*}
    \Delta v&=\underbrace{
        v(x_0+\Delta x,y_0+\Delta y)-v(x_0+\Delta x,y_0)
    }_{\Delta\eta}\\&\qquad+
    \underbrace{
        v(x_0+\Delta x,y_0)-v(x_0,y_0)
    } _{\Delta\mu}
    \end{align*}
    $$

<!-- slide -->
- $$
    \theta(y):=u(x_0+\Delta x,y)\\[12pt] ⇒
    \Delta\theta=
    \theta(y_0+\Delta y)-\theta(y_0)\\[12pt]
    \theta'(y)=u_y(x_0+\Delta x,y)
    $$

- <!-- .fragment -->
    By Mean Value Theorem, $∃\ y_1$ between $y_0+\Delta y$ and $y_0$ such that

    $$
    \theta'(y_1)=\frac{\theta(y_0+\Delta y)-\theta(y_0)}{\Delta y}
    $$

- <!-- .fragment -->
    $$
    ⇒ u_y(x_0+\Delta x,y_1)=\frac{\Delta\theta}{\Delta y}
    $$

<!-- slide -->
- $u_y$ is continuous at $z_0 ⇒$
- <!-- .fragment -->
    $∃\ \delta_1>0$ such that

    $$
    \left|
        u_y(x_0+\Delta x,y_0+\Delta y)-u_y(x_0,y_0)
    \right|<\frac{\varepsilon}{4}\\[6pt]
    \text{whenever }\sqrt{(\Delta x)^2+(\Delta y)^2}<\delta_1.
    $$

- <!-- .fragment -->
    $$
    y_1-y_0≤\Delta y ⇒
    \sqrt{(\Delta x)^2+(y_1-y_0)^2}<\delta_1
    $$

- <!-- .fragment -->
    $$
    ⇒ \left|
        u_y(x_0+\Delta x,y_1)-u_y(x_0,y_0)
    \right|<\frac{\varepsilon}{4}\\[12pt] ⇒
    \left|
        \frac{\Delta\theta}{\Delta y}+v_x(x_0,y_0)
    \right|<\frac{\varepsilon}{4} ⇒
    \left|
        \frac{\Delta\theta}{\Delta y}+B
    \right|<\frac{\varepsilon}{4}
    $$

<!-- slide -->
$$
\phi(x):=u(x,y_0)\\[12pt] ⇒
\Delta\phi=
\phi(x_0+\Delta x)-\phi(x_0)\\[12pt]
\phi'(x)=u_x(x,y_0)
$$

By Mean Value Theorem, $∃\ x_1$ between $x_0+\Delta x$ and $x_0$ such that

$$
\phi'(x_1)=\frac{\phi(x_0+\Delta x)-\phi(x_0)}{\Delta x}\\[12pt] ⇒
u_x(x_1,y_0)=\frac{\Delta\phi}{\Delta x}
$$

<!-- slide -->
$u_x$ is continuous at $z_0 ⇒ ∃\ \delta_2>0$ such that

$$
\left|
    u_x(x_0+\Delta x,y_0+\Delta y)-u_x(x_0,y_0)
\right|<\frac{\varepsilon}{4}\\[6pt]
\text{whenever }\sqrt{(\Delta x)^2+(\Delta y)^2}<\delta_2.\\[12pt]
x_1-x_0≤\Delta x\\[12pt] ⇒
\sqrt{(x_1-x_0)^2+0^2}<\delta_2\\[12pt] ⇒
\left|
    u_x(x_1,y_0)-u_x(x_0,y_0)
\right|<\frac{\varepsilon}{4}\\[12pt] ⇒
\left|
    \frac{\Delta\phi}{\Delta x}-A
\right|<\frac{\varepsilon}{4}
$$

<!-- slide -->
Similarly, for $\Delta\eta$ and $\Delta\mu$:

$∃\ \delta_3>0$ such that

$$
\sqrt{(\Delta x)^2+(\Delta y)^2}<\delta_3\\[6pt] ⇒
\left|
    \frac{\Delta\eta}{\Delta y}-v_y(x_0,y_0)
\right|=
\left|
    \frac{\Delta\eta}{\Delta y}-u_x(x_0,y_0)
\right|=
\left|
    \frac{\Delta\eta}{\Delta y}-A
\right|<\frac{\varepsilon}{4}
$$

$∃\ \delta_4>0$ such that

$$
\sqrt{(\Delta x)^2+(\Delta y)^2}<\delta_4\\[6pt] ⇒
\left|
    \frac{\Delta\mu}{\Delta x}-v_x(x_0,y_0)
\right|=
\left|
    \frac{\Delta\mu}{\Delta x}-B
\right|<\frac{\varepsilon}{4}
$$

<!-- slide -->
- Choose $\delta = \min \left\{ \delta_1, \delta_2, \delta_3, \delta_4 \right\}$, then whenever $\sqrt{(\Delta x)^2+(\Delta y)^2}<\delta$,
- <!-- .fragment -->
    $$
    \begin{align*}
    &\left|
        \frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}-(u_x(x_0, y_0) + i v_x(x_0, y_0))
    \right|\\[6pt]
    =&\left|
        \frac{\Delta u +i \Delta v}{\Delta x + i \Delta y} - (A+i B)
    \right|\\[6pt]
    =&\left|
        \frac{\Delta u +i \Delta v -A\Delta x - iA\Delta y -iB\Delta x +B\Delta y}{\Delta x + i \Delta y}
    \right|\\[6pt]
    =&\left|
        \frac{\Delta \theta + \Delta \phi +i (\Delta \eta+ \Delta \mu) -A\Delta x - iA\Delta y -iB\Delta x +B\Delta y}{\Delta x + i \Delta y}
    \right|\\[6pt]
    =&\left|
        \frac{(\Delta \theta +B\Delta y) +(\Delta \phi -A\Delta x) +i (\Delta \eta- A\Delta y) +i (\Delta \mu -B\Delta x) }{\Delta x + i \Delta y}
    \right|\\[6pt]
    =&\frac{\left|
        \Delta y (\frac{\Delta \theta}{\Delta y} +B) + \Delta x(\frac{\Delta \phi}{\Delta x} -A) +i \left(
            \Delta y(\frac{\Delta \eta}{\Delta y}- A) +\Delta x(\frac{\Delta \mu}{\Delta x} -B)
        \right)
    \right|}{|\Delta x + i\Delta y|}\\[12pt]
    \end{align*}
    $$

<!-- slide -->
- $$
    \left|
        \frac{f(z_0+\Delta z)-f(z_0)}{\varepsilon z}-(u_x(x_0, y_0) + i v_x(x_0, y_0))
    \right|\qquad\qquad\qquad
    $$
- <!-- .fragment -->
    $$
    \begin{align*}
    ≤&\frac{\left|
        \Delta y (\frac{\Delta \theta}{\Delta y} +B) + \Delta x(\frac{\Delta \phi}{\Delta x} -A)
    \right| + \left|
        \Delta y(\frac{\Delta \eta}{\Delta y}- A) +\Delta x(\frac{\Delta \mu}{\Delta x} -B)
    \right|}{|\Delta z|}\\[12pt]
    ≤&\frac{|\Delta y|\left|
         \frac{\Delta \theta}{\Delta y} +B
    \right|+ |\Delta x|\left|\frac{\Delta \phi}{\Delta x} -A
    \right| + |\Delta y|\left|
        \frac{\Delta \eta}{\Delta y}- A\right| +|\Delta x|\left|
        \frac{\Delta \mu}{\Delta x} -B
    \right|}{|\Delta z|}\\[12pt]
    <&\frac{
        \frac{\varepsilon}{4}|\Delta y| + \frac{\varepsilon}{4}|\Delta x| + \frac{\varepsilon}{4}|\Delta y| +\frac{\varepsilon}{4}|\Delta x|
    }{|\Delta z|}\\[6pt]
    =&\frac{\varepsilon}{2}\frac{|\Delta y| + |\Delta x|}{|\Delta z|}\\[6pt]
    ≤&\frac{\varepsilon}{2}\frac{|\Delta z| + |\Delta z|}{|\Delta z|}
    = \varepsilon
    \end{align*}
    $$

<!-- slide -->
- Now we have proved $\forall\ \varepsilon > 0$, $\exists$ $\varepsilon > 0$, such that
    $$
    \left|
        \frac{f(z_0+\Delta z)-f(z_0)}{\varepsilon z}-(u_x(x_0, y_0) + i v_x(x_0, y_0))
    \right|<\varepsilon
    $$
    whenever $|z-z_0|<\delta$.

- <!-- .fragment .proof-end -->
    That is to say $f'(z_0)$ exists and $f'(z_0)=u_x(x_0,y_0)+iv_x(x_0,y_0)$.

<!-- slide -->
# Theorems today

Suppose $f^{\prime}(z)$ exists at $z_0=\left(x_0, y_0\right)$. Then, the first partial derivatives of $u$ and $v$ satisfy
$$
\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}, \quad \frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}
$$
and $f^{\prime}\left(z_0\right)=\frac{\partial u}{\partial x}+\mathrm{i} \frac{\partial v}{\partial x}$, all evaluated at $\left(x_0, y_0\right)$.

---

$f(z)=u(x, y)+\mathrm{i} v(x, y)$ is defined.
$∀\ z\in U_\varepsilon\left(z_0\right)$,
$u_x,u_y,v_x,v_y$ exist and are continuous.
Cauchy-Riemann equations are satisfied.

Then, $f'(z_0)$ exists and

$$
f'(z_0)=u_x(x_0,y_0)+iv_x(x_0,y_0).
$$
