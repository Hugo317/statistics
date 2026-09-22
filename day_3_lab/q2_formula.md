# Q2 — Solving P(A|B)

## Given
- P(A) = 0.01 — base rate of fake posts
- P(B|A) = 0.80 — recall (P(flagged | truly fake))
- P(¬B|¬A) = 0.80 — specificity (P(not flagged | truly real))

## Step 1 — Derive the missing conditional
$$ P(B|\neg A) = 1 - P(\neg B|\neg A) $$

## Step 2 — Law of total probability (get P(B))
$$ P(B) = P(B|A) \cdot P(A) \;+\; P(B|\neg A) \cdot P(\neg A) $$

## Step 3 — Bayes' theorem (solve for P(A|B))
$$ P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)} $$

# Q3 — Joint probabilities (confusion matrix cells)

| Cell | Formula |
|---|---|
| TP = P(A ∩ B)   | pa \* p_b_a |
| FP = P(¬A ∩ B)  | (1 - pa) \* p_b_na |
| FN = P(A ∩ ¬B)  | pa \* (1 - p_b_a) |
| TN = P(¬A ∩ ¬B) | (1 - pa) \* (1 - p_b_na) |

Where:
- `pa` = P(A)
- `p_b_a` = P(B\|A) — recall
- `p_b_na` = P(B\|¬A) — 1 - specificity

Multiply each joint probability by 100,000 to get expected counts.
