# Differential Equations

A Differential Equation is a math equation that connects a function with its derivatives. In simple words, it is an equation that involves the derivatives of a function. The function can be of one or more variables, and the derivatives can be of any order.

---

## Table of Contents

1. [What is a Differential Equation?](#1-what-is-a-differential-equation)
2. [First-Order Differential Equation](#2-first-order-differential-equation)
3. [Second-Order Differential Equation](#3-second-order-differential-equation)
4. [Constant Coefficients](#4-constant-coefficients)
5. [What is a Laplace Transform?](#5-what-is-a-laplace-transform)

## 1. What is a Differential Equation?

A **differential equation** is an equation that contains a function and one or more of its derivatives.

Example:

```math
\frac{dy}{dx} = 2x
```

This means:

> "The derivative of y is 2x. Find y."

We solve it by integrating both sides:

```math
y = \int 2x\,dx
```

```
 y = x^2 + C
```

where `C` is the constant of integration.

---

## 2. First-Order Differential Equation

A **first-order** differential equation contains only the **first derivative**.

Example:

```math
\frac{dy}{dx} = 3x^2
```

### Step 1: Integrate

```math
y = \int 3x^2\,dx
```

### Step 2: Solve

```math
y = x^3 + C
```

✅ Final answer:

```math
y = x^3 + C
```

---

### Another Example

Given:

```math
\frac{dy}{dx} = 5
```

Integrate:

```math
y = \int 5\,dx = 5x + C
```

Final answer:

```math
y = 5x + C
```

---

## 3. Second-Order Differential Equation

A **second-order** differential equation contains the **second derivative**.

Example:

```math
\frac{d^2 y}{dx^2} = 6x
```

Notice this is the second derivative. We integrate **twice**.

### First integration

```math
\frac{dy}{dx} = \int 6x\,dx = 3x^2 + C_1
```

### Second integration

```math
y = \int (3x^2 + C_1)\,dx = x^3 + C_1 x + C_2
```

Answer:

```math
y = x^3 + C_1 x + C_2
```

A second-order equation gives **two constants** because we integrated twice.

---

## 4. Constant Coefficients

Sometimes the equation looks like:

```math
y'' + 3y' + 2y = 0
```

where:

- `y''` is the second derivative
- `y'` is the first derivative
- coefficients are `3` and `2`

These numbers are constants, so this is called a **constant coefficient differential equation**.

These equations are usually solved using the **characteristic equation**.

### Example

Solve:

```math
y'' - y = 0
```

Replace:

- `y'' \to r^2`
- `y \to 1`

Characteristic equation:

```math
r^2 - 1 = 0
```

Factor:

```math
(r - 1)(r + 1) = 0
```

Roots:

```math
r = 1, \quad r = -1
```

Therefore:

```math
y = C_1 e^x + C_2 e^{-x}
```

For introductory courses, you mainly need to know the method rather than derive it.

---

## 5. What is a Laplace Transform?

A **Laplace Transform** converts a difficult differential equation into an easier algebraic equation.

Think of it like **translating one language into another**.

```
Differential Equation        │        Laplace Transform        │        Simple Algebra Equation        │        Inverse Laplace        │        Original Solution
```

---

## Example

Suppose:

```math
\frac{dy}{dt} + y = 0
```

This differential equation is difficult to solve directly for beginners.

Applying the Laplace Transform changes it into an algebraic equation in the variable `s`:

```math
(s + 1) Y(s) = y(0)
```

Now solve for `Y(s)`:

```math
Y(s) = \frac{y(0)}{s + 1}
```

Then apply the **Inverse Laplace Transform**:

```math
y(t) = y(0) e^{-t}
```

So Laplace transforms make many differential equations much easier to solve.

---

## Common Laplace Transform Formulas

| Function | Laplace Transform |
| --- | --- |
| `1` | `1/s` |
| `t` | `1/s^2` |
| `t^2` | `2/s^3` |
| `e^{at}` | `1/(s - a)` |
| `\sin(at)` | `a/(s^2 + a^2)` |
| `\cos(at)` | `s/(s^2 + a^2)` |

Students usually memorize these formulas.