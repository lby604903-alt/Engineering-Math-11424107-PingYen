# Solving a Second-Order Differential Equation Using Laplace Transform

## Problem Statement

Solve the differential equation:

```text
2x'' + 7x' + 3x = 0
```

with initial conditions:

```text
x(0) = 0
x'(0) = 1
```

---

## Step 1: Apply the Laplace Transform

Let

```text
X(s) = L{x(t)}
```

Using the Laplace transform properties:

```text
L{x'(t)}  = sX(s) - x(0)
L{x''(t)} = s²X(s) - sx(0) - x'(0)
```

Substituting the initial conditions:

```text
x(0) = 0
x'(0) = 1
```

gives

```text
L{x''(t)} = s²X(s) - 1
L{x'(t)}  = sX(s)
```

Substitute into the differential equation:

```text
2(s²X(s) - 1) + 7sX(s) + 3X(s) = 0
```

---

## Step 2: Solve for X(s)

Expand:

```text
2s²X(s) - 2 + 7sX(s) + 3X(s) = 0
```

Factor out X(s):

```text
X(s)(2s² + 7s + 3) = 2
```

Therefore:

```text
X(s) = 2 / (2s² + 7s + 3)
```

Factor the denominator:

```text
2s² + 7s + 3
= (2s + 1)(s + 3)
```

Thus:

```text
X(s) = 2 / [(2s + 1)(s + 3)]
```

---

## Step 3: Partial Fraction Decomposition

Assume:

```text
2 / [(2s + 1)(s + 3)]
=
A/(2s + 1) + B/(s + 3)
```

Multiply both sides by `(2s + 1)(s + 3)`:

```text
2 = A(s + 3) + B(2s + 1)
```

Expand:

```text
2 = (A + 2B)s + (3A + B)
```

Compare coefficients:

```text
A + 2B = 0
3A + B = 2
```

From the first equation:

```text
A = -2B
```

Substitute into the second equation:

```text
3(-2B) + B = 2
-5B = 2
B = -2/5
```

Then:

```text
A = 4/5
```

Therefore:

```text
X(s)
=
(4/5)/(2s + 1)
-
(2/5)/(s + 3)
```

Rewrite:

```text
X(s)
=
(2/5)/(s + 1/2)
-
(2/5)/(s + 3)
```

---

## Step 4: Inverse Laplace Transform

Using:

```text
L⁻¹{1/(s+a)} = e^(-at)
```

we obtain:

```text
x(t)
=
(2/5)e^(-t/2)
-
(2/5)e^(-3t)
```

Factor out `2/5`:

```text
x(t)
=
(2/5)[e^(-t/2) - e^(-3t)]
```

---

## Verification

### Check x(0)

```text
x(0)
=
(2/5)(1 - 1)
=
0
```

### Check x'(0)

Differentiate:

```text
x'(t)
=
-(1/5)e^(-t/2)
+
(6/5)e^(-3t)
```

Substitute t = 0:

```text
x'(0)
=
-1/5 + 6/5
=
1
```

Both initial conditions are satisfied.

---

## Final Answer

```text
x(t) = (2/5)[e^(-t/2) - e^(-3t)]
```
