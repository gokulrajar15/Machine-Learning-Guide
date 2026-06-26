# Calculus

Calculus is the branch of mathematics that studies change and accumulation. It helps us understand how quantities change over time (using derivatives) and how to measure the total effect of those changes (using integrals).


## Table of Contents

1. [Introduction to Calculus](#introduction-to-calculus)
2. [Functions, Ranges, Domains and Graphs](#functions-ranges-domains-and-graphs)
3. [Limits](#limits)


## Introduction to Calculus
Calculus is divided into two main branches: differential calculus and integral calculus. Differential calculus focuses on the concept of the derivative, which represents the rate of change of a function. Integral calculus, on the other hand, deals with the concept of the integral, which represents the accumulation of quantities and the area under curves.


## Functions, Ranges, Domains and Graphs

### 1. What is a Function?

A function is simply a rule that takes an input and produces exactly one output.

**Example:**

$$f(x) = x^2$$

Input $x = 2$:
$$f(2) = 2^2 = 4$$

Input $x = 3$:
$$f(3) = 3^2 = 9$$

Think of a function as a machine:

```
Input → Function → Output
  3    →  x²    →  9
```

**Interview answer:**

A function maps each input to exactly one output.

### 2. Domain and Range

**Domain:** The set of all allowed inputs.

**Range:** The set of all possible outputs.

#### Example 1
$$f(x) = x^2$$

Allowed inputs: $-\infty < x < \infty$

Domain: $(-\infty, \infty)$

Outputs: $0, 1, 4, 9, 16, ...$

Notice: $x^2 \geq 0$

Range: $[0, \infty)$

#### Example 2
$$f(x) = \frac{1}{x}$$

Can we put $x = 0$?

No. Division by zero is undefined.

Domain: $(-\infty, 0) \cup (0, \infty)$

Range: $(-\infty, 0) \cup (0, \infty)$

### 3. Graph of y = x

```
      |
  12  |
  10  |
   8  |                     /
   6  |                   /
   4  |                 /
   2  |               /
      |             /
−8 −6 −4 −2 (0,0)/2  4  6  8
      |         /
  -2  |       /
  -4  |     /
  -6  |   /
  -8  | /
      |
```

**Properties:**
- Straight line
- Passes through origin
- Increasing everywhere

**Examples:**

| x  | y  |
|----|---|
| -2 | -2 |
| -1 | -1 |
| 0  | 0  |
| 1  | 1  |
| 2  | 2  |

As x increases, y increases.


## Limits

### What is a Limit?

A limit describes the behavior of a function as its input approaches a specific value from either side. It tells us what value the function is getting closer to, even if it doesn't actually reach that value.

**Notation:**
$$\lim_{x \to a} f(x) = L$$

This means: as x gets closer and closer to a, f(x) gets closer and closer to L.

**Simple interview answer:**
- A limit is the value a function is approaching when the input gets near a point.
- It is about what happens as we get closer, not necessarily what happens at the point itself.

**Think of it like this:**
- You are walking toward a door. The limit is the door you are getting near, even if you stop one step before.

### Example: The Indeterminate Form

Consider:
$$f(x) = \frac{x^2 - 1}{x - 1}$$

At $x = 1$:
$$\frac{1^2 - 1}{1 - 1} = \frac{0}{0}$$

This is indeterminate. Let's approach from different values:

**Approaching from the left:**

| x     | f(x)    |
|-------|---------|
| 0.5   | 1.50000 |
| 0.9   | 1.90000 |
| 0.99  | 1.99000 |
| 0.999 | 1.99900 |

**Approaching from the right:**

| x     | f(x)    |
|-------|---------|
| 1.5   | 2.50000 |
| 1.1   | 2.10000 |
| 1.01  | 2.01000 |
| 1.001 | 2.00100 |

As $x \to 1$, $f(x) \to 2$

Therefore:
$$\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = 2$$

**Key insight:** The limit can exist even when the function is undefined at that point.

### Testing Both Sides

For a limit to exist, the left-hand limit and right-hand limit must be equal:

$$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)$$

**Example of non-existent limit:**

If approaching from the left gives 3.8 and from the right gives 1.3, the limit does not exist.

### Limits at Infinity

**Question:** What is $\frac{1}{\infty}$?

We can't evaluate directly, but we can approach it:

$$f(x) = \frac{1}{x}$$

| x      | f(x)    |
|--------|---------|
| 1      | 1.00000 |
| 10     | 0.10000 |
| 100    | 0.01000 |
| 1,000  | 0.00100 |
| 10,000 | 0.00010 |

As $x$ gets larger, $\frac{1}{x}$ approaches 0.

$$\lim_{x \to \infty} \frac{1}{x} = 0$$

**Remember:** When you see "limit", think "approaching".

### Evaluating Limits

"Evaluating" means to find the value of the limit. Here are methods to calculate limits:

#### 1. Direct Substitution

Simply substitute the value into the function.

**Example:**
$$\lim_{x \to 10} \frac{x}{2} = \frac{10}{2} = 5$$

**Example (doesn't work):**
$$\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = \frac{0}{0}$$

When you get $\frac{0}{0}$, try another method.

#### 2. Factoring

Factor the expression to cancel common terms.

**Example:**
$$\lim_{x \to 1} \frac{x^2 - 1}{x - 1}$$

Factor the numerator:
$$\lim_{x \to 1} \frac{(x-1)(x+1)}{x-1} = \lim_{x \to 1} (x+1) = 2$$

#### 3. Conjugate Method

Multiply by the conjugate to eliminate square roots.

**Example:**
$$\lim_{x \to 4} \frac{2 - \sqrt{x}}{4 - x}$$

Multiply by conjugate $\frac{2 + \sqrt{x}}{2 + \sqrt{x}}$:

$$= \lim_{x \to 4} \frac{4 - x}{(4-x)(2+\sqrt{x})} = \lim_{x \to 4} \frac{1}{2+\sqrt{x}} = \frac{1}{4}$$

#### 4. Rational Functions at Infinity

For $f(x) = \frac{P(x)}{Q(x)}$, compare the degrees of polynomials:

- If degree(P) < degree(Q): limit = 0
- If degree(P) = degree(Q): limit = ratio of leading coefficients
- If degree(P) > degree(Q): limit = $\pm\infty$

#### 5. L'Hôpital's Rule

For indeterminate forms $\frac{0}{0}$ or $\frac{\infty}{\infty}$:

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

Take derivatives of numerator and denominator separately.

## Continuous Functions

### What Makes a Function Discontinuous?

If a function is not continuous, it is called **discontinuous**. This usually happens because of three common issues:

- **Holes:** A single point is missing from the graph.
- **Jumps:** The graph breaks and abruptly snaps to a higher or lower value.
- **Vertical Asymptotes:** The graph shoots off toward positive or negative infinity (like the function $f(x) = \frac{1}{x-1}$ does at $x = 1$).

### The Formal Definition

Mathematically, a function $f$ is continuous at a specific value $c$ within its domain if it meets three strict conditions:

1. **$f(c)$ is defined:** There is an actual value at that point (no hole).
2. **The limit exists:** As $x$ gets closer and closer to $c$ from both the left and the right sides, it approaches the same value (no jump).
3. **The limit equals the actual value:** Written formally as:

$$\lim_{x \to c} f(x) = f(c)$$

**Simple interview answer:**
- A function is continuous at a point when you can draw it there without lifting your pen.
- It means the function has no hole, no jump, and no vertical break at that point.

**Think of it like a road:**
- Continuous means the road is smooth at that point.
- Discontinuous means the road has a gap, a cliff, or a sudden jump.

### Example of Continuity

Function: $f(x) = x^2$

At $x = 2$:
- $f(2)$ is defined and equals 4.
- $\\lim_{x \to 2} x^2 = 4$.
- The limit equals the function value, so $f(x)$ is continuous at 2.

### Example of Discontinuity

Function: $f(x) = \frac{1}{x}$

At $x = 0$:
- $f(0)$ is not defined.
- The limit does not exist because the function goes to $+\infty$ on one side and $-\infty$ on the other.
- Therefore, $f(x)$ is discontinuous at 0.

**Quick interview tip:**
- Say: "Continuity means the function's value and its approaching value match at the point."
- Add: "If either the value is missing or the left and right approach are different, it is not continuous."


