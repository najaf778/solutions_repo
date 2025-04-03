# Problem 2

## 1) Differential Equation of the Forced Damped Pendulum

The equation governing the motion of a forced damped pendulum is:

$$
\frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \sin\theta = A \cos(\omega t)
$$

where:
- $\theta(t)$ is the angular displacement,
- $b$ is the damping coefficient,
- $g$ is the acceleration due to gravity,
- $L$ is the length of the pendulum,
- $A$ is the amplitude of the external driving force,
- $\omega$ is the frequency of the external force.

This equation represents a second-order nonlinear differential equation due to the presence of $\sin\theta$.

---

## 2) Approximate Solution for Small-Angle Oscillations

For small angles ($\theta \approx 0$), we can use the small-angle approximation:

$$
\sin\theta \approx \theta
$$

This simplifies the equation to a linear form:

$$
\frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \theta = A \cos(\omega t)
$$

This is a standard damped, forced harmonic oscillator equation:

$$
\ddot{\theta} + 2\beta \dot{\theta} + \omega_0^2 \theta = A \cos(\omega t)
$$

where:
- $\omega_0 = \sqrt{\frac{g}{L}}$ is the natural frequency of the pendulum,
- $2\beta = b$ is the damping term.

### Steady-State Solution:
The particular solution to this equation takes the form:

$$
\theta_p(t) = \theta_0 \cos(\omega t - \delta)
$$

where:

$$
\theta_0 = \frac{A}{\sqrt{(\omega_0^2 - \omega^2)^2 + 4\beta^2 \omega^2}}
$$

and

$$
\tan\delta = \frac{2\beta\omega}{\omega_0^2 - \omega^2}
$$

This shows that the amplitude of oscillation depends on the driving frequency $\omega$, and the phase lag $\delta$ increases as damping increases.

---

## 3) Resonance Conditions and Energy Implications

### Resonance:
Resonance occurs when the driving frequency $\omega$ matches the natural frequency $\omega_0$, leading to a significant increase in the amplitude of oscillation.

From the amplitude formula, the response is maximized when:

$$
\omega \approx \omega_0
$$

In the presence of damping, the peak amplitude occurs at:

$$
\omega_{\text{res}} = \sqrt{\omega_0^2 - 2\beta^2}
$$

This shift in resonance frequency is a key characteristic of damped oscillators.

### Energy Considerations:
- The system continuously absorbs energy from the external force.
- In the resonance condition, the absorbed energy is maximized, leading to large oscillations.
- If damping is low, energy builds up significantly, which can lead to system failure in engineering applications (e.g., bridges, buildings, mechanical systems).
- If damping is high, the system dissipates energy efficiently, preventing large oscillations.
