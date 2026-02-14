# 📊 Data-Driven Risk Management: Integrating Strategy with Monte Carlo Simulation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Simulation](https://img.shields.io/badge/Simulation-Monte%20Carlo-success)
![Risk Management](https://img.shields.io/badge/Strategy-PESTLE%20%7C%20Value%20Chain-yellow)

## 📑 Table of Contents
1. [Context](#context)
2. [Preparation](#preparation)
3. [Implementation](#implementation)
4. [Business Value Achievements](#business-value-achievements)
5. [Individual Achievements](#individual-achievements)

---

## 🌍 Context <a name="context"></a>

In today's volatile manufacturing environment, a pharmaceutical enterprise faces a multitude of both internal and external risks. These range from macroeconomic shifts and stringent regulatory updates to internal bottlenecks like aging infrastructure and human errors. Left unmanaged, these risks translate directly into financial losses, SLA breaches, and severe reputational damage.

The **Chief Risk Officer (CRO) / Plant Manager** required a holistic, bird's-eye view of the entire **Corporate Risk Portfolio** to allocate the annual mitigation budget effectively. While the portfolio contains various qualitative risks (e.g., Regulatory Inspections, Inventory Shortages, Tender Failures), the core operational risk—**OP1: Production Delay**—is highly dynamic, measurable, and directly controllable. 

Therefore, this project was initiated to map out the entire risk landscape while applying advanced quantitative simulation specifically to the operational risk (OP1), providing the C-suite with a comprehensive, actionable dashboard.

---

## 🛠️ Preparation <a name="preparation"></a>

To ensure the project aligns with business objectives, I adopted a **Bottom-Up Approach**:
* **Defining the Output First:** The ultimate goal was to deliver a standard Managerial Risk Heatmap and a concrete 4T (Treat, Transfer, Tolerate, Terminate) Mitigation Plan.
* **Data Collection & Strategic Analysis:** Before any coding began, I utilized standard strategic management frameworks to identify and categorize the initial risk pool:
  * **PESTLE Analysis:** To capture macro-environmental risks (Political, Economic, Social, Technological, Legal, Environmental).
  * **Porter’s 5 Forces:** To assess industry-level and market-driven risks (e.g., Supplier bargaining power causing material delays).
  * **Value Chain Analysis:** To pinpoint internal vulnerabilities across primary and support activities, ultimately highlighting the critical weakness in Inbound Logistics and Operations (OP1).

---

## 🚀 Implementation <a name="implementation"></a>

The project workflow integrates qualitative strategy with quantitative data science. 

### Project Flowchart
*(Note: Flowchart designed via Draw.io)*
![Project Flowchart](assets/flowchart.png) 
*(Please upload your draw.io exported image to `assets/flowchart.png`)*

### Step-by-Step Execution:

**Step 1: Strategic Risk Identification (Qualitative)**
* **Tool:** Expert Judgment / Strategic Frameworks.
* **Action:** Identified and scored static risks (R2 to R5) such as GMP Non-conformity and Inventory Risks on a standard 1-5 scale. These act as the contextual background for our portfolio.

**Step 2: Black-Box Historical Data Generation**
* **Tool:** `NumPy`, `Pandas` (Python).
* **Action:** Simulated 5,000 records of raw ERP data. Instead of hardcoding a risk formula, I generated variables representing a degraded factory state (e.g., Machine Age ranging from 5-15 years, high system noise/volatility). This mirrors the reality of extracting messy data from a real-world manufacturing execution system.

**Step 3: Machine Learning Root Cause Discovery**
* **Tool:** `Scikit-Learn` (Linear Regression).
* **Action:** Applied Machine Learning to the historical data to autonomously "discover" the causal relationships. The model successfully quantified that increasing *Machine Age* heavily delays production, whereas increasing *Worker Skill* accelerates it.

**Step 4: Future Risk Simulation (Monte Carlo)**
* **Tool:** `SciPy`, `NumPy`.
* **Action:** Projected the next fiscal year by simulating 10,000 production batches under an "Aging Equipment" scenario (Age + 1 year). Using the formula learned in Step 3, I calculated the exact Probability of Failure (1 - Cumulative Distribution Function) against our critical SLA threshold (74 minutes).

**Step 5: Visualizing the Managerial Dashboard**
* **Tool:** `Matplotlib`, `Seaborn`.
* **Action:** Translated the statistical probability (13-14%) into a standard Likelihood Score (Level 3 - Possible). Plotted this dynamic quantitative risk (OP1) as a prominent focal point alongside the qualitative risks (R2-R5) on a unified Corporate Risk Heatmap.

---

## 💎 Business Value Achievements <a name="business-value-achievements"></a>

This project delivers precisely what executive management expects from a robust Risk Management initiative:

1. **Eradicating "Gut-Feeling" Decisions:** Transitioned the core operational risk assessment from subjective guessing to a mathematically proven, data-driven approach.
2. **Optimized Capital Allocation (CapEx vs. OpEx):** By quantifying the exact impact of *Machine Age* vs. *Worker Skill*, management can now mathematically justify whether to invest in buying new machines (CapEx) or funding intensive worker training programs (OpEx) to pull the risk back to the acceptable zone.
3. **Holistic Executive Visibility:** Delivered a unified "Risk Portfolio" dashboard that seamlessly integrates both qualitative strategic risks and quantitative operational risks, allowing the CRO to see the whole picture at a glance.
4. **Proactive Early Warning:** By simulating the future state (Aging scenario), the project acts as an early warning system, prompting proactive 4T mitigation strategies before actual SLA breaches occur.

---

## 🏆 Individual Achievements <a name="individual-achievements"></a>

Through the execution of this project, I have successfully:
* **Bridged the Gap between Strategy and Data Science:** Demonstrated the ability to translate high-level business frameworks (PESTLE, Value Chain) into actionable Python code and statistical models.
* **Mastered Advanced Simulation Techniques:** Gained hands-on proficiency in Monte Carlo simulations, normal distributions, and using Machine Learning (`Scikit-Learn`) for root cause discovery rather than just prediction.
* **Enhanced Managerial Communication:** Developed the acumen to convert complex statistical outputs (like 1-CDF percentages) into standard corporate Likert scales (1-5), presenting them in clear, executive-ready visualizations (`Matplotlib/Seaborn`).
* **Strengthened Problem-Solving:** Successfully reverse-engineered data parameters to ensure the simulation output accurately reflects the real-world operational bottlenecks of a pharmaceutical plant.

---
*Developed as a comprehensive Case Study for the Risk Management Course (20251).*
