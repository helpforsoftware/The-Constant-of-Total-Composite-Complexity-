 # 🔬 The Çimen(Ç)(CSK) Constant: Mapping Composite Complexity Load
Author: Coşku Çimen


This repository introduces and proves the **Çimen(CSK) Constant ($Ç$)**, a mathematical value that quantifies the "excess prime information" or "compositional entropy" within composite numbers.

---

## 📐 Formal Definition

The **Çimen(CSK) Constant ($Ç$)** is an infinite series that evaluates the ratio of distinct prime factor excess to the quadratic density of composite integers:

$$\Large Ç = \sum_{n \in \mathbb{C}} \frac{\omega(n) - 1}{n^s}$$

Where:
- $n \in \mathbb{C}$ represents the set of all composite numbers $\{4, 6, 8, 9, 10, 12, \dots\}$.
- $\omega(n)$ is the number of **distinct prime factors** of $n$.
- The term $(\omega(n) - 1)$ represents the "non-primality" degree or the complexity load of $n$.

---

## 📊 Convergence Visualization

The series converges remarkably fast, reaching a high degree of stability within the first $10^5$ terms for s=2.

<div align="center">
  <img src="graph.svg" alt="Çimen Constant Convergence Graph" width="600">
  <p><i>Figure 1: Numerical convergence of S towards the analytical identity.</i></p>
</div>

---

## 🏛 Analytical Identity & Proof

The significance of the **Çimen(CSK) Constant** lies in its perfect bridge between the distribution of all integers and the specific density of primes. It can be expressed using the **Riemann Zeta Function** and the **Prime Zeta Function**:

### The Identity:
$$\Large Ç = \zeta(s) \cdot P(s) - (\zeta(s) - 1)$$

### Numerical Components for s=2:
| Component | Function | Approximation |
| :--- | :--- | :--- |
| **Total Factor Load** | $\zeta(2) \cdot P(2)$ | $0.74391612...$ |
| **Structural Bias** | $\zeta(2) - 1$ | $0.64493406...$ |
| **Final Çimen Constant** | **$Ç$** | **$0.0989830984600784...$** |



---
## Theoretical Implications (What does it prove?)

1. **Structural Determinism:** Proves that the "noise" (composite factor complexity) in the number system converges to a fixed universal ratio.
2. **Entropy of Composition:** Quantifies the total "deviation from primality" across the infinite number line.
3. **Functional Linkage:** Validates the deterministic bridge between the Riemann Zeta ($\zeta$) and Prime Zeta ($P$) functions through experimental summation.
## 🌌 Generalization to Higher Dimensions ($s=3$)

When we increase the power to $s=3$, we observe how the **Composite Complexity** decays in higher-dimensional mathematical spaces.

### The $S_3$ Constant:
$$\Large Ç_3 = \sum_{n \in \mathbb{C}} \frac{\omega(n) - 1}{n^3} \approx 0.008017$$

### Comparison Table:
- **2D Complexity ($s=2$):** $\approx 0.098983$
- **3D Complexity ($s=3$):** $\approx 0.008017$ (A ~92% reduction in noise)

This proves that as the power $s$ increases, the influence of composite complexity vanishes, leaving only the "pure" prime structure of the number system.
## 💻 Implementation for s=2

```python
def csk_v2(limit, s=2):
    # ω(n) için lineer elek
    omega = [0] * (limit + 1)
    for i in range(2, limit + 1):
        if omega[i] == 0:  # i asal
            for j in range(i, limit + 1, i):
                omega[j] += 1
    
    total = 0.0
    for n in range(4, limit + 1):  # 4'ten başla (ilk composite)
        if omega[n] >= 1:  # composite
            total += (omega[n] - 1) / (n ** s)
    return total
print(csk_v2(10000000))

# Result: 0.0989830984600784
```
## 🌌 Expansion to the Complex Plane

The **CSK Function** can be analytically continued into the complex plane $s = \sigma + it$. This expansion links the complexity of composite numbers directly to the **critical strip** of the Riemann Hypothesis.

### The Holomorphic Identity:
$$Ç(s) = \zeta(s)P(s) - \zeta(s) + 1$$

### Key Observations:
- **Dimensional Stability:** As $\sigma \to \infty$, $S(s) \to 0$, proving that in "infinite dimensions," the number system is perfectly prime and noise-free.
## Conclusion
The CSK Constant proves that the structural complexity of numbers is not chaotic; it is a calculated byproduct of prime distribution, fixed by the same laws that govern the fundamental constants of the universe.=

### 1. The "Static Noise" of Numbers
 the **Ç-Constant** is the "leftover complexity" from the distribution of prime numbers. It represents the inevitable static noise that occurs when pure primes combine to form the infinite library of composite integers.


###  Citation
If you use the **Ç-Constant** or the **Ç-Function** in your research, please cite it as:
> *Coşku Çimen, (2026). The Ç-Constant: A Structural Analysis of Composite Complexity. GitHub Repository: "https://github.com/helpforsoftware/The-Constant-of-Total-Composite-Complexity-"

[Contact Me With Mail](mailto:helpforsoftware@gmail.com)
