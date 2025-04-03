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
