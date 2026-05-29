# Linear Algebra

Linear algebra is a fundamental branch of mathematics that deals with vectors, matrices, and linear transformations. 
It's used to represent and manipulate data mathematically. 

## Table of Contents

- [Vectors](#vectors)
  - [Magnitude & Direction](#magnitude--direction)
- [Vector Addition](#vector-addition)
- [Scalar Multiplication](#scalar-multiplication)
- [Basis Vectors](#basis-vectors)
- [Linear Combinations](#linear-combinations)
- [Span](#span)
- [Linear Dependence and Independence](#linear-dependence-and-independence)
- [Linear Transformations](#linear-transformations)

---

## Vectors

A **vector** is an object that stores **magnitude** and **direction**.

> **Note:** A vector in 2D space can be represented as an ordered pair of numbers, such as (x, y), where x and y are the components of the vector along the x and y axes, respectively.

<details>
<summary><strong>📐 Vector Representation</strong></summary>

A vector $\vec{v}$ with components $(x, y)$ can be written as:

$$\vec{v} = \begin{bmatrix} x \\ y \end{bmatrix}$$

**Example:** $\vec{v} = \begin{bmatrix} 2 \\ 3 \end{bmatrix}$

</details>


### Magnitude & Direction

| Property | Formula | Example for $\vec{v} = [2, 3]$ |
|----------|---------|-------------------------------|
| **Magnitude** | $\|\vec{v}\| = \sqrt{x^2 + y^2}$ | $\sqrt{2^2 + 3^2} = \sqrt{13} \approx 3.61$ |
| **Direction** | $\theta = \arctan\left(\frac{y}{x}\right)$ | $\arctan\left(\frac{3}{2}\right) \approx 56.31°$ |

---

## Vector Addition

Vector addition combines two vectors by adding their corresponding components.

<details>
<summary><strong>🧮 Formula</strong></summary>

Given vectors $\vec{a} = \begin{bmatrix} a_1 \\ a_2 \end{bmatrix}$ and $\vec{b} = \begin{bmatrix} b_1 \\ b_2 \end{bmatrix}$:

$$\vec{a} + \vec{b} = \begin{bmatrix} a_1 + b_1 \\ a_2 + b_2 \end{bmatrix}$$

</details>

### Example: 

Given $\vec{a} = [2, 3]$ and $\vec{b} = [4, -1]$:
$$\vec{a} + \vec{b} = [2 + 4, 3 + (-1)] = [6, 2]$$

---

## Scalar Multiplication

Scalar multiplication scales a vector by a constant factor. which means stretching, squishing, or flipping its direction—by multiplying its components by a number (or "scalar")

<details>
<summary><strong>🧮 Formula</strong></summary>

Given a scalar $k$ and vector $\vec{v} = \begin{bmatrix} v_1 \\ v_2 \end{bmatrix}$:

$$k \cdot \vec{v} = \begin{bmatrix} k \cdot v_1 \\ k \cdot v_2 \end{bmatrix}$$

</details>

### Interactive Example: Scalar Multiplication

<div style="background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%); padding: 20px; border-radius: 12px; color: white; margin: 15px 0;">

**Try different scalars!**

| Scalar $k$ | Vector $\vec{v}$ | Result $k \cdot \vec{v}$ | Effect |
|------------|------------------|--------------------------|--------|
| 2 | $[2, 3]$ | $[4, 6]$ | 🔼 Doubles length |
| 0.5 | $[2, 3]$ | $[1, 1.5]$ | 🔽 Halves length |
| -1 | $[2, 3]$ | $[-2, -3]$ | 🔄 Reverses direction |
| 0 | $[2, 3]$ | $[0, 0]$ | ⭕ Zero vector |

</div>

---

## Basis Vectors

The coordinate systems(vectors) are built upon a set of basis vectors. Coordinates(vectors) are treated as scalars that stretch or squish these basis vectors. The chosen basis vectors are the reference frame that gives numerical meaning to vectors.

### Example:

Given $\vec{a} = [3, -2]$

In simple terms, scaling a basis vector $\hat{i}$ by 3 gives us $3\hat{i}$, and scaling a basis vector $\hat{j}$ by -2 gives us $-2\hat{j}$. Adding these together gives us the original vector $\vec{a}$.

---

## Linear Combinations

A linear coombination of vectors is a sum of scalar multiples of those vectors. It allows us to express a vector as a combination of other vectors.

Linear combination of $\vec{v} and \vec{w}$ can be expressed as:

$$a \vec{v} + b \vec{w}$$

Where $a$ and $b$ are scalars.

by adjusting the values of $a$ and $b$, we can create different vectors from $\vec{v}$ and $\vec{w}$, demonstrating how they can be combined to form new vectors in the same space.

---

## Span

The span of a set of vectors is the collection of all possible vectors reachable by creating all possible linear combinations of them. It represents the entire space that can be covered by those vectors.

![Span of Vectors](https://i.makeagif.com/media/8-19-2022/VLZ0cJ.gif)

---

## Linear Dependence and Independence

| Type | Description |
|------|-------------|
| **Linearly Dependent** | Occurs when at least one vector in a set is redundant, meaning it lies within the span of the others and contributes no new dimensions. |
| **Linearly Independent** | Occurs when every vector in a set adds a new dimension to the span, meaning none can be expressed as a linear combination of the others. |


## Linear Transformations

A linear transformation is a mapping between vector spaces that preserves vector addition and scalar multiplication. Geometrically, it performs operations like scaling, rotation, reflection, or shearing without breaking the linear structure of space.

> **Note:** A linear transformation preserves the structure of vector operations. Whether we add vectors before transformation or transform them individually and then add, the result remains the same. The same applies to scalar multiplication.

### Properties

A transformation $T$ is linear if and only if it satisfies both:

| Property | Condition |
|----------|----------|
| **Preserves Addition** | $T(\vec{v} + \vec{w}) = T(\vec{v}) + T(\vec{w})$ |
| **Preserves Scalar Multiplication** | $T(c\vec{v}) = cT(\vec{v})$ |

### Example:

<details>
<summary><strong>🧮 Proving Linearity</strong></summary>

Suppose:

$$T(x, y) = (2x, 2y)$$

Take: $\vec{v} = (1, 2)$ and $\vec{w} = (3, 1)$

---

**Method 1 — Add first, then transform:**

$$\vec{v} + \vec{w} = (4, 3)$$

$$T(4, 3) = (8, 6)$$

**Method 2 — Transform first, then add:**

$$T(1, 2) = (2, 4)$$

$$T(3, 1) = (6, 2)$$

$$(2, 4) + (6, 2) = (8, 6)$$

---

Same result. So it preserves addition.

But remember:

A transformation is linear only if it also preserves scalar multiplication:

$$T(c\vec{v}) = cT(\vec{v})$$

</details>