# State-Space Model and Error Dynamics Derivation

## Original State-Space Model

The original state-space model of the system is given by the following equations:

`x_dot = Ax + Bu + Bf * f(x, d(t))`
`y = Cx`

For what each variable means check the article.

## Error Equation

`e(t) = x(t) - r(t)`
`e_dot(t) = x_dot(t) - r_dot(t)`

Substituting `x_dot(t)` from the state-space model:

`e_dot(t) = (Ax + Bu + Bf * f(x, d(t))) - r_dot(t)`

Then we get:

`e_dot(t) = A*(e + r) + B*u + Bf * f(e + r, d(t)) - r_dot(t)`

Expanding the terms gives us the error dynamics:

`e_dot(t) = A*e(t) + B*u(t) + Bf * f(e + r, d(t)) + A*r(t) - r_dot(t)`
`y_e(t) = C*e(t) + C*r(t)`

"Given a state-space model with matrices A, B, and C, control input u, and disturbance function f depending on the state x and a disturbance d(t), derive the error dynamics equations when the error e(t) is defined as the difference between the system's state x(t) and a reference trajectory r(t). Please show all the steps involved in the derivation."

Make sure to replace the matrices A, B, and C, the control input u, and the disturbance function f with the specific values or functions from your system when you provide them to ChatGPT.

% Original Error Dynamics (Image 1)
% These equations represent the behavior of the system in terms of the error dynamics, where the error is the difference between the system state and the reference trajectory.
\begin{equation}
\begin{cases}
\dot{e}(t) = Ae(t) + B_{u}u(t) + B_{f}f(e + r, d(t)) + Ar(t) - \dot{r}(t) \\
y_{e}(t) = Ce(t) + Cr(t)
\end{cases}
\end{equation}

% Introducing New State (Image 2)
% A new state is introduced to encapsulate the effects of the disturbance, the reference trajectory, and the derivative of the reference. This helps in simplifying the system representation and possibly in the design of control laws.
\begin{equation}
\tilde{e}_{n+1}(t) = B_{f}f(x, d(t)) + Ar(t) - \dot{r}(t)
\end{equation}
% Here, \tilde{e}_{n+1}(t) is denoted as h(t) to simplify the notation.

% New State-Space Model (Image 3)
% The error dynamics are redefined to include the new state, leading to a modified state-space model. This model now includes the disturbance effects directly in the state representation.
\begin{equation}
\begin{cases}
\dot{\tilde{e}}(t) = \tilde{A}\tilde{e}(t) + B_{u}\tilde{u}(t) + B_{h}h(t) \\
y_{e}(t) = \tilde{C}\tilde{e}(t) + Cr(t)
\end{cases}
\end{equation}

% The notation \tilde{A}, \tilde{C}, and B_{h} represents the modified system matrices to include the effects of the new state h(t).

