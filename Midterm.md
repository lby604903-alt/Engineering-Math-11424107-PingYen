# My Midterm Report : Calculating the terminal velocity of a parachute.

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
## 1. Problem Understanding (What are we trying to describe?)

We are analyzing an object falling through air.  
The goal is to understand how its velocity changes over time under the influence of gravity and air resistance.

---

## 2. Problem Solving Basis (Mathematical Modeling)

To describe the motion scientifically, we start from Newton’s Second Law:

$$
F = ma
$$

Now we identify the forces acting on the object:

- Gravity: \( mg \), pulling the object downward  
- Air resistance: \( cv \), opposing the motion  

By combining these forces, we construct the governing equation of motion:

$$
m \frac{dv}{dt} = mg - cv
$$

---

## 3. Bringing the Model into a Solvable Form (Rewriting the Equation)

To make the equation easier to solve, we rearrange it into a standard mathematical form:

$$
\frac{dv}{dt} + \frac{c}{m}v = g
$$

At this stage, we recognize that this is a first-order linear differential equation, which has a known solution method.

---

## 4. Solving Strategy (Using an Analytical Method)

To solve the equation systematically, we apply the integrating factor method.

### Step 1: Construct the integrating factor

The integrating factor is:

$$
\mu(t) = e^{\frac{c}{m}t}
$$

---

### Step 2: Transform the equation

Multiplying both sides by the integrating factor gives:

$$
e^{\frac{c}{m}t} \frac{dv}{dt} + \frac{c}{m} e^{\frac{c}{m}t} v = g e^{\frac{c}{m}t}
$$

This can be rewritten as a single derivative:

$$
\frac{d}{dt} \left( e^{\frac{c}{m}t} v \right) = g e^{\frac{c}{m}t}
$$

---

### Step 3: Integrate both sides

We integrate both sides with respect to time:

$$
\int \frac{d}{dt} \left( e^{\frac{c}{m}t} v \right) dt = \int g e^{\frac{c}{m}t} dt
$$

This yields:

$$
e^{\frac{c}{m}t} v = \frac{mg}{c} e^{\frac{c}{m}t} + C
$$

---

### Step 4: Solve for velocity function

Rearranging gives the general solution:

$$
v(t) = \frac{mg}{c} + C e^{-\frac{c}{m}t}
$$

---

## 5. Applying Initial Condition (What happens at the start?)

We assume the object starts from rest:

$$
v(0) = 0
$$

Substituting into the equation:

$$
0 = \frac{mg}{c} + C
$$

So we obtain:

$$
C = -\frac{mg}{c}
$$

---

## 6. Final Result (The complete solution)

Substituting the constant back gives the final velocity function:

$$
v(t) = \frac{mg}{c} \left(1 - e^{-\frac{c}{m}t}\right)
$$
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
