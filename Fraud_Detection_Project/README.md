# FinTech Fraud Detection & Strategic Simulation Dashboard

## 📁 Data Source
This project utilizes the [Credit Card Fraud Detection Dataset] https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud hosted on Kaggle. The dataset was selected for its high imbalance and temporal features, providing an ideal sandbox for simulating defensive financial thresholds.

## 📊 Project Overview
This repository contains an end-to-end enterprise business intelligence solution designed to analyze financial fraud lifecycles, track operational breach timelines, and simulate defensive security thresholds. Built with a premium dark-themed UI/UX, this 4-page dashboard bridges the gap between deep forensic data engineering and executive decision-making.

### 🧠 Core Business Problem
When a security breach or fraud wave hits a financial pipeline, executives need to know three things instantly: *What is the damage? When did it happen? How do we stop it without locking out real customers?* This project answers all three by combining temporal anomaly tracking with an interactive dynamic simulation tool.

---

## 🛠️ Tech Stack & Architecture
* **BI Platform:** Power BI Desktop
* **Data Layer:** `creditcard_powerbi` relational schema 
* **Languages:** DAX (Data Analysis Expressions) for complex modeling & dynamic measures
* **Design Philosophy:** Human-Centric UI/UX, High-Contrast Dark Theme, Scannable Information Hierarchy

---

## 📐 Key Data Engineering & DAX Measures
The simulation engine utilizes a What-If parameter boundary slider (`0.00` to `1.00`) to let users model risk tolerance dynamically.

### Dynamic Capital Recovery Formula
* **Formula:** `Simulated Recovered Capital = [Total Fraud Loss] * (1 - [Model Threshold Value])`
* **`Total Fraud Loss`**: Calculated via an optimized row-filter counting transactions flagged as `Class = 1` (Fraud).
* **`Model Threshold Value`**: A dynamic scalar captured straight from the user's live slider interaction.

---

## 🖥️ Dashboard Architecture (The 4-Page Story)

### 1. Executive Summary
* **Intent:** The high-level hook for C-suite stakeholders.
* **Metrics:** High-impact KPI blocks showing immediate losses, total transaction spikes, and a macro timeline of the breach event to establish the baseline narrative.

![Dashboard Preview](./Fraud_Detection_Project/Executive%20Summary.png)

### 2. Temporal Analysis
* **Intent:** Deep-dive behavioral tracking across time dimensions.
* **Metrics:** Advanced scatter plots and dense matrix cross-examinations mapping fraud events against `Operational Day` and `True Hour` to identify system vulnerabilities and attacker operating schedules.

### 3. Financial Metrics
* **Intent:** Quantification of fiscal risk.
* **Metrics:** Granular breakdown of asset damage, loss velocity tracking, and case volume distributions to isolate which transaction categories took the heaviest financial hit.

### 4. Deep Dive & Model Simulation
* **Intent:** Proactive defensive strategy and live forensic auditing.
* **Features:** 
  * **Interactive Slider:** Lets users dynamically scale system sensitivity, tracking simulated savings between a strict security posture (**$58.59K recovered**) and an open-gate scenario (**$2.93K recovered**).
  * **Forensic Ledger Table:** A structured, high-readability data grid mapping `Transaction_Type`, `Operational Day`, and `True Hour` against `Sum of Amount` to enable instantaneous root-cause analysis.

---

## 🚀 Key Analytical Takeaways
1. **The Defensive Trade-Off:** Calibrating system security directly impacts consumer retention. A strict `0.00` threshold catches all fraud but causes massive operational backlogs.
2. **Optimal Boundary Tuning:** Data modeling suggests that deploying an operational threshold between `0.35` and `0.45` maximizes capital recovery while protecting legitimate consumer checkouts from false positives.
