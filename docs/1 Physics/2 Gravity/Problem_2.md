# Problem 2

## Cosmic Velocities: First, Second, and Third

The concept of escape velocity is crucial for understanding the conditions required to leave a celestial body's gravitational influence. Extending this concept, the first, second, and third cosmic velocities define the thresholds for orbiting, escaping, and leaving a star system. These principles underpin modern space exploration, from launching satellites to interplanetary missions.

---

## 1. First Cosmic Velocity — *Orbital Velocity*

### **Definition**:
The **first cosmic velocity** is the **minimum speed** that an object must have to **enter a stable circular orbit around a celestial body**, such as Earth, **without additional propulsion**.

### **Physical Meaning**:
- Launching an object horizontally at this speed causes it to "fall around" the planet.
- The object remains in continuous free-fall, creating an orbit.
- It is independent of the object’s mass (ignoring air resistance).

### **On Earth**:
- **Value**: ~**7.9 km/s** (≈ 28,400 km/h)
- **Altitude**: Close to Earth's surface (Low Earth Orbit)
- **Applications**: ISS, GPS satellites, other orbital spacecraft

---

## 2. Second Cosmic Velocity — *Escape Velocity*

### **Definition**:
The **second cosmic velocity** is the **minimum speed** required to **escape the gravitational field of a celestial body** without further propulsion.

### **Physical Meaning**:
- The object’s kinetic energy matches the gravitational potential energy.
- It escapes the planet’s pull and continues moving away indefinitely (ignoring other forces).

### **On Earth**:
- **Value**: ~**11.2 km/s** (≈ 40,320 km/h)
- **Applications**: Lunar missions, Mars missions, interplanetary probes

---

## 3. Third Cosmic Velocity — *Heliocentric Escape Velocity*

### **Definition**:
The **third cosmic velocity** is the **minimum speed** needed to **escape the Sun’s gravity** starting from Earth's orbit.

### **Physical Meaning**:
- A spacecraft already in solar orbit (after escaping Earth) needs this speed to **leave the Solar System**.
- It’s calculated relative to the Sun.

### **From Earth’s Orbit**:
- **Value**: ~**16.7 km/s** (≈ 60,120 km/h)
- **Applications**: Voyager 1 & 2, Pioneer, New Horizons missions

---

## Summary Table

| Cosmic Velocity | Description                        | Speed from Earth (approx.) | Used For                          |
|------------------|------------------------------------|-----------------------------|-----------------------------------|
| 1st              | Stable orbit around Earth          | ~7.9 km/s                   | Satellites, space stations        |
| 2nd              | Escape Earth's gravity             | ~11.2 km/s                  | Moon missions, interplanetary     |
| 3rd              | Escape Solar System from Earth     | ~16.7 km/s                  | Deep space probes (Voyager, etc.) |

---
# Mathematical Derivation and Parameters of Cosmic Velocities

## 1. First Cosmic Velocity (Orbital Velocity)

### Formula:
$$
v_1 = \sqrt{\frac{GM}{R}}
$$

- $v_1$: first cosmic velocity (orbital speed)  
- $G$: universal gravitational constant ($6.674 \times 10^{-11} \ \text{m}^3/\text{kg} \cdot \text{s}^2$)  
- $M$: mass of the planet (e.g., Earth)  
- $R$: radius from the center of the planet to the object  

### Derivation:
Equating **centripetal force** and **gravitational force**:

$$
\frac{mv^2}{R} = \frac{GMm}{R^2}
\Rightarrow v = \sqrt{\frac{GM}{R}}
$$

### Parameters Affecting It:
- **Mass of planet** $M$: ↑ → $v_1$ ↑  
- **Radius** $R$: ↑ → $v_1$ ↓

---

## 2. Second Cosmic Velocity (Escape Velocity)

### Formula:
$$
v_2 = \sqrt{\frac{2GM}{R}}
$$

### Derivation:
From conservation of energy:

$$
\frac{1}{2}mv^2 = \frac{GMm}{R}
\Rightarrow v = \sqrt{\frac{2GM}{R}}
$$

Relation to first velocity:

$$v_2 = \sqrt{2} \cdot v_1$$

### Parameters Affecting It:
- **Mass of planet** $M$: ↑ → $v_2$ ↑  
- **Radius** $R$: ↑ → $v_2$ ↓  
- No dependence on the object’s mass

---

## 3. Third Cosmic Velocity (Escape from Solar System)

### Formula:
From Earth’s orbit:

$$v_3 = \sqrt{v_\text{escape\_sun}^2 - v_\text{earth\_orbit}^2}$$

Or: 

$$v_3 = \sqrt{\frac{2GM_{\odot}}{r}} - v_{\text{Earth orbit}}$$

Where:  
- $M_{\odot}$: mass of the Sun  
- $r$: distance from Sun (Earth’s orbit)  
- $v_{\text{Earth orbit}}$: orbital speed of Earth (~29.78 km/s)

### Derivation:
Total mechanical energy must be zero or more to escape Sun:

$$
E = \frac{1}{2}v^2 - \frac{GM_{\odot}}{r} \ge 0
\Rightarrow v = \sqrt{\frac{2GM_{\odot}}{r}}
$$

To find additional speed needed from Earth:
$$
v_3 = \sqrt{\frac{2GM_{\odot}}{r}} - v_{\text{Earth orbit}}
$$

### Parameters Affecting It:
- **Sun's Mass** $M_{\odot}$: ↑ → $v_3$ ↑  
- **Distance from Sun** $r$: ↑ → $v_3$ ↓  
- **Launch direction**: Prograde (with Earth's orbit) is efficient

---

## General Notes

| Parameter | Influence |
|----------|-----------|
| Gravitational Constant $G$ | Constant across all calculations |
| Central Body Mass $M$ | Higher → higher required velocity |
| Distance $R$ | Higher → lower velocity needed |
| Launch Direction (for $v_3$) | Prograde launch helps; retrograde wastes energy |
| Atmosphere | Not included in these equations (ideal vacuum assumed) |

---

## Summary Table

| Cosmic Velocity | Formula | Description |
|------------------|---------|-------------|
| First ($v_1$) | $\sqrt{\frac{GM}{R}}$ | Orbit around planet |
| Second ($v_2$) | $\sqrt{\frac{2GM}{R}}$ | Escape from planet |
| Third ($v_3$) | $\sqrt{\frac{2GM_{\odot}}{r}} - v_{\text{Earth orbit}}$ | Escape Solar System |

---

# Calculating and visualizing cosmic velocities for different celestial bodies

We will calculate the **first** (orbital) and **second** (escape) cosmic velocities for:

- Earth  
- Mars  
- Jupiter

## Constants

| Parameter              | Earth                     | Mars                    | Jupiter                 |
|------------------------|---------------------------|-------------------------|-------------------------|
| Mass $M$ (kg)          | $5.972 \times 10^{24}$    | $6.417 \times 10^{23}$  | $1.898 \times 10^{27}$  |
| Radius $R$ (m)         | $6.371 \times 10^6$       | $3.390 \times 10^6$     | $6.9911 \times 10^7$    |
| Gravitational Constant $G$ | $6.674 \times 10^{-11} \ \text{m}^3/\text{kg} \cdot \text{s}^2$ | $6.674 \times 10^{-11} \ \text{m}^3/\text{kg} \cdot \text{s}^2$ | $6.674 \times 10^{-11} \ \text{m}^3/\text{kg} \cdot \text{s}^2$ |
| Gravitational Acceleration $g$ (m/s²) | 9.81                      | 3.71                    | 24.79                   |


---

## Formulas

- First Cosmic Velocity (orbital speed):

$$v_1 = \sqrt{\frac{GM}{R}}$$

- Second Cosmic Velocity (escape speed):

$$v_2 = \sqrt{\frac{2GM}{R}}$$

---

## Calculated Values

| Body     | $v_1$ (km/s) | $v_2$ (km/s) |
|----------|--------------|--------------|
| Earth    | 7.91         | 11.19        |
| Mars     | 3.55         | 5.03         |
| Jupiter  | 42.1         | 59.5         |

> Note: $v_2 = \sqrt{2} \cdot v_1$, so values are internally consistent.

---

## Visualization 

![bar chart](firsst%20and%20second%20and%20third%20cosmic%20velocities%20for%20different%20celestial%20bodies.png)

# Importance of Cosmic Velocities in Space Exploration

Cosmic velocities — **first** (orbital velocity), **second** (escape velocity), and **third** (solar system escape velocity) — are fundamental concepts in space exploration. These velocities define the speed required to achieve various milestones in the exploration of outer space.

---

## 1. **Launching Satellites**

### **First Cosmic Velocity (Orbital Velocity)**
- **Importance**: The **first cosmic velocity** is essential for **launching satellites** into orbit. To achieve orbit, a satellite must reach a **specific speed** to counteract the force of gravity while maintaining a stable orbit around Earth or another celestial body.
- **Application**: 
  - Satellites such as weather satellites, communication satellites, and GPS satellites are launched at speeds close to Earth’s orbital velocity of around **7.91 km/s**.
  - Achieving this velocity means that the satellite is in a constant state of free fall, which causes it to orbit the planet rather than fall back to the surface.
  - Without achieving the first cosmic velocity, a satellite would not be able to remain in orbit and would eventually fall back to the planet.

---

## 2. **Missions to Other Planets**

### **Second Cosmic Velocity (Escape Velocity)**
- **Importance**: The **second cosmic velocity** is crucial for **escaping Earth's gravity** or the gravity of any celestial body in order to travel to other planets, moons, or asteroids.
- **Application**:
  - For space missions such as those that travel to **Mars**, **Jupiter**, or **other planets**, rockets must exceed the **escape velocity** to break free from Earth's gravitational influence.
  - For example, Earth's escape velocity is **11.19 km/s**, which is the minimum speed required for a spacecraft to leave Earth’s gravitational field and enter interplanetary space.
  - **Spacecrafts like the Mars Rovers** (e.g., Perseverance, Curiosity) or missions to outer planets (e.g., Juno to Jupiter) require this speed to initiate their journey.

---

## 3. **Interstellar Travel (Beyond the Solar System)**

### **Third Cosmic Velocity (Solar System Escape Velocity)**
- **Importance**: The **third cosmic velocity** is required to escape not just Earth's gravity but the entire **solar system**. It represents the speed needed to overcome the Sun's gravitational pull and travel to other stars.
- **Application**:
  - The **third cosmic velocity** is currently far beyond the capabilities of modern spacecraft, as it’s approximately **42.1 km/s** (to escape from Earth’s orbit around the Sun).
  - **Interstellar probes**, such as **Voyager 1**, would need to achieve speeds close to this velocity to leave the solar system and travel toward other star systems. However, the current technology (such as chemical rockets) can only achieve velocities much lower than this, meaning practical interstellar travel is not yet possible.
  - Concepts like **nuclear propulsion** or **solar sails** may eventually allow spacecraft to reach the required speeds for interstellar travel, but this remains an area of active research.

---

## 4. **Space Exploration: Broader Implications**

### **Cost and Fuel Efficiency**
- Achieving the required cosmic velocities efficiently is crucial for the **cost-effectiveness** of space missions.
  - The higher the velocity, the more fuel is needed, especially when overcoming the **escape velocity** from Earth.
  - Future advances in propulsion technologies could potentially reduce fuel requirements, making missions to other planets and interstellar travel more feasible.

### **Mission Planning**
- **Orbital Mechanics**: Understanding these velocities helps engineers plan optimal **launch windows** and **trajectories** for missions. For example, planetary **launch windows** are based on the position of planets and the velocities required to reach them at the most efficient time.
- **Gravity Assists**: Space missions can also use **gravity assists** (slingshot maneuvers) around planets to gain additional speed without needing extra fuel, relying on the natural gravitational influences of other celestial bodies.

### **Technological Advancements**
- As technologies improve, such as **ion propulsion** or **nuclear thermal rockets**, the ability to achieve higher speeds (approaching or exceeding the third cosmic velocity) could unlock new frontiers in space exploration. Missions that were once considered far-reaching, like those to other star systems, could eventually become a reality.

---

## Summary of Cosmic Velocities' Role in Space Exploration

| Cosmic Velocity    | Purpose                        | Application | Example Missions |
|--------------------|--------------------------------|-------------|------------------|
| First ($v_1$)      | Achieve orbit around a planet  | Satellite launches, space stations | International Space Station (ISS), Hubble Space Telescope |
| Second ($v_2$)     | Escape from a planet's gravity | Missions to other planets | Mars rovers, New Horizons |
| Third ($v_3$)      | Escape the solar system       | Interstellar probes | Voyager 1, Breakthrough Starshot (future concept) |

---

### Conclusion

The first, second, and third cosmic velocities define the **fundamental thresholds** for space exploration. As we progress toward **interplanetary** and eventually **interstellar** travel, understanding and applying these velocities will remain essential for mission success, efficiency, and the expansion of humanity's presence beyond Earth.


[Google Colab](https://colab.research.google.com/drive/1ZHGjilnHYHhXESIlShsM10CCeE96TL-1?usp=sharing)