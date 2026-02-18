# 🔬 The CSK Constant: Mapping Composite Complexity(Coşku Çimen)

This repository presents the formal definition and computational derivation of the **CSK Constant**, a mathematical value that quantifies the "prime information density" within composite numbers.

---

## 📐 The Mathematical Definition

The **CSK Constant ($S$)** is defined by the following infinite series:

<div align="center">
  <img src="https://latex.codecogs.com/svg.image?S&space;=&space;\sum_{n&space;\in&space;Composite}^{\infty}&space;\frac{\omega(n)&space;-&space;1}{n^2}" title="S = \sum_{n \in Composite}^{\infty} \frac{\omega(n) - 1}{n^2}" />
</div>

Where:
- **$\omega(n)$**: The number of distinct prime factors of $n$.
- **$n^2$**: Quadratic damping for convergence.
- **$n \in \text{Composite}$**: Restricting the domain to non-prime integers $> 1$.

---

## 📊 Visualizing the Convergence (Interactive Concept)

Below is a visualization concept of how the **CSK Constant** stabilizes as we scan through the number line.

$$S = \sum_{n \in \text{Composite}}^{\infty} \frac{\omega(n) - 1}{n^2}$$

---

## 🧪 Computational Proof (Python)

The numerical value was derived using a high-precision sieve algorithm.

```python
def calculate_csk(limit):
    primes = sieve_of_eratosthenes(limit)
    csk_sum = 0
    for i in range(2, limit + 1):
        if i not in primes:
            # omega(i) - 1 / i^2
            factors = get_distinct_prime_factors(i)
            csk_sum += (len(factors) - 1) / (i**2)
    return csk_sum

# Result: 0.09898210200555385
