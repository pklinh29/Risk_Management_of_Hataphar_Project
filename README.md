# 📊 Data-Driven Corporate Risk Portfolio: Strategy & Monte Carlo Simulation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Simulation](https://img.shields.io/badge/Simulation-Monte%20Carlo-success)
![Risk Management](https://img.shields.io/badge/Strategy-PESTLE%20%7C%20Value%20Chain-yellow)

## 📑 Table of Contents
- [Context](#context)
- [Preparation](#preparation)
- [Implementation](#implementation)
- [Business Value Achievements](#business-value-achievements)
- [Individual Achievements](#individual-achievements)

---

## 🌍 Context <a name="context"></a>

In the highly regulated and volatile pharmaceutical manufacturing industry, enterprises face a barrage of risks from multiple fronts. Externally, macro-economic shocks, strict regulatory updates (e.g., EU-GMP compliance), and supply chain disruptions constantly threaten stability. Internally, aging infrastructure and human skill gaps create operational bottlenecks. Left unchecked, these risks compound, leading to severe SLA penalties, loss of market share, and critical reputational damage.

The **Chief Risk Officer (CRO) / Plant Manager** requires a holistic, bird's-eye view of the *entire* corporate risk landscape to effectively allocate the annual mitigation budget. While the company's risk portfolio contains various qualitative risks (e.g., Tender Failures, Regulatory Inspections), the core operational risk—**OP1: Production Delay**—is highly dynamic, measurable, and directly controllable. 

I initiated this project to provide executive management with a comprehensive **Corporate Risk Heatmap** that captures all identified risks, while applying advanced, data-driven quantitative simulation exclusively to the operational bottleneck (OP1) that we have the power to change.

---

## 🛠️ Preparation <a name="preparation"></a>

To ensure the project aligns perfectly with business objectives rather than just being a coding exercise, I adopted a **Bottom-Up Approach**:

1. **Defining the Output First:** The end goal was clearly defined: A standard Managerial Risk Heatmap (Likert 1-5 scale) and a concrete 4T Treatment Plan (Treat, Transfer, Tolerate, Terminate) ready for C-suite review.
2. **Strategic Data Collection:** Before writing any code, I conducted rigorous strategic data collection to build the Initial Risk Register. This involved:
   * **PESTLE Analysis:** To capture macro-environmental threats (Political, Economic, Social, Technological, Legal, Environmental).
   * **Porter’s 5 Forces:** To assess industry-level and market-driven risks.
   * **Value Chain Analysis:** To pinpoint internal vulnerabilities across primary and support activities. This systemic scan successfully highlighted the critical weakness in our Inbound Logistics and Operations, pointing directly to the Production Delay Risk.

---

## 🚀 Implementation <a name="implementation"></a>

This project seamlessly bridges qualitative strategic frameworks with quantitative Data Science.

### Project Flowchart
*(Workflow diagram illustrating the end-to-end ISO 31000 Risk Management process)*
![Project Flowchart](assets/flowchart.png) 
*(Note: Upload your draw.io exported image to `assets/flowchart.png` in the repository)*

### Step-by-Step Execution:

**Step 1: Strategic Risk Identification & Scoping (The Filter)**
* **Tool:** Expert Judgment / Excel Risk Register.
* **Execution:** Synthesized the PESTLE and Value Chain outputs into a list of 11 initial risks. Through a filtering process based on "Data Availability" and "Frequency of Occurrence", I selected **OP1: Production Delay Risk** as the primary candidate for quantitative simulation. The remaining critical risks (R2-R5) were retained for qualitative expert assessment to provide a complete portfolio context.

**Step 2: Black-Box Historical Data Generation**
* **Tool:** `NumPy`, `Pandas` (Python).
* **Execution:** Simulated 5,000 records of raw ERP data. I deliberately avoided hard-coding a "hidden formula". Instead, I generated independent variables reflecting a degraded factory state (`Machine_Age` 5-15 years, `Worker_Skill`) and injected real-world variance and noise. This creates a realistic, messy dataset mirroring actual manufacturing execution systems.

**Step 3: Machine Learning Root Cause Discovery**
* **Tool:** `Scikit-Learn` (Linear Regression).
* **Execution:** Fed the simulated ERP data into a Machine Learning model to autonomously "discover" causal relationships. The model mathematically quantified that increasing *Machine Age* heavily delays batch release times, whereas higher *Worker Skill* accelerates it.

**Step 4: Future Risk Forecasting (Monte Carlo Simulation)**
* **Tool:** `SciPy`, `NumPy`.
* **Execution:** Simulated 10,000 production batches for the upcoming fiscal year. I applied a "Dynamic Shift" scenario (aging the machinery by 1 year: Age 6-16) to see what happens if the company does nothing. Using the ML formula, I calculated the exact Probability of Failure (1-CDF) against our critical 74-minute threshold, resulting in a **~14% Risk Probability**.

**Step 5: Visualizing the Managerial Dashboard**
* **Tool:** `Matplotlib`, `Seaborn`.
* **Execution:** Translated the 14% statistical probability into a standard Likelihood Score (Level 3 - Possible). I then plotted this dynamic quantitative risk (OP1 - Red) alongside the static qualitative risks (R2-R5 - Diverse colors) onto a unified Corporate Risk Heatmap, clearly showing OP1 in the Unacceptable Zone.

**Step 6: Risk Treatment & Continuous Monitoring**
* **Tool:** Fishbone Diagram (4M/4P), 4T Framework.
* **Execution:** Proposed actionable *Treat* strategies targeting the ML-discovered root causes: Predictive Maintenance (for Age) and Cross-Training (for Skill). Established a feedback loop to monitor the Key Risk Indicator (Batch Release Time) and re-simulate the model every 6 months to verify the effectiveness of the solutions.

---

## 💎 Business Value Achievements <a name="business-value-achievements"></a>

This project delivers exactly what executive management expects from a robust Enterprise Risk Management (ERM) initiative:

1. **Holistic Portfolio Visibility:** The CRO receives a single, unified dashboard that seamlessly combines both qualitative strategic risks (Expert Judgment) and quantitative operational risks (AI Simulation), allowing for a complete view of the company's vulnerabilities.
2. **Eradicating "Gut-Feeling" Decisions:** Transitioned the core operational risk assessment from subjective guessing to a mathematically proven, data-driven approach. The root causes are backed by Regression Analysis, not assumptions.
3. **Optimized Capital Allocation (CapEx vs. OpEx):** By quantifying the exact impact of *Machine Age* vs. *Worker Skill*, the C-suite can mathematically justify whether to invest the annual budget in buying new machinery (CapEx) or funding intensive worker training programs (OpEx) to pull the risk back to the acceptable zone.
4. **Proactive Early Warning System:** The Monte Carlo simulation acts as a forward-looking radar, capturing the ~14% failure rate *before* the next fiscal year even starts, enabling proactive mitigation rather than reactive firefighting.

---

## 🏆 Individual Achievements <a name="individual-achievements"></a>

Through the execution of this end-to-end project, I have successfully:

* **Bridged the Gap between Strategy and Data Science:** Demonstrated the rare ability to translate high-level business frameworks (PESTLE, 5 Forces, Value Chain) into actionable Python code and statistical models.
* **Mastered Advanced Simulation Techniques:** Gained deep, hands-on proficiency in Monte Carlo simulations, Normal Distributions, and utilizing Machine Learning (`Scikit-Learn`) for root cause discovery rather than just basic prediction.
* **Enhanced Executive Communication:** Developed the acumen to convert complex statistical outputs (like 1-CDF percentages) into standard corporate formats (1-5 Likert scales) and present them via clear, executive-ready visualizations (`Matplotlib/Seaborn`).
* **Executed Full-Cycle Project Management:** Successfully navigated the entire ISO 31000 Risk Management process—from initial identification and deep-dive analysis to strategy formulation (4T) and establishing monitoring mechanisms.

---
*Developed as a comprehensive Case Study for the Risk Management Course (20251).*
