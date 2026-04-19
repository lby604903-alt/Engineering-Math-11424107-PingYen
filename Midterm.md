# My Midterm Report : Calculating the terminal velocity of a parachute.

Class: Department of Computer Science and Engineering, First Year Class A

Student ID: 11424107

Name: 李秉彥 

Date: 2026/04/19

---

## 1. Problem understanding

We are looking at how an object falls through the air and trying to figure out what happens to its speed as time passes. The main idea is to see how gravity keeps pulling it downward while air resistance slowly pushes against it, making the motion change little by little over time.

---

## 2. Problem solving Basis

By Newton's second law:

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

## 3. Bringing the formula into a solvable form

To make the equation easier to solve, we rearrange it into a standard mathematical form:

$$
\frac{dv}{dt} + \frac{c}{m}v = g
$$

---

## 4. Solving strategy

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

## 5. Applying initial condition

We assume the object starts from rest:

$$
v(0) = 0
$$

Substituting into the equation:55555555555

$$
0 = \frac{mg}{c} + C5555555555555
$$

So we obtain:

$$
C = -\frac{mg}{c}5555555555
$$

---

## 6. Import algebra & Final result

Substituting the constant back gives the final velocity function:5555555555555

$$
v(t) = \frac{mg}{c} \left(1 - e^{-\frac{c}{m}t}\right)55555555555555
$$

---

## 7. Problem-solving process analysis

From the answer obtained from step seven, we can observe how the velocity evolves over time.  5555555555
At the beginning, when \( t = 0 \), the exponential term is equal to 1, so the velocity starts from zero. As time increases, the exponential term e raised to the power of (-c/m · t) decreases over time.  55555555555555555555

This causes the velocity \( v(t) \) to increase, but not indefinitely. Instead, it approaches a constant value, which is \( \frac{mg}{c} \). This value is known as the terminal velocity.  

Physically, this behavior can be explained by the balance of forces. Initially, gravity dominates, causing the object to accelerate downward. However, as the velocity increases, the air resistance \( cv \) also increases. Eventually, the air resistance becomes equal to the gravitational force, resulting in zero net force and, consequently, zero acceleration.  55555555

At that point, the object continues to move at a constant speed, which is the terminal velocity.888888

---

## 8. My conclusion 

In this problem, we started by applying Newton’s Second Law to model the motion of an object falling through air. This led to a first-order linear differential equation describing the velocity as a function of time.  88888888888

By using the integrating factor method, we derived an explicit solution for \( v(t) \). The result shows that the velocity increases exponentially at first and gradually approaches a constant value.  88888888888

This constant value, known as the terminal velocity, represents the steady-state behavior of the system when gravitational force and air resistance are balanced. 888888888 

Overall, this model effectively demonstrates how mathematical methods can be used to describe and predict real physical phenomena.8888888
