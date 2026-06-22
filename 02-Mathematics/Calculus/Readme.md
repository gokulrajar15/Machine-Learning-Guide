# Calculus

Calculus is the branch of mathematics that studies change and accumulation. It helps us understand how quantities change over time (using derivatives) and how to measure the total effect of those changes (using integrals).


## Table of Contents

1. [Introduction to Calculus](#introduction-to-calculus)
2. [Functions, Ranges, Domains and Graphs](#functions-ranges-domains-and-graphs)
3. [Limits](#limits)
4. [Derivatives](#derivatives)
5. [Applications of Derivatives](#applications-of-derivatives)
6. [Integrals](#integrals)
7. [Applications of Integrals](#applications-of-integrals)
8. [Partial Derivatives](#partial-derivatives)
9. [Maxima and Minima](#maxima-and-minima)
10. [Taylor Series](#taylor-series)


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

A limit describes the value that a function approaches as the input approaches a particular point.

### What is a Limit?

Notation:
$$\lim_{x \to a} f(x) = L$$

Read as: "The limit of f(x) as x approaches a equals L"

This means: As x gets closer and closer to a, f(x) gets closer and closer to L.

### Examples of Limits

#### Example 1: Simple Limit
$$\lim_{x \to 2} (3x + 1)$$

Let's see what happens as x approaches 2:

| x    | f(x) = 3x + 1 |
|------|---------------|
| 1.9  | 6.7           |
| 1.99 | 6.97          |
| 1.999| 6.997         |
| 2.001| 7.003         |
| 2.01 | 7.03          |
| 2.1  | 7.3           |

As $x \to 2$, $f(x) \to 7$

Therefore: $\lim_{x \to 2} (3x + 1) = 7$

#### Example 2: Limit at a Discontinuity
$$f(x) = \frac{x^2 - 4}{x - 2}$$

At $x = 2$, the function is undefined (division by zero).

But we can simplify:
$$f(x) = \frac{(x-2)(x+2)}{x-2} = x + 2 \quad \text{(for } x \neq 2\text{)}$$

So: $\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2} (x + 2) = 4$

**Key insight:** The limit can exist even when the function is undefined at that point.

### When Does a Limit Exist?

A limit exists at a point if and only if:

1. **The left-hand limit exists**
2. **The right-hand limit exists**
3. **Both limits are equal**

$$\lim_{x \to a} f(x) = L \quad \text{if and only if} \quad \lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = L$$

### Left-Hand and Right-Hand Limits

#### Left-Hand Limit (LHL)
$$\lim_{x \to a^-} f(x)$$

The value that f(x) approaches as x approaches a **from the left** (values less than a).

#### Right-Hand Limit (RHL)
$$\lim_{x \to a^+} f(x)$$

The value that f(x) approaches as x approaches a **from the right** (values greater than a).

### Example: Piecewise Function

$$f(x) = \begin{cases} 
x + 1 & \text{if } x < 2 \\
5 & \text{if } x = 2 \\
2x & \text{if } x > 2
\end{cases}$$

**Find:** $\lim_{x \to 2} f(x)$

**Left-Hand Limit:**
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^-} (x + 1) = 2 + 1 = 3$$

**Right-Hand Limit:**
$$\lim_{x \to 2^+} f(x) = \lim_{x \to 2^+} (2x) = 2(2) = 4$$

**Conclusion:**

Since $\lim_{x \to 2^-} f(x) = 3$ and $\lim_{x \to 2^+} f(x) = 4$

$$\text{LHL} \neq \text{RHL}$$

Therefore, **the limit does NOT exist** at $x = 2$.

**Note:** Even though $f(2) = 5$ is defined, the limit doesn't exist because left and right limits don't match.

### Visual Understanding

```
For limit to exist:
    
    LHL = RHL
     ↓     ↓
     3 ≠ 4    → Limit does NOT exist

If LHL = RHL = 3:
     ↓     ↓
     3 = 3    → Limit exists and equals 3
```

### Interview Summary

**Q: When does a limit exist?**

A: A limit exists at a point when the left-hand limit equals the right-hand limit. The function doesn't need to be defined at that point, but the values from both sides must approach the same number.

**Key Points:**
- Limit can exist even if f(a) is undefined
- If LHL = RHL, limit exists
- If LHL ≠ RHL, limit does not exist
- f(a) and limit can be different values


## Continuity

A function is continuous at a point if the limit exists and equals the function value at that point.

### Definition of Continuity

A function $f(x)$ is **continuous at** $x = a$ if:

1. $f(a)$ is defined (the function exists at that point)
2. $\lim_{x \to a} f(x)$ exists (the limit exists)
3. $\lim_{x \to a} f(x) = f(a)$ (the limit equals the function value)

**All three conditions must be satisfied!**

### Example 1: Continuous Function

$$f(x) = x^2 + 3$$

**Check continuity at** $x = 2$:

1. **Is** $f(2)$ **defined?**
   
   $f(2) = 2^2 + 3 = 7$ ✓

2. **Does** $\lim_{x \to 2} f(x)$ **exist?**
   
   $\lim_{x \to 2} (x^2 + 3) = 2^2 + 3 = 7$ ✓

3. **Does** $\lim_{x \to 2} f(x) = f(2)$?
   
   $7 = 7$ ✓

**Conclusion:** The function is **continuous** at $x = 2$.

### Example 2: Discontinuous Function (Removable Discontinuity)

$$f(x) = \begin{cases} 
\frac{x^2 - 4}{x - 2} & \text{if } x \neq 2 \\
5 & \text{if } x = 2
\end{cases}$$

**Check continuity at** $x = 2$:

1. **Is** $f(2)$ **defined?**
   
   $f(2) = 5$ ✓

2. **Does** $\lim_{x \to 2} f(x)$ **exist?**
   
   $\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x + 2) = 4$ ✓

3. **Does** $\lim_{x \to 2} f(x) = f(2)$?
   
   $4 \neq 5$ ✗

**Conclusion:** The function is **NOT continuous** at $x = 2$ because the limit (4) does not equal the function value (5).

### Example 3: Discontinuous Function (Jump Discontinuity)

$$f(x) = \begin{cases} 
x + 1 & \text{if } x < 2 \\
2x & \text{if } x \geq 2
\end{cases}$$

**Check continuity at** $x = 2$:

1. **Is** $f(2)$ **defined?**
   
   $f(2) = 2(2) = 4$ ✓

2. **Does** $\lim_{x \to 2} f(x)$ **exist?**
   - Left-hand limit: $\lim_{x \to 2^-} f(x) = 2 + 1 = 3$
   - Right-hand limit: $\lim_{x \to 2^+} f(x) = 2(2) = 4$
   - Since $3 \neq 4$, the limit does NOT exist ✗

**Conclusion:** The function is **NOT continuous** at $x = 2$ because the limit doesn't exist (jump discontinuity).

### Example 4: Discontinuous Function (Infinite Discontinuity)

$$f(x) = \frac{1}{x}$$

**Check continuity at** $x = 0$:

1. **Is** $f(0)$ **defined?**
   
   $f(0) = \frac{1}{0}$ is undefined ✗

**Conclusion:** The function is **NOT continuous** at $x = 0$ because it's not even defined there.

### Types of Discontinuities

| Type | Description | Example |
|------|-------------|---------|
| **Removable** | Limit exists but doesn't equal f(a) | Hole in the graph |
| **Jump** | Left and right limits exist but are different | Step function |
| **Infinite** | Function approaches $\pm\infty$ | Vertical asymptote |

### Visual Comparison

```
Continuous:           Removable:           Jump:
    •                    ○   •               •
   /                    /                   /
  /                    /                     
 /                    /                 •---
/                    /                 
```

### Interview Summary

**Q: What does it mean for a function to be continuous?**

A: A function is continuous at a point if you can draw it without lifting your pencil. Mathematically, three conditions must be met:
1. The function is defined at that point
2. The limit exists at that point
3. The limit equals the function value

**Quick Check:**
- Can you evaluate f(a)? → Is it defined?
- Do left and right limits match? → Does limit exist?
- Does the limit equal f(a)? → Is it continuous?


## Derivatives