# Understanding the Magnetic Levitation Device Model

## 1. Controlling the Device for Floating
The control objective for the device is to maintain the object floating in the magnetic field by
adjusting the current in the electromagnet. This floating occurs at a specific current level, 
and the control system modifies this current based on various parameters to keep the object afloat.

## 2. Model Based on Newton's Second Law
The model of the device is based on Newton's Second Law (Fg - Fm = ma), representing the primary
forces acting on the device: gravitational force (Fg) and magnetic force (Fm). No additional forces
are indicated as necessary for the model.

## 3. Magnetic Constant and Working Point
The magnetic constant varies based on the working point, which refers to specific operating conditions
such as the current and distance at which the object is maintained afloat. The concept of a single
working point implies specific conditions under which the system is analyzed.

## 4. Analysis in Steady State
In a steady state (ustaljeno stanje), all derivatives of the system's state variables are zero,
indicating no change over time. It means the system's behavior is stable and unchanging at that moment.

## 5. Purpose of the Electrical Circuit
The electrical circuit models the relationship between voltage and current in the electromagnet, 
crucial for understanding how input voltage translates to current, affecting the magnetic force 
and the system's behavior.

## 6. Model of Magnetic Constant
The magnetic constant is characteristic, dependent on the working point. It changes based on 
different intervals of distance, showing that the system's behavior varies with changes in 
operating conditions.

## 7. Sensor Model Purpose
The sensor model is necessary for transforming real-world physical measurements into digital signals. 
It is important for accurate simulation and control algorithm implementation, given the distinction 
between digital and analog signal processing.

## 8. Actuator Model
The actuator model represents the transformation of digital control signals into physical actions, 
crucial for understanding how control inputs result in physical changes in the system.

## 9. Role of electrical circuit
Electrical circuit is used as an actuator, the article provides 2 transfer functions for actuator as there is one with parameters L and R and there is another one writen based on gain and time constant, it is better to use the latter. 
