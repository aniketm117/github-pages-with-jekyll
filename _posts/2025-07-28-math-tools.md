---
title: "Mathematical Tools"
date: 2025-07-28
---

<td style="text-align: left"><a href = "https://aniketm117.github.io/github-pages-with-jekyll/">Back</a></td>

# Mathematical Tools for Class 11

- Maths is the language of physics. Following text is a curated resource for mastering key mathematical concepts for the JEE exam.

---

## 1. Trigonometry

Trigonometry deals with angles, triangles, and their ratios. It's a fundamental part of JEE.

### Trigonometric Ratios

$$\sin \theta = \frac{b}{h}$$
$$\cos \theta = \frac{b}{h}$$
$$\tan \theta = \frac{b}{h}$$

### 📌 Common Formula in Trigonometry:

$$\sin(90 + \theta) = -\cos \theta$$
$$\cos(90 - \theta) = \sin \theta$$

$$\sin 30^\circ = \frac{1}{2}$$
$$\sin 45^\circ = \frac{1}{\sqrt{2}}$$
$$\sin 60^\circ = \frac{\sqrt{3}}{2}$$
$$\sin 90^\circ = 1$$

<table>
 <thead>
   <tr>
     <th style="text-align: left">Col 1</th>
     <th style="text-align: left">Col 2</th>
     <th style="text-align: left">Col 3</th>
   </tr>
 </thead>
 <tbody>
   <tr>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin²θ + cos²θ = 1</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">1 + cot²θ = cosec²θ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">1 + tan²θ = sec²θ</code></td>
   </tr>
   <tr>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin (90 + θ) = cos θ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin (180 - θ) = sin θ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin (90 - θ) = cos θ</code></td>
   </tr>
   <tr>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">cos (90 + θ) = - sin θ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">cos (180 - θ) = - cos θ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">cos (90 - θ) = sin θ</code></td>
   </tr>
 </tbody>
</table>


### ✅ Example:

**Q:** If `sinθ = 3/5` and θ is in the first quadrant, find `cosθ` and `tanθ`.

**Solution:**

- `sinθ = 3/5` ⇒ Opposite = 3, Hypotenuse = 5  
- Adjacent = √(5² - 3²) = √16 = 4  
- `cosθ = 4/5`, `tanθ = 3/4`

<table>
 <thead>
   <tr>
     <th style="text-align: left">Col 1</th>
     <th style="text-align: left">Col 2</th>
     <th style="text-align: left">Col 3</th>
   </tr>
 </thead>
 <tbody>
   <tr>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin(360+θ) = sinθ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">cos(360+θ) = cosθ</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">cos(360-θ) = cosθ</code></td>
   </tr>
   <tr>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin(A+B) = sinA·cosB + sinB·cosA</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">cos(A+B) = cosA·cosB - sinA·sinB</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">sin(2A) = 2sinA·cosA</code></td>
   </tr>
   <tr>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">1+cos(2A) = 2cos²(A)</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">1-cos(2A) = 2sin²(A)</code></td>
     <td style="text-align: left"><code class="language-plaintext highlighter-rouge">tan (90 + θ) = - cot θ</code></td>
   </tr>
 </tbody>
</table>

---

## 2. Straight Lines

Straight lines are part of coordinate geometry and deal with equations of lines in a plane.

### 📌 Forms of Line:

- Slope-intercept form: `y = mx + c`
- Point-slope form: `y - y₁ = m(x - x₁)`
- General form: `Ax + By + C = 0`

### ✅ Example:

**Q:** Find the equation of the line passing through (2, 3) with slope 4.

**Solution:**

Use point-slope form:

`y - 3 = 4(x - 2)`  
⇒ `y = 4x - 5`

---

## 3. Differentiation

Differentiation is the rate of change of a function. It’s essential for calculus-based problems in JEE. Say (displacement) and $x_1, x_2$ time

$V_{av} = \langle v \rangle = \frac{y_2 - y_1}{t_2 - t_1} = 0$.

as the time interval $(t_2 - t_1)$ becomes very small the average velocity becomes instantaneous velocity.

so $V_{av}$ changes to $v$; $\Delta v / \Delta t$ becomes closer to $x_1, x_2$ line.

which was intersecting the curve at two points would eventually touch at just at a single point

### 📌 Basic Derivatives:

- `d/dx(xⁿ) = nxⁿ⁻¹`
- `d/dx(sin x) = cos x`
- `d/dx(eˣ) = eˣ`
- `d/dx(ln x) = 1/x`

### ✅ Example:

**Q:** Differentiate `f(x) = x³ + 2x² - 5x + 1`

**Solution:**

`f'(x) = 3x² + 4x - 5`

---

## 4. Integration

Integration is the reverse of differentiation. It’s used to calculate area, displacement, and more.

### 📌 Basic Integrals:

- `∫xⁿ dx = xⁿ⁺¹ / (n+1) + C`, `n ≠ -1`
- `∫1/x dx = ln|x| + C`
- `∫eˣ dx = eˣ + C`
- `∫cos x dx = sin x + C`

### ✅ Example:

**Q:** Find `∫(3x² + 2x - 1) dx`

**Solution:**

`∫(3x² + 2x - 1) dx = x³ + x² - x + C`

---

## 5. Vectors

Equal Vectors
$\vec{A} = \vec{B}$
If two vectors are equal then their magnitudes and directions are identical,

Multiply vector by a scalar

$\vec{B} = 2\vec{A}$

$\vec{A}$ + $\vec{A}$ = $\vec{B}$

### Triangle rule of vector addition

When two vectors are arranged such that the need of one vector coincides with the tail of the other, then the vector obtained in completing the triangle, in the direction from tail to head is the sum of the two vectors.

## 📎 Note:

Practice these concepts regularly with mock papers and past year questions. Tricky problems often require blending concepts across these topics.

---

