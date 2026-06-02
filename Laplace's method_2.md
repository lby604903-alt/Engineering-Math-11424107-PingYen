# Solving a Second-Order Differential Equation Using Laplace Transform

## Problem Statement

Solve the following differential equation using the Laplace Transform:

\[
2\frac{d^2x}{dt^2}+7\frac{dx}{dt}+3x=0
\]

with the initial conditions

\[
x(0)=0,\qquad x'(0)=1
\]

---

## Step 1: Apply the Laplace Transform

Let

\[
X(s)=\mathcal{L}\{x(t)\}
\]

Using the Laplace transform formulas:

\[
\mathcal{L}\{x'(t)\}=sX(s)-x(0)
\]

\[
\mathcal{L}\{x''(t)\}=s^2X(s)-sx(0)-x'(0)
\]

Substituting the initial conditions:

\[
x(0)=0,\qquad x'(0)=1
\]

gives

\[
\mathcal{L}\{x''(t)\}=s^2X(s)-1
\]

and

\[
\mathcal{L}\{x'(t)\}=sX(s)
\]

Substitute these into the differential equation:

\[
2(s^2X(s)-1)+7sX(s)+3X(s)=0
\]

---

## Step 2: Solve for \(X(s)\)

Expand and simplify:

\[
2s^2X(s)-2+7sX(s)+3X(s)=0
\]

Factor out \(X(s)\):

\[
X(s)(2s^2+7s+3)=2
\]

Thus,

\[
X(s)=\frac{2}{2s^2+7s+3}
\]

Factor the denominator:

\[
2s^2+7s+3=(2s+1)(s+3)
\]

Therefore,

\[
X(s)=\frac{2}{(2s+1)(s+3)}
\]

---

## Step 3: Partial Fraction Decomposition

Assume

\[
\frac{2}{(2s+1)(s+3)}
=
\frac{A}{2s+1}
+
\frac{B}{s+3}
\]

Multiplying both sides by \((2s+1)(s+3)\):

\[
2=A(s+3)+B(2s+1)
\]

Expand:

\[
2=(A+2B)s+(3A+B)
\]

Comparing coefficients:

\[
A+2B=0
\]

\[
3A+B=2
\]

From the first equation:

\[
A=-2B
\]

Substitute into the second equation:

\[
3(-2B)+B=2
\]

\[
-5B=2
\]

\[
B=-\frac{2}{5}
\]

\[
A=\frac{4}{5}
\]

Thus,

\[
X(s)=
\frac{\frac{4}{5}}{2s+1}
-
\frac{\frac{2}{5}}{s+3}
\]

Rewrite the first term:

\[
\frac{\frac{4}{5}}{2s+1}
=
\frac{2}{5}\cdot\frac{1}{s+\frac{1}{2}}
\]

Therefore,

\[
X(s)
=
\frac{2}{5}\frac{1}{s+\frac{1}{2}}
-
\frac{2}{5}\frac{1}{s+3}
\]

---

## Step 4: Apply the Inverse Laplace Transform

Using

\[
\mathcal{L}^{-1}
\left\{
\frac{1}{s+a}
\right\}
=
e^{-at}
\]

we obtain

\[
x(t)
=
\frac{2}{5}e^{-t/2}
-
\frac{2}{5}e^{-3t}
\]

Factor out \(\frac{2}{5}\):

\[
\boxed{
x(t)=\frac{2}{5}
\left(
e^{-t/2}-e^{-3t}
\right)
}
\]

---

## Verification

### Check \(x(0)\)

\[
x(0)
=
\frac{2}{5}(1-1)
=
0
\]

### Check \(x'(0)\)

Differentiate:

\[
x'(t)
=
-\frac{1}{5}e^{-t/2}
+
\frac{6}{5}e^{-3t}
\]

Substitute \(t=0\):

\[
x'(0)
=
-\frac{1}{5}
+
\frac{6}{5}
=
1
\]

Both initial conditions are satisfied.

---

## Final Answer

\[
\boxed{
x(t)=\frac{2}{5}
\left(
e^{-t/2}-e^{-3t}
\right)
}
\]
