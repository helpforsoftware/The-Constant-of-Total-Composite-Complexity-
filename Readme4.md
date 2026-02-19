# 🌿 Çimen Constant and Ç(s) Function

This repository contains the study of the **Çimen (CSK) Constant** and the function Ç(s), which evaluates the "prime factor excess" of composite integers.

---

## 1️⃣ Definition

The **Çimen Constant (Ç(s))** is defined as a Dirichlet series:

$$
Ç(s) = \sum_{n \in \mathbb{C}} \frac{\omega(n)-1}{n^s} = (\zeta(s)-1) P(s)
$$

Where:

- $n \in \mathbb{C}$ → the set of composite numbers  
- $\omega(n)$ → number of distinct prime factors of $n$  
- $P(s)$ → Prime zeta function: $P(s) = \sum_p \frac{1}{p^s}$

---

## 2️⃣ Key Properties

- **Convergence:** Ç(s) converges for Re(s) > 1; it has a logarithmic pole at $s = 1$  
- **Riemann zeta zeros:** They indirectly influence Ç(s), producing oscillations  
- **Analytic continuation:** Possible via Perron/Mellin transform  
- Ç(s) measures **prime factor density**, not the primes themselves  

---

## 3️⃣ Derivative and ζ'/ζ Relation

$$
Ç'(s) = \zeta'(s) P(s) + (\zeta(s)-1) \sum_{k=1}^{\infty} \mu(k) \frac{\zeta'(ks)}{\zeta(ks)}
$$

- Using Mellin/Perron transform, an **explicit formula** can be derived  
- Riemann zeros appear explicitly as oscillatory terms  
- Cumulative sum approximation:

$$
\sum_{n \le x, n\in \mathbb C} (\omega(n)-1) \log n
\approx x \log\log x - \sum_\rho \frac{x^\rho}{\rho} + \text{smaller terms}
$$

---

## 4️⃣ Numerical Examples

- Calculated for $n = 1..210$  
- Comparison between **explicit formula approximation** and **actual composite numbers**  
- Oscillations from zeta zeros are small but visible  
- Explicit formula captures both **trend and fluctuations** accurately

**Visualizations:**

1. Explicit formula approximation (Approx Ç(n))  
2. Actual cumulative Ç(n) from composite numbers  
3. Oscillation term contribution from zeta zeros  

- Small $n$ → more irregular due to composite distribution  
- Large $n$ → trends align very closely  

---

## 5️⃣ Key Observations

1. Ç(s) measures the **prime factor excess of composites**, not primes themselves  
2. Explicit formula and zeta zeros reveal oscillations in prime factor density  
3. Main growth term: $x \log \log x$; oscillations: zeta zeros contribution  
4. Small $n$ → irregularities; large $n$ → trend dominates  
5. Graphs provide both **numerical and analytical insight**

---

## 6️⃣ Next Steps

- Extend comparison to **larger $n$** (1–500 or 1–1000)  
- Histogram/density analysis of oscillations → explore **heavy-tail and rare maxima**  
- Extend $\omega(n)$ to **prime correlation functions** in Ç(s)  

---

🌿 **Summary:**  
The Ç(s) function and its derivative Ç′(s) provide a framework to **link composite prime factor excess with Riemann zeta zeros**, offering both analytical and numerical insight. The explicit formula matches real data closely, revealing the oscillatory behavior induced by zeta zeros.
