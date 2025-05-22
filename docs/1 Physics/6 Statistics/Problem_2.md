# Problem 2

## Estimating π Using Monte Carlo Methods  
---
## Theoretical Foundation

To estimate π using randomness, we consider a geometric probability setup.

- Draw a **square** of side length 2, centered at the origin. This square spans from $-1$ to $1$ along both the x and y axes.
- Inside this square, draw a **unit circle** (radius $r = 1$) also centered at the origin.

Now we generate random points $(x, y)$, where $x, y \in [-1, 1]$, such that the points are uniformly distributed across the square.

### Geometric Areas:

- **Area of the square**:  
$$A_{\text{square}} = 2 \times 2 = 4$$

- **Area of the unit circle**:  
$$A_{\text{circle}} = \pi \times r^2 = \pi \times 1^2 = \pi$$

The **probability** that a randomly chosen point lands **inside the circle** is given by the ratio of the areas:

$$
P(\text{inside circle}) = \frac{A_{\text{circle}}}{A_{\text{square}}} = \frac{\pi}{4}
$$

Therefore, if we generate a large number of random points and count how many fall inside the circle, we expect:

$$
\frac{\text{Points inside circle}}{\text{Total points}} \approx \frac{\pi}{4}
$$

---

## Derivation of the Estimation Formula

Given the theoretical relationship:

$$
\frac{\text{Points inside circle}}{\text{Total points}} \approx \frac{\pi}{4}
$$

We can solve for $\pi$ to get an estimate:

$$
\pi \approx 4 \times \frac{\text{Points inside circle}}{\text{Total points}}
$$

This is the core **Monte Carlo estimation formula** for π.

---

## How to Check if a Point is Inside the Circle

For any randomly generated point $(x, y)$, it lies **inside the unit circle** if:

$$
x^2 + y^2 \leq 1
$$

Thus, for each point, compute $x^2 + y^2$.  
If the result is less than or equal to 1, the point is counted as **inside the circle**.

---
