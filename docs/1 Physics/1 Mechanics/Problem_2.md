## Solution

# Theoretical Foundation for the Forced Damped Pendulum

## 1. Differential Equation Governing the Motion
The motion of the forced damped pendulum is governed by the following second-order nonlinear differential equation:

$$
\frac{d^2\theta}{dt^2} + b\frac{d\theta}{dt} + \frac{g}{L}\sin\theta = A\cos(\omega t)
$$

where:
- $$\theta(t)$$: Angular displacement of the pendulum at time $$t$$ (in radians).
- $$\frac{d^2\theta}{dt^2}$$: Angular acceleration.
- $$\frac{d\theta}{dt}$$: Angular velocity.
- $$b$$: Damping coefficient (describing resistive forces like air drag or friction).
- $$\frac{g}{L}$$: Restoring force per unit angular displacement ($$g$$ is gravitational acceleration and $$L$$ is pendulum length).
- $$A\cos(\omega t)$$: External periodic driving force with amplitude $$A$$ and angular frequency $$\omega$$.

This equation captures the combined effects of:
1. The restoring torque $$-\frac{g}{L}\sin\theta$$.
2. Damping torque $$-b\frac{d\theta}{dt}$$.
3. Driving torque $$A\cos(\omega t)$$.

---

## 2. Approximate Solutions for Small-Angle Oscillations

For small angular displacements ($$\theta \ll 1$$), we can use the small-angle approximation:

$$
\sin\theta \approx \theta
$$

Substituting this approximation into the governing equation:

$$
\frac{d^2\theta}{dt^2} + b\frac{d\theta}{dt} + \frac{g}{L}\theta = A\cos(\omega t)
$$

This is now a **linear differential equation** that can be solved analytically.

### Solution of the Linearized Equation

The solution consists of two parts:
1. **Transient Solution**: Depends on initial conditions and decays due to damping ($$b$$).
2. **Steady-State Solution**: A sinusoidal solution synchronized with the driving force.

Let the steady-state solution be:

$$
\theta(t) = \Theta \cos(\omega t - \phi)
$$

where:
- $$\Theta$$: Amplitude of oscillation.
- $$\phi$$: Phase difference between the driving force and pendulum motion.

Substitute this into the linearized equation:

$$
-\omega^2\Theta\cos(\omega t - \phi) + b\omega\Theta\sin(\omega t - \phi) + \frac{g}{L}\Theta\cos(\omega t - \phi) = A\cos(\omega t)
$$

Using trigonometric identities and matching coefficients, the amplitude $$\Theta$$ is:

$$
\Theta = \frac{A}{\sqrt{\left(\frac{g}{L} - \omega^2\right)^2 + (b\omega)^2}}
$$

and the phase difference $$\phi$$ is:

$$
\tan\phi = \frac{b\omega}{\frac{g}{L} - \omega^2}
$$

### Interpretation

- $$\Theta$$: Depends on the driving frequency $$\omega$$, damping $$b$$, and natural frequency $$\omega_0 = \sqrt{\frac{g}{L}}$$.
- $$\phi$$: Indicates how the motion lags behind the driving force.

---

## 3. Resonance Conditions and Energy Implications

### Resonance Condition

Resonance occurs when the driving frequency $$\omega$$ matches the natural frequency $$\omega_0$$:

$$
\omega = \omega_0 = \sqrt{\frac{g}{L}}
$$

At resonance, the denominator of the amplitude equation is minimized:

$$
\Theta_{\text{resonance}} = \frac{A}{b\omega_0}
$$

This results in a maximum amplitude of oscillation, limited only by damping ($$b$$).

### Implications for System's Energy

1. **Energy Transfer**: At resonance, the driving force is perfectly in phase with the pendulum's motion, allowing maximum energy transfer.
2. **Large Amplitudes**: Without damping ($$b = 0$$), the amplitude $$\Theta$$ would grow indefinitely at resonance, causing instability. However, damping dissipates energy and limits amplitude.
3. **Practical Systems**:
   - **Mechanical Systems**: Resonance can lead to catastrophic failures (e.g., bridge oscillations).
   - **Energy Harvesting**: Resonance can be exploited for efficient energy transfer in devices like pendulum-based generators.
   
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import solve_ivp

# Parameters
g = 9.81  # gravitational acceleration (m/s^2)
L = 1.0   # length of the pendulum (m)
b = 0.5   # damping coefficient
A = 1.5   # driving force amplitude
omega = 2.0  # driving force frequency

# Differential equation
def forced_damped_pendulum(t, y):
    theta, omega_dot = y
    dtheta_dt = omega_dot
    domega_dt = -(b * omega_dot + (g / L) * np.sin(theta)) + A * np.cos(omega * t)
    return [dtheta_dt, domega_dt]

# Time span and initial conditions
t_span = (0, 50)  # simulate from t=0 to t=50 seconds
t_eval = np.linspace(*t_span, 10000)  # time points for evaluation
y0 = [0.1, 0]  # initial angle (radians) and angular velocity (rad/s)

# Solve the differential equation
solution = solve_ivp(forced_damped_pendulum, t_span, y0, t_eval=t_eval, method="RK45")

# Extract results
t = solution.t
theta = solution.y[0]
omega_dot = solution.y[1]

# Plotting results
plt.figure(figsize=(12, 8))

# Time series plot
plt.subplot(3, 1, 1)
plt.plot(t, theta, label="Theta (angle)")
plt.plot(t, omega_dot, label="Angular velocity")
plt.title("Time Series of the Forced Damped Pendulum")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")
plt.legend()
plt.grid()

# Phase portrait
plt.subplot(3, 1, 2)
plt.plot(theta, omega_dot, label="Phase Portrait")
plt.title("Phase Portrait")
plt.xlabel("Theta (angle)")
plt.ylabel("Angular velocity")
plt.legend()
plt.grid()

# Poincaré section
def poincare_section(theta, omega_dot, time, period):
    poincare_theta = []
    poincare_omega = []
    for i in range(1, len(time) - 1):
        if abs(time[i] % period - 0) < (time[1] - time[0]):
            poincare_theta.append(theta[i])
            poincare_omega.append(omega_dot[i])
    return poincare_theta, poincare_omega

# Compute Poincaré section
T = 2 * np.pi / omega  # period of the driving force
poincare_theta, poincare_omega = poincare_section(theta, omega_dot, t, T)

plt.subplot(3, 1, 3)
plt.scatter(poincare_theta, poincare_omega, s=10, label="Poincaré Section", color="red")
plt.title("Poincaré Section")
plt.xlabel("Theta (angle)")
plt.ylabel("Angular velocity")
plt.legend()
plt.grid()

plt.tight_layout()
plt.show()

# Bifurcation diagram (basic setup)
def bifurcation_diagram(param_values, initial_conditions, t_span, t_eval):
    bifurcation_data = []
    for param in param_values:
        global A
        A = param  # vary the driving force amplitude
        solution = solve_ivp(forced_damped_pendulum, t_span, initial_conditions, t_eval=t_eval, method="RK45")
        theta = solution.y[0]
        time = solution.t
        # Sample theta at driving force periods
        sampled_theta = [theta[i] for i in range(len(time)) if abs(time[i] % T - 0) < (time[1] - time[0])]
        bifurcation_data.append((param, sampled_theta))
    return bifurcation_data

# Parameters for bifurcation diagram
param_values = np.linspace(0.5, 2.0, 50)  # range of A values
t_eval = np.linspace(0, 200, 20000)  # longer simulation time
bifurcation_data = bifurcation_diagram(param_values, y0, (0, 200), t_eval)

# Plot bifurcation diagram
plt.figure(figsize=(10, 6))
for param, sampled_theta in bifurcation_data:
    plt.scatter([param] * len(sampled_theta), sampled_theta, s=1, color="blue")
plt.title("Bifurcation Diagram")
plt.xlabel("Driving Force Amplitude (A)")
plt.ylabel("Theta (angle)")
plt.grid()
plt.show()

```