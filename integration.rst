===========
Integration
===========

Let’s define inner products!
============================

In this talk we mainly consider real linear spaces, e.g.,
:math:`\mathbb{R}^d`. You may consider complex linear spaces if you know
complex numbers.

We assume you agree with the existence of higher dimensional spaces. We
want to define angles and length of vectors as in two or three
dimensional ones. One reason to consider them is application to physics.
There is a projection hypothesis in quantum mechanics: this projection
comes from orthogonal projection, and it is just a shadow of objects in
three dimensional objects when one shine a light from above.

At first we consider how to define angles between infinite dimensional
vectors, especially, functions. Take a look at the following inner
product formula in high school.

.. math::

   \begin{align*}
    a \cdot b
    =
    \left|a\right| \, \left|b\right| \cos \theta.\end{align*}

We deform this:

.. math::

   \begin{align*}
    \cos \theta
    =
    \frac{ a \cdot b} {\left|a\right| \, \left|b\right|}.\end{align*}

We can derive an angle :math:`\theta` from the value of the cosine
function. Lengths [4]_ of vectors can be computed by inner products,
from :math:`\left|a\right|^2 = a \cdot a`. So we can derive angles if we
can define an inner product. Hence we have to define an inner product.
Note that an inner product is not a divine concept.

At first we write an inner product in :math:`\mathbb{R}^3`. We write a
vector :math:`f = (f_1, f_2, f_3)` as :math:`f = (f(1), f(2), f(3))` for
later use. This is just a notational convention. We define an inner
product for three dimensional vectors :math:`f` and :math:`g` as

.. math::

   \begin{align*}
    f \cdot g
    :=
    \left\langle f,\,g\right\rangle
    :=
    \sum_{k=1}^3 f(k)g(k).\end{align*}

The first notation is one in high school. The second is usual one when
considering a functional inner product. There are several notations for
an inner product such as

.. math::

   \begin{align*}
    \left (f, g\right), \quad \left (f | g\right), \quad \langle f | g \rangle.\end{align*}

The last one is the famous Dirac’s braket notation in quantum mechanics.

Inner products in higher dimensional spaces
-------------------------------------------

We wrote an inner product as

.. math::

   \begin{align*}
    \langle f , g \rangle
    =
    \sum_{k=1}^3 f(k)g(k).\end{align*}

Since there is no reason to restrict our consideration to a three
dimensional space we generalize a dimension three to general :math:`d`.

.. math::

   \begin{align*}
    \langle f , g \rangle
    =
    \sum_{k=1}^d f(k)g(k),\end{align*}

where we set

.. math::

   \begin{align*}
    f = \left (f(1), f(2), \dots, f(d)\right), \quad
    g = \left (g(1), g(2), \dots, g(d)\right).\end{align*}

If you want to consider one in :math:`\mathbb{C}^d` you should set

.. math::

   \begin{align*}
    \left\langle f,\,g\right\rangle
    =
    \sum_{k=1}^d \overline{f(k)} g(k)\end{align*}

because it is desirable that a length (norm) of a vector is properly
defined, i.e.,
:math:`\left\Vert f\right\Vert^2 := \left\langle f,\,g\right\rangle \geq 0`.

We take a limit :math:`d \to \infty`. We face a problem whether a series
converges or not, but we can overcome this by considering converging
ones.

.. math::

   \begin{align*}
    \left\langle f,\,g\right\rangle
    =
    \sum_{k=1}^{\infty} f(k)g(k).\end{align*}

An infinite dimensional vector :math:`f = (f(1), f(2), \dots)` can be
viewed as a sequence. In quantum mechanics we use sequences and matrices
living in an infinite dimensional space when considering Heisenberg’s
matricial mechanics.

Note that our temporal task is to make how to define an inner product
for functions. Let’s go back to a finite sum, think
:math:`1 = \Delta k`, and rewrite a sum as

.. math::

   \begin{align*}
    \sum_{k=1}^{d} f(k)g(k) \Delta k.\end{align*}

Rewrite :math:`k` as :math:`k/d` and :math:`\Delta k` as :math:`1/d`.
Then we get a sum

.. math::

   \begin{align*}
    \sum_{k=1}^{d} f \left( \frac{k}{d} \right) g \left( \frac{k}{d} \right) \frac{1}{d}.\end{align*}

This is an expression, known as 区分求積法 in high school [5]_.

Taking a limit :math:`d \to \infty` the above sum becomes an integral.

.. math::

   \begin{align*}
    \langle f, g \rangle
    =
    \int_{0}^{1} f(x) g(x) dx.\end{align*}

Now the interval is :math:`[0, 1]` here, but we can take any
(measurable) subset of :math:`\mathbb{R}`.

Hence we find that an inner product for functions can be defined using
integral. In fact anything is good if it satisfies the axiom of an inner
product.

A linear space with inner product is called pre-Hilbert space. A
pre-Hilbert space is called a Hilbert space if it is complete for metric
induced by inner product. A Hilbert space is famous as a space where
wave functions in quantum mechanics live.

Axiom for inner products
========================

Let :math:`L` be a linear space and
:math:`\left\langle\cdot,\,\cdot\right\rangle \colon L \times L \to \mathbb{R}`
is a map of two variables. The pair
:math:`\left (L, \left\langle\cdot,\,\cdot\right\rangle\right)` is an
inner product space if the map
:math:`\left\langle\cdot,\,\cdot\right\rangle` is an inner product,
i.e., it satisfies the following properties.

#. Symmetry:

   .. math::

      \begin{align*}
      \left\langle f, \, g \right\rangle
      =
      \left\langle g, \, f \right\rangle
      \end{align*}

#. Linearity in the second argument:

   .. math::

      \begin{align*}
         \left\langle f,\,\alpha g + \beta h\right\rangle
         =
         \alpha \left\langle f,\,g\right\rangle + \beta \left\langle f,\,h\right\rangle.
        \end{align*}

#. Positive definiteness:

   .. math::

      \begin{align*}
         \left\langle f,\,f\right\rangle \geq 0, \quad
         \left\langle f,\,f\right\rangle = 0 \Longleftrightarrow f = 0.
        \end{align*}

The usual three dimensional inner product satisfies the above, of
course.

Examples of inner products
==========================

There are many inner products in a function space. Let :math:`\Omega` be
a (open) subset of :math:`\mathbb{R}` and
:math:`h \colon \Omega \to \mathbb{R}_{\geq}` be a function satisfying

.. math::

   \begin{align*}
    h(x) \geq 0, \quad
    h \neq 0, \quad
    0 < \int_\Omega h(x) dx < \infty.\end{align*}

Then the following becomes an inner product:

.. math::

   \begin{align*}
    \left\langle f,\,g\right\rangle_{h}
    :=
    \int_{\Omega} f(x) g(x) h(x) dx.\end{align*}

We show some examples of inner products.

.. math::

   \left\langle f,\,g\right\rangle_1
   &:=
   \int_{-1}^{1} f(x) g(x) dx, \\
   \left\langle f,\,g\right\rangle_2
   &:=
   \int_{0}^{\infty} f(x) g(x) e^{-x} dx, \\
   \left\langle f,\,g\right\rangle_3
   &:=
   \int_{\mathbb{R}} f(x) g(x) e^{-x^2} dx.

The above inner products are related to the Legendre polynomials,
Laguerre polynomials, Hermite polynomials.

Furthermore we take the following inner product.

.. math::

   \begin{align*}
    \int_{- \pi}^{\pi} f(x) g(x) dx.\end{align*}

Then we get the following expressions.

.. math::

   \frac{1}{\pi} \int_{-\pi}^{\pi} \sin nx \sin mx
   &=
   \delta_{n,m}, \\
   \frac{1}{\pi} \int_{-\pi}^{\pi} \cos nx \cos mx
   &=
   \delta_{n,m}, \\
   \frac{1}{\pi} \int_{-\pi}^{\pi} \cos nx \sin mx
   &= 0.

This means that the functions :math:`\left\{\cos nx\right\}` and
:math:`\left\{\sin nx\right\}` are orthogonal. This relates to the
famous Fourier series expansion. This is used for wave analysis in
physics.

Physics for the space :math:`L^2 \left (\Omega\right)`
======================================================

The symbol :math:`L^2 \left (\Omega\right)` in the title means the space
of square integrable functions in the sense of Lebesgue on
:math:`\Omega`.

We introduce a physical meaning of the space
:math:`L^2 \left (\Omega\right)`. [6]_

The elements of the space :math:`L^2 \left (\Omega\right)` have finite
energy. Let us consider a wave equation.

.. math::

   \begin{align*}
    \frac{\partial^2 u}{\partial t^2}
    =
    \Delta u.\end{align*}

The energy for its solution is written by

.. math::

   \begin{align*}
    E
    =
    \int_{\mathbb{R}^d} \left (\left (\nabla u\right)^2 + \left (\frac{\partial u}{\partial t}\right)^2\right)dx.\end{align*}

We want to restrict solutions whose energy is finite since it is
physically meaningless to consider solutions with infinite energy. The
elements of :math:`L^2` have finite energy, by definition, and hence it
is the reason why the space :math:`L^2` is important in physics. To be
precise our derived functions are in :math:`L^2`, so we have to consider
a Sobolev space :math:`H^1`.

In quantum mechanics probabilistic interpretation forces us to consider
functions in :math:`L^2`. Furthermore we have to impose more severe
restriction to functions, i.e., the domain of Hamiltonians.

Linear operators have their domains and, for Hamiltonians, their domains
are functions having finite energy.

.. [4]
   In general we call it a norm of a vector. We can consider many norms
   for a vector since there are many senses of distances.

.. [5]
   This is a definition of the Riemann integral.

.. [6]
   To be precise the proper space is not :math:`L^2` but :math:`H^1`.
