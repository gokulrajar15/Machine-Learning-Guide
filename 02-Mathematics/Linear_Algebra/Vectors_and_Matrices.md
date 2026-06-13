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
- [Matrices](#matrices)
- [Matrix Composition](#matrix-composition)
  - [Numerical Computation](#numerical-computation)
  - [Properties of Matrix Multiplication](#properties-of-matrix-multiplication)
- [Determinant](#determinant)
  - [Key Determinant Values](#key-determinant-values)
  - [Determinant in 3D](#determinant-in-3d)
  - [2×2 Formula Intuition](#2x2-formula-intuition)
- [Inverse Matrices, Column Space & Null Space](#inverse-matrices-column-space--null-space)
  - [Linear Systems of Equations](#linear-systems-of-equations)
  - [Inverse Matrices](#inverse-matrices)
  - [Rank & Column Space](#rank--column-space)
  - [Null Space (Kernel)](#null-space-kernel)
- [Dot Products & Duality](#dot-products--duality)
  - [Geometric Interpretation](#geometric-interpretation)
  - [Symmetry of the Dot Product](#symmetry-of-the-dot-product)
  - [Duality](#duality)
- [Eigenvectors & Eigenvalues](#eigenvectors--eigenvalues)
  - [Finding Eigenvectors & Eigenvalues](#finding-eigenvectors--eigenvalues)
  - [Special Geometric Scenarios](#special-geometric-scenarios)
  - [Eigenbasis & Diagonal Matrices](#eigenbasis--diagonal-matrices)
- [Interview Explanations](#interview-explanations)

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

A linear transformation is a rule or function that maps vectors from one space to another while preserving the structural properties of vector addition and scalar multiplication

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

---

## Matrices

A **matrix** is a rectangular array of numbers arranged in rows and columns. It encodes a linear transformation by storing where the basis vectors land after the transformation.

> **Key Insight:** A 2×2 matrix stores the transformed $\hat{i}$ as its first column and the transformed $\hat{j}$ as its second column. The transformation is entirely determined by these two columns.

<details>
<summary><strong>📐 Matrix Representation</strong></summary>

A 2×2 matrix representing a linear transformation:

$$M = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$$

Where:
- First column $\begin{bmatrix} a \\ c \end{bmatrix}$ = where $\hat{i}$ lands
- Second column $\begin{bmatrix} b \\ d \end{bmatrix}$ = where $\hat{j}$ lands

Applying this to a vector $\vec{v} = \begin{bmatrix} x \\ y \end{bmatrix}$:

$$M\vec{v} = x \begin{bmatrix} a \\ c \end{bmatrix} + y \begin{bmatrix} b \\ d \end{bmatrix} = \begin{bmatrix} ax + by \\ cx + dy \end{bmatrix}$$

</details>

---

## Matrix Composition

Matrix composition captures the idea of applying multiple linear transformations **sequentially** and representing the combined effect as a single matrix.

> **Core Idea:** If you rotate the plane and then shear it, the net effect is itself a linear transformation — representable by one matrix called the **composition**.

### How It Works

1. Apply the **right** matrix first (transforms basis vectors)
2. Then apply the **left** matrix to the result
3. The product matrix stores the final landing positions of $\hat{i}$ and $\hat{j}$

> **Reading Order:** Matrix multiplication reads **right to left**, following function notation — $M_2 \cdot M_1$ means "apply $M_1$ first, then $M_2$".

### Properties of Matrix Multiplication

| Property | Statement | Intuition |
|----------|-----------|----------|
| **Non-commutative** | $AB \neq BA$ (in general) | Shear → Rotate ≠ Rotate → Shear; order changes the geometric outcome |
| **Associative** | $A(BC) = (AB)C$ | Both sides mean: apply $C$, then $B$, then $A$ — same sequence, same result |

<details>
<summary><strong>🔄 Why Order Matters (Non-commutativity)</strong></summary>

Consider a rotation $R$ and a shear $S$:

- $R \cdot S$ → shear first, then rotate
- $S \cdot R$ → rotate first, then shear

These yield **different** final positions for the basis vectors, hence different matrices. Geometrically, the intermediate grid looks completely different depending on which transformation is applied first.

</details>

<details>
<summary><strong>✅ Why Associativity Holds</strong></summary>

$A(BC) = (AB)C$ because both expressions describe the same sequence of geometric actions:

1. Transform by $C$
2. Transform by $B$
3. Transform by $A$

Grouping doesn't change the sequence — only the intermediate "packaging" of partial compositions differs, not the final outcome.

</details>

---

## Determinant

The **determinant** of a matrix measures the factor by which a linear transformation scales areas (in 2D) or volumes (in 3D). It answers: "How much does the transformation stretch or squish space?"

> **Geometric Definition:** Track the 1×1 unit square formed by $\hat{i}$ and $\hat{j}$. After transformation, whatever factor that square's area changes by — that's the determinant. All other regions scale by the same factor.

$$\det\begin{bmatrix} a & b \\ c & d \end{bmatrix} = ad - bc$$

### Key Determinant Values

| Determinant Value | Geometric Meaning |
|-------------------|-------------------|
| $\det = 1$ | Area is preserved (no scaling) |
| $\det = 3$ | Areas tripled |
| $\det = 0$ | Space collapses to a line or point — columns are **linearly dependent** |
| $\det < 0$ | Orientation is **flipped** (e.g., $\hat{j}$ ends up on the opposite side of $\hat{i}$) |

> **Zero Determinant:** If $\det(M) = 0$, the transformation squishes all of 2D space onto a lower dimension (a line or point). This is equivalent to saying the columns of $M$ are linearly dependent.

> **Negative Determinant:** The absolute value still tells you the area scaling factor, but the negative sign indicates the transformation inverts the orientation of space — like flipping a sheet of paper.

### Determinant in 3D

In 3D, the determinant measures **volume** scaling:

- Track the 1×1×1 unit cube formed by $\hat{i}$, $\hat{j}$, $\hat{k}$
- After transformation, it becomes a **parallelepiped**
- The determinant = volume of that parallelepiped (with sign indicating orientation)

| Sign | Meaning |
|------|---------|
| $\det > 0$ | Right-hand rule preserved |
| $\det < 0$ | Orientation flipped (left-handed) |
| $\det = 0$ | Volume squished to zero — space collapses to a plane, line, or point |

### 2×2 Formula Intuition

For $M = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$, the formula $ad - bc$ can be understood geometrically:

<details>
<summary><strong>📐 Breaking Down ad − bc</strong></summary>

- $a$ and $d$ represent diagonal stretching — they scale the unit square along its natural axes → contribute to area growth ($ad$)
- $b$ and $c$ represent off-diagonal shearing — they skew the square, effectively "stealing" area → subtract from the total ($bc$)

The net signed area of the parallelogram formed by the transformed basis vectors = $ad - bc$.

</details>

### Composition Property

$$\det(AB) = \det(A) \cdot \det(B)$$

> **Intuition:** If $A$ scales areas by factor 3 and $B$ scales areas by factor 2, then applying $B$ then $A$ scales areas by $3 \times 2 = 6$. Successive scaling factors multiply.

---

## Inverse Matrices, Column Space & Null Space

This section connects linear transformations to solving systems of equations and introduces the key subspaces associated with a matrix.

### Linear Systems of Equations

A system of linear equations is a collection of two or more linear equations involving the same variables, where we need to find values of the variables that satisfy all equations simultaneously.

A system of linear equations can be expressed as a single matrix-vector equation:

$$A\vec{x} = \vec{v}$$

> **Geometric Interpretation:** Solving $A\vec{x} = \vec{v}$ means finding the vector $\vec{x}$ that, after being transformed by $A$, lands exactly on $\vec{v}$.

<details>
<summary><strong>🧮 Example</strong></summary>

The system:
$$2x + 5y + 3z = -3$$
$$4x + 0y + 8z = 0$$
$$1x + 3y + 0z = 2$$

Becomes:

$$\begin{bmatrix} 2 & 5 & 3 \\ 4 & 0 & 8 \\ 1 & 3 & 0 \end{bmatrix} \begin{bmatrix} x \\ y \\ z \end{bmatrix} = \begin{bmatrix} -3 \\ 0 \\ 2 \end{bmatrix}$$

We seek the input vector that the transformation $A$ maps onto $\vec{v}$.

</details>

---

### Inverse Matrices

The **inverse** $A^{-1}$ is the unique transformation that undoes the action of $A$ — it "runs the transformation in reverse."

$$A^{-1} A = I \quad \text{(Identity matrix — does nothing to space)}$$

To solve $A\vec{x} = \vec{v}$:

$$\vec{x} = A^{-1}\vec{v}$$

| Condition | Inverse Exists? | Reason |
|-----------|----------------|--------|
| $\det(A) \neq 0$ | ✅ Yes | Space isn't collapsed — every output traces back to a unique input |
| $\det(A) = 0$ | ❌ No | Space is squished to a lower dimension — you can't "unsquish" a line back into a plane |

> **Why no inverse when det = 0?** A function can only map each input to a single output. If a transformation collapses 2D space onto a line, there's no function that maps each point on that line back to the unique original 2D point — multiple inputs collapsed onto the same output.

---

### Rank & Column Space

**Column Space** — the set of all possible outputs of the transformation $A$. It is the span of the columns of the matrix (i.e., where the basis vectors can reach).

**Rank** — the number of dimensions in the column space.

In simple terms, the rank tells you how many dimensions after transformation. 
| Rank | Output Space | Example (3×3 matrix) |
|------|-------------|---------------------|
| 1 | Line | All outputs collapse to a line |
| 2 | Plane | All outputs collapse to a plane |
| 3 (full rank) | All of 3D space | No collapse — inverse exists |

> **Full Rank:** A matrix is full rank when its rank equals its number of columns. This means the transformation doesn't collapse any dimension, and the only vector that maps to the origin is $\vec{0}$ itself.

---

### Null Space (Kernel)

The **null space** (or kernel) of a matrix $A$ is the set of all vectors that land on the **origin** after the transformation:

$$\text{Null}(A) = \{\vec{x} \mid A\vec{x} = \vec{0}\}$$

| Matrix Rank | Null Space |
|-------------|------------|
| Full rank | Only $\vec{0}$ (trivial) |
| Rank 2 (in 3D) | A line of vectors squished to origin |
| Rank 1 (in 3D) | A plane of vectors squished to origin |

> **Connection to Systems:** When solving $A\vec{x} = \vec{0}$, the null space gives you the complete set of solutions. For non-full-rank matrices, this is an entire line or plane of vectors — not just the zero vector.

<details>
<summary><strong>💡 Geometric Intuition</strong></summary>

If a 3D transformation squishes space onto a 2D plane (rank 2), then an entire line of vectors perpendicular to that plane gets collapsed to the origin. That line *is* the null space.

If it squishes space onto a line (rank 1), then a whole plane of vectors gets collapsed to the origin — that plane is the null space.

</details>

---

## Dot Products & Duality

The **dot product** connects algebra (multiplying coordinates) with geometry (projecting vectors). It also reveals a deep relationship between vectors and linear transformations called **duality**.

### Numerical Definition

Multiply corresponding coordinates and sum:

$$\vec{v} \cdot \vec{w} = v_1 w_1 + v_2 w_2$$

**Example:** $(1, 2) \cdot (3, 4) = 1(3) + 2(4) = 11$

### Geometric Interpretation

The dot product equals the length of the projection of $\vec{v}$ onto $\vec{w}$, multiplied by the length of $\vec{w}$:

$$\vec{v} \cdot \vec{w} = \|\vec{v}\| \cdot \|\vec{w}\| \cdot \cos\theta$$

| Dot Product Value | Geometric Meaning |
|-------------------|-------------------|
| $> 0$ | Vectors point in a similar direction |
| $= 0$ | Vectors are **perpendicular** (orthogonal) |
| $< 0$ | Vectors point in generally opposite directions |

### Symmetry of the Dot Product

The dot product is **commutative**: $\vec{v} \cdot \vec{w} = \vec{w} \cdot \vec{v}$

> **Why?** Although projecting $\vec{v}$ onto $\vec{w}$ looks visually different from projecting $\vec{w}$ onto $\vec{v}$, the resulting products are equal. When both vectors are unit length, their projections onto each other are symmetric. Scaling one vector by a constant scales both sides equally.

### From 2D to 1D: The 1×2 Matrix

A linear transformation from 2D to the number line (1D) is encoded by a **1×2 matrix**:

$$\begin{bmatrix} u_1 & u_2 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = u_1 x + u_2 y$$

This is computationally **identical** to the dot product $\vec{u} \cdot \vec{v}$. This isn't a coincidence — it's the key to understanding duality.

### Duality

**Duality** is the natural correspondence between two seemingly different mathematical objects:

| Object | Perspective |
|--------|------------|
| A **vector** $\vec{u}$ in 2D | A geometric arrow with magnitude and direction |
| A **1×2 matrix** $[u_1 \; u_2]$ | A linear transformation projecting 2D space onto a number line |

These are **the same thing** viewed from two angles:

- Every vector $\vec{u}$ defines a linear transformation: "project onto $\vec{u}$ and scale"
- Every linear transformation to 1D corresponds to a unique vector

> **Why the formula works geometrically:** Taking the dot product with a unit vector $\hat{u}$ is the same as projecting onto the line spanned by $\hat{u}$. The 1×2 matrix $[u_1 \; u_2]$ literally performs this projection. The algebraic formula (multiply and add) and the geometric operation (project and scale) are two descriptions of the same linear transformation.

<details>
<summary><strong>💡 Summary of the Connection</strong></summary>

1. A 1×2 matrix transforms 2D vectors into numbers
2. Computing that matrix-vector product looks exactly like a dot product
3. Therefore, dotting with a vector $\vec{u}$ = applying the linear transformation that projects space onto the line of $\vec{u}$
4. This vector ↔ transformation correspondence is **duality**

</details>

---

## Eigenvectors & Eigenvalues

When a linear transformation is applied, most vectors get knocked off their original span. But certain special vectors **stay on their own line** — the transformation only stretches, squishes, or reverses them without changing their direction.

- **Eigenvector:** A nonzero vector that remains on the same span (line) after the transformation.
- **Eigenvalue:** The scalar factor by which that eigenvector is stretched or squished during the transformation.

$$A\vec{v} = \lambda\vec{v}$$

Where $A$ is the transformation matrix, $\vec{v}$ is the eigenvector, and $\lambda$ is the eigenvalue.

> **3D Rotation Example:** An eigenvector with eigenvalue 1 in a 3D rotation identifies the **axis of rotation** — the line that stays fixed while everything else rotates around it.

---

### Finding Eigenvectors & Eigenvalues

Rewrite the eigen-equation using the identity matrix $I$:

$$A\vec{v} = \lambda\vec{v} \quad \Rightarrow \quad (A - \lambda I)\vec{v} = \vec{0}$$

For a **nonzero** $\vec{v}$ to satisfy this, the matrix $(A - \lambda I)$ must squish space into a lower dimension, which means:

$$\det(A - \lambda I) = 0$$

<details>
<summary><strong>🧮 Step-by-Step Process</strong></summary>

1. Set up $(A - \lambda I)$ by subtracting $\lambda$ from each diagonal entry of $A$
2. Compute the determinant and set it equal to zero
3. Solve the resulting polynomial — roots are the **eigenvalues**
4. For each eigenvalue $\lambda$, plug back into $(A - \lambda I)\vec{v} = \vec{0}$ to find the corresponding **eigenvectors**

</details>

---

### Special Geometric Scenarios

| Scenario | Eigenvalues | Eigenvectors | Geometric Intuition |
|----------|-------------|--------------|--------------------|
| **90° Rotation (2D)** | $i, -i$ (complex) | None (real) | Every vector is knocked off its span — no line stays fixed |
| **Shear** | $\lambda = 1$ (repeated) | Single line (e.g., x-axis) | Only vectors along one axis remain on their span |
| **Uniform Scaling by 2** | $\lambda = 2$ | Every vector | All vectors stay on their span — everything just doubles in length |

---

### Eigenbasis & Diagonal Matrices

If a transformation has enough eigenvectors to **span the entire space**, you can use them as a new coordinate basis — called an **eigenbasis**.

In this eigenbasis, the transformation matrix becomes **diagonal**:

$$\begin{bmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{bmatrix}$$

The diagonal entries are the eigenvalues — each basis vector simply gets scaled.

> **Why this matters:** Computing $M^{100}$ with a general matrix is extremely expensive. With a diagonal matrix, you just raise each diagonal entry to the 100th power:

$$\begin{bmatrix} \lambda_1^{100} & 0 \\ 0 & \lambda_2^{100} \end{bmatrix}$$

<details>
<summary><strong>⚡ Diagonalization Workflow</strong></summary>

1. Find the eigenvectors of $A$ and form a change-of-basis matrix $P$
2. Convert to eigenbasis: $D = P^{-1}AP$ (diagonal matrix)
3. Compute the power: $D^n$ (trivial — just raise each eigenvalue)
4. Convert back: $A^n = P D^n P^{-1}$

This bypasses immense amounts of matrix multiplication.

</details>

---

## Interview Explanations

Concise answers to common interview questions on linear algebra fundamentals.

---

### Q: What is a matrix and what does it represent?

> A matrix is a rectangular grid of numbers that represents a **linear transformation**. Each column tells you where a basis vector lands after the transformation. So a 2×2 matrix completely describes how 2D space gets stretched, rotated, or squished — you just need to know where $\hat{i}$ and $\hat{j}$ end up.

---

### Q: What is the rank of a matrix?

> The rank is the **number of dimensions in the output** after the transformation. If a 3×3 matrix has rank 2, it means the transformation collapses 3D space onto a 2D plane. Rank tells you how much "information" the transformation preserves. A full-rank matrix preserves all dimensions and has an inverse.

---

### Q: Explain eigenvalues and eigenvectors.

> Most vectors change direction when you apply a transformation. An **eigenvector** is special — it stays on the same line it was on before; the transformation only scales it. The **eigenvalue** is that scaling factor.
>
> For example, if I apply a transformation and a vector just gets doubled in length without rotating, that vector is an eigenvector with eigenvalue 2. They reveal the "natural axes" of a transformation — the directions along which the transformation acts most simply.

---

### Q: What is a system of linear equations and how does it connect to matrices?

> A system of linear equations asks: "What input gives me this specific output?" When you write it as $A\vec{x} = \vec{b}$, you're asking: "What vector $\vec{x}$, when transformed by matrix $A$, lands on $\vec{b}$?"
>
> If the matrix is invertible ($\det \neq 0$), there's exactly one answer: $\vec{x} = A^{-1}\vec{b}$. If the determinant is zero, the transformation squishes space and you either have no solution or infinitely many.

---

### Q: What is a vector space?

> A vector space is a collection of vectors where you can **add** any two vectors and **scale** any vector by a number, and the result always stays within the same collection. It must include the zero vector, and these operations must follow rules like commutativity and distributivity.
>
> Examples: all 2D vectors form a vector space; all 3D vectors form a vector space; even the set of all polynomials of degree ≤ n forms a vector space. The key subspaces we encounter are the **column space** (all possible outputs of a matrix) and the **null space** (all inputs that map to zero).

---

### Q: How do rank, null space, and invertibility connect?

> They're all faces of the same coin:
> - **Full rank** → null space is just $\{\vec{0}\}$ → matrix is invertible → unique solution to every $A\vec{x} = \vec{b}$
> - **Not full rank** → null space is a line/plane → no inverse exists → the transformation loses information by collapsing a dimension
>
> The rank tells you what dimension the output lives in. The null space tells you what got "destroyed" (mapped to zero). Together they always add up to the number of columns (Rank-Nullity Theorem).

---

### Q: Why do eigenvalues matter beyond theory?

> Eigenvalues tell you the **fundamental behavior** of a transformation:
> - If all $|\lambda| < 1$: the system shrinks over time (stable)
> - If any $|\lambda| > 1$: the system grows over time (unstable)
> - If $\lambda = 0$: that direction gets completely collapsed
>
> They're essential in solving differential equations, analyzing stability of systems, computing matrix powers efficiently (via diagonalization), and understanding what directions a transformation "prefers."

---

### Q: What happens when a matrix has no real eigenvalues?

> This means the transformation has **no fixed direction** in real space. A classic example is a 90° rotation — every vector gets moved off its line, so no real eigenvector exists. The eigenvalues become complex numbers ($i, -i$), which algebraically encode the rotational behavior. Complex eigenvalues always signal rotation-like action in the transformation.