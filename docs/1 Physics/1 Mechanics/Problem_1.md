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

#### Plot showing how the range varies with the angle of projection. As expected, the range is maximized at 45°, and it symmetrically decreases for angles above and below this value

![alt text](/docs/1%20Physics/1%20Mechanics/Projectile%20Range%20vs%20Angle%20of%20Projection.png)

#### Effect of Initial Velocity on Range: Higher initial velocity significantly increases the range, following a quadratic relationship

![alt text](/docs/1%20Physics/1%20Mechanics/Effect%20of%20Initial%20Velocity%20on%20Range.png)