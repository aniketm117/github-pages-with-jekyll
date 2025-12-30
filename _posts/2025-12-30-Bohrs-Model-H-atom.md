---
title: "Bohr's Model of H & H-like species"
description: "A physics lecture note on Bohr’s atomic model with key derivations and results."
date: 2025-12-30
---

<a href="https://aniketm117.github.io/github-pages-with-jekyll/2020/06/24/intro-to-kinematics.html">Back</a> 

# Bohr’s Model of the Hydrogen Atom

---

## 1. Introduction

Classical physics failed to explain the stability of atoms and the discrete nature of atomic spectra.  
Rutherford’s nuclear model predicted that orbiting electrons should continuously radiate energy and spiral into the nucleus. To resolve these contradictions, **Niels Bohr (1913)** proposed a quantum model for the hydrogen atom.

---

## 2. Experimental Motivation

- Atoms emit **line spectra**, not continuous spectra  
- Hydrogen spectrum consists of well-defined series:
  - Lyman (ultraviolet)
  - Balmer (visible)
  - Paschen and Brackett (infrared)
- Classical electrodynamics cannot explain these observations

---

## 3. Bohr’s Postulates

### (i) Stationary Orbits
Electrons revolve around the nucleus only in certain allowed circular orbits without radiating energy.

### (ii) Quantization of Angular Momentum
The angular momentum of the electron is quantized:

$$
mvr = n\hbar, \quad n = 1,2,3,\dots
$$

### (iii) Emission and Absorption of Radiation
Radiation is emitted or absorbed only during transitions between allowed orbits:

$$
h\nu = E_i - E_f
$$

---

## 4. Force Balance in the Atom

For an electron in a circular orbit, the electrostatic force provides the centripetal force:

$$
\frac{1}{4\pi\varepsilon_0}\frac{e^2}{r^2} = \frac{mv^2}{r}
$$

---

## 5. Radius of Allowed Orbits

Using force balance and angular momentum quantization, the radius of the $n^{\text{th}}$ orbit is:

$$
\boxed{
r_n = \frac{4\pi\varepsilon_0 \hbar^2}{m e^2} \, n^2
}
$$

The smallest allowed radius (Bohr radius):

$$
\boxed{
a_0 = 0.529 \, \text{Å}
}
$$

Hence,

$$
\boxed{
r_n = n^2 a_0
}
$$

---

## 6. Velocity of the Electron

The velocity of the electron in the $n^{\text{th}}$ orbit is:

$$
\boxed{
v_n = \frac{e^2}{2\varepsilon_0 h} \frac{1}{n}
}
$$

For the ground state ($n=1$):

$$
v_1 \approx 2.18 \times 10^6 \, \text{m s}^{-1}
$$

---

## 7. Energy of the Electron

### Kinetic Energy
$$
K = \frac{1}{2}mv^2
$$

### Potential Energy
$$
U = -\frac{1}{4\pi\varepsilon_0}\frac{e^2}{r}
$$

### Total Energy
$$
E = K + U = -\frac{1}{8\pi\varepsilon_0}\frac{e^2}{r}
$$

Substituting $r_n$:

$$
\boxed{
E_n = -\frac{m e^4}{8 \varepsilon_0^2 h^2} \frac{1}{n^2}
}
$$

Numerically,

$$
\boxed{
E_n = -\frac{13.6}{n^2} \, \text{eV}
}
$$

---

## 8. Hydrogen Spectrum

For a transition from $n_i$ to $n_f$:

$$
h\nu = E_{n_i} - E_{n_f}
$$

Thus,

$$
\boxed{
\nu = \frac{13.6\,\text{eV}}{h}
\left(\frac{1}{n_f^2} - \frac{1}{n_i^2}\right)
}
$$

### Rydberg Formula

$$
\boxed{
\frac{1}{\lambda} = R
\left(\frac{1}{n_f^2} - \frac{1}{n_i^2}\right)
}
$$

where

$$
R = 1.097 \times 10^7 \, \text{m}^{-1}
$$

---

## 9. Ionization Energy of Hydrogen

Ionization corresponds to $n=1 \rightarrow n=\infty$:

$$
\boxed{
E_{\text{ion}} = 13.6 \, \text{eV}
}
$$

---

## 10. Successes of Bohr’s Model

- Explains atomic stability
- Accurately predicts hydrogen spectrum
- Correct atomic size and energy scales
- Introduced quantization into atomic theory

---

## 11. Limitations of Bohr’s Model

- Applicable only to hydrogen-like atoms
- Cannot explain fine structure or Zeeman effect
- Assumes circular orbits
- Ignores wave nature of electrons

---

## 12. Bohr Model and Quantum Mechanics

- Superseded by Schrödinger’s wave mechanics
- Orbits replaced by probability-based orbitals
- Remains foundational in atomic physics education

---
