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

## 7. Analysis (Discussion Format)

**Student:** What happens to the velocity as time increases?  

**Instructor:** As time goes on, the exponential term \( e^{-\frac{c}{m}t} \) decreases toward zero. This means the velocity gradually approaches a constant value.  

**Student:** What is that constant value?  

**Instructor:** It is \( \frac{mg}{c} \), which is called the terminal velocity.  

**Student:** Why doesn’t the object keep accelerating?  

**Instructor:** Because as velocity increases, the air resistance \( cv \) also increases. Eventually, it balances the gravitational force \( mg \), resulting in zero net force and no further acceleration.  

**Student:** So the motion stabilizes over time?  

**Instructor:** Exactly. The object starts by accelerating, then slows its acceleration, and finally moves at a constant speed.

---

## 8. Conclusion (Discussion Format)

**Student:** So what is the main takeaway from this problem?  

**Instructor:** The key idea is that we used Newton’s Second Law to model the motion and obtained a first-order linear differential equation.  

**Student:** And how did we solve it?  

**Instructor:** We applied the integrating factor method to find an explicit expression for velocity as a function of time.  

**Student:** What does the solution tell us physically?  

**Instructor:** It shows that the velocity increases exponentially at first and then approaches a constant terminal velocity.  

**Student:** So this model explains real falling motion in air?  

**Instructor:** Yes, it captures the essential behavior of objects falling with air resistance.
