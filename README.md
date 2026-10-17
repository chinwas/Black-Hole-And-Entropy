# Black Holes and Entropy

A Beamer presentation (43 slides, including appendix) on Jacob D. Bekenstein's classic paper *"Black Holes and Entropy"* (Phys. Rev. D, 1973). It walks through the argument for why a black hole's horizon area should be treated as a genuine thermodynamic entropy, and tests the resulting Generalized Second Law with thought experiments.

**Presented by:** Advik Adatiya, Ashish Paul and Chinmay Wasnik

📄 **[Read the slides (PDF)](Ensemble__Black_Holes_and_Entropy.pdf)**

---

## What the presentation covers

### 1. Introduction and thermodynamic analogies
- Background results: Christodoulou's irreducible mass, Floyd & Penrose, and Hawking's area theorem ($\Delta A \ge 0$).
- The rationalized horizon area $\alpha = A/4\pi$ for a Kerr–Newman black hole.
- The differential mass formula, the black-hole analogue of the first law of thermodynamics:

$$dM = \Theta\, d\alpha + \vec{\Omega}\cdot d\vec{L} + \Phi\, dQ$$

- A side-by-side table comparing ordinary thermodynamics with black-hole mechanics.

### 2. Information theory and black-hole entropy
- Entropy as missing information (Shannon entropy, $\Delta I = -\Delta S$).
- Why $S_{\text{bh}}$ must be a monotonically increasing function of $\alpha$.
- Using a black-hole merger argument to show $S_{\text{bh}} \propto \alpha$ (sub-linear powers are ruled out).

### 3. Fixing the constant
- A particle falling into the hole gives a minimum area increase $(\Delta\alpha)_{\min} = 2\mu b$.
- Quantum limits (Compton wavelength vs. gravitational radius) push this to $2\hbar$, which is identified with one bit of lost information.
- The result:

$$S_{\text{bh}} = \tfrac12 \ln 2\;\hbar^{-1}\,\alpha = \frac{\ln 2}{8\pi}\,\frac{k c^3}{\hbar G}\,A$$

- Consequences: the enormous entropy of a solar-mass black hole (~$10^{60}$ erg/K) and the characteristic temperature $T_{\text{bh}}$.

### 4. The Generalized Second Law (GSL)
- The puzzle of entropy disappearing behind a horizon, and the statement $\Delta S_{\text{bh}} + \Delta S_c \ge 0$.
- **Example 1:** a harmonic oscillator in a box lowered into the hole.
- **Example 2:** Geroch's heat-engine process. The apparent paradox of efficiency $\to 1$ is resolved by a quantum limit on box size, which gives the Carnot bound $\epsilon < 1 - T_{\text{bh}}/T$.

### 5. Appendix
- Assumptions behind $(\Delta\alpha)_{\min} = 2\mu b$.
- The differential proof that $S_{\text{bh}}$ must be strictly linear in $\alpha$, and why $p<1$ and $p>1$ powers break thermodynamics.
- Microstate counting ($S = k\ln W$), area quantization into bits, and how this reproduces Bekenstein's formula.

---

## Repository contents

| File | Description |
|---|---|
| `main.tex` | LaTeX (Beamer) source for the presentation |
| `Ensemble__Black_Holes_and_Entropy.pdf` | Compiled slides |
| `image.png` | Figure used on the "Rationalized Horizon Area" slide |
| `overlay-image (2).jpg` | Figure used on the Geroch process slides |
| `500px-Sphere.png` | Sphere image asset |

---

## Building from source

You need a LaTeX distribution (TeX Live, MiKTeX or MacTeX) with the `beamer`, `amsmath`, `amssymb`, `bbding` and `tikz` packages, all of which are included in a standard full install.

```bash
pdflatex main.tex
pdflatex main.tex   # run twice to resolve slide numbers and references
```

The output is `main.pdf`. The theme is Beamer's `Madrid` at a 16:9 aspect ratio.

---

## Reference

J. D. Bekenstein, "Black Holes and Entropy," *Physical Review D* **7**, 2333 (1973).

## Acknowledgements

All physical results presented here are due to Bekenstein and the earlier work of Christodoulou, Floyd & Penrose, Hawking and Geroch. This repository is a student presentation of that material.
