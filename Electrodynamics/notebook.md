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

Similarly, $$\mathbf \nabla \times (\mathbf\nabla \times \mathbf B)= \nabla (\mathbf \nabla \cdot \mathbf E) - \nabla ^2 \mathbf B$$ 

$$
\mathbf \nabla \times \left(\mu_0 \varepsilon_0 \frac{\partial \mathbf B}{\partial t}\right) = 0 - \nabla^2 \mathbf B
$$

$$
\mu_0 \varepsilon_0 \frac{\partial }{\partial t} \left(\mathbf \nabla \times \mathbf E\right) = -\nabla^2 \mathbf B
$$

($J=0 \because \text{source-free} \uparrow$)

$$ \boxed{\mu_0 \varepsilon_0 \frac{\partial^2 \mathbf B}{\partial t^2} = \nabla^2 \mathbf B} = \frac{\partial ^2 \mathbf B}{\partial x^2} + \frac{\partial ^2 \mathbf B}{\partial y^2} + \frac{\partial ^2 \mathbf B}{\partial z^2}$$

is a wave eqution for $\mathbf B$ with waves travelling at $c = \frac{1}{\sqrt{\mu_0 \varepsilon_0}}$.
