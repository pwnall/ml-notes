# Limits

The concept of a **limit** in calculus addresses the behavior of a function
close to a particular input.

Informally, a function $f(x)$ has a limit $L$ as $x$ approaches a value $a$ if
$f(x)$ gets arbitrarily close to $L$ as $x$ gets sufficiently close to $a$.  The
value of the function at $a$, $f(a)$, does not matter when determining the
limit.

The information above is lifted from
[a Wikipedia article](https://en.wikipedia.org/wiki/Limit_of_a_function).

## Formal definitions

The informal definition of a limit is made precise by the
[($\epsilon, \delta$)-definition](https://en.wikipedia.org/wiki/(%CE%B5,_%CE%B4)-definition_of_a_limit),
which is presented below.

### Two-sided limit

The statement $\lim_{x \to a} f(x) = L$ is read as "the limit of $f(x)$ as $x$
approaches $a$ is $L$". The statement is formally defined as:

$$
\forall \epsilon > 0,
\exists \delta > 0 \text{ s.t. }
0 < |x - a| < \delta \implies |f(x) - L| < \epsilon
$$

The definition can be understood as a challenge-response game. An opponent
challenges us with a small positive number $\epsilon$, which represents the
desired closeness to the limit $L$. We must produce a small positive number
$\delta$, which represents the required closeness to the point $a$. If we can
always produce a $\delta$ for any given $\epsilon$, the limit exists.

### One-sided limits

The statement $\lim_{x \to a^+} f(x) = L$ is read as "the limit of $f(x)$ as $x$
approaches $a$ from the right is $L$". The statement is defined as:

$$
\forall \epsilon > 0,
\exists \delta > 0 \text{ s.t. }
0 < x - a < \delta \implies |f(x) - L| < \epsilon
$$

The statement $\lim_{x \to a^-} f(x) = L$ is read as "the limit of $f(x)$ as $x$
approaches $a$ from the left is $L$". The statement is defined as:

$$
\forall \epsilon > 0,
\exists \delta > 0 \text{ s.t. }
-\delta < x - a < 0 \implies |f(x) - L| < \epsilon
$$

One-sided limits consider the behavior of the function as $x$ approaches $a$
from only one side. The same challenge-response game applies, but the closeness
condition on $x$ is restricted to one side of $a$.

### Relationship

The two-sided limit exists if and only if both one-sided limits exist and are
equal.

$$
\lim_{x \to a} f(x) = L \iff
\lim_{x \to a^+} f(x) = L \text{ and } \lim_{x \to a^-} f(x) = L
$$
