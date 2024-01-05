# Active Disturbance Rejection Control (ADRC) Summary

This document summarizes key points from our conversation regarding the design of Active Disturbance Rejection Control (ADRC), particularly focusing on the mathematical model and components of ADRC as described in the referenced article.

## Overview of ADRC Design

Active Disturbance Rejection Control (ADRC) is a control strategy that effectively handles uncertainties and disturbances in a system. The ADRC approach, as detailed in the article, emphasizes the use of an error-based state equation, a linearized model for controller design, and incorporates non-linearities and uncertainties through an Extended State Observer.

### Key Components of ADRC

1. **Error-Based State Equation**: 
   - Simplifies the ADRC structure.
   - Transforms the state equation of the system into an error-based form.
   - Makes the reference signal constant, simplifying control objectives.

2. **Linearized Model for Controller Design**:
   - The controller is designed using the Linear Quadratic (LQ) method.
   - Based on a linearized model, indicating that the system dynamics are approximated to a linear form for controller design purposes.

3. **Generalized Extended State Observer (GESO)**:
   - Estimates the non-linear part, model uncertainty, and external disturbance.
   - These are collectively regarded as "total disturbance."
   - Indicates that while the controller design is based on a linearized model, the system's non-linearities and uncertainties are considered in the disturbance estimation process.

4. **Lyapunov Stability Theory for Disturbance Compensator Design**:
   - Used to design the disturbance compensator in the ADRC.
   - Ensures that the derivative of the Lyapunov function is negative definite to decrease the function more quickly, thereby enhancing the convergence rate of ADRC.

### Mathematical Model Requirements for ADRC

- **Linear vs. Non-linear Models**:
  - The choice depends on the system characteristics.
  - Linear models are simpler and suitable for LQ method applications.
  - Non-linear models are more appropriate for systems with pronounced non-linear behaviors.
  - ADRC's methodology can accommodate both linear and non-linear models.

- **Time Dependency**:
  - Time-invariant models are generally used unless the system explicitly depends on time.
  - Choose between discrete or continuous time models based on the data sampling or control implementation nature.

- **Inclusion of Disturbances and Uncertainties**:
  - Essential for ADRC, as it focuses on rejecting disturbances and handling uncertainties.
  - Model should estimate or measure disturbances impacting the system.

- **Model Validation**:
  - Crucial to validate the model against real-world data or through experiments for accuracy.

- **Iterative Approach**:
  - Start with a simple model, validate it, and refine as needed based on experimental data or further analysis.

## Conclusion

The ADRC design, as described in the article, provides a comprehensive approach for handling disturbances and uncertainties in control systems. The emphasis on using a linearized model for controller design, along with considerations for non-linearities and uncertainties through GESO and Lyapunov stability theory, makes ADRC a versatile and effective control strategy.

