# Market Basket Analysis for Retailers

**Author:** [Neel Shrivastava](https://linkedin.com/in/neelshrivastava)  
**Role:** Data Analyst Intern – Hackveda  
**Date:** October 2025  

---

## Project Overview

Market Basket Analysis (MBA) is a data mining technique used to discover associations and correlations between products that are frequently bought together. This project aims to help retailers **understand customer purchasing behavior** to improve **product placement, cross-selling, and bundling strategies**.

---

## Objective

To identify relationships between items often purchased together using **association rule mining** and generate actionable insights for **business growth and marketing strategies**.

---

## Problem Statement

Retailers need to uncover relationships between items frequently bought together.  
For instance, if customers buying **bread** are also likely to buy **butter**, supermarkets can:
- Place these products near each other
- Create combo discounts
- Improve shelf strategy for increased sales

---

## Dataset Overview

- **Dataset:** Online Retail II (Kaggle)
- **Source:** [Kaggle – Online Retail II Dataset](https://www.kaggle.com/datasets)
- **Description:** Transactional data from a UK-based online retailer
- **Filtered Region:** Germany
- **Key Fields:**  
  - `Invoice`  
  - `StockCode`  
  - `Description`  
  - `Quantity`  
  - `InvoiceDate`  
  - `Country`

---

## Methodology

This project uses the **Apriori Algorithm** to find frequent itemsets and generate association rules.

### Steps Involved:
1. **Data Cleaning**
   - Remove missing values and duplicates  
   - Filter transactions from Germany  

2. **Generate Itemsets**
   - Create combinations of items (1-item, 2-item, 3-item sets)  

3. **Calculate Support**
   - Frequency of itemset appearance across transactions  

4. **Apply Apriori Algorithm**
   - Keep only itemsets with support ≥ minimum threshold  

5. **Generate Association Rules**
   - Create rules like `A → B` (if A is bought, B is likely bought)  

6. **Evaluate Rules**
   - Using metrics:  
     - **Support:** Frequency of itemset in all transactions  
     - **Confidence:** Likelihood of buying B when A is bought  
     - **Lift:** Strength of association between A and B  

---

## Example Walkthrough

Example with 4 transactions:
| Transaction | Items |
|--------------|-------|
| 1 | Bread, Milk |
| 2 | Bread, Butter |
| 3 | Bread, Milk, Butter |
| 4 | Milk, Butter |

- **Frequent Itemsets:** Bread (0.75), Milk (0.75), Butter (0.75)
- **Association Example:** Bread → Butter (Support=0.5, Confidence=0.67)

---

## Evaluation Metrics

| Metric | Definition | Interpretation |
|---------|-------------|----------------|
| **Support** | Frequency of an itemset | Higher = More frequent |
| **Confidence** | Probability of consequent given antecedent | Reliability of rule |
| **Lift** | Strength of association | Lift > 1 = Strong rule |

---

