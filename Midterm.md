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

## 7. Analysis (Presentation Style)

From the answer obtained from step seven, we can observe how the velocity evolves over time.  
At the beginning, when \( t = 0 \), the exponential term is equal to 1, so the velocity starts from zero. As time increases, the exponential term e raised to the power of (-c/m · t) decreases over time.  

This causes the velocity \( v(t) \) to increase, but not indefinitely. Instead, it approaches a constant value, which is \( \frac{mg}{c} \). This value is known as the terminal velocity.  

Physically, this behavior can be explained by the balance of forces. Initially, gravity dominates, causing the object to accelerate downward. However, as the velocity increases, the air resistance \( cv \) also increases. Eventually, the air resistance becomes equal to the gravitational force, resulting in zero net force and, consequently, zero acceleration.  

At that point, the object continues to move at a constant speed, which is the terminal velocity.

---

## 8. My Conclusion 

In this problem, we started by applying Newton’s Second Law to model the motion of an object falling through air. This led to a first-order linear differential equation describing the velocity as a function of time.  

By using the integrating factor method, we derived an explicit solution for \( v(t) \). The result shows that the velocity increases exponentially at first and gradually approaches a constant value.  

This constant value, known as the terminal velocity, represents the steady-state behavior of the system when gravitational force and air resistance are balanced.  

Overall, this model effectively demonstrates how mathematical methods can be used to describe and predict real physical phenomena.
