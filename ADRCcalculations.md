# Error-Based State-Space Model Derivation

## Original State-Space Model

The state-space model for a system with a disturbance factor is given by:

```math
\begin{cases}
\dot{x} = Ax + Bu + B_f f(x, d(t)) \\
y = Cx
\end{cases}
```
The error is defined as the difference between the state and the reference:

```math
e(t) = x(t) - r(t)
```
Derivative of an error is:

```math
\dot{e}(t) = \dot{x}(t) - \dot{r}(t)
```
We can substitute in derivative x_dot(t) from the original state space model:
```math
\dot{e}(t) = Ax + Bu + B_f f(x, d(t)) - \dot{r}(t)
```
then we express x as r + e:
```math
\dot{e}(t) = A(e + r) + Bu + B_f f(e + r, d(t)) - \dot{r}(t)
```
final error based form:
```math
\begin{cases}
\dot{e}(t) = Ae + Bu_u + B_f f(e + r, d(t)) + Ar - \dot{r}(t) \\
y(t) = Ce + Cr
\end{cases}
```
Next step was to generate a new state that takes into account disturbance and other factors like change in idk what doesnt matter, these are the equations: 
```math
\text{Let } e_{n+1}(t) = h(t) \text{, then the new state-space model is:}
```
```math
\begin{align*}
\dot{\tilde{e}}(t) &= \tilde{A}\tilde{e}(t) + \tilde{B}_u u(t) + B_h h \\
v(t) &= \tilde{C}\tilde{e}(t) + Cr(t)
\end{align*}
```
% Defining h(t)
```math
\text{Where } h(t) = B_f f(e(t) + r(t), d(t)) + Ar(t) - \dot{r}(t) \text{.}
```
From this state space equation generalized ESO is designed, this is the equation: 
```math
\dot{\hat{e}}(t) = \tilde{A}\hat{e}(t) + \tilde{B}_u u(t) + L\big(y(t) - \tilde{C}\hat{e}(t) - C r(t)\big)
```
