# This is my (humble) attempt to digitally recreate the notes of Hamilton College professor Kate Brown.

## Prof. Brown encouraged us to keep a notebook "as a record of our leraning". So strongly, in fact, that it was worth 25% of our grades. As such, this is the neatest documentation of physics I've ever done. I'm documenting it here on GitHub to hold myself accountable as part of studying for the qualification exam. 

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

$$ \vec v = v_x \hat x + v_y \hat y + v_z\hat z = v_x \hat i + v_y \hat j + v_z \hat k$$ 

but $v_x$ can, say, depend on $x$, $y$, and $z$. 

The above is all in Cartesian coordinates. 

Spherical:
$$\vec v = v_r \hat r + v_\theta \hat \theta + v_\phi \hat \phi$$

Cylindrical: $(r, \phi, z)$ or $(s, \phi, z)$.

$$\vec v = v_r \hat r + v_\phi \hat \phi + v_z \hat z$$

Q: So how do we express vector fields mathematically? Or rather, how are they determined?
A: Vector fields are determined by only two features: `div` and `curl`. 

* Divergence: how much the field is radiating to/from a point, given by $\vec \nabla \cdot \vec v$
* Curl: how mych the field is circulating about a point given by $\vec \nabla \times \vec v$.

So if you tell me the `div` and `curl` of a vector field, I can reconstruct it all!

Caveat: boundary conditions. 

Maxwell's Equations: these specify div, curl of $\vec E$, $\vec B$!

$$\vec \nabla \cdot \vec E = \rho / \varepsilon_0$$

$$\vec \nabla \times \vec E = -\frac{\partial \vec B}{\partial t}$$

$$\vec \nabla \cdot \vec B = 0$$

$$\vec \nabla \times \vec B = \mu_0 \vec J+\mu_0 \varepsilon_0 \frac{\partial \vec E}{\partial t}$$

Comments: "sources" usally refer to $\vec \rho$ and $\vec J$.

* $\rho$ = source of electric charge ("charged stuff")

    $\rho$ and $\varepsilon_0$ together are sources of electric phenomena

* $\vec J$ = source of magnetic field, or current(moving charge)

    $\mu_0$ and $\vec J$ together are sources of magnetic phenomena

In general, for these PDE's:

[Derivatives on LHS] = "source". (can be 0)

Source free $\implies$ $\vec \rho = \vec J = \vec 0$ in the Gaussian surface (no charges/current).

## Corrections to Maxwell's Equations:

In statics $\vec \nabla \times \vec E = 0$, but $\vec \nabla \times \vec E = -\frac{\partial \vec B}{\partial t}$ is **FARADAY'S CORRECTION**

Faraday conjectured that the above is true. 

$$\vec \nabla \times \vec B = \mu_0 \vec J+\mu_0 \varepsilon_0 \frac{\partial \vec E}{\partial t}$$

The second term here (sadly can't use underbrace) is Maxwell's law/correction. 

Ampere's law, without this correction, is $\vec \nabla \times \vec B = \mu_0 \vec J$.

Source free regime of Maxwell's Equations (where $\vec \rho = \vec J = 0$):

$$\vec \nabla \cdot \vec E = 0$$

$$\vec \nabla \times \vec E = -\frac{\partial \vec B}{\partial t}$$

$$\vec \nabla \cdot \vec B = 0$$

$$\vec \nabla \times \vec B = \mu_0 \varepsilon_0 \frac{\partial \vec E}{\partial t}$$

These are Maxwell's EQ'ns in a vaccuum. 

Start with Eq 11, inside cover of Griffiths:

$$\vec \nabla \times (\vec \nabla \times \vec A) = \vec \nabla (\vec \nabla \cdot \vec A) - \nabla ^2 \vec A$$ 
(equation 11). 

Thus... TOBECONTINUED...