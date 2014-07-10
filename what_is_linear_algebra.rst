=======================
What is linear algebra?
=======================

Main targets of linear algebra are vectors and matrices. We learn them
in high school but linear algebra in university mathematics has somewhat
different flavor from one in high school. Furthermore linear algebra is
difficult to imagine where we use it compared to calculus. So we first
consider its different points and its usage in mathematics and physics.

In high school we consider vectors as geometric objects. However we now
consider them as algebraic objects, since they are ones in linear
“algebra”! Our vectors are a generalized/abstract version of ones in
high school. A vector needs not have direction nor length. Then, what
properties should vectors have?

Abstract definition of vectors
==============================

In the following we sometimes use the terms linear spaces or vector
spaces. These words have the same meaning.

Let :math:`\mathbb{R}` be a field of real numbers: a real number is also
called a scaler. A set :math:`L` is called a linear space if its elements have the
following properties. Elements :math:`x, y, z \in L` are vectors and
:math:`a, b \in \mathbb{R}` are real numbers in the following
expressions.

#. Associativity:

   .. math::

      \begin{align*}
         \left (x + y\right) + z
         =
         x + \left (y + z\right), \quad \forall x, y, z \in L.
        \end{align*}

#. Commutativity of sum:

   .. math::

      \begin{align*}
         x + y = y + x,  \quad \forall x, y \in L.
        \end{align*}

#. Existence of unit for sum: there is an element :math:`0 \in L` such that

   .. math::

      \begin{align*}
         x + 0 = x, \quad \forall x \in L.
        \end{align*}

#. Existence of an inverse element for sum: for any :math:`x \in L` there is an element :math:`y \in L` such that

   .. math::

      \begin{align*}
         x + y = 0
        \end{align*}

   for the above :math:`0`. In fact we can prove the uniqueness of an
   inverse element.

#. Relation of scalers (real numbers) and vectors:

   .. math::

      a \cdot \left (x + y\right)
      &=
      a \cdot x + a \cdot y, \\
      \left( ab \right) \cdot x
      &=
      a \cdot \left( b x \right), \\
      \left (a + b \right) \cdot x
      &=
      a \cdot x + b \cdot x,

#. Multiplication law for a scaler unit in :math:`\mathbb{R}`:

   .. math::

      \begin{align*}
         1 \cdot x = x, \quad \forall x \in L.
        \end{align*}

Important points are

#. vectors are summable and sum is commutative operation, and

#. vectors and scalers satisfy some multiplication laws.

The above properties hold for geometric vectors in high school, of
course. Our purpose is different from it: we consider vectors as
algebraic objects and we derive many interesting properties using
(mainly) algebraic thinking!

Examples of linear spaces
=========================

#. The set of real numbers :math:`\mathbb{R}` itself with scaler
   :math:`\mathbb{R}`.

#. The set of complex numbers :math:`\mathbb{C}` itself with scaler
   :math:`\mathbb{R}`.

#. The set of complex numbers :math:`\mathbb{C}` itself with scaler
   :math:`\mathbb{C}`.

#. A plane :math:`\mathbb{R}^2` with scaler :math:`\mathbb{R}`.

#. A three dimensional space :math:`\mathbb{R}^3` with scaler
   :math:`\mathbb{R}`.

#. Higher dimensional space :math:`\mathbb{R}^d` (:math:`d \geq 4`) with
   scaler :math:`\mathbb{R}`.

#. Some subsets of the set of (numerical) sequences, e.g., :math:`c_0`,
   :math:`c_{\infty}`, :math:`\ell^2` with scaler :math:`\mathbb{R}`.

#. Some subsets of the set of functions, e.g., :math:`C^k(\Omega)`,
   :math:`L^p \left (\Omega\right)`, :math:`H^k \left (\Omega\right)`
   with scaler :math:`\mathbb{R}`.

#. A set of linear operators with scaler :math:`\mathbb{R}`.

Today’s main targets are introduction to the last three items and its
relation to calculus.

Examples of finite, but higher dimensional spaces than three
============================================================

We have many examples for higher dimensional objects in real world,
e.g.,

#. (time evolution of) stock prices,

#. players’ movement in soccer,

#. computerized control in robots.

For (time evolution of) stock prices, there are many listing companies
and its time evolution is important in real world. This evolution is
mathematically representable in higher dimensional space picture.

Other examples are also similar characterization. These are related to
analytical mechanics in physics. Moreover analytical mechanics is
closely related to geometry.

Function as a vector
====================

First recall the definition of vectors in three dimension: letting
:math:`f = (f(1), f(2), f(3))` and :math:`g = (g(1), g(2), g(3))` be
three dimensional vectors then their sum :math:`f + g` is defined by

.. math::

   \begin{align*}
    f + g
    :=
    \left (f\left (1\right) + g \left (1\right), f(2) + g(2), f(3) + g(3)\right).\end{align*}

I.e., sum of vectors is defined by component-wise. Hence we also try to
define a sum of functions as

.. math::

   \begin{align*}
    f + g
    :=
    \left (f(x) + g(x), f(y) + g(y), \dots\right).\end{align*}

In short we define a sum by

.. math::

   \begin{align*}
    \left (f + g\right) (x)
    :=
    f(x) + g(x).\end{align*}

For scalar multiplication we set

.. math::

   \begin{align*}
    \left (\alpha f\right) (x)
    :=
    \alpha f (x).\end{align*}

Sum and scalar multiplication defined above satisfy the axioms of a
linear space. Thus we conclude a space of functions is a linear
one [2]_.

Function spaces: examples of infinite dimensional spaces
========================================================

We have infinitely many infinite dimensional objects. Examples are
weather maps and wind direction maps.

Take a point in a world map, and then there are infinitely many
directions to blow wind. In classical point of view there are infinitely
many space points, and hence there are infinitely many space points and
directions of the wind are also infinitely many patterns.

What do we represent this infinitely many probability of the wind in
real world? We use functions in several variables,
:math:`w(x,y,z,t) \in \mathbb{R}^3`. A value of a function
:math:`w(x,y,z,t)` represents a direction of wind and its strength
(length of a vector) at a space-time point
:math:`\left (x, y, z, t\right)`. We always use this type of mathematics
in physics.

Furthermore there are infinitely many types of wind distribution, i.e.,
we have infinitely many functions. For systematic thinking it is useful
to think where functions live in. This is called a function space. There
are many useful function spaces and we select a proper space as the
situation demands.

In this way, in mathematics we will encounter various types of spaces
other than a three dimensional, geometric space. We consider spaces
where functions live and ones where spaces itself live.

Linear maps, functionals
========================

We usually consider maps instead of functions in university mathematics.
In fact a map is just a function whose domain and range are general
sets. First we define a linear map and linear functional.

Assume :math:`L_1` and :math:`L_2` are linear spaces. Then a function
:math:`F \colon L_1 \to L_2` is called a map or operator. If :math:`F` preserves
linearity, i.e., :math:`F` has a property

.. math::

   \begin{align*}
     F \left (\alpha f + \beta g\right)
     =
     \alpha F(f) + \beta F(g), \quad \alpha, \beta \in \mathbb{R}, f, g \in L_1,
    \end{align*}

then an operator :math:`F` is called a linear operator.

If :math:`L_2` is :math:`\mathbb{R}` then :math:`F` is usually called a functional.
Furthermore :math:`F` is called a linear functional if it is linear.

Here are some examples.

#. Coordinate maps: Let :math:`f = (f(1), f(2), \dots, f(d)) \in \mathbb{R}^d`. We write
   a vector :math:`f = (f_1, f_2, \dots, f_d)` as
   :math:`f = (f(1), f(2), \dots, f(d))` for later use. This is just a
   notational convention. Then we get functionals by

   .. math::

      \begin{align*}
          x_i \colon f \mapsto f(i).
         \end{align*}

   This is a linear functional since this has a property

   .. math::

      \begin{align*}
          x_i \left (\alpha f + \beta g\right)
          =
          \alpha x_i \left (f\right) + \beta x_i \left (g\right).
         \end{align*}

#. Definite integrals: First we define a map :math:`I` as

   .. math::

      \begin{align*}
           I \colon
           f \mapsto \int_{\mathbb{R}^d} f(x) dx \in \mathbb{R}.
         \end{align*}

   This is a linear functional since this has a property

   .. math::

      \begin{align*}
          I \left (\alpha f + \beta g\right)
          =
          \alpha I \left (f\right) + \beta I \left (g\right).
         \end{align*}

#. Another type of a definite integral:

   .. math::
      :label: linear-algebra-and-calculus-4

      \begin{align*}
          E \colon
          f \mapsto \int_{\mathbb{R}^d} \left (\left|\nabla f(x, t)\right|^2 + \left (\frac{\partial f(x, t)}{\partial t}\right)^2\right) dx.
         \end{align*}

   This is a nonlinear functional. In physics this :math:`E` is called
   an energy functional.

#. Differential operators: Define an operator as

   .. math::

      \begin{align*}
          D \colon f \mapsto \frac{d}{dx} f.
         \end{align*}

   This is a linear operator since it satisfies

   .. math::

      \begin{align*}
          D \left (\alpha f + \beta g\right)
          =
          \alpha Df + \beta Dg.
         \end{align*}

In this way we connects linear algebra with calculus. For analysis of
nonlinear functionals we also need various linear spaces and some
technique from linear algebra.

Eigenvalues, eigenvectors
=========================

These are not learned explicitly in high school. However they sometimes
appears in entrance exams.

Let :math:`A` be a linear operator on a linear space :math:`L`. A real
number :math:`\lambda` resp. a vector :math:`f` are called an eigenvalue resp. eigenvector if
they satisfy

.. math::

   \begin{align*}
     A f = \lambda f, \quad
     f \neq 0.
    \end{align*}

Here are examples.

Let :math:`D^2` be a second order differential operator (this is linear)
with respect to time and consider

.. math::

   \begin{align*}
      m D^2 x
      =
      -k x,
     \end{align*}

i.e.,

.. math::

   \begin{align*}
      m \frac{d^2 x (t)}{dt^2}
      =
      -k x(t).
     \end{align*}

This is an equation of motion for a spring in physics. A solution
(eigenvector) is

.. math::

   \begin{align*}
      x(t)
      =
      A \sin \left (\omega t + \theta\right), \quad
      \omega
      =
      \sqrt{\frac{k}{m}}.
     \end{align*}

We can write a solution using a celebrated Euler’s formula:

.. math::

   \begin{align*}
      x(t)
      =
      A e^{i \left (\omega t + \theta\right)}.
     \end{align*}

Consideration of eigenvalues for a differential equation is somewhat
difficult and we omit it.

Mathematical application of linear algebra
==========================================

There many branches related to linear algebra. Here are some examples.
See also .

#. Theory of Lie group and its representation theory.

#. General algebra.

#. Algebraic geometry.

#. Analysis of differential equations.

#. Functional analysis.

#. Operator algebra.

Physical application
====================

There many branches related to linear algebra in physics, too.

For example, in quantum mechanics, one of the most fundamental physical
theory, linearity is important and fundamental. We say “a superposition
principle valids for wave functions,” and this “superposition” means
linearity.

In high school we learn a superposition principle for wave. This holds
because our wave equation is linear in high school.

Linear algebra and statistics
=============================

We use statistics in many branches, including humanities and sociology.
E.g., natural language processing has many humanity and information
theoretic elements. This area needs broad knowledge including
probability and statistics. Interested readers should learn, e.g.,
principal component analysis.

Linear algebra and computer science
===================================

We have applications in computer science. In numerical analysis we use
linear algebra. See the code theory or Google’s page rank for real
world application. [3]_

.. [2]
   A function space is linear if an image of its elements is a linear
   space. Function spaces can be non-linear, e.g., an image of its
   elements is a manifold or general set.

.. [3]
   See, e.g, my movies, http://www.nicovideo.jp/watch/sm7599426,
   http://www.nicovideo.jp/watch/sm10684363.
