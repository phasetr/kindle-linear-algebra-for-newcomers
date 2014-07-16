===============
Differentiation
===============

Taylor expansion
================

We start from Taylor’s theorem. Assume a function :math:`f` is
differentiable. Fundamental theorem of calculus and integration by parts
lead

.. math::

   f(x) - f(x_0)
   &=
   \int_{x_0}^{x} f'(y) dy
   =
   \int_{x_0}^x (x - y)^{0} f'(y) dy \\
   &=
   \left[- \left (x - y\right) f'(y)\right]_{x_0}^x + \int_{x_0}^x \left (x - y\right) f^{(2)} (y) dy \\
   &=
   (x - x_0) f'(x_0) + \left[- \frac{(x-y)^2}{2} f^{(2)}(y)\right]_{x_0}^x + \int_{x_0}^x \frac{(x - y)^2}{2} f^{(3)} (y)dy. \\
   &=
   (x - x_0) f'(x_0) + \frac{(x-x_0)^2}{2} f^{(2)}(x_0) + \int_{x_0}^x \frac{(x - y)^2}{2} f^{(3)} (y)dy.

Further iteration leads the following Taylor’s theorem.

.. math::

   \begin{align*}
    f(x)
    =
    \sum_{k=0}^{n} \frac{(x - x_0)^k}{k!} \left( D^k f \right) (x_0) +
     \int_{x_0}^{x} \frac{(x - y)^{n}}{n!} f^{(n+1)} (y) dy,\end{align*}

where :math:`D^k f` is a shorthand notation for :math:`d^k f/ dx^k`, the
last term of the RHS is called the remainder term and denoted by
:math:`R_n`.

Now assume the remainder term :math:`R_n` converges to 0 as
:math:`n \to \infty` and the above series also converges in some
suitable sense. Let :math:`x_0 = 0`. Then we get

.. math::

   \begin{align*}
    f(x)
    =
    \sum_{k=0}^{\infty} \frac{x^k}{k!} \left( D^k f \right) (0).\end{align*}

This series is called a **Taylor series** around 0 and this power series
expansion is called a **Taylor expansion** around 0.

A Taylor expansion of an exponential function :math:`e^x` around
:math:`0` is as follows.

.. math::

   \begin{align*}
    e^{x}
    =
    \sum_{k=0}^{\infty} \frac{x^k}{k!}.\end{align*}

We compare the above two expressions and set :math:`x` to :math:`x D` in
the expansion of :math:`e^x`. Then we have the following clear
expression.

.. math::

   \begin{align*}
    f(x)
    =
    \left( e^{xD} f \right) (0)\end{align*}

If we use quantum mechanical notation, :math:`p = -i D`, the above
expression becomes

.. math::

   \begin{align*}
    f(x)
    =
    \left( e^{ixp} f \right) (0).\end{align*}

Unitary representation of a group
=================================

The above story closely related to a unitary representation theory of a
group. Simply speaking a underlying space :math:`\mathbb{R}` itself is a
group and it acts on itself. This action lifts up to a function space
living on a underlying space. See for details.

One point. Physicists often define functions of operators by Taylor
expansion. However it is not good and insufficient in view of
mathematics. We can see it when we consider the action of
:math:`e^{ixp}`.

The operator :math:`e^{i x p}` shifts an argument of a function
:math:`x`, and this shift is defined without differentiability of
functions, i.e., we can define an action of :math:`e^{ixp}` for more
general functions. However if we define it by a Taylor expansion, the
operator :math:`e^{ixp}` is defined for only analytic functions.

Fourier expansion
-----------------

A simple argument can deduce a Fourier expansion. We can formally
consider for :math:`\mathbb{R}`, but this is a little bit mathematically
problematic. Instead we consider on an interval :math:`[ - \pi, \pi]`.

Consider a linear differential equation (eigenequation for self-adjoint
operator :math:`p`)

.. math::

    p f
    &=
    k f, \quad k \in \mathbb{R}, \\
    f(-\pi)
    &=
    f(\pi).

Then the above solutions are

.. math::

   \begin{align*}
    f_k(x)
    =
    e^{ikx}\end{align*}

for each :math:`k \in \mathbb{Z}`.
Note that computation shows the set of
eigenvalues :math:`\{k\}` is, in fact, :math:`\mathbb{Z}` and that
the above solutions :math:`\{f_k\}` are the eigenfunctions of each eigenequation :math:`p f_k = k f_k`.

Euler’s formula says

.. math::

   \begin{align*}
    e^{ikx}
    =
    \cos kx + i \sin kx,\end{align*}

and this leads a Fourier expansion.

Analitical mechanics and quantum mechanics
==========================================

In quantum mechanics a momentum becomes a differential operator and
denotes :math:`p = -i D`.

In analytical mechanics a momentum can be viewed as a generator of space
shift. A differential operator :math:`- i d/dx` is also a generator of
space shift in view of representation theory. Hence these are common
property, generator of space shift. This is an important **formal**
connection to classical mechanics and quantum mechanics. This connection
is also important in geometry.

Physics and representation theory
=================================

Representation theory is also important for theory of relativity and
relativistic quantum field theory.

A variational problem is an infinite dimensional version of differential
theory. This is important and interesting in both physics and
mathematics.

It is a mathematically and physically famous problem that why soap
bubble becomes round. This type of problems is called a geometric
variational problem.
