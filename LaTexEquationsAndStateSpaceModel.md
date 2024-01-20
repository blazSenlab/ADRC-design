# Equations for linear model of the system:

% Saved Latex equations for later use with chat gpt
Non-linear model of moving of metal body in the system is give by these equations:
```math
F_g - F_m = ma
```
```math
mg - F_m = ma
```
```math
mg - F_m = m \frac{d^2x}{dt^2}
```
```math
Magnetic force can be calculated by this equation:
F_m = \frac{C i^2}{x^2}
```
```math
Magnetic constant is dependent on the working point, where working point is defined by parameters x and i
C = mg\frac{x_0^2}{i_0^2}
```
Equation for electric circuit, which models dependency between input voltage and current:
```math
\frac{di}{dt} = -\frac{R}{L}i(t) + \frac{1}{L}u_{RL}(t)
```
for the calculation of the linearized model we need to set a working point around which we want to linearize, working point is when all the derivatives equal to 0
```math
mg - \frac{C i^2}{x^2} = m \frac{d^2 x}{dt^2} \quad (2.11a)
```
```math
mg - \frac{C i_0^2}{x_0^2} = 0 \quad (2.11b)
```
```math
i_0 = x_0 \sqrt{\frac{mg}{C}} \quad (2.11c)
```
We linearize equation with help of the taylors sequence
```math
mg - \frac{C i^2}{x^2} = m \frac{d^2 x}{dt^2} \quad (2.12a)
```
```math
\frac{d^2 x}{dt^2} = mg - \frac{C i^2}{x^2} = f(i, x) \quad (2.12b)
```
```math
\frac{d^2 x}{dt^2} = f(i_0, x_0) + \frac{\partial f}{\partial i}\bigg|_{i_0, x_0} (i - i_0) + \frac{\partial f}{\partial x}\bigg|_{i_0, x_0} (x - x_0) \quad (2.12c)
```
```math
f(i_0, x_0) = mg - \frac{C i_0^2}{x_0^2} = 0 \quad (2.13a)
```
```math
i - i_0 = \Delta i \quad (2.13b)
```
```math
x - x_0 = \Delta x \quad (2.13c)
```
```math
\frac{\partial f}{\partial i}\bigg|_{i_0, x_0} = \alpha = -\frac{2C i_0}{x_0^2} \quad (2.13d)
```
```math
\frac{\partial f}{\partial x}\bigg|_{i_0, x_0} = \beta = \frac{2C i_0^2}{x_0^3} \quad (2.13e)
```
From the equations above we can calculate the linearized model:
```math
m \frac{d^2 \Delta x}{dt^2} = \alpha \Delta i + \beta \Delta x
```
In the first phase we define the states of the system, in our case those are speed of movement of metal body, distance of movement as the second and current as the third, 3 equations of the system are then calculated like this:
```math
\Delta \dot{v} = \frac{\alpha}{m} \Delta i + \frac{\beta}{m} \Delta x \quad (2.15a)
```
```math
\Delta \dot{x} = \Delta v \quad (2.15b)
```
```math
\Delta \dot{i} = -\frac{R}{L} \Delta i + \frac{1}{L} \Delta u \quad (2.15c)
```
from 3 equations above we can calculate state space equation, which is written as: 
```math
\begin{equation}
\begin{bmatrix}
\dot{x} \\
\dot{v} \\
\dot{i}
\end{bmatrix} = 
\begin{bmatrix}
0 & 1 & 0 \\
\frac{\beta}{m} & 0 & -\frac{\alpha}{m} \\
0 & 0 & -\frac{R}{L}
\end{bmatrix}
\begin{bmatrix}
x \\
v \\
i
\end{bmatrix} + 
\begin{bmatrix}
0 \\
0 \\
\frac{1}{L}
\end{bmatrix} u
\end{equation}
```
```math
\begin{equation}
\Delta{y} =
\begin{bmatrix}
1 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
\Delta{x} \\
\Delta{v} \\
\Delta{i}
\end{bmatrix}
\end{equation}
```
