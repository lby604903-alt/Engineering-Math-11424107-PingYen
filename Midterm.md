# Problem 2: Mechanical Engineering Case — Parachute Terminal Velocity

## 1. Problem Description
Consider an object falling through air under the influence of gravity and air resistance. Determine how its velocity \( v(t) \) changes with time.

---

## 2. Mathematical Modeling

According to Newton's Second Law:

$$
F = ma
$$

Forces acting on the object:

- Gravity: \( mg \) (downward)  
- Air resistance: \( cv \) (opposite to velocity)

Thus, the equation of motion is:

$$
m \frac{dv}{dt} = mg - cv
$$

---

## 3. Standard Form of the Differential Equation

Rewriting the equation:

$$
\frac{dv}{dt} + \frac{c}{m}v = g
$$

This is a first-order linear ordinary differential equation.

---

## 4. Solution Using Integrating Factor Method

### (1) Integrating Factor

$$
\mu(t) = e^{\int \frac{c}{m} dt} = e^{\frac{c}{m}t}
$$

---

### (2) Multiply Both Sides

$$
e^{\frac{c}{m}t} \frac{dv}{dt} + \frac{c}{m} e^{\frac{c}{m}t} v = g e^{\frac{c}{m}t}
$$

Left-hand side becomes:

$$
\frac{d}{dt} \left( e^{\frac{c}{m}t} v \right) = g e^{\frac{c}{m}t}
$$

---

### (3) Integrate Both Sides

$$
\int \frac{d}{dt} \left( e^{\frac{c}{m}t} v \right) dt = \int g e^{\frac{c}{m}t} dt
$$

Result:

$$
e^{\frac{c}{m}t} v = \frac{mg}{c} e^{\frac{c}{m}t} + C
$$

---

### (4) Solve for \( v(t) \)

$$
v(t) = \frac{mg}{c} + C e^{-\frac{c}{m}t}
$$

---

## 5. Apply Initial Condition

Assume initial velocity:

$$
v(0) = 0
$$

Substitute:

$$
0 = \frac{mg}{c} + C
$$

$$
C = -\frac{mg}{c}
$$

---

## 6. Final Solution

$$
v(t) = \frac{mg}{c} \left(1 - e^{-\frac{c}{m}t}\right)
$$

---

## 7. Analysis

### (1) Terminal Velocity

As \( t \to \infty \):

$$
v(t) \to \frac{mg}{c}
$$

---

### (2) Physical Interpretation

- Initial stage: velocity increases rapidly  
- Intermediate stage: air resistance grows  
- Long-term: velocity approaches a constant value (terminal velocity)

---

## 8. Conclusion

Using Newton’s Second Law, a first-order linear differential equation is established and solved via the integrating factor method. The solution shows that velocity increases exponentially and approaches a constant terminal velocity over time.
