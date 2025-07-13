# 📦 Production Planning Optimization with PuLP

This project solves a **multi-period production planning problem** using **linear programming** with [PuLP](https://coin-or.github.io/pulp/). The model minimizes total costs related to production, inventory, shortages (backorders), workforce usage, resource activation/deactivation, and maintenance.

The solution includes data visualization using **Matplotlib** and **Seaborn**.

---

## 📈 Problem Description

The goal is to determine:

- How many units to **produce** in each period.
- How many units to **store** or **backorder**.
- How many **resources (workers/machines)** to activate, deactivate, or send to maintenance.

Subject to:

- Daily **production capacity** per worker.
- **Demand** fulfillment for each period.
- Limits on **inventory**, **backorders**, and **available workers**.
- **Workforce dynamics**: activation, deactivation, maintenance.
- Minimum and maximum available operators.

---

## 🔧 Model Components

### Objective Function

Minimize total cost:

- Production cost
- Inventory holding cost
- Backorder cost
- Resource usage cost (varies by period)
- Activation/deactivation costs
- Maintenance cost

### Constraints

- Production capacity based on working days and available workers.
- Demand satisfaction via production, inventory, or backorders.
- Workforce balance (hiring/firing over time).
- Inventory and backorder limits.
- Workforce availability (total = active + maintenance).

---

## 📊 Outputs

- Total cost of the optimal solution.
- DataFrame with detailed results for each time period.
- Two line charts:
  - **Production vs Inventory vs Shortages**
  - **Resource Usage and Transitions**

---

## 🛠️ Technologies Used

- Python 3.x
- [PuLP](https://pypi.org/project/PuLP/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

