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

## Original Error Dynamics (Image 1)

The behavior of the system in terms of the error dynamics is described by the following equations, where the error `e(t)` is the difference between the system state and the reference trajectory:

- Error dynamics equation: `e_dot(t) = A*e(t) + B_u*u(t) + B_f*f(e + r, d(t)) + A*r(t) - r_dot(t)`
- Output equation: `y_e(t) = C*e(t) + C*r(t)`

## Introducing New State (Image 2)

A new state is introduced to simplify the system representation and possibly assist in the design of control laws. It encapsulates the effects of the disturbance, the reference trajectory, and the derivative of the reference:

- New state equation: `e_tilde_n+1(t) = B_f*f(x, d(t)) + A*r(t) - r_dot(t)`

## New State-Space Model (Image 3)

The error dynamics are redefined to include the new state, leading to a modified state-space model that now directly includes the disturbance effects:

- Modified error dynamics: `e_tilde_dot(t) = A_tilde*e_tilde(t) + B_u*u_tilde(t) + B_h*h(t)`
- Modified output equation: `y_e(t) = C_tilde*e_tilde(t) + C*r(t)`


