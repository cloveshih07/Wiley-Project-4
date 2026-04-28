# Wiley-Project-4
---
# Wiley Presentation – Tanzania Food Demand & Nutrition Analysis

## 📌 Project Overview

This project analyzes how households in Tanzania make food consumption decisions both **what they eat and how much they consume** and how these choices relate to **prices, income, and nutritional outcomes**.

Food choices do not always align with nutritional recommendations, even when affordable options exist. Household demand is shaped by:

* Economic constraints (income, prices)
* Access to food options
* Preferences and consumption patterns

### 🎯 Project Goal

The goal is to **quantitatively characterize the relationship between food demand and nutrition**, and evaluate how economic and policy changes impact dietary outcomes.

We specifically aim to:

* Identify gaps between **actual diets and recommended nutrition**
* Measure **nutritional deficiencies**
* Simulate **policy interventions** to improve outcomes

---

## 📂 Repository Structure

```
├── data/
│   ├── raw/                # Original Tanzania household datasets
│   ├── cleaned/            # Processed datasets used for analysis
│
├── code/
│   ├── data_cleaning/      # Scripts for cleaning and preparing data
│   ├── demand_estimation/  # Demand system estimation
│   ├── nutrient_mapping/   # Mapping food to nutrients (FCT)
│   ├── policy_simulations/ # Counterfactual simulations
│   ├── visualization/      # Graphs and figures
│
├── outputs/
│   ├── tables/             # Regression results, summary stats
│   ├── figures/            # Graphs for presentation
│
├── docs/
│   ├── methodology.md      # Detailed methodology explanation
│   ├── replication.md      # Step-by-step replication guide
│
├── README.md
```

---

## 📊 Data Description

### Dataset: Tanzania Household Survey

* ~5,800 households
* 2 waves: 2019–2020 and 2020–2021
* Includes:

  * Food expenditures (by category)
  * Prices
  * Household characteristics (demographics, size)

### Food Categories

* Initially 59 food items → aggregated to 29 categories
* Includes staples (maize, rice), proteins, fruits, vegetables, etc.

---

## ⚙️ Methodology

### 1. Demand System Estimation

We estimate a system of food demand equations to model how consumption responds to:

* Prices
* Income
* Household characteristics

Output: Price and income elasticities

---

### 2. Nutrient System Construction

Food consumption is mapped into nutrient intake using a **Food Composition Table (FCT)**.

Nutrients analyzed:

* Calories
* Protein
* Calcium
* Vitamin A
* Iron
* Zinc
* Vitamin C

---

### 3. Nutritional Adequacy Analysis

We compare predicted intake to recommended standards:

| Nutrient  | Recommended Intake |
| --------- | ------------------ |
| Energy    | 2000–2200 kcal     |
| Protein   | 50–60 g            |
| Calcium   | ~1000 mg           |
| Vitamin A | ~500 µg RAE        |
| Iron      | ~18 mg             |
| Zinc      | 8–11 mg            |
| Vitamin C | 75–90 mg           |

---

## Key Findings: Nutritional Challenges

* ✔ Calories: generally sufficient
* ❌ Micronutrient deficiencies:

  * Calcium (very low adequacy)
  * Vitamin A (low intake)
  * Iron and zinc deficiencies

### Core Insight

> Diets are **calorie-sufficient but nutrient-deficient**

### Economic Explanation

* Low income → budget constraints
* High cost of nutrient-dense foods
* Households optimize:

  * “calories per dollar” rather than nutrition

---

## Policy Simulations

We evaluate how different policies affect nutrition:

### 1. Income Transfers

* +10%, +20%, +50% income increases
* Result:

  * Slight improvements across nutrients
  * Limited effect on major deficiencies

---

### 2. Food Subsidies

* Target nutrients (Vitamin A, Calcium, or all)
* Result:

  * Moderate improvements
  * Effect depends on which foods are subsidized

---

### 3. Fortification (Most Effective)

* Oil → Vitamin A
* Maize flour → Vitamin A + Calcium
* Wheat flour → Calcium

### Result:

* Large improvements in:

  * Vitamin A
  * Calcium
* Outperforms all other policies

Reason:

* Improves nutrition **without requiring behavior change**

---

## 💡 Innovation in Food & Nutrition

### Key Issue: Hidden Hunger

* Micronutrient deficiencies persist despite sufficient calories

### Existing Policies in Tanzania

* Mandatory fortification (since 2011):

  * Oil → Vitamin A
  * Flour → Iron, folate

### Challenges

* Low compliance (~16% in some cases)
* Weak enforcement

### Recommendations

* Improve fortification compliance
* Expand biofortified crops
* Combine with economic policies

---

## 💸 Policy Cost Analysis

| Policy           | Cost | Efficiency        | Effectiveness |
| ---------------- | ---- | ----------------- | ------------- |
| Income transfers | High | Efficient         | Low–Moderate  |
| Subsidies        | High | Inefficient (DWL) | Moderate      |
| Fortification    | Low  | Highly efficient  | High          |

### Key Insight

> Fortification provides the largest nutritional gains at the lowest economic cost.

---

## 🔁 Replication Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-repo/tanzania-food-demand.git
cd tanzania-food-demand
```

### 2. Install dependencies

(Example for Python)

```bash
pip install -r requirements.txt
```

### 3. Run data cleaning

```bash
python code/data_cleaning/clean_data.py
```

### 4. Estimate demand system

```bash
python code/demand_estimation/run_model.py
```

### 5. Construct nutrient system

```bash
python code/nutrient_mapping/nutrients.py
```

### 6. Run policy simulations

```bash
python code/policy_simulations/simulate.py
```

### 7. Generate figures

```bash
python code/visualization/plots.py
```

---

### Contributors

* Christian
* Chloe
* Kritin
* Mahika
* Layla
* Micah

---

## 📌 Final Takeaway

This project shows that:

> Improving nutrition is not just about increasing food consumption, but improving the **quality of diets**, which is constrained by economic factors.

Policies that directly improve nutrient content—especially **fortification**—are the most effective and efficient way to close the gap between actual and recommended nutrition.


* Customize this to match your **actual file names/code structure**
* Or shorten it into a **clean 1-page version (some professors prefer that)**
