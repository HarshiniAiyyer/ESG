# 🌿 ESGRecommender

A recommender system that selects companies with low ESG (Environmental, Social, and Governance) risk scores using **Genetic Algorithms**. This project encourages socially responsible investing by promoting portfolios with minimal sustainability risks.

---

## 🧠 Overview

This notebook-based project uses an **evolutionary optimization** technique to select a subset of companies from the S&P 500 that collectively have the **lowest ESG risk**, supporting ESG-aligned investment decisions.

---

## 🔍 Project Goals

- Recommend a small portfolio of companies with **low ESG Risk Scores**.
- Use **Genetic Algorithms (GA)** to evolve and optimize company subsets.
- Provide a reproducible and educational example of how evolutionary methods can be used in sustainable finance.

---

## 📂 Dataset

- Source: Publicly available S&P 500 ESG Risk Ratings from Sustainalytics.
- Columns used: `Symbol`, `Name`, `Sector`, `Total ESG Risk score`.

---

## ⚙️ Methodology

### 1. Preprocessing
- Load ESG scores.
- Remove missing data.
- Normalize ESG scores between 0 and 1.

### 2. Genetic Algorithm

| Step         | Description |
|--------------|-------------|
| **Population Initialization** | Randomly select subsets of companies |
| **Fitness Function**         | Calculate mean ESG score of the subset (lower is better) |
| **Selection**                | Keep top-performing subsets |
| **Crossover**                | Combine parts of parent subsets to create children |
| **Mutation**                 | Replace a random company in a subset to encourage diversity |
| **Iteration**                | Repeat for multiple generations |

---

## 🏁 Output

After evolving over several generations, the algorithm returns a recommended list of companies with **minimal ESG risk**:

```text
Recommended Companies:
Symbol     Name               Sector            Total ESG Risk Score
AAPL       Apple Inc.         Information Tech.  12.3
MSFT       Microsoft Corp.    Information Tech.  11.9
...
