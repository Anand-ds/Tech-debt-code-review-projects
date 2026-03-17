# Tech Debt Scoring Model

This scoring model provides a consistent way to evaluate and prioritize technical debt.

Each item is scored across **four dimensions**, each from 1–5:

| Category | Description |
|---------|-------------|
| **Impact** | How much the debt affects performance, maintainability, or delivery |
| **Risk** | Likelihood of causing failures, outages, or regressions |
| **Cost to Fix** | Estimated effort required to remediate |
| **Frequency** | How often the debt affects developers or users |

---

## Formula



\[
\text{Priority Score} = \frac{(Impact \times 2) + (Risk \times 2) + Frequency - Cost}{2}
\]



### Why this formula?
- **Impact** and **Risk** are weighted more heavily.
- **Frequency** increases urgency.
- **Cost** reduces priority (high cost = lower score).

---

## Score Interpretation

| Score Range | Meaning |
|-------------|---------|
| **8–10** | Critical — must be addressed immediately |
| **6–7.9** | High — schedule in next sprint |
| **4–5.9** | Medium — backlog and monitor |
| **1–3.9** | Low — fix opportunistically |

---

## Example

Given:
- Impact = 4  
- Risk = 5  
- Frequency = 3  
- Cost = 2  



\[
\text{Priority Score} = \frac{(4 \times 2) + (5 \times 2) + 3 - 2}{2} = 8.5
\]



This item is **critical**.
