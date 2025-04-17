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
