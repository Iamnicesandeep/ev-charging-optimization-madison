
# ⚡ Optimizing Electric Vehicle (EV) Charging Station Placement in Madison

This project applies prescriptive analytics to determine the optimal placement of EV charging stations in Madison. Using a Mixed-Integer Programming (MIP) model, it minimizes total cost while maximizing service coverage under real-world constraints.

---

## 🎯 Problem Statement

Current EV infrastructure is unevenly distributed, creating accessibility gaps for users in residential and rural areas. The goal is to develop a cost-effective, demand-sensitive placement plan that ensures broader and more equitable EV access across Madison.

---

## 📊 Model Overview

- **Objective**: Minimize total cost = Installation Cost + Penalty for Unmet Demand
- **Solver**: CBC (open-source MIP solver)
- **Time Limit**: 300 seconds to avoid infinite runs

---

## 📥 Inputs & Parameters

| Parameter           | Description |
|---------------------|-------------|
| `installation_costs` | Cost to install at each candidate site |
| `demand`            | EV charging need across demand zones |
| `capacity`          | Max load each station can support |
| `budget`            | Total installation cost constraint |
| `distance matrix`   | Distance between candidate sites and demand zones |
| `distance limit`    | Max allowable distance to serve a zone |

---

## 🔗 Decision Variables

- `Install_Site[i]`: Binary – whether to install a station at site *i*
- `Serve_Zone[i][j]`: Binary – whether site *i* serves demand zone *j*

---

## 📌 Constraints

- **Coverage**: Every demand zone must be served by at least one nearby station.
- **Capacity**: Stations must not exceed their service limits.
- **Budget**: Total install costs must stay within budget.

---

## ✅ Results

- The CBC solver provided a **Global Optimal** solution within time limit.
- Optimal number and location of stations selected.
- Maximum demand covered with available budget.

---

## 🛠️ Tools Used

- Python
- PuLP (MIP modeling)
- CBC Solver
- Google Colab

---

## 📄 Project Report

📑 [`Prescriptive Final.pdf`](docs/Prescriptive%20Final.pdf)

---

## 📬 Contact

Sandeep Karumudi  
📧 sandeepkarumudi3@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/sandeepk96)  
💻 [Portfolio](https://github.com/iamnicesandeep)
