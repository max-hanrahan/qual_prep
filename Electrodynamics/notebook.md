# This is my (humble) attempt to digitally recreate the notes of Hamilton College professor Kate Brown.

## Prof. Brown encouraged us to keep a notebook "as a record of our leraning". 
So strongly, in fact, that it was worth 25% of our grades. As such, this is the neatest documentation of physics I've ever done. I'm documenting it here on GitHub to hold myself accountable as part of studying for the qualification exam. 

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

$$ \bold v = v_x \hat x + v_y \hat y + v_z\hat z = v_x \hat i + v_y \hat j + v_z \hat k$$ 

but $v_x$ can, say, depend on $x$, $y$, and $z$. 

The above is all in Cartesian coordinates. 

Spherical:
$$\bold v = v_r \hat r + v_\theta \hat \theta + v_\phi \hat \phi$$

Cylindrical: $(r, \phi, z)$ or $(s, \phi, z)$.

$$\bold v = v_r \hat r + v_\phi \hat \phi + v_z \hat z$$

Q: So how do we express vector fields mathematically? Or rather, how are they determined?
A: Vector fields are determined by only two features: `div` and `curl`. 

* Divergence: how much the field is radiating to/from a point, given by $\bold \nabla \cdot \bold v$
* Curl: how mych the field is circulating about a point given by $\bold \nabla \times \bold v$.

So if you tell me the `div` and `curl` of a vector field, I can reconstruct it all!

Caveat: boundary conditions. 

Maxwell's Equations: these specify div, curl of $\bold E$, $\bold B$!

$$\bold \nabla \cdot \bold E = \rho / \varepsilon_0$$

$$\bold \nabla \times \bold E = -\frac{\partial \bold B}{\partial t}$$

$$\bold \nabla \cdot \bold B = 0$$

$$\bold \nabla \times \bold B = \mu_0 \bold J+\mu_0 \varepsilon_0 \frac{\partial \bold E}{\partial t}$$

Comments: "sources" usally refer to $\bold \rho$ and $\bold J$.

* $\rho$ = source of electric charge ("charged stuff")

    $\rho$ and $\varepsilon_0$ together are sources of electric phenomena

* $\bold J$ = source of magnetic field, or current(moving charge)

    $\mu_0$ and $\bold J$ together are sources of magnetic phenomena

In general, for these PDE's:

[Derivatives on LHS] = "source". (can be 0)

Source free $\implies$ $\bold \rho = \bold J = \bold 0$ in the Gaussian surface (no charges/current).

## Corrections to Maxwell's Equations:

In statics $\bold \nabla \times \bold E = 0$, but $\bold \nabla \times \bold E = -\frac{\partial \bold B}{\partial t}$ is **FARADAY'S CORRECTION**

Faraday conjectured that the above is true. 

$$\bold \nabla \times \bold B = \mu_0 \bold J+\mu_0 \varepsilon_0 \frac{\partial \bold E}{\partial t}$$

The second term here (sadly can't use underbrace) is Maxwell's law/correction. 

Ampere's law, without this correction, is $\bold \nabla \times \bold B = \mu_0 \bold J$.

Source free regime of Maxwell's Equations (where $\bold \rho = \bold J = 0$):

$$\bold \nabla \cdot \bold E = 0$$

$$\bold \nabla \times \bold E = -\frac{\partial \bold B}{\partial t}$$

$$\bold \nabla \cdot \bold B = 0$$

$$\bold \nabla \times \bold B = \mu_0 \varepsilon_0 \frac{\partial \bold E}{\partial t}$$

These are Maxwell's EQ'ns in a vaccuum. 

Start with Eq 11, inside cover of Griffiths:

$$\bold \nabla \times (\bold \nabla \times \bold A) = \bold \nabla (\bold \nabla \cdot \bold A) - \nabla ^2 \bold A$$ 
(equation 11). 

Thus, 

$$\bold \nabla \times (\bold \nabla \times \bold E) = \nabla (\bold \nabla \cdot \bold E) - \nabla ^2 \bold E$$ 

$$
\nabla \times \left(- \frac{\partial \bold B}{\partial t}\right) = \bold \nabla (0) - \nabla^2 \bold E \text{ by $\rho=0$ (source-free regime)}
$$

$$
\bold \nabla \times \left(- \frac{\partial \bold B}{\partial t}\right) = - \nabla ^2 \bold E
$$

$$
-\frac{\partial }{\partial t} \left(\bold \nabla \times \bold B\right) = -\nabla^2 \bold E
$$

$$
-\frac{\partial }{\partial t} \left( \mu_0 \varepsilon_0 \frac{\partial \bold E}{\partial t}\right) = -\nabla ^2 \bold E
$$

$$
 \mu_0 \varepsilon_0 \frac{\partial^2 \bold E}{\partial t^2} = \boxed{\nabla ^2 E = \frac{\partial ^2 E}{\partial x^2} + \frac{\partial ^2 E}{\partial y^2} + \frac{\partial ^2 E}{\partial z^2}}
$$

Thus, 
$
 \mu_0 \varepsilon_0 \frac{\partial^2 \bold E}{\partial t^2} = \frac{\partial ^2 E}{\partial x^2} + \frac{\partial ^2 E}{\partial y^2} + \frac{\partial ^2 E}{\partial z^2}
$ is a wave if $c^2 = \frac{1}{\mu_0 \varepsilon_0}$

and $\bold E$ obeys the wave equation for waves travelling at speed $c = \frac{1}{\sqrt{\mu_0\varepsilon_0}}$.

Similarly, $$\bold \nabla \times (\bold\nabla \times \bold B)= \nabla (\bold \nabla \cdot \bold E) - \nabla ^2 \bold B$$ 

$$
\bold \nabla \times \left(\mu_0 \varepsilon_0 \frac{\partial \bold B}{\partial t}\right) = 0 - \nabla^2 \bold B
$$

$$
\mu_0 \varepsilon_0 \frac{\partial }{\partial t} \left(\bold \nabla \times \bold E\right) = -\nabla^2 \bold B
$$
($J=0 \because \text{source-free} \uparrow$)
$$
\boxed{\mu_0 \varepsilon_0 \frac{\partial^2 \bold B}{\partial t^2} = \nabla^2 \bold B} = \frac{\partial ^2 \bold B}{\partial x^2} + \frac{\partial ^2 \bold B}{\partial y^2} + \frac{\partial ^2 \bold B}{\partial z^2}
$$
is a wave eqution for $\bold B$ with waves travelling at $c = \frac{1}{\sqrt{\mu_0 \varepsilon_0}}$.
