# Integral Calculus (Integration)

Integral calculus is a branch of calculus focused on accumulation and finding the area under a curve. It is the inverse process of differentiation. The two primary types are indefinite integrals (which find the antiderivative of a function) and definite integrals (which calculate a specific numerical value over a bounded interval).


## Table of Contents

1. [Introduction to Integration](#introduction-to-integration)
2. [Rules of Integration](#rules-of-integration)
3. [Definite Integrals](#definite-integrals)
4. [Integration by Parts](#integration-by-parts)
5. [Integration by Substitution](#integration-by-substitution)
6. [Fundamental Theorems of Calculus](#fundamental-theorems-of-calculus)

---

## Introduction to Integration

Integration is a way of adding slices to find the whole.

Integration can be used to find areas, volumes, central points and many useful things. But it is easiest to start with finding the **area between a function and the x-axis** like this:

![integral area = ?](https://www.mathsisfun.com/calculus/images/integral-area.svg)

*What is the area?*

---

### Slices

We could calculate the function at a few points and **add up slices of width Δx** like this (but the answer won't be very accurate):

![integral area big deltax](https://www.mathsisfun.com/calculus/images/integral-area3.svg)

We can make **Δx** a lot smaller and **add up many small slices** (answer is getting better):

![integral area small deltax](https://www.mathsisfun.com/calculus/images/integral-area1.svg)

And as the slices **approach zero in width**, the answer approaches the **true answer**.

We now write **dx** to mean the **Δx** slices are approaching zero in width.

![integral area dx](https://www.mathsisfun.com/calculus/images/integral-area0.svg)

---

### The Shortcut: Integrals and Derivatives

But we don't have to add them up, as there is a "shortcut", because...

> **Finding an Integral is the *reverse* of finding a Derivative.**

(So you should really know about [Derivatives](https://www.mathsisfun.com/calculus/derivatives-introduction.html) before reading more!)

#### Example: Integral of 2x

An integral of 2x is x² ...

![integral vs derivative](https://www.mathsisfun.com/calculus/images/integral-vs-derivative.svg)

... because the derivative of x² is 2x (More about "+C" later.)

That simple example can be confirmed by calculating the area:

![integral 2x is x^2](https://www.mathsisfun.com/calculus/images/integral-2x-graph.svg)

**Area of triangle** = ½ × (base) × (height) = ½ × (x) × (2x) = **x²**

Integration can sometimes be that easy!

---

### Notation

The symbol for "Integral" is a stylish "S" (for "Sum", the idea of summing slices):

![integral notation](https://www.mathsisfun.com/calculus/images/integral-notation-1.svg)

After the Integral Symbol we put the function we want to find the integral of (called the **Integrand**), and then finish with **dx** to mean the slices go in the x direction (and approach zero in width).

And here is how we write the answer:

![integral of 2x dx = x^2 + C](https://www.mathsisfun.com/calculus/images/integral-notation-2.svg)

---

### The Constant of Integration (+C)

We wrote the answer as x² but why **+C**?

It is the **"Constant of Integration"**. It is there because of all the functions whose derivative is 2x:

![many integrals vs one derivative](https://www.mathsisfun.com/calculus/images/integrals-vs-derivative.svg)

- The derivative of **x²** is **2x**
- The derivative of **x² + 4** is also **2x**
- The derivative of **x² + 99** is also **2x**
- And so on!

Because the derivative of a constant is zero.

So when we **reverse** the operation (to find the integral) we only know **2x**, but there could have been a **constant of any value**.

So we wrap up the idea by just writing **+ C** at the end.

---

### Practical Example: Tap and Tank

![integral tap tank](https://www.mathsisfun.com/calculus/images/integral-tap-tank.svg)

Let us use a tap to fill a tank.

- **Input** (before integration): the **flow rate** from the tap
- **Output** (after integration): the **volume of water** in the tank

#### Constant Flow Rate

Imagine a **Constant Flow Rate** of 1:

![integral tap tank constant flow](https://www.mathsisfun.com/calculus/images/integral-tap-tank-constant.svg)

With a flow rate of **1**, the tank volume increases by **x**. That is **Integration**!

> An integral of 1 is x

With a flow rate of 1 liter per second, the volume increases by 1 liter every second, so would increase by 10 liters after 10 seconds, 60 liters after 60 seconds, and so on.

**And it works the other way too:**

If the tank volume increases by **x**, then the flow rate must be **1**.

> The derivative of x is 1

This shows that **integrals and derivatives are opposites!**

![integral vs derivative](https://www.mathsisfun.com/calculus/images/integral-vs-derivative-1-x.svg)

#### Increasing Flow Rate

Imagine the flow starts at 0 and gradually increases (maybe a motor is slowly opening the tap):

![integral tap tank flow rate 2x gives volume x^2](https://www.mathsisfun.com/calculus/images/integral-tap-tank-2x.svg)

As the flow rate increases, the tank fills up faster and faster:

| Direction | Relationship |
|-----------|-------------|
| **Integration** | With a flow rate of **2x**, the tank volume increases by **x²** |
| **Derivative** | If the tank volume increases by **x²**, then the flow rate must be **2x** |

![integral vs derivative](https://www.mathsisfun.com/calculus/images/integral-vs-derivative.svg)

We can write it down this way:

- The integral of the flow rate **2x** tells us the volume of water: `∫2x dx = x² + C`
- The derivative of the volume **x² + C** gives us back the flow rate: `d/dx(x² + C) = 2x`

![integral tap tank graphs](https://www.mathsisfun.com/calculus/images/integral-tap-tank-graphs3.svg)

And hey, we even get a nice explanation of that "C" value... maybe the tank already has water in it!

- The flow still increases the volume by the same amount
- And the increase in volume can give us back the flow rate

Which teaches us to always remember **"+C"**.

---

### Integrating Other Functions

How do we integrate other functions?

If we are lucky enough to find the function on the **result** side of a derivative, then (knowing that derivatives and integrals are opposites) we have an answer. But remember to add C.

#### Example: ∫cos(x) dx

![integral vs derivative, cos(x) vs sin(x)](https://www.mathsisfun.com/calculus/images/integral-vs-derivative-sin-cos.svg)

From the [Rules of Derivatives table](https://www.mathsisfun.com/calculus/derivatives-rules.html) we see the derivative of sin(x) is cos(x) so:

> **∫cos(x) dx = sin(x) + C**

But a lot of this "reversing" has already been done (see [Rules of Integration](https://www.mathsisfun.com/calculus/integration-rules.html)).

#### Example: ∫x³ dx

On [Rules of Integration](https://www.mathsisfun.com/calculus/integration-rules.html) there is a "Power Rule" that says:

> **∫xⁿ dx = xⁿ⁺¹/(n+1) + C**

We can use that rule with n=3:

> **∫x³ dx = x⁴/4 + C**

Knowing how to use those rules is the key to being good at Integration.

**Learn the [Rules of Integration](https://www.mathsisfun.com/calculus/integration-rules.html) and Practice! Practice! Practice!**

---

### Definite vs Indefinite Integrals

We have been doing **Indefinite Integrals** so far.

A **Definite Integral** has actual values to calculate between (they are put at the bottom and top of the "S"):

| Type | Description | Symbol |
|------|-------------|--------|
| **Indefinite Integral** | No bounds, includes +C | ![indefinite integral](https://www.mathsisfun.com/calculus/images/indefinite-integral.gif) |
| **Definite Integral** | Has upper and lower bounds | ![definite integral](https://www.mathsisfun.com/calculus/images/definite-integral.gif) |

Read [Definite Integrals](https://www.mathsisfun.com/calculus/integration-definite.html) to learn more.

---

## Rules of Integration

![integral area](https://www.mathsisfun.com/calculus/images/integral-area.svg)

[Integration](https://www.mathsisfun.com/calculus/integration-introduction.html) can be used to find areas, volumes, central points and many useful things. It is often used to find the **area underneath the graph of a function and the x-axis**.

The first rule to know is that integrals and [derivatives](https://www.mathsisfun.com/calculus/derivatives-introduction.html) are opposites!

![integral vs derivative](https://www.mathsisfun.com/calculus/images/integral-vs-derivative.svg)

*Sometimes we can work out an integral, because we know a matching derivative.*

---

### Common Functions Table

| Function Type | Function | Integral |
|--------------|----------|----------|
| **Constant** | ∫a dx | ax + C |
| **Variable** | ∫x dx | x²/2 + C |
| **Square** | ∫x² dx | x³/3 + C |
| **Reciprocal** | ∫(1/x) dx | ln\|x\| + C |
| **Exponential** | ∫eˣ dx | eˣ + C |
| | ∫aˣ dx | aˣ/ln(a) + C |
| **Logarithm** | ∫ln(x) dx | x·ln(x) − x + C |
| **Trigonometry** | ∫cos(x) dx | sin(x) + C |
| *(x in [radians](https://www.mathsisfun.com/geometry/radians.html))* | ∫sin(x) dx | −cos(x) + C |
| | ∫sec²(x) dx | tan(x) + C |

---

### Integration Rules Table

| Rule | Function | Integral |
|------|----------|----------|
| **Multiplication by Constant** | ∫c·f(x) dx | c·∫f(x) dx |
| **Power Rule** (n ≠ −1) | ∫xⁿ dx | xⁿ⁺¹/(n+1) + C |
| **Sum Rule** | ∫(f + g) dx | ∫f dx + ∫g dx |
| **Difference Rule** | ∫(f − g) dx | ∫f dx − ∫g dx |
| **Integration by Parts** | | See [Integration by Parts](https://www.mathsisfun.com/calculus/integration-by-parts.html) |
| **Substitution Rule** | | See [Integration by Substitution](https://www.mathsisfun.com/calculus/integration-by-substitution.html) |

---

### Examples

#### Example: ∫sin(x) dx

From the table above it is listed as being **−cos(x) + C**

It is written as:

> **∫sin(x) dx = −cos(x) + C**

---

#### Example: ∫(1/x) dx

From the table above it is listed as being **ln|x| + C**

It is written as:

> **∫(1/x) dx = ln|x| + C**

The vertical bars **| |** either side of **x** mean [absolute value](https://www.mathsisfun.com/numbers/absolute-value.html), because we don't want to give negative values to the [natural logarithm](https://www.mathsisfun.com/sets/function-logarithmic.html) function **ln**.

---

### Power Rule Examples

#### Example: ∫x³ dx

The question is asking "what is the integral of x³?"

We can use the Power Rule, where n=3:

> **∫xⁿ dx = xⁿ⁺¹/(n+1) + C**

Therefore:

> **∫x³ dx = x⁴/4 + C**

---

#### Example: ∫√x dx

√x is also **x⁰·⁵**

We can use the Power Rule, where n=0.5:

> **∫xⁿ dx = xⁿ⁺¹/(n+1) + C**

Therefore:

> **∫x⁰·⁵ dx = x¹·⁵/1.5 + C**

---

### Multiplication by Constant Example

#### Example: ∫6x² dx

We can move the 6 outside the integral:

```
∫6x² dx = 6∫x² dx
```

And now use the Power Rule on x²:

```
= 6 × (x³/3) + C
= 2x³ + C
```

---

### Sum Rule Example

#### Example: ∫(cos x + x) dx

Use the Sum Rule:

```
∫(cos x + x) dx = ∫cos x dx + ∫x dx
```

Work out the integral of each (using table above):

> **= sin x + x²/2 + C**

---

### Difference Rule Example

#### Example: ∫(eʷ − 3) dw

Use the Difference Rule:

```
∫(eʷ − 3) dw = ∫eʷ dw − ∫3 dw
```

Then work out the integral of each (using table above):

> **= eʷ − 3w + C**

---

### Combined Rules Example

#### Example: ∫(8z + 4z³ − 6z²) dz

**Step 1:** Use the Sum and Difference Rule:

```
∫(8z + 4z³ − 6z²) dz = ∫8z dz + ∫4z³ dz − ∫6z² dz
```

**Step 2:** Apply Constant Multiplication:

```
= 8∫z dz + 4∫z³ dz − 6∫z² dz
```

**Step 3:** Apply Power Rule:

```
= 8(z²/2) + 4(z⁴/4) − 6(z³/3) + C
```

**Step 4:** Simplify:

> **= 4z² + z⁴ − 2z³ + C**

---

## Definite Integrals

You might like to read [Introduction to Integration](https://www.mathsisfun.com/calculus/integration-introduction.html) first!

### What is a Definite Integral?

[Integration](https://www.mathsisfun.com/calculus/integration-introduction.html) can be used to find areas, volumes, central points and many useful things. But it is often used to find the **area under the graph of a function** like this:

![Area under a curve shaded in blue](https://www.mathsisfun.com/calculus/images/integral-area.svg)

The area is found by adding slices that **approach zero in width** (dx):

And there are [Rules of Integration](https://www.mathsisfun.com/calculus/integration-rules.html) that help us get the answer.

![Area under a curve divided into thin vertical slices of width dx](https://www.mathsisfun.com/calculus/images/integral-area-dx.svg)

---

### Notation

![Integral symbol followed by the integrand f(x) and the differential dx](https://www.mathsisfun.com/calculus/images/integral-notation-1.svg)

The symbol for "Integral" is a stylish "S" (for "Sum", the idea of summing slices):

After the Integral Symbol we put the function we want to find the integral of (called the **Integrand**). And then finish with **dx** to mean the slices go in the x direction (and approach zero in width).

---

### Understanding Definite Integrals

A **Definite Integral** has start and end values: in other words there's an **interval** [a, b].

**a** and **b** (called limits, bounds or boundaries) are put at the bottom and top of the "S", like this:

| Type | Notation | Description |
|------|----------|-------------|
| **Definite Integral** | ![Definite integral notation showing limits a and b on the integral symbol](https://www.mathsisfun.com/calculus/images/integral-definite.svg) | From **a** to **b** |
| **Indefinite Integral** | ![indefinite integral](https://www.mathsisfun.com/calculus/images/integral-indefinite.svg) | No specific values |

We find the Definite Integral by calculating the *Indefinite* Integral at **a**, and at **b**, then subtracting:

---

### Example: ∫₁² 2x dx

![Graph of the line y=2x with the area between x=1 and x=2 shaded](https://www.mathsisfun.com/calculus/images/integral-def-1graph.svg)

We are being asked for the **Definite Integral**, from 1 to 2, of **2x** dx

**Step 1:** Find the *Indefinite Integral*

Using the [Rules of Integration](https://www.mathsisfun.com/calculus/integration-rules.html) we find that:

> **∫2x dx = x² + C**

**Step 2:** Calculate at both limits

- At x=1: ∫2x dx = **1² + C**
- At x=2: ∫2x dx = **2² + C**

**Step 3:** Subtract

```
(2² + C) − (1² + C)
= 2² + C − 1² − C
= 4 − 1 + C − C
= 3
```

And "C" gets cancelled out... so with **Definite Integrals we can ignore C**.

**Result:**

> **∫₁² 2x dx = 3**

![area of y=2x from 1 to 2 equals 3](https://www.mathsisfun.com/calculus/images/integral-def-12.svg)

**Check:** With such a simple shape, let's also try calculating the area by geometry:

A = (2+4)/2 × 1 = 3

Yes, it does have an area of 3. (Yay!)

**Notation:** It is usual to show the indefinite integral (without the +C) inside square brackets, with the limits **a** and **b** after, like this:

```
∫₁² 2x dx = [x²]₁² = 2² − 1² = 3
```

---

### Example: ∫₀.₅¹ cos(x) dx

![definite integral y=cos(x) from 0.5 to 1 graph](https://www.mathsisfun.com/calculus/images/integral-def-5.svg)

The Definite Integral, from 0.5 to 1.0, of **cos(x)** dx:

> **∫₀.₅¹ cos(x) dx**

(Note: x must be in [radians](https://www.mathsisfun.com/geometry/radians.html))

The *Indefinite* Integral is:

> **∫cos(x) dx = sin(x) + C**

We can ignore C for definite integrals (as we saw above) and we get:

```
∫₀.₅¹ cos(x) dx = [sin(x)]₀.₅¹
                 = sin(1) − sin(0.5)
                 = 0.841... − 0.479...
                 = 0.362...
```

---

### Example: ∫₀¹ sin(x) dx - An Important Point

![definite integral y=sin(x) from 0 to 1 graph](https://www.mathsisfun.com/calculus/images/integral-def-9.svg)

The Definite Integral, from 0 to 1, of **sin(x)** dx:

> **∫₀¹ sin(x) dx**

The *Indefinite* Integral is:

> **∫sin(x) dx = −cos(x) + C**

Since we are going from 0, **can we** just calculate the integral at x=1?

```
−cos(1) = −0.540...
```

What? It is **negative**? But it looks positive in the graph.

Well... we made a **mistake**!

Because **we need to subtract the integral at x=0**. We shouldn't assume it is zero.

So let's do it properly, subtracting one from the other:

```
∫₀¹ sin(x) dx = [−cos(x)]₀¹
               = −cos(1) − (−cos(0))
               = −0.540... − (−1)
               = 0.460...
```

That's better!

---

### Negative Regions

But we ***can*** have negative regions, when the curve is below the axis:

![definite integral y=cos(x) from 1 to 3](https://www.mathsisfun.com/calculus/images/integral-def-cos-1-3.svg)

#### Example: ∫₁³ cos(x) dx

The Definite Integral, from 1 to 3, of **cos(x)** dx:

Notice that some of it is positive, and some negative. The definite integral will work out the **net** value.

Let's do the calculations:

```
∫₁³ cos(x) dx = [sin(x)]₁³
               = sin(3) − sin(1)
               = 0.141... − 0.841...
               = −0.700...
```

So there's more negative than positive with a net result of −0.700...

**Important Rule:**

> **∫ₐᵇ f(x) dx = (Area above x axis) − (Area below x axis)**

Try integrating cos(x) with different start and end values to see for yourself how positives and negatives work.

---

### Positive Area Only

But sometimes we want all area treated as **positive** (without the part below the axis being subtracted).

In that case we must calculate the areas **separately**, like in this example:

![area y=cos(x) from 1 to 3 positive both above and below](https://www.mathsisfun.com/calculus/images/integral-def-cos-1-3p.svg)

#### Example: Total Area between y = cos(x) and the x-axis, from x = 1 to x = 3

This is like the example we just did, but now we expect that **it is all positive** (imagine we had to paint it).

So now we have to do the parts separately:

- One for the area above the x-axis
- One for the area below the x-axis

The curve crosses the x-axis at x = π/2 so we have:

**From 1 to π/2:**

```
∫₁^(π/2) cos(x) dx = sin(π/2) − sin(1)
                    = 1 − 0.841...
                    = 0.158...
```

**From π/2 to 3:**

```
∫_(π/2)³ cos(x) dx = sin(3) − sin(π/2)
                    = 0.141... − 1
                    = −0.859...
```

That last one comes out negative, but we want it to be positive, so:

> **Total area = 0.158... + 0.859... = 1.017...**

This is very different from the answer in the previous example.

---

### Continuity Requirement

Oh yes, the function we are integrating must be [Continuous](https://www.mathsisfun.com/calculus/continuity.html) between **a** and **b**: no holes, jumps or vertical asymptotes (where the function heads up/down toward infinity).

![Graph of a function with a vertical asymptote between limits a and b](https://www.mathsisfun.com/calculus/images/continuous-asymp-no.gif)

#### Example:
A vertical asymptote between **a** and **b** affects the definite integral.

---

### Properties of Definite Integrals

#### 1. Area Above − Area Below

The integral adds the area above the axis but subtracts the area below, for a "net value":

> **∫ₐᵇ f(x) dx = (Area above x axis) − (Area below x axis)**

#### 2. Adding Functions

The integral of **f+g** equals the integral of **f** plus the integral of **g**:

> **∫ₐᵇ [f(x) + g(x)] dx = ∫ₐᵇ f(x) dx + ∫ₐᵇ g(x) dx**

#### 3. Reversing the Interval

![definite integral negative property](https://www.mathsisfun.com/calculus/images/integral-def-propneg.svg)

Reversing the direction of the interval gives the negative of the original direction:

> **∫ₐᵇ f(x) dx = −∫ᵇₐ f(x) dx**

#### 4. Interval of Zero Length

![definite integral area zero](https://www.mathsisfun.com/calculus/images/integral-def-prop0.svg)

When the interval starts and ends at the same place, the result is zero:

> **∫ₐₐ f(x) dx = 0**

#### 5. Adding Intervals

![area a to b = a to c plus c to b](https://www.mathsisfun.com/calculus/images/integral-def-prop-add.svg)

We can also add two adjacent intervals together:

> **∫ₐᵇ f(x) dx = ∫ₐᶜ f(x) dx + ∫ᶜᵇ f(x) dx**

---

### Summary

> **The Definite Integral between a and b is the Indefinite Integral at b minus the Indefinite Integral at a.**

---

## Integration by Parts

Integration by Parts is a special method of integration that is often useful when two functions are multiplied together, but is also helpful in other ways.

You will see plenty of examples soon, but first let us see the rule:

> **∫u v dx = u∫v dx − ∫u' (∫v dx) dx**

Where:
- **u** is the function u(x)
- **v** is the function v(x)
- **u'** is the [derivative](https://www.mathsisfun.com/calculus/derivatives-rules.html) of the function u(x)

The rule as a diagram:

![integration by parts general](https://www.mathsisfun.com/calculus/images/integral-parts-general.svg)

---

### The Process

Follow these steps:

1. Choose u and v
2. Differentiate u: u'
3. Integrate v: ∫v dx
4. Put u, u' and ∫v dx into: **u∫v dx − ∫u' (∫v dx) dx**
5. Simplify and solve

In English we can say that **∫u v dx** becomes:

> **(u integral v) minus integral of (derivative u, integral v)**

Let's get straight into examples:

---

### Example: ∫x cos(x) dx

OK, we have **x** *multiplied by* **cos(x)**, so integration by parts is a good choice.

**Step 1:** Choose which functions for **u** and **v**:

- u = x
- v = cos(x)

So now it is in the format **∫u v dx** we can proceed:

**Step 2:** Differentiate **u**: 

```
u' = x' = 1
```

**Step 3:** Integrate **v**: 

```
∫v dx = ∫cos(x) dx = sin(x)
```

*(see [Integration Rules](https://www.mathsisfun.com/calculus/integration-rules.html))*

**Step 4:** Now we can put it together:

![integration by parts x cos(x) dx](https://www.mathsisfun.com/calculus/images/integral-parts-x-cosx.svg)

**Step 5:** Simplify and solve:

```
= x sin(x) − ∫sin(x) dx
= x sin(x) + cos(x) + C
```

Done!

### The ILATE Rule

Choose a **u** that gets simpler when you differentiate it and a **v** that doesn't get any more complicated when you integrate it.

A helpful rule of thumb is **ILATE**. Choose **u** based on which of these comes first:

| Priority | Type | Examples |
|----------|------|----------|
| **I** | [Inverse trigonometric functions](https://www.mathsisfun.com/algebra/trig-inverse-sin-cos-tan.html) | sin⁻¹(x), cos⁻¹(x), tan⁻¹(x) |
| **L** | [Logarithmic](https://www.mathsisfun.com/sets/function-logarithmic.html) functions | ln(x), log(x) |
| **A** | [Algebraic](https://www.mathsisfun.com/numbers/algebraic-numbers.html) functions | x², x³ |
| **T** | [Trigonometric functions](https://www.mathsisfun.com/sine-cosine-tangent.html) | sin(x), cos(x), tan(x) |
| **E** | [Exponential functions](https://www.mathsisfun.com/sets/function-exponential.html) | eˣ, 3ˣ |

---

### Footnote: Where Did "Integration by Parts" Come From?

It is based on the [Product Rule for Derivatives](https://www.mathsisfun.com/calculus/derivatives-rules.html):

> **(uv)' = uv' + u'v**

Integrate both sides and rearrange:

```
∫(uv)' dx = ∫uv' dx + ∫u'v dx
uv = ∫uv' dx + ∫u'v dx
∫uv' dx = uv − ∫u'v dx
```

Some people prefer that last form, but I like to replace **v' with w** and **v with ∫w dx** which makes the left side simpler:

> **∫uw dx = u∫w dx − ∫u'(∫w dx) dx**

---

## Integration by Substitution

"Integration by Substitution" (also called "u-Substitution" or "The Reverse Chain Rule") is a method to find an integral, but only when it can be set up in a special way.

---

### Understanding Substitution Step by Step

Let's break down exactly what happens when we do substitution, using a real example.

---

#### Step 1: Start With The Integral

We want to solve:

> **∫10x(x² + 1)⁴ dx**

Forget integration for a moment. Look only at the pieces:

```
  10x      (x² + 1)⁴
   ↑            ↑
outside      inside expression
```

---

#### Step 2: Identify the Complicated Part

The complicated part is:

> **x² + 1**

So we decide:

> **u = x² + 1**

This is just giving it a nickname.

**Think:** u = x² + 1

Now everywhere we see **x² + 1**, we'll eventually replace it by **u**.

---

#### Step 3: Why Find du?

We need to replace everything involving **x**.

The integral must become completely in terms of **u**.

So differentiate:

```
u = x² + 1
```

Derivative:

```
du/dx = 2x
```

Now multiply both sides by **dx**:

> **du = 2x dx**

This is the step students usually memorize.

---

#### Step 4: What Does du = 2x dx Mean?

It means:

> **2x dx** can be replaced by **du**

They're the same thing.

**Think of it like this:**

- 1 dozen eggs = 12 eggs
- If I see 12 eggs, I can replace it with 1 dozen
- If I see **2x dx**, I can replace it with **du**

---

#### Step 5: Go Back To The Integral

We had:

```
∫10x(x² + 1)⁴ dx
```

Let's focus on the **10x dx** part.

Write:

> **10x dx = 5(2x dx)**

**Why?**

Because 5(2x) = 10x

Nothing magical happened. Just factoring out a 5.

---

#### Step 6: Replace Using du

We know:

> **du = 2x dx**

So replace **2x dx** by **du**:

```
5(2x dx) = 5 du
```

Thus:

> **10x dx = 5 du**

That's the step that looked mysterious.

---

#### Step 7: Replace The Other Part

Remember:

> **u = x² + 1**

Therefore:

> **(x² + 1)⁴ = u⁴**

---

#### Step 8: Replace Everything

**Original:**

```
∫10x(x² + 1)⁴ dx
```

**Replace:**

- 10x dx → 5 du
- (x² + 1)⁴ → u⁴

**So:**

> **∫10x(x² + 1)⁴ dx = ∫5u⁴ du**

Now there is **no x left**. Only **u**.

---

#### Step 9: Integrate

Use the power rule:

```
∫u⁴ du = u⁵/5
```

So:

```
∫5u⁴ du = 5(u⁵/5)
```

The 5's cancel:

> **= u⁵**

Thus:

> **u⁵ + C**

---

#### Step 10: Replace u Back

Remember:

> **u = x² + 1**

So:

> **u⁵ = (x² + 1)⁵**

**Final Answer:**

> **∫10x(x² + 1)⁴ dx = (x² + 1)⁵ + C**

---

### The Substitution Method Summary

**The Process:**

1. **Identify** the complicated part → call it **u**
2. **Differentiate** u to get **du/dx**
3. **Rearrange** to get **du = ... dx**
4. **Rewrite** the integral in terms of **u** and **du**
5. **Integrate** with respect to **u**
6. **Substitute** back to get the answer in terms of **x**

**Key Point:** Everything must be replaced. No **x** should remain after substitution!


---

## Fundamental Theorems of Calculus

### Overview

In **simple terms** these are the fundamental theorems of calculus:

**1. Derivatives and Integrals are Opposites**

[Derivatives](https://www.mathsisfun.com/calculus/derivatives-introduction.html) and [Integrals](https://www.mathsisfun.com/calculus/integration-introduction.html) are the inverse (opposite) of each other.

![integral vs derivative](https://www.mathsisfun.com/calculus/images/integral-vs-derivative.svg)

**2. The Evaluation Theorem**

When we know the indefinite integral:

> **F = ∫f(x) dx**

We can then calculate a [definite integral](https://www.mathsisfun.com/calculus/integration-definite.html) between a and b by the **difference** between the values of the indefinite integrals at b and a:

> **∫ₐᵇ f(x) dx = F(b) − F(a)**

Let's explore the details:

---

### First Fundamental Theorem of Calculus

For a continuous function *f(x)* on an interval *[a, b]* with the integral:

> **F(x) = ∫ₐˣ f(t) dt**

then the **derivative of the integral** F(x) gets us the original function f(x) back again:

> **F'(x) = f(x)**

This means that the **derivative of the integral** of **f** with respect to its upper limit is the function **f** itself.

---

#### Example: f(x) = 2x

The integral of 2x is x², and using the second theorem (below):

```
F(x) = ∫ₐˣ 2t dt = x² − a²
```

Taking the derivative:

```
F'(x) = d/dx(x² − a²) = 2x − 0 = 2x
```

So the **derivative of the integral** of 2x got us 2x back again.

---

#### Example: Constant Speed

A car travels at a constant speed of 50 km per hour for exactly one hour:

| Concept | Value |
|---------|-------|
| **Speed** | 50 km per hour |
| **Integral** of 50 km per hour for one hour | 50 km |
| **Derivative** of 50 km over one hour | 50 km per hour |

![integral vs derivative](https://www.mathsisfun.com/calculus/images/integral-vs-derivative-ex1.svg)

*Note: "C" is however far the car had traveled already.*

---

### Second Fundamental Theorem of Calculus

When we have a continuous function *f(x)* on an interval *[a, b]*, and its indefinite integral is F(x), then:

> **∫ₐᵇ f(x) dx = F(b) − F(a)**

In other words the definite integral of *f(x)* from *a* to *b* equals the difference in the values of *F(x)* at *b* and *a*

This makes calculating a definite integral easy if we can find its indefinite integral.

---

#### Example: Filling a Tank

Imagine we're filling a tank with water, and the rate at which water flows into the tank is given by *f(t)*, where *t* is time in minutes.

If *F(t)* measures the total volume of water in the tank at any time *t*, then the amount of water added to the tank between times *a* and *b* is *F(b) - F(a)*.

**Given:**
- f(t) = t²
- F(t) = t³/3

So the amount of water added to the tank between 3 and 6 minutes is:

```
∫₃⁶ f(t) dt = F(6) − F(3)
             = 6³/3 − 3³/3
             = 72 − 9
             = 63
```

**Result:** 63 cubic units of water were added to the tank.

---

### Key Takeaways

To find a definite integral (the area between two specific points, **a** and **b**), you use the indefinite integral function (**F**) as your tool.

**Think of it this way:**

- The **indefinite integral** gives you a general formula **F(x)** for the accumulation or area
- The **definite integral** uses that formula at the specific boundary numbers **b** and **a** to get a final, concrete numerical answer

**The process is always:**

1. Find the indefinite function first: **F(x) = ∫f(x) dx**
2. Plug in the top number: **F(b)**
3. Plug in the bottom number: **F(a)**
4. Subtract: **F(b) − F(a)**

---

### Summary of Both Theorems

| Theorem | Statement | Meaning |
|---------|-----------|---------|
| **First Fundamental Theorem** | If F(x) = ∫ₐˣ f(t) dt, then F'(x) = f(x) | The derivative "undoes" the integral |
| **Second Fundamental Theorem** | ∫ₐᵇ f(x) dx = F(b) − F(a) | Provides an easy way to calculate definite integrals |

**Together:** These theorems connect differentiation and integration as inverse operations and provide practical methods for calculation.