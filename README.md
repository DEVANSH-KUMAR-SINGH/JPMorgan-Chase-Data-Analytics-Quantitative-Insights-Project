# 📊 Quantitative Research & Risk Analytics – JPMorgan Chase Job Simulation

This repository contains my completed work for the **JPMorgan Chase & Co. Quantitative Research Job Simulation** hosted on **Forage**.  
The project simulates real-world problems faced by **trading desks and risk teams**, covering **commodity pricing, contract valuation, credit risk modeling, and credit score quantization**.

---

## 📌 Project Overview

The objective of this project is to design **prototype quantitative models** that help financial institutions:
- Price commodity storage contracts
- Estimate future prices using historical data
- Predict credit default risk
- Quantize continuous credit scores into categorical risk buckets

All models are implemented in **Python**, following industry-style assumptions and constraints.

---

## 🧩 Project Structure

```text
📂 Quantitative-Research-JPMC
│
├── Nat_Gas.csv
├── Task 1_Natural_Gas_Price_Model.ipynb
├── Task 2_Storage_Contract_Pricing.ipynb
├── Task 3_Loan_Default_PD_Model.ipynb
├── Task 4_FICO_Quantization_DP.ipynb
├── FICO_DP_LL_and_MSE_Buckets.csv
└── README.md
```

## 🧠 Tasks Breakdown

### 🟡 **Task 1: Natural Gas Price Modeling**

**Goal:**  
Estimate the price of natural gas on any given date using historical monthly data.

**Approach:**
- Loaded historical natural gas prices  
- Identified seasonal patterns (winter spikes, summer lows)  
- Built a regression-based model using:
  - Time trend  
  - Month-based seasonality  
- Extrapolated prices one year into the future  

**Output:**  
A function that takes a date as input and returns an **estimated gas price**.

---

### 🟡 **Task 2: Commodity Storage Contract Pricing**

**Goal:**  
Calculate the value of a natural gas storage contract.

**Inputs Considered:**
- Injection dates and volumes  
- Withdrawal dates and volumes  
- Gas prices on respective dates  
- Injection / withdrawal rate limits  
- Maximum storage capacity  
- Storage costs  

**Key Concept:**

\[
\textbf{Contract Value} = \text{Revenue} - \text{Purchase Cost} - \text{Storage \& Operational Costs}
\]

**Output:**  
A pricing function that evaluates the **net value of the storage contract**.

---

### 🔴 **Task 3: Credit Risk & Expected Loss Modeling**

**Goal:**  
Predict the **Probability of Default (PD)** for personal loan borrowers and estimate expected loss.

**Approach:**
- Built a logistic regression model  
- Used borrower financial features  
- Calculated:
  - Probability of Default (PD)  
  - Expected Loss (with fixed recovery rate)

**Expected Loss Formula:**

\[
\textbf{Expected Loss} = \text{PD} \times \text{Exposure} \times (1 - \text{Recovery Rate})
\]

---

### 🔴 **Task 4: FICO Score Quantization (Dynamic Programming)**

**Goal:**  
Convert continuous FICO scores into **categorical risk ratings** for machine learning models.

**Why Quantization?**
- Some models require categorical inputs  
- Credit scores span a large range (300–850)

**Techniques Implemented:**
- Dynamic Programming for **optimal bucketing**
- Two optimization objectives:
  - Log-Likelihood Maximization  
  - Mean Squared Error (MSE) Minimization  

**Output:**
- Optimal **FICO bucket boundaries**
- Credit ratings where:

> **Lower rating = better credit quality**

---

## 🛠️ Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Jupyter Notebook  
- Dynamic Programming  
- Statistical Modeling  

---

## 📈 Key Learnings

- How quantitative models support **trading and risk decisions**  
- Importance of **seasonality in commodity markets**  
- Practical implementation of **credit risk analytics**  
- Applying **optimization & dynamic programming in finance**  
- Translating raw data into **actionable financial insights**  

---

## 🚀 How to Run

**Clone the repository:**

```bash
git clone https://github.com/your-username/Quantitative-Research-JPMC.git
```

**Install dependencies**

```bash
pip install pandas numpy scikit-learn matplotlib
```

**Open notebook**

```bash
jupyter notebook
```

## 📜 Certificate

This project was completed as part of the
JPMorgan Chase & Co. – Quantitative Research Job Simulation
issued by Forage (December 2025).

## 👤 Author

Devansh Kumar Singh
Aspiring Quantitative Researcher | Risk Analytics | Financial Modeling

## ⭐ If you find this project useful, feel free to star the repository!
