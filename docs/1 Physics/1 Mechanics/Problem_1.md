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