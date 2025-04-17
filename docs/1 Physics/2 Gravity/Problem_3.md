# Problem 3

#  Trajectories of a Freely Released Payload Near Earth

When a payload is released from a moving rocket near Earth, it follows a trajectory determined by its **initial velocity** and **Earth's gravitational pull**. The paths are described by **conic sections** and depend on the **total mechanical energy** of the payload.

---

##  Orbital Trajectories Overview

| Type         | Condition (Total Energy)            | Description                                   |
|--------------|-------------------------------------|-----------------------------------------------|
| **Elliptical** | $E < 0$                             | Bound orbit — the object stays around Earth.  |
| **Parabolic**  | $E = 0$                             | Escape trajectory — barely escapes gravity.   |
| **Hyperbolic** | $E > 0$                             | Escape trajectory — escapes Earth permanently.|

---

##  Total Mechanical Energy Formula

$$
E = \frac{1}{2}mv^2 - \frac{GMm}{r}
$$

Where:  
- $m$: mass of payload  
- $v$: velocity at release  
- $G$: gravitational constant  
- $M$: mass of Earth  
- $r$: distance from Earth's center  

---

## 1. Elliptical Trajectory

- **Condition**: $v < v_{esc}$  
- **Path**: Closed orbit  
- **Use Case**: Satellites, orbital payloads  

---

## 2. Parabolic Trajectory

- **Condition**: $v = v_{esc} = \sqrt{\frac{2GM}{r}}$  
- **Path**: Open curve — marginal escape  
- **Use Case**: Theoretical edge case  

---

## 3. Hyperbolic Trajectory

- **Condition**: $v > v_{esc}$  
- **Path**: Open curve — permanent escape  
- **Use Case**: Deep space missions, escape from Earth  

---
##  4. Sub-Orbital (Ballistic) Trajectory

- **Condition**: Low horizontal speed, released in or near atmosphere  
- **Path**: Parabolic, short-lived path  
- **Use Case**: Missiles, test launches, re-entry capsules  

---

## Summary

- **Elliptical**: Object stays bound to Earth.  
- **Parabolic**: Perfect escape speed — ideal case.  
- **Hyperbolic**: Exceeds escape velocity — leaves Earth.  
- **Sub-orbital**: Follows a curved trajectory back to Earth (if low speed and low altitude).

## Numerical Analysis: Modeling the Motion of a Payload

### Gravitational Force
The motion of the payload is determined by the gravitational force exerted by the Earth. According to Newton's Law of Universal Gravitation:

$$
F = -\frac{G M m}{r^2} \hat{r}
$$

Where:
- $G$ is the gravitational constant ($6.674 \times 10^{-11} \, \text{m}^3 \, \text{kg}^{-1} \, \text{s}^{-2}$)
- $M$ is the mass of Earth ($5.972 \times 10^{24} \, \text{kg}$)
- $m$ is the mass of the payload
- $r$ is the radial distance from the center of the Earth
- $\hat{r}$ is the unit vector pointing from Earth toward the payload

Using Newton's Second Law of Motion, $F = ma$, we derive the equation of motion as:

$$
\frac{d^2 r}{dt^2} = -\frac{G M r}{r^3}
$$

### Numerical Integration Approach
To solve this second-order differential equation, we employ the **Runge-Kutta 4th Order (RK4)** method. This method provides a higher level of accuracy than the simpler Euler method. We transform the second-order differential equation into a system of first-order equations:

$$
\frac{d r}{dt} = v, \quad \frac{d v}{dt} = -\frac{G M r}{r^3}
$$

### Initial Conditions
- **Initial Position**: The payload begins at an altitude of 500 km above the Earth's surface. Thus, the initial radial distance is $r_0 = R_{\text{Earth}} + 500 \, \text{km}$.
- **Initial Velocity**: The initial velocity is adjustable to achieve different types of trajectories, such as elliptical, parabolic, or hyperbolic paths.

## Relating Trajectories to Orbital Insertion, Reentry, and Escape

### 1. **Orbital Insertion (Elliptical/Circular Trajectories)**
- **When?** A payload is released with just the right tangential velocity.
- **What happens?** It enters a **closed orbit** (circular or elliptical) around Earth.
- **Conditions:**
  - Velocity is less than escape speed, but enough to counteract gravity.
  - Total energy $E < 0$ (negative specific orbital energy).
- **Used in:**
  - Satellites
  - Space stations
  - Parking orbits before interplanetary maneuvers

**Example:**
$$v_{\text{circular}} = \sqrt{\frac{GM}{r}} \approx 7.7 \, \text{km/s at 300 \, \text{km altitude}}$$

---

### 2. **Reentry (Suborbital or Decaying Orbit)**
- **When?** A payload is released with **too little velocity** or enters a **degrading orbit**.
- **What happens?** Gravity pulls it back to Earth — a **suborbital arc** or **spiral reentry** (with drag).
- **Conditions:**
  - Velocity is not enough for stable orbit.
  - Path intersects Earth’s surface.
- **Used in:**
  - Space capsules (Apollo, Soyuz)
  - Test reentry vehicles
  - Ballistic missile trajectories

**Visual Signature:** Curved path arcing back into Earth like a parabola or short ellipse.

---

### 3. **Escape (Hyperbolic Trajectory)**
- **When?** The payload is released with **escape velocity** or higher.
- **What happens?** The object breaks free of Earth’s gravity and **escapes into space**.
- **Conditions:**
  - $v \geq \sqrt{\frac{2GM}{r}}$
  - Total energy $E \geq 0$
- **Used in:**
  - Deep space missions (Voyager, New Horizons)
  - Interplanetary probes
  - Earth-departing payloads

**Example:**
$$v_{\text{escape}} \approx 11.2 \, \text{km/s at sea level}$$

---

## Summary Table

| Scenario          | Trajectory Type         | Speed (approx)  | Use Case                      |
|-------------------|--------------------------|------------------|-------------------------------|
| Orbital Insertion | Elliptical/Circular     | ~7.7 km/s        | Satellites, ISS               |
| Reentry           | Suborbital              | < 7.7 km/s       | Capsules, ballistic missiles  |
| Escape            | Hyperbolic              | > 11.2 km/s      | Deep space missions           |
