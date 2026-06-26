# Differential Calculus (Derivatives)

Differential calculus is a branch of calculus that deals with the study of rates of change and slopes of curves. It focuses on the concept of the derivative, which measures how a function changes as its input changes. The derivative provides information about the instantaneous rate of change of a function at a specific point.

## Table of Contents
1. [Introduction to Derivatives](#introduction-to-derivatives)
2. [Finding a Derivative](#finding-a-derivative)
3. [Formal Notation](#formal-notation)
4. [Difference Quotient](#difference-quotient)
5. [Derivative Rules](#derivative-rules)
6. [Second Derivatives](#second-derivatives)
7. [Partial Derivatives (Multi-Variable Calculus)](#partial-derivativesmulti-variable-calculus)
8. [Maxima and Minima (Stationary Points)](#maxima-and-minima-stationary-points)
9. [Taylor Series](#taylor-series)
---

## Introduction to Derivatives

It is all about **slope**!

$$\text{Slope} = \frac{\text{Change in Y}}{\text{Change in X}} = \frac{\Delta y}{\Delta x}$$

![gradient](https://www.mathsisfun.com/algebra/images/slope.svg)

We can find an **average** slope between two points.

![average slope](https://www.mathsisfun.com/calculus/images/slope-average.svg)

But how do we find the slope **at a point**? There is nothing to measure!

![slope at a point](https://www.mathsisfun.com/calculus/images/slope-0-0.svg)

With derivatives we use a small difference, then have it **shrink towards zero**.

![slope delta y delta x](https://www.mathsisfun.com/calculus/images/slope-dy-dx.svg)

## Finding a Derivative

To find the derivative of a function $y = f(x)$ we use the slope formula:

$$\text{Slope} = \frac{\Delta y}{\Delta x}$$

![slope formula visualization](https://www.mathsisfun.com/calculus/images/slope-dy-dx2.svg)

Where:
- x changes from $x$ to $x + \Delta x$
- y changes from $f(x)$ to $f(x + \Delta x)$

**Steps:**
1. Fill in the slope formula: $\frac{f(x+\Delta x) - f(x)}{\Delta x}$
2. Simplify as best we can
3. Make $\Delta x$ shrink towards zero

### Example 1: f(x) = x²

**Step 1:** Slope formula
$$\frac{f(x+\Delta x) - f(x)}{\Delta x}$$

**Step 2:** Use $f(x) = x^2$
$$\frac{(x+\Delta x)^2 - x^2}{\Delta x}$$

**Step 3:** Expand $(x+\Delta x)^2$
$$\frac{x^2 + 2x\Delta x + (\Delta x)^2 - x^2}{\Delta x}$$

**Step 4:** Simplify
$$\frac{2x\Delta x + (\Delta x)^2}{\Delta x} = 2x + \Delta x$$

**Step 5:** As $\Delta x \to 0$
$$2x$$

**Result:** The derivative of $x^2$ is $2x$

**Notation:**
$$\frac{d}{dx}x^2 = 2x$$

This means the slope or "rate of change" at any point is $2x$.

![slope of x^2 at x=2](https://www.mathsisfun.com/calculus/images/slope-x2-2.svg)

- When $x = 2$, the slope is $2(2) = 4$
- When $x = 5$, the slope is $2(5) = 10$

**Alternative notation:**
$$f'(x) = 2x$$

### Example 2: f(x) = x³

**Step 1:** Slope formula
$$\frac{(x+\Delta x)^3 - x^3}{\Delta x}$$

**Step 2:** Use $(x+\Delta x)^3 = x^3 + 3x^2\Delta x + 3x(\Delta x)^2 + (\Delta x)^3$
$$\frac{x^3 + 3x^2\Delta x + 3x(\Delta x)^2 + (\Delta x)^3 - x^3}{\Delta x}$$

**Step 3:** Simplify
$$\frac{3x^2\Delta x + 3x(\Delta x)^2 + (\Delta x)^3}{\Delta x} = 3x^2 + 3x\Delta x + (\Delta x)^2$$

**Step 4:** As $\Delta x \to 0$
$$3x^2$$

**Result:** The derivative of $x^3$ is $3x^2$

$$\frac{d}{dx}x^3 = 3x^2$$

## Formal Notation

The derivative is written as a limit:

$$f'(x) = \lim_{\Delta x \to 0} \frac{f(x+\Delta x) - f(x)}{\Delta x}$$

Or equivalently:

$$\frac{dy}{dx} = \frac{f(x+dx) - f(x)}{dx}$$

The process of finding a derivative is called **differentiation**.

## Difference Quotient

The **difference quotient** gives the average slope between two points on a curve $f(x)$ that are $\Delta x$ apart:

$$\frac{f(x+\Delta x) - f(x)}{\Delta x}$$

![slope visualization](https://www.mathsisfun.com/calculus/images/slope-dy-dx2.svg)

### Example: Average Slope

Find the average slope of $f(x) = x^2 - 2x + 1$ at $x = 3$ and $\Delta x = 0.1$

**Step 1:** Evaluate $f(3)$
$$f(3) = 3^2 - 2(3) + 1 = 4$$

**Step 2:** Evaluate $f(3.1)$
$$f(3.1) = (3.1)^2 - 2(3.1) + 1 = 4.41$$

**Step 3:** Calculate the difference quotient
$$\frac{f(3.1) - f(3)}{0.1} = \frac{4.41 - 4}{0.1} = \frac{0.41}{0.1} = 4.1$$

**Try a smaller Δx = 0.01:**

$$f(3.01) = (3.01)^2 - 2(3.01) + 1 = 4.0401$$

$$\frac{f(3.01) - f(3)}{0.01} = \frac{4.0401 - 4}{0.01} = \frac{0.0401}{0.01} = 4.01$$

**Observation:** As $\Delta x$ heads towards 0, the slope approaches **4**.

This is the idea behind derivatives - finding the exact slope by having $\Delta x \to 0$.

## Derivative Rules

The derivative tells us the slope of a function at any point.

![slope examples](https://www.mathsisfun.com/calculus/images/slope-examples.svg)

There are **rules** we can follow to find many derivatives:
- The slope of a **constant** value (like 3) is always 0
- The slope of a **line** like 2x is 2, or 3x is 3

### Common Functions

| Function | Derivative |
|----------|------------|
| Constant $c$ | $0$ |
| Linear $x$ | $1$ |
| Linear $ax$ | $a$ |
| Square $x^2$ | $2x$ |
| Square Root $\sqrt{x}$ | $\frac{1}{2\sqrt{x}}$ |
| Exponential $e^x$ | $e^x$ |
| Exponential $a^x$ | $a^x \ln(a)$ |
| Natural Log $\ln(x)$ | $\frac{1}{x}$ |
| Log $\log_a(x)$ | $\frac{1}{x \ln(a)}$ |
| Sine $\sin(x)$ | $\cos(x)$ |
| Cosine $\cos(x)$ | $-\sin(x)$ |
| Tangent $\tan(x)$ | $\sec^2(x)$ |

### Derivative Rules

| Rule | Function | Derivative |
|------|----------|------------|
| **Constant Multiple** | $cf$ | $cf'$ |
| **Power Rule** | $x^n$ | $nx^{n-1}$ |
| **Sum Rule** | $f + g$ | $f' + g'$ |
| **Difference Rule** | $f - g$ | $f' - g'$ |
| **Product Rule** | $fg$ | $fg' + f'g$ |
| **Quotient Rule** | $\frac{f}{g}$ | $\frac{f'g - fg'}{g^2}$ |
| **Chain Rule** | $f(g(x))$ | $f'(g(x)) \cdot g'(x)$ |

### Power Rule

![power rule visualization](https://www.mathsisfun.com/calculus/images/power-rule.svg)

"Multiply by power, then reduce power by 1"

**Example 1:**
$$\frac{d}{dx}x^3 = 3x^{3-1} = 3x^2$$

**Example 2:**
$$\frac{d}{dx}\frac{1}{x} = \frac{d}{dx}x^{-1} = -1x^{-2} = -\frac{1}{x^2}$$

### Constant Multiple Rule

**Example:**
$$\frac{d}{dx}5x^3 = 5 \cdot \frac{d}{dx}x^3 = 5 \cdot 3x^2 = 15x^2$$

### Sum Rule

**Example:**
$$\frac{d}{dx}(x^2 + x^3) = \frac{d}{dx}x^2 + \frac{d}{dx}x^3 = 2x + 3x^2$$

### Difference Rule

**Example:**
$$\frac{d}{dv}(v^3 - v^4) = \frac{d}{dv}v^3 - \frac{d}{dv}v^4 = 3v^2 - 4v^3$$

### Combined Rules

**Example:**
$$\frac{d}{dz}(5z^2 + z^3 - 7z^4) = 10z + 3z^2 - 28z^3$$

### Product Rule

For $\frac{d}{dx}(fg)$: differentiate first, keep second + keep first, differentiate second

**Example:**
$$\frac{d}{dx}[\cos(x)\sin(x)] = \cos(x)\cos(x) + (-\sin(x))\sin(x) = \cos^2(x) - \sin^2(x)$$

### Quotient Rule

"Low dHigh minus High dLow, over the line and square the Low"

$$\left(\frac{f}{g}\right)' = \frac{gf' - fg'}{g^2}$$

**Example:**
$$\frac{d}{dx}\frac{\cos(x)}{x} = \frac{x(-\sin(x)) - \cos(x)(1)}{x^2} = \frac{-x\sin(x) - \cos(x)}{x^2}$$

### Chain Rule

For composite functions: differentiate outer function, keep inner, multiply by derivative of inner

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

**Example 1:**
$$\frac{d}{dx}\sin(x^2) = \cos(x^2) \cdot 2x = 2x\cos(x^2)$$

**Example 2:**
$$\frac{d}{dx}\frac{1}{\cos(x)} = \frac{-1}{\cos^2(x)} \cdot (-\sin(x)) = \frac{\sin(x)}{\cos^2(x)}$$

**Example 3:**
$$\frac{d}{dx}(5x-2)^3 = 3(5x-2)^2 \cdot 5 = 15(5x-2)^2$$

#### Chain Rule - Intuitive Example

# Example 1: Chain Rule Forward

Find the derivative of

$$y=(x^2+1)^5$$

### Step 1: Identify the layers

Think of it as a machine inside a machine.

```
x
↓
x²+1
↓
( )⁵
```

Inner function:

$$u=x^2+1$$

Outer function:

$$y=u^5$$

---

### Step 2: Differentiate the outer function

Treat $u$ as a variable.

$$\frac{dy}{du}=5u^4$$

---

### Step 3: Differentiate the inner function

$$\frac{du}{dx}=2x$$

---

### Step 4: Multiply them

Chain rule says:

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

So

$$\frac{dy}{dx} = 5u^4(2x)$$

Replace $u$:

$$\boxed{\frac{dy}{dx}=10x(x^2+1)^4}$$

---

# Now Reverse It

Suppose someone gives you

$$\int 10x(x^2+1)^4\,dx$$

Look carefully.

This is exactly the derivative we just got!

So the answer must be

$$\boxed{(x^2+1)^5+C}$$

Substitution is simply a systematic way to see this.

## Second Derivatives

The second derivative is essentially the "derivative of the derivative." While the first derivative tells you how fast a function is changing (its slope or velocity), the second derivative tells you how fast that change itself is changing.

**Notation:**
- $f''(x)$ or $\frac{d^2y}{dx^2}$

**Example:**

$$f(x) = x^3$$

First derivative:
$$f'(x) = 3x^2$$

Second derivative:
$$f''(x) = 6x$$

## Partial Derivatives(Multi-Variable Calculus)

Partial derivatives are used when dealing with functions of multiple variables. Instead of finding the derivative with respect to all variables at once, we take the derivative with respect to one variable while keeping the others constant.

A partial derivative is a derivative where we hold some variables constant.

![partial derivative on surface](https://www.mathsisfun.com/calculus/images/partial-derivative.gif)

**Example:** For a function that depends on two variables x and y:
- Find the slope in the **x** direction (while keeping y fixed)
- Find the slope in the **y** direction (while keeping x fixed)

### Single vs Multi-Variable Functions

**One variable:**
$$f(x) = x^2$$
$$f'(x) = 2x$$

**Two variables:**
$$f(x, y) = x^2 + y^3$$

**Partial derivative with respect to x** (treat y as constant):
$$f'_x = 2x + 0 = 2x$$

**Partial derivative with respect to y** (treat x as constant):
$$f'_y = 0 + 3y^2 = 3y^2$$

**Key rule:** Treat all other variables as if they are constants.

### Example: Cylinder Volume

![Cylinder Dimensions](https://www.mathsisfun.com/geometry/images/cylinder-dimensions.svg)

$$V = \pi r^2 h$$

In multi-variable form:
$$f(r, h) = \pi r^2 h$$

**With respect to r** (hold h constant):

![Cylinder with r changing](https://www.mathsisfun.com/calculus/images/cylinder-r-changes.svg)

$$f'_r = \pi (2r) h = 2\pi rh$$

As only the radius changes, the volume changes by $2\pi rh$ (like adding a thin skin).

**With respect to h** (hold r constant):

![Cylinder with h changing](https://www.mathsisfun.com/calculus/images/cylinder-h-changes.svg)

$$f'_h = \pi r^2 (1) = \pi r^2$$

As only the height changes, the volume changes by $\pi r^2$ (like adding a thin disk on top).

### Notation

**Common notations:**
- $f'_x$ - partial derivative with respect to x
- $\frac{\partial f}{\partial x}$ - using the symbol ∂ (pronounced "del", "dee", or "curly dee")

Both mean the same thing:
$$\frac{\partial f}{\partial x} = f'_x$$

**Example:** Find partial derivatives of $f(x, y, z) = x^4 - 3xyz$

$$\frac{\partial f}{\partial x} = 4x^3 - 3yz$$

$$\frac{\partial f}{\partial y} = -3xz$$

$$\frac{\partial f}{\partial z} = -3xy$$


## Maxima and Minima (Stationary Points)

Maxima and minima are points on a function where the function reaches its highest or lowest value. These points are also known as **stationary points** because the slope of the function at these points is zero.

### Definitions

**Local Maximum:**
- Highest point in a local region
- Function transitions from increasing to decreasing
- $f'(x) = 0$ and $f''(x) < 0$

**Local Minimum:**
- Lowest point in a local region
- Function transitions from decreasing to increasing
- $f'(x) = 0$ and $f''(x) > 0$

**Saddle Point (Point of Inflection):**
- Slope is zero but doesn't change direction
- $f'(x) = 0$ and $f''(x) = 0$

### Steps to Find Stationary Points

**Step 1:** Find the first derivative $f'(x)$

**Step 2:** Set $f'(x) = 0$ and solve for x

**Step 3:** Find the second derivative $f''(x)$

**Step 4:** Apply the Second Derivative Test:
- If $f''(x) < 0$ → **Local Maximum**
- If $f''(x) > 0$ → **Local Minimum**  
- If $f''(x) = 0$ → **Inconclusive** (check nearby points)

**Step 5:** Find the y-coordinates by substituting x-values into $f(x)$

### Complete Example

Find and classify all stationary points of $f(x) = x^3 - 3x^2 + 2$

**Step 1: Find the first derivative**

$$f(x) = x^3 - 3x^2 + 2$$

$$f'(x) = 3x^2 - 6x$$

**Step 2: Set first derivative to zero**

$$3x^2 - 6x = 0$$

Factor:
$$3x(x - 2) = 0$$

Solutions:
$$x = 0 \text{ or } x = 2$$

**Step 3: Find the second derivative**

$$f''(x) = 6x - 6$$

**Step 4: Apply Second Derivative Test**

**At x = 0:**
$$f''(0) = 6(0) - 6 = -6 < 0$$

Since $f''(0) < 0$, this is a **local maximum**

**At x = 2:**
$$f''(2) = 6(2) - 6 = 6 > 0$$

Since $f''(2) > 0$, this is a **local minimum**

**Step 5: Find y-coordinates**

**At x = 0:**
$$f(0) = (0)^3 - 3(0)^2 + 2 = 2$$

Local maximum at $(0, 2)$

**At x = 2:**
$$f(2) = (2)^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2$$

Local minimum at $(2, -2)$

**Summary:**
- **Local Maximum:** $(0, 2)$
- **Local Minimum:** $(2, -2)$

**Application:** These points are useful in optimization problems, where we want to find the best (maximum) or worst (minimum) values of a function in a given context.

## Taylor Series

A Taylor Series represents a function as an infinite sum of polynomial terms built from the function's derivatives at a particular point.

### The Problem

Functions like:

$$e^x, \quad \sin(x), \quad \cos(x), \quad \ln(x)$$

are not polynomials. They can be harder to calculate exactly.

### The Problem

**Example:** Calculate $\sin(0.13)$ without a calculator.

This is not easy to compute directly.

### The Taylor Series Idea

Replace the complicated function with a polynomial that behaves almost the same near a chosen point.

**Example: Approximating sin(x)**

$$\sin(x) \approx x - \frac{x^3}{3!} + \frac{x^5}{5!}$$

$$\sin(x) \approx x - \frac{x^3}{6} + \frac{x^5}{120}$$

Now if $x = 0.13$:

$$\sin(0.13) \approx 0.13 - \frac{(0.13)^3}{6} + \frac{(0.13)^5}{120}$$

$$\sin(0.13) \approx 0.13 - 0.000366 + 0.0000004$$

$$\sin(0.13) \approx 0.1296$$

This is much easier to compute using basic arithmetic!

**Key insight:** The more terms we add, the better the approximation becomes.

### Summary

The Polynomial functions are easier to solve than non-polynomial functions. The Taylor Series allows us to approximate complex functions using polynomials, which are easier to work with.

*In simple terms, the Taylor Series allows us to approximate complex functions using polynomials, which are easier to work with.*