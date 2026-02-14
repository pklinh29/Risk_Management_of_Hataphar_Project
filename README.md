# Risk Management of Hataphar 
## Table Of Contents 
---
# 📊 Data-Driven Risk Management: Production Delay Simulation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Simulation](https://img.shields.io/badge/Simulation-Monte%20Carlo-success)
![Risk Management](https://img.shields.io/badge/Risk%20Management-ISO%2031000-yellow)

## 📖 Project Overview
This project presents a **Quantitative Risk Assessment** approach for manufacturing operations, specifically targeting **OP1: Production Delay Risk**. 

Instead of relying solely on subjective expert judgment, this project integrates **Machine Learning (Linear Regression)** for Root Cause Analysis and **Monte Carlo Simulation** for future risk forecasting. The results are mapped onto a standard Corporate Risk Heatmap to facilitate data-driven decision-making.

## 🏭 Business Context
In a pharmaceutical manufacturing environment (e.g., GMP facility), production delays can lead to severe SLA penalties, market share loss, and reputational damage. Our objective is to:
1. Identify the hidden drivers of production delays.
2. Quantify the probability of future delays if no action is taken.
3. Propose actionable mitigation strategies (4T Framework).

---

## ⚙️ Methodology

Our analytical pipeline consists of 4 main phases:

1. **Black-Box Data Generation:** Simulating historical ERP data representing a degrading factory state (high machine age, variable worker skills) without hard-coding direct formulas.
2. **Machine Learning Discovery:** Applying `Scikit-Learn`'s Linear Regression to autonomously discover the causal relationship between Machine Age, Worker Skill, and Batch Release Time.
3. **Future Risk Forecasting:** Running a **10,000-iteration Monte Carlo Simulation** representing the next fiscal year (aging machinery scenario) to calculate the Probability of Failure (1-CDF) against a critical threshold of 74 minutes.
4. **Managerial Evaluation:** Translating the statistical probability into a standard 1-5 Likelihood Score and plotting it on a Risk Portfolio Heatmap alongside qualitative risks.

---

## 📈 Key Visualizations & Findings

### 1. ML Discovery: Root Cause Analysis
The Machine Learning model successfully identified that **Machine Age** and **Worker Skill** are the primary drivers of production delays.
* *Insight:* Every 1-year increase in Machine Age adds ~1.97 minutes to production time.
* *Insight:* Every 1-point increase in Worker Skill reduces time by ~1.57 minutes.

*(Placeholder: Upload your chart to `assets/1_ml_discovery.png`)*
![ML Discovery](assets/1_ml_discovery.png)

### 2. Monte Carlo Future Forecast
Simulating the next fiscal year shows a shifting distribution towards the danger zone. The probability of exceeding the 74-minute threshold (Risk Probability) is calculated at **~13.2%**.

*(Placeholder: Upload your chart to `assets/2_future_forecast.png`)*
![Future Forecast](assets/2_future_forecast.png)

### 3. Risk Portfolio Heatmap
The simulated quantitative risk (**OP1**) is plotted alongside other qualitative risks (R2-R5) evaluated by expert judgment. OP1 falls into the **Unacceptable Zone** (Likelihood 3, Impact 5).

*(Placeholder: Upload your chart to `assets/3_risk_heatmap.png`)*
![Risk Heatmap](assets/3_risk_heatmap.png)

---

## 🛡️ Risk Treatment Strategy (4T Framework)

Based on the quantitative findings, we propose a primary **TREAT (Mitigate)** strategy targeting the root causes:

1. **Targeting Machine Age (Predictive Maintenance):** Install IoT sensors on machines >10 years old to detect anomalies early, reducing unplanned downtime by an expected 30%.
2. **Targeting Worker Skill (Advanced Training):** Implement rigorous cross-training programs to elevate the average worker skill score from 6.5 to 8.0, mathematically pulling the risk curve back into the acceptable zone.

**Secondary Strategies:**
* **Transfer:** Outsource excess capacity to OEM partners during peak demand.
* **Tolerate:** Maintain buffer safety stock for non-critical SKUs.
* **Terminate:** Decline impossible deadlines that exceed the calculated capacity of aging machines.

---

## 🚀 How to Run the Project

**1. Clone the repository**
```bash
git clone [https://github.com/your-username/Data-Driven-Risk-Management.git](https://github.com/your-username/Data-Driven-Risk-Management.git)
cd Data-Driven-Risk-Management

