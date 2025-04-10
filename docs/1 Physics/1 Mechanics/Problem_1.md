# Problem 1

## Theoretical Foundation of Projectile Motion

### **Step 1: Deriving the Governing Equations**
Projectile motion is governed by Newton’s Second Law:

$$
\vec{F} = m\vec{a}
$$

For a projectile in freefall (neglecting air resistance), the only force acting on it is gravity, acting downward:

$$
F_y = -mg, \quad F_x = 0
$$

This results in the following equations of motion:

$$
m \frac{d^2 x}{dt^2} = 0
$$

$$
m \frac{d^2 y}{dt^2} = -mg
$$

Dividing by $m$ and integrating twice:

#### **1. Horizontal Motion**
- $\frac{d^2x}{dt^2} = 0$ ⟶ First integration ⟶ $\frac{dx}{dt} = v_{0x}$ (constant)
- Second integration ⟶ $x = v_{0x} t + x_0$

Since $v_{0x} = v_0 \cos\theta$, we get:

$$
x = v_0 \cos\theta \cdot t
$$

#### **2. Vertical Motion**
- $\frac{d^2y}{dt^2} = -g$ ⟶ First integration ⟶ $\frac{dy}{dt} = -gt + v_{0y}$
- Second integration ⟶ $y = -\frac{1}{2}gt^2 + v_{0y} t + y_0$

Since $v_{0y} = v_0 \sin\theta$, we get:

$$
y = -\frac{1}{2}gt^2 + v_0 \sin\theta \cdot t + y_0
$$

### **Step 2: Family of Solutions Due to Initial Conditions**
The key initial conditions influencing projectile motion are:
- **Initial velocity ($v_0$)**: A higher velocity results in a longer range and greater height.
- **Angle of launch ($\theta$)**: The range depends on $\sin 2\theta$, peaking at $\theta = 45^\circ$.
- **Initial height ($y_0$)**: A nonzero height alters flight time and can extend range.

By varying these parameters, we obtain different trajectories, illustrating how a simple equation generates a rich set of solutions.

## Practical Applications of Projectile Motion

### 1. **Uneven Terrain**
When the projectile is launched on uneven terrain (with different launch and landing heights), the vertical motion equation becomes:

$$y = y_0 + v_0 \sin\theta \cdot t - \frac{1}{2} g t^2$$

To find the range, we solve for the time when $y = 0$, which may require solving a quadratic equation.

### 2. **Air Resistance**
Air resistance modifies the trajectory, causing the projectile to deviate from the ideal parabolic path. The drag force is given by:

$$\vec{F}_d = - \frac{1}{2} C_d \rho A v^2 \hat{v}$$

This force alters the equations of motion, resulting in non-linear differential equations that require numerical methods to solve.

### 3. **Launch Angle and Velocity Adaptations**
Real-world factors like wind and non-uniform gravity affect launch angles and velocities. For example, wind can alter both the horizontal and vertical motion of the projectile.

### 4. **Example Applications**
- **Sports**: In soccer or basketball, air resistance affects ball trajectories.
- **Ballistics**: Air resistance and gravity are crucial for calculating missile trajectories.
- **Space Exploration**: Rockets need to account for changing gravity and air resistance.
- **Engineering**: Calculating trajectories for demolition charges requires adjustments for terrain and air resistance.

### 5. **Numerical Solutions**
For complex scenarios (e.g., air resistance), numerical methods like Euler’s method or Runge-Kutta are used to approximate the motion.

## Analysis of the Range

## Horizontal Range and Angle of Projection

The *horizontal range* $R$ of a projectile is the horizontal distance it travels before returning to the same vertical level from which it was launched (i.e., when $y = y_0$).

For a projectile launched from ground level ($y_0 = 0$), the total time of flight $T$ is given by:

$$
T = \frac{2 v_0 \sin \theta}{g}
$$

The horizontal range is then:

$$
R = v_0 \cos \theta \cdot T = v_0 \cos \theta \cdot \frac{2 v_0 \sin \theta}{g}
$$

Simplifying:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

This formula shows a clear dependency on the *angle of projection*:

- The range is *maximum* when $\sin(2\theta) = 1$, which occurs at $2\theta = 90^\circ \Rightarrow \theta = 45^\circ$.
- The function $\sin(2\theta)$ is symmetric about $\theta = 45^\circ$, meaning:
  - $R(30^\circ) = R(60^\circ)$
  - $R(10^\circ) = R(80^\circ)$, etc.

---

## Influence of Other Parameters

### 1. Initial Velocity $v_0$

From the range equation:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

- The range increases *quadratically* with $v_0$.
- Doubling the velocity *quadruples* the range.
- Higher velocity = longer flight time and faster horizontal travel.

### 2. *Gravitational Acceleration $g$*

- The range is *inversely proportional* to $g$.
- On planets with weaker gravity (e.g., the Moon), the same projectile would travel much farther.
- Example:
  - On Earth: $g \approx 9.8\, \text{m/s}^2$
  - On Moon: $g \approx 1.6\, \text{m/s}^2 \Rightarrow R_{\text{moon}} \approx 6.1 \times R_{\text{earth}}$

---

## Summary

- The range depends on the angle of projection via the term $\sin(2\theta)$.
- It is *maximum at 45°* and symmetric around it.
- Increasing *initial velocity* extends range significantly.
- Decreasing *gravity* also increases range.

These insights show how adjusting launch conditions can precisely control the motion of a projectile — a principle used in everything from sports to space travel.

#### Plot showing how the range varies with the angle of projection. As expected, the range is maximized at 45°, and it symmetrically decreases for angles above and below this value

![alt text](Projectile%20Range%20vs%20Angle%20of%20Projection.png)

#### Effect of Initial Velocity on Range: Higher initial velocity significantly increases the range, following a quadratic relationship

![alt text](Effect%20of%20Initial%20Velocity%20on%20Range.png)

#### Effect of Gravity on Range: Weaker gravity (e.g., on the Moon) allows for much longer travel distances, while stronger gravity (e.g., on Jupiter) greatly reduces the range.

![alt text](Effect%20of%20Gravity%20on%20Range.png)

## Conslusion

The study of projectile motion, particularly its range and dependence on parameters like launch angle, velocity, and gravity, provides essential insights into a variety of real-world phenomena. By understanding these relationships, we can optimize motion for practical applications, from sports to space exploration


[Google Colab](https://colab.research.google.com/drive/1-I-A9Pedj6hjRlk3durAIV-ijCtRUuiA?usp=sharing)