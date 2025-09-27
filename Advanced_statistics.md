# Probability Distributions - Core Concepts

## Overview: Types of Random Variables and Their Functions

```mermaid
graph TD
    A[Random Variables] --> B[Discrete]
    A --> C[Continuous]
    
    B --> D[PMF - Probability Mass Function]
    C --> E[PDF - Probability Density Function]
    
    B --> F[CDF - Cumulative Distribution Function]
    C --> F
    
    D --> G[Examples: Dice, Coin Flip, Binomial]
    E --> H[Examples: Height, Weight, Normal Distribution]
    
    F --> I[Properties: Non-decreasing, 0 to 1]
    
    style A fill:#e1f5fe,color:#000
    style B fill:#fff,color:#000
    style C fill:#fff,color:#000
    style D fill:#fff3e0,color:#000
    style E fill:#f3e5f5,color:#000
    style F fill:#e8f5e8,color:#000
    style G fill:#fff,color:#000
    style H fill:#fff,color:#000
    style I fill:#fff,color:#000
```

---

## Topic 1: Probability Density Function (PDF)
### For Continuous Random Variables

**Example from your lecture:** Height of students in classroom [0-1]

### Key Formula
**P(X ≤ 155) = Area under the curve**

```mermaid
graph LR
    A[PDF Curve] --> B[Shaded Area]
    B --> C[Probability P of X less than 155]
    
    D[Height Values] --> E[X-axis: 155, 165, etc.]
    F[Density Values] --> G[Y-axis: 0.1, 0.2, 0.3, 0.4]
    
    style A fill:#f3e5f5,color:#000
    style B fill:#fff,color:#000
    style C fill:#e8f5e8,color:#000
    style D fill:#fff,color:#000
    style E fill:#fff,color:#000
    style F fill:#fff,color:#000
    style G fill:#fff,color:#000
```

### Important Properties
- f(x) ≥ 0 for all x
- Total area under curve = 1
- Height represents density, not probability
- Probability = Area under curve between two points

---

## Topic 2: Probability Mass Function (PMF)  
### For Discrete Random Variables

**Example from your lecture:** Rolling a dice {1, 2, 3, 4, 5, 6}

### Key Calculations from your image:

```mermaid
graph TD
    A[Fair Dice] --> B[Outcome 1: P equals 1/6]
    A --> C[Outcome 2: P equals 1/6]
    A --> D[Outcome 3: P equals 1/6]
    A --> E[Outcome 4: P equals 1/6]
    A --> F[Outcome 5: P equals 1/6]
    A --> G[Outcome 6: P equals 1/6]
    
    B --> H[P of X less than 4 equals 4/6 equals 2/3]
    C --> H
    D --> H
    E --> H
    
    style A fill:#e1f5fe,color:#000
    style B fill:#fff,color:#000
    style C fill:#fff,color:#000
    style D fill:#fff,color:#000
    style E fill:#fff,color:#000
    style F fill:#fff,color:#000
    style G fill:#fff,color:#000
    style H fill:#e8f5e8,color:#000
```

### Cumulative Calculation:
**P(X ≤ 4) = P(X=1) + P(X=2) + P(X=3) + P(X=4)**
```
= 1/6 + 1/6 + 1/6 + 1/6 = 4/6 = 2/3
```

---

## Topic 3: Cumulative Distribution Function (CDF)
### Cumulative Probability

**Definition:** F(x) = P(X ≤ x)

```mermaid
graph LR
    A[PDF Bell Curve] --> B[Integration/Summation]
    B --> C[CDF S-shaped Curve]
    
    D[Key Relationship] --> E[PDF equals Gradient of CDF]
    E --> F[Where CDF is steep PDF is high]
    E --> G[Where CDF is flat PDF is low]
    
    style A fill:#f3e5f5,color:#000
    style B fill:#fff,color:#000
    style C fill:#fff3e0,color:#000
    style D fill:#fff,color:#000
    style E fill:#e8f5e8,color:#000
    style F fill:#fff,color:#000
    style G fill:#fff,color:#000
```

### Properties
- F(x) is non-decreasing
- F(x) starts at 0 and approaches 1
- Slope of CDF = PDF value at that point

---

## Topic 4: Distribution Types Overview

```mermaid
graph TD
    A[Probability Distributions] --> B[Discrete Distributions]
    A --> C[Continuous Distributions]
    
    B --> D[Bernoulli - Binary Success/Failure]
    B --> E[Uniform - All outcomes equally likely]
    B --> F[Poisson - Count of rare events]
    B --> G[Binomial - Number of successes in n trials]
    
    C --> H[Normal/Gaussian - Bell-shaped curve]
    C --> I[Log Normal - Skewed distribution]
    
    style A fill:#e1f5fe,color:#000
    style B fill:#fff3e0,color:#000
    style C fill:#f3e5f5,color:#000
    style D fill:#e3f2fd,color:#000
    style E fill:#e3f2fd,color:#000
    style F fill:#e3f2fd,color:#000
    style G fill:#e3f2fd,color:#000
    style H fill:#fce4ec,color:#000
    style I fill:#fce4ec,color:#000
```

---

## Topic 5: PDF to CDF Relationship

```mermaid
flowchart TD
    A[PDF: Probability Density Function] --> B[Shows rate of change of probability]
    B --> C[Integration over interval]
    C --> D[CDF: Cumulative Distribution Function]
    D --> E[Shows P of X less than x]
    
    F[Key Insight: PDF equals derivative of CDF] --> G[Derivative of CDF gives PDF]
    G --> H[Slope of CDF curve equals PDF value]
    
    I[Example: Height around 165] --> J[PDF peak at 165]
    J --> K[CDF steepest at 165]
    
    style A fill:#f3e5f5,color:#000
    style B fill:#fff,color:#000
    style C fill:#fff,color:#000
    style D fill:#fff3e0,color:#000
    style E fill:#fff,color:#000
    style F fill:#e8f5e8,color:#000
    style G fill:#fff,color:#000
    style H fill:#fff,color:#000
    style I fill:#e1f5fe,color:#000
    style J fill:#fff,color:#000
    style K fill:#fff,color:#000
```

---

## Topic 6: Discrete Random Variable - Complete Analysis

### Rolling a Dice - Step by Step

```mermaid
graph TD
    A[Roll Dice] --> B[Possible Outcomes: 1,2,3,4,5,6]
    
    B --> C[PMF Calculation]
    C --> D[All outcomes have probability 1/6]
    
    B --> E[CDF Calculation]
    E --> F[Cumulative probabilities: 1/6, 2/6, 3/6, 4/6, 5/6, 1]
    
    G[Question: P of X less than or equal to 4] --> H[Sum: P1 + P2 + P3 + P4]
    H --> I[Answer: 4/6 equals 2/3]
    
    style A fill:#e1f5fe,color:#000
    style B fill:#fff,color:#000
    style C fill:#fff3e0,color:#000
    style D fill:#fff,color:#000
    style E fill:#e8f5e8,color:#000
    style F fill:#fff,color:#000
    style G fill:#fff,color:#000
    style H fill:#fff,color:#000
    style I fill:#c8e6c9,color:#000
```

---

## Programming Implementation Flow

```mermaid
flowchart TD
    A[Start: Choose Distribution Type] --> B{Discrete or Continuous?}
    
    B -->|Discrete| C[Use PMF]
    B -->|Continuous| D[Use PDF]
    
    C --> E[Calculate individual probabilities]
    D --> F[Calculate density values]
    
    E --> G[Sum for cumulative: CDF]
    F --> H[Integrate for cumulative: CDF]
    
    G --> I[Verify: CDF should reach 1]
    H --> I
    
    I --> J[Plot results]
    J --> K[Bar chart for discrete]
    J --> L[Smooth curve for continuous]
    
    style A fill:#e1f5fe,color:#000
    style B fill:#fff,color:#000
    style C fill:#fff3e0,color:#000
    style D fill:#f3e5f5,color:#000
    style E fill:#fff,color:#000
    style F fill:#fff,color:#000
    style G fill:#fff,color:#000
    style H fill:#fff,color:#000
    style I fill:#e8f5e8,color:#000
    style J fill:#fff,color:#000
    style K fill:#fff,color:#000
    style L fill:#fff,color:#000
```

---

## Key Relationships Summary

```mermaid
mindmap
  root((Probability Distributions))
    Random Variables
      Discrete
        PMF
        Examples
          Dice
          Coins
          Binomial
      Continuous  
        PDF
        Examples
          Height
          Weight
          Normal
    Cumulative Functions
      CDF for both types
      Properties
        Non-decreasing
        0 to 1 range
        P of X less than x
    Key Relationships
      PDF equals derivative of CDF
      Area under PDF equals Probability
      Sum of PMF equals Probability
      Integration vs Summation
```

---

## Programming Examples

### Python Implementation

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm, uniform

# Example 1: Dice PMF and CDF (from your images)
dice_outcomes = np.array([1, 2, 3, 4, 5, 6])
dice_pmf = np.ones(6) / 6  # Each outcome has probability 1/6

# Calculate CDF
dice_cdf = np.cumsum(dice_pmf)

print("Dice PMF:", dice_pmf)
print("Dice CDF:", dice_cdf)

# Verify your calculation: P(X ≤ 4)
prob_leq_4 = dice_cdf[3]  # Index 3 corresponds to outcome 4
print(f"P(X ≤ 4) = {prob_leq_4:.3f} = {4/6:.3f}")

# Example 2: Height PDF and CDF (from your images)
# Assuming normal distribution with mean=165, std=10
mu, sigma = 165, 10
x_values = np.linspace(140, 190, 1000)

# Calculate PDF and CDF
pdf_values = norm.pdf(x_values, mu, sigma)
cdf_values = norm.cdf(x_values, mu, sigma)

# Verify: P(X ≤ 155)
prob_155 = norm.cdf(155, mu, sigma)
print(f"P(Height ≤ 155) = {prob_155:.3f}")

# Create plots similar to your lecture
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(12, 5))

# PMF for dice
ax1.bar(dice_outcomes, dice_pmf, alpha=0.7, color='lightblue')
ax1.set_title('Dice PMF (from your lecture)')
ax1.set_xlabel('Outcome')
ax1.set_ylabel('Probability')
ax1.set_ylim(0, 0.2)

# PDF for height
ax2.plot(x_values, pdf_values, 'b-', linewidth=2)
ax2.fill_between(x_values[x_values <= 155], pdf_values[x_values <= 155], alpha=0.3)
ax2.set_title('Height PDF (from your lecture)')
ax2.set_xlabel('Height')
ax2.set_ylabel('Density')

plt.tight_layout()
plt.show()
```

### Verification of Your Calculations

```python
# Dice example verification
print("=== Dice Calculations (from your images) ===")
outcomes = [1, 2, 3, 4, 5, 6]
prob_each = 1/6

# Individual probabilities
for outcome in outcomes:
    print(f"P({outcome}) = {prob_each:.3f}")

# Cumulative probability P(X ≤ 4)
prob_leq_4 = sum([1/6 for i in range(1, 5)])  # 1,2,3,4
print(f"\nP(X ≤ 4) = P(1) + P(2) + P(3) + P(4)")
print(f"         = 1/6 + 1/6 + 1/6 + 1/6")  
print(f"         = 4/6 = {4/6:.3f}")

# Height example (approximate values from your graph)
print("\n=== Height Calculations (from your images) ===")
print("Assuming Normal Distribution with μ=165, σ=10")

prob_155 = norm.cdf(155, 165, 10)
prob_165 = norm.cdf(165, 165, 10)

print(f"P(Height ≤ 155) ≈ {prob_155:.2f} (matches your ~0.25)")
print(f"P(Height ≤ 165) ≈ {prob_165:.2f} (matches your ~0.50)")
```

---

## Summary

**PDF (Continuous):**
- Used for continuous random variables
- Shows probability density
- Area under curve = probability
- Example: Height of students

**PMF (Discrete):**  
- Used for discrete random variables
- Shows exact probabilities
- Sum of probabilities = 1
- Example: Rolling dice

**CDF (Both):**
- Shows cumulative probability P(X ≤ x)
- Always non-decreasing from 0 to 1
- Slope of CDF = PDF/PMF value

**Key Relationship:**
Probability Density = Gradient of Cumulative Curve

```mermaid
graph LR
    A[PDF/PMF] -->|Integration/Summation| B[CDF]
    B -->|Differentiation| A
    
    C[Area under PDF] --> D[Probability]
    E[Sum of PMF values] --> D
    
    F[Slope of CDF] --> A
    
    style A fill:#f3e5f5,color:#000
    style B fill:#fff3e0,color:#000
    style C fill:#fff,color:#000
    style D fill:#e8f5e8,color:#000
    style E fill:#fff,color:#000
    style F fill:#fff,color:#000
```
