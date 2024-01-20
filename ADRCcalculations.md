# Error-Based State-Space Model Derivation

## Original State-Space Model

The state-space model for a system with a disturbance factor is given by:

```latex
\begin{cases}
\dot{x} = Ax + Bu + B_f f(x, d(t)) \\
y = Cx
\end{cases}
