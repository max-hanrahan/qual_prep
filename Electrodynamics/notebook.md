# This is my (humble) attempt to digitally recreate the notes of Hamilton College professor Kate Brown.

## Prof. Brown encouraged us to keep a notebook "as a record of our leraning". 
So strongly, in fact, that it was worth 25% of our grades. As such, this is the neatest documentation of physics I've ever done. I'm committing it here on GitHub to hold myself accountable, as part of studying for my qualification exam. 

# (Basically) The Greatest Story Ever Told
## (at least according to KB)

Review:

* wave equation
* structure and content of Maxwell's Equations
    * vector fields
    * Maxwell's Equations themselves
* **¡Fiat Lux, mi amigo!**

WAVE EQUATION: 2nd order PDE in space & time:

1D wave equation ("1 + 1") = one spacial dimension $x$ and temporal dimension $t$. 

$$
\frac{1}{v^2} \frac{\partial ^2 f}{\partial t^2} = \frac{\partial ^2 f}{\partial x^2}$$

$f = f(x, t)$, where $v $ = speed = $dx/dt$. 

But in 2D + 1 time: $f = f(x, y, t)$

$$ \frac{\partial ^2 f}{\partial x^2} + \frac{\partial ^2 f}{\partial y^2} = \frac{1}{v^2} \frac{\partial ^2 f}{\partial t^2} $$

DEF: A "wave" is anything that satisfies the wave equation. 

and in 3D: $f = f(x, y, z, t)$

$$ \frac{\partial ^2 f}{\partial x^2} + \frac{\partial ^2 f}{\partial y^2} + \frac{\partial ^2 f}{\partial z^2} = \frac{1}{v^2} \frac{\partial ^2 f}{\partial t^2} $$

Vector fields are lots of info, and hard to draw. The good news is that they're easy to write mathematically:

$$ \mathbf v = v_x \hat x + v_y \hat y + v_z\hat z = v_x \hat i + v_y \hat j + v_z \hat k$$ 

but $v_x$ can, say, depend on $x$, $y$, and $z$. 

The above is all in Cartesian coordinates. 

Spherical:
$$\mathbf v = v_r \hat r + v_\theta \hat \theta + v_\phi \hat \phi$$

Cylindrical: $(r, \phi, z)$ or $(s, \phi, z)$.

$$\mathbf v = v_r \hat r + v_\phi \hat \phi + v_z \hat z$$

Q: So how do we express vector fields mathematically? Or rather, how are they determined?
A: Vector fields are determined by only two features: `div` and `curl`. 

* Divergence: how much the field is radiating to/from a point, given by $\mathbf \nabla \cdot \mathbf v$
* Curl: how mych the field is circulating about a point given by $\mathbf \nabla \times \mathbf v$.

So if you tell me the `div` and `curl` of a vector field, I can reconstruct it all!

Caveat: boundary conditions. 

Maxwell's Equations: these specify div, curl of $\mathbf E$, $\mathbf B$!

$$\mathbf \nabla \cdot \mathbf E = \rho / \varepsilon_0$$

$$\mathbf \nabla \times \mathbf E = -\frac{\partial \mathbf B}{\partial t}$$

$$\mathbf \nabla \cdot \mathbf B = 0$$

$$\mathbf \nabla \times \mathbf B = \mu_0 \mathbf J+\mu_0 \varepsilon_0 \frac{\partial \mathbf E}{\partial t}$$

Comments: "sources" usally refer to $\mathbf \rho$ and $\mathbf J$.

* $\rho$ = source of electric charge ("charged stuff")

    $\rho$ and $\varepsilon_0$ together are sources of electric phenomena

* $\mathbf J$ = source of magnetic field, or current(moving charge)

    $\mu_0$ and $\mathbf J$ together are sources of magnetic phenomena

In general, for these PDE's:

[Derivatives on LHS] = "source". (can be 0)

Source free $\implies$ $\mathbf \rho = \mathbf J = \mathbf 0$ in the Gaussian surface (no charges/current).

## Corrections to Maxwell's Equations:

In statics $\mathbf \nabla \times \mathbf E = 0$, but $\mathbf \nabla \times \mathbf E = -\frac{\partial \mathbf B}{\partial t}$ is **FARADAY'S CORRECTION**

Faraday conjectured that the above is true. 

$$\mathbf \nabla \times \mathbf B = \mu_0 \mathbf J+\mu_0 \varepsilon_0 \frac{\partial \mathbf E}{\partial t}$$

The second term here (sadly can't use underbrace) is Maxwell's law/correction. 

Ampere's law, without this correction, is $\mathbf \nabla \times \mathbf B = \mu_0 \mathbf J$.

Source free regime of Maxwell's Equations (where $\mathbf \rho = \mathbf J = 0$):

$$\mathbf \nabla \cdot \mathbf E = 0$$

$$\mathbf \nabla \times \mathbf E = -\frac{\partial \mathbf B}{\partial t}$$

$$\mathbf \nabla \cdot \mathbf B = 0$$

$$\mathbf \nabla \times \mathbf B = \mu_0 \varepsilon_0 \frac{\partial \mathbf E}{\partial t}$$

These are Maxwell's EQ'ns in a vaccuum. 

Start with Eq 11, inside cover of Griffiths:

$$\mathbf \nabla \times (\mathbf \nabla \times \mathbf A) = \mathbf \nabla (\mathbf \nabla \cdot \mathbf A) - \nabla ^2 \mathbf A$$ 
(equation 11). 

Thus, 

$$\mathbf \nabla \times (\mathbf \nabla \times \mathbf E) = \nabla (\mathbf \nabla \cdot \mathbf E) - \nabla ^2 \mathbf E$$ 

$$
\nabla \times \left(- \frac{\partial \mathbf B}{\partial t}\right) = \mathbf \nabla (0) - \nabla^2 \mathbf E \text{ by $\rho=0$ (source-free regime)}
$$

$$
\mathbf \nabla \times \left(- \frac{\partial \mathbf B}{\partial t}\right) = - \nabla ^2 \mathbf E
$$

$$
-\frac{\partial }{\partial t} \left(\mathbf \nabla \times \mathbf B\right) = -\nabla^2 \mathbf E
$$

$$
-\frac{\partial }{\partial t} \left( \mu_0 \varepsilon_0 \frac{\partial \mathbf E}{\partial t}\right) = -\nabla ^2 \mathbf E
$$

$$
 \mu_0 \varepsilon_0 \frac{\partial^2 \mathbf E}{\partial t^2} = \boxed{\nabla ^2 E = \frac{\partial ^2 E}{\partial x^2} + \frac{\partial ^2 E}{\partial y^2} + \frac{\partial ^2 E}{\partial z^2}}
$$

Thus, 
$
 \mu_0 \varepsilon_0 \frac{\partial^2 \mathbf E}{\partial t^2} = \frac{\partial ^2 E}{\partial x^2} + \frac{\partial ^2 E}{\partial y^2} + \frac{\partial ^2 E}{\partial z^2}
$ is a wave if $c^2 = \frac{1}{\mu_0 \varepsilon_0}$

and $\mathbf E$ obeys the wave equation for waves travelling at speed $c = \frac{1}{\sqrt{\mu_0\varepsilon_0}}$.

Similarly, $$\mathbf \nabla \times (\mathbf\nabla \times \mathbf B)= \mathbf \nabla (\mathbf \nabla \cdot \mathbf E) - \nabla ^2 \mathbf B$$ 

$$
\mathbf \nabla \times \left(\mu_0 \varepsilon_0 \frac{\partial \mathbf B}{\partial t}\right) = 0 - \nabla^2 \mathbf B
$$

$$
\mu_0 \varepsilon_0 \frac{\partial }{\partial t} \left(\mathbf \nabla \times \mathbf E\right) = -\nabla^2 \mathbf B
$$

($J=0 \because \text{source-free} \uparrow$)

$$ \boxed{\mu_0 \varepsilon_0 \frac{\partial^2 \mathbf B}{\partial t^2} = \nabla^2 \mathbf B} = \frac{\partial ^2 \mathbf B}{\partial x^2} + \frac{\partial ^2 \mathbf B}{\partial y^2} + \frac{\partial ^2 \mathbf B}{\partial z^2}$$

is a wave eqution for $\mathbf B$ with waves travelling at $c = \frac{1}{\sqrt{\mu_0 \varepsilon_0}}$.

Therefore, both $\mathbf E$ and $\mathbf B$ are waves that travel at $c$. Light consists in the "transverse undulations" in the same medium[^1] that causes electromagnetic phenomena. 
[^1]: Although there is no medium, but that's another story...
# Fundamental Theorems

Today we cover:

* Maxwell's Equations in Integral/Differential Form
* Fundamental Theorems

But ... we must also establish:


- $\mathbf r, \mathbf r', \mathcal{r}$
- $\delta_{ij}$                        
- $\text{point charge physics}$          

Which is all part of **Ch. 1 of Griffiths**. 

(Note: $\mathcal{r}$ is gonna have to cut it as Griffith's "script r", cause I can't render it in GFM. Maybe I'll switch to jupyter notebook...stay tuned.)

Anyway:

$$\mathbf \nabla \cdot \mathbf E = \rho / \varepsilon_0 \iff \oint \mathbf E \cdot d \mathbf a = \frac{q_{\text{enclosed}}}{\varepsilon_0}$$

$$\mathbf \nabla \times \mathbf E = -\frac{\partial \mathbf B}{\partial t} \iff \oint \mathbf E \cdot d \mathbf l = -\frac{\partial \Phi_{B}}{\partial t}$$

$$\mathbf \nabla \cdot \mathbf B = 0 \iff \oint \mathbf B \cdot d \mathbf a = 0$$

$$\mathbf \nabla \times \mathbf B = \mu_0 \mathbf J+\mu_0 \varepsilon_0 \frac{\partial \mathbf E}{\partial t} \iff \oint \mathbf B \cdot d \mathbf l = \mu_0 I_{\text{enclosed}} + \mu_0 \varepsilon_0 \frac{\partial \Phi_B}{\partial t}$$

"If you graduate knowing this and the fundamental theorems, that's not nothing". 

<u>Recall</u>: Fundamental theorem of calculus for *univariate*:

$$
\int_a^b \frac{df}{dx} = f(b) - f(a)
$$

"Integral of a derivative over some region equals to the function **itself** evaluated on the boundary of said region. 

Goal: go from 1D to 3D:

$$\text{derivative} \longleftrightarrow \text{gradient operator} \mathbf \nabla $$

(Contains partial derivatives: $\mathbf \nabla f$, $\mathbf \nabla \cdot f$, $\mathbf \nabla \times f$.)

In English: you can onlu do three things with $\mathbf \nabla$: gradient, divergence, and curl. 

There is a fundamental theorem for each operation! And they all have the same structure as the fundamental theorem of calculus:

1. Fundamental Theorem of Gradients (or, Fundamental Theorem of Vector Calculus)

$$
\boxed{\int_{\mathcal a}^{\mathcal b} \mathbf \nabla f \cdot d \mathbf l = f(b) - f(a)}
$$

"Integral of a derivative is equal to the difference of the function values at the boundary"

2. Fundamental theorem of Divergences (or, Gauss's Law / The Divergence Theorem)

Imagine a field, all div no curl, w/ volume $V$ and surface $S$:

$$
\boxed{\int_V \left(\mathbf \nabla \cdot \mathbf f \right)d \tau = \int_S \mathbf f \cdot da}
$$

**Again**: "integral of derivative over some region evaluated on boundary of some region."

Another way to fphrase this: `divergence` of a field through a volme `equals` the flux of a field through the surface. 

3. Fundamental theorem of Curl (Stokes' Theorem)

For path $P$ and a surface $S$

$$\boxed{
\int_S \left(\mathbf \nabla \times \mathbf f \right) \cdot d \mathbf a = \int_P \mathbf f \cdot d \mathbf l
}
$$

"integral of a derivative over some region..."

Ex: Start with Maxwell's Equations in differential form, and get to integral form:

If we apply $\left(\mathbf \nabla \cdot \mathbf E = \rho/\varepsilon_0 \right)$ using the divergence theorem:

$$
\int\limits_{{\text{volume} \,V }} \left(\mathbf \nabla \cdot \mathbf E\right) d\tau = \int\limits_{\text{volume} \,V } \rho/\varepsilon_0\, d\tau
$$

$$
\int\limits_{{\text{surface} \,S }} \left(\mathbf E \cdot d \mathbf a\right) d\tau =  \frac{q_{\text{enclosed}}}{\varepsilon_0}.
$$


# 9/7/21:

A note on notebooks: actively read the book and fill in the missing steps. 

* Will not dock if you have scratchwork (as long as you have a big X)

Is your writing neat, have you filled in gaps?

## We are fully in Griffths Material now!

Today we revisit the Dirac-Delta function (DDF). 

Agenda:

* 1D DDF
    * def
    * neat properties
* 3D DDF
    * def
    * neat properties
    * Divergence field: a $\bot$! (contradiction!) and resolution. 

    Now: 1D DDF is defined like so:

$$
\delta(x) = \left\{
                \begin{array}{ll}
                  0, x \neq 0\\
                  \infty, x = 0
                \end{array}
                \right.
$$

such that $\int\limits_{-\infty}^{\infty} \delta(x)dx = 1$.

Noteworthy properties:

1. $\int\limits_{-\infty}^{\infty} f(x)\delta(x)dx = f(0)$


DDF selects the one value wher DDF is non-zero on $f(x)$. 

2. if $\delta(x-a)$ is defined as

$$
\delta(x-a) = \left\{
    \begin{array}{ll}
    0, x \neq 0 \\
    \infty, x = a
    \end{array}
    \right.
$$
and $\int\limits_\infty^\infty f(x)\delta(x)dx = 1$, then (1.) still holds. 

This is AKA the **shifting property**:

$$
\int\limits_\infty^\infty f(x)\delta(x-a) dx = f(a)
$$

Now we will generalize to 3D:

## Generalization to 3D DDF:

$$
\bf {Def:} \quad \delta^3(x) = \left\{
    \begin{array}{ll}
    0, \quad (x, y, z) \neq (0, 0, 0) \\
    \infty, \quad (x, y, z) = (0, 0, 0)
    \end{array}
    \right.
$$

such that $\int \delta^3(\vec r)d\tau = 1$ over all 3d space. 

Other notations of which one should generally be aware:

$\delta^3(\vec r) = \delta(x) \delta(y) \delta(z)$

$\delta^3(\vec r) d^3 \vec r = 1$

$\int \limits_{\text{All Space}}\delta^3 (\vec r) d \vec r = 1$

$\int \int \int \delta(x) \delta (y) \delta (z) dx dy dz$

The two properties discussed above still hold!

1. 
$$\boxed{
\int\limits_{\text{All Space}} f(\vec r)\delta^3(\vec r)d\tau = f(0, 0, 0)
}
\newline \text{The "SELECT-OUT" property}. 

$$

2. 
$$ \text{If} \quad
\delta^3(\vec r - \vec a) = 
    \left\{
    \begin{array}{ll}
    0, \quad \vec r \neq \vec a \\
    \infty, \quad\vec r  = \vec a
    \end{array}
    \right.

    \ni \int \limits_{\text{All Space}}\delta^3 (\vec r - \vec a) d \tau = 1, \quad \text{then}
$$

$$\boxed{
\int\limits_{\text{All Space}} f(\vec r)\delta^3(\vec r - \vec a)d\tau = f(\vec a)
}
\newline \text{SHIFT property}
$$


# HENCEFORTH, this pure-markdown notebook will only be for scratch. 
The real notebook is the jupyter one. 