---
title: Projectile Motion
date: 2025-07-24
---

<a href = "https://aniketm117.github.io/github-pages-with-jekyll/">Back</a>

## Projectile Motion

In a projectile motion of an object imparted a velocity (v), the key assumptions are:

- no air resistance to the motion of the object
- earth is flat
- acceleration due to gravity is uniform everywhere

Motion of the object along x and y direction are independent of each other. The important quantities in a projectile motion are R = Horizontal Range, H = Maximum Height above ground, and T = Time of flight.

For a particle projected with velocity 'v' and at an angle 'θ' with the horizontal.

<p><img src="https://latex.codecogs.com/svg.image?&space;R=v^2*sin(2\Theta)/g"></p>

<p><img src="https://latex.codecogs.com/svg.image?&space;H=v^2*sin^2(\Theta)/2g"></p>

<p><img src="https://latex.codecogs.com/svg.image?&space;T=2*v*sin(\Theta)/g"></p>

Here's the full derivation using the intersection method — a beautifully elegant approach where we treat the projectile as a parabola and the incline as a line, then find where they meet.

---

## Setup

Set up coordinates at the launch point. The projectile is launched with speed $v_0$ at angle $\alpha$ above the inclined plane, which itself makes angle $\beta$ with the horizontal. So the absolute launch angle with the horizontal is $(\alpha + \beta)$.

**Equations of motion** (standard x–y axes, horizontal and vertical):

$$x = v_0 \cos(\alpha+\beta)\, t$$
$$y = v_0 \sin(\alpha+\beta)\, t - \tfrac{1}{2}g t^2$$

Eliminating $t$ from these gives the **parabola**:

$$y = x\tan(\alpha+\beta) - \frac{g x^2}{2v_0^2\cos^2(\alpha+\beta)}$$

---

## The incline as a line

The inclined plane passing through the origin at angle $\beta$:

$$y = x\tan\beta$$

---

## Finding the intersection

Set the parabola equal to the line:

$$x\tan\beta = x\tan(\alpha+\beta) - \frac{gx^2}{2v_0^2\cos^2(\alpha+\beta)}$$

One solution is $x = 0$ (the launch point). For the *other* intersection (landing point), divide through by $x$:

$$\tan\beta = \tan(\alpha+\beta) - \frac{gx}{2v_0^2\cos^2(\alpha+\beta)}$$

Solving for $x$:

$$x = \frac{2v_0^2\cos^2(\alpha+\beta)}{g}\bigl[\tan(\alpha+\beta) - \tan\beta\bigr]$$

Using the identity $\tan A - \tan B = \dfrac{\sin(A-B)}{\cos A \cos B}$ with $A=\alpha+\beta$, $B=\beta$:

$$x = \frac{2v_0^2\cos^2(\alpha+\beta)}{g} \cdot \frac{\sin\alpha}{\cos(\alpha+\beta)\cos\beta} = \frac{2v_0^2\cos(\alpha+\beta)\sin\alpha}{g\cos\beta}$$

---

## Converting to range along the slope

The range $R$ along the incline relates to the horizontal landing distance by $x = R\cos\beta$, so $R = x/\cos\beta$:

$$\boxed{R = \frac{2v_0^2 \sin\alpha\,\cos(\alpha+\beta)}{g\cos^2\beta}}$$

Using the product-to-sum identity $2\sin A\cos B = \sin(A+B)+\sin(A-B)$:

$$R = \frac{v_0^2}{g\cos^2\beta}\bigl[\sin(2\alpha+\beta) - \sin\beta\bigr]$$

## Maximum range

$R$ is maximised when $\sin(2\alpha+\beta)=1$, i.e. $2\alpha+\beta = 90°$, giving the optimal launch angle:

$$\alpha_\text{opt} = \frac{90°-\beta}{2} = 45° - \frac{\beta}{2}$$

And the **maximum range** on the incline:

$$R_\text{max} = \frac{v_0^2}{g\cos^2\beta}(1-\sin\beta) = \frac{v_0^2}{g(1+\sin\beta)}$$

Let me illustrate the geometry of this intersection:---

## Summary of the method

The key insight is elegant: instead of computing the time of flight and range separately, we treat the problem purely geometrically — the projectile traces a **parabola**, the incline is a **straight line** through the origin, and the range is simply the distance from the origin to their non-trivial **intersection**.

This gives us $R = \dfrac{2v_0^2 \sin\alpha\cos(\alpha+\beta)}{g\cos^2\beta}$, which reduces correctly to the flat-ground formula $R = \dfrac{v_0^2\sin 2\alpha}{g}$ when $\beta = 0$.

---
