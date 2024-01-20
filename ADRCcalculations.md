# Error-Based State-Space Model Derivation

## Original State-Space Model

The state-space model for a system with a disturbance factor is given by:

```math
\begin{cases}
\dot{x} = Ax + Bu + B_f f(x, d(t)) \\
y = Cx
\end{cases}

The error is defined as the difference between the state and the reference:

e(t) = x(t) - r(t)

Derivative of an error is:

\dot{e}(t) = \dot{x}(t) - \dot{r}(t)

We can substitute in derivative x_dot(t) from the original state space model:

\dot{e}(t) = Ax + Bu + B_f f(x, d(t)) - \dot{r}(t)

then we express x as r + e:

\dot{e}(t) = A(e + r) + Bu + B_f f(e + r, d(t)) - \dot{r}(t)

final error based form:

\begin{cases}
\dot{e}(t) = Ae + Bu_u + B_f f(e + r, d(t)) + Ar - \dot{r}(t) \\
v(t) = Ce + Cr
\end{cases}
