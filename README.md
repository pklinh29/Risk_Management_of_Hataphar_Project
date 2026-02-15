# Data-Driven Corporate Risk Portfolio: Strategy & Monte Carlo Simulation


## Table of Contents
- [Context](#context)
- [Preparation](#preparation)
- [Implementation](#implementation)
- [Business Value Achievements](#business-value-achievements)
- [Individual Achievements](#individual-achievements)

---

## Context <a name="context"></a>

In the highly regulated and volatile pharmaceutical manufacturing industry, enterprises face a barrage of risks from multiple fronts. Externally, macro-economic shocks, strict regulatory updates (e.g., EU-GMP compliance), and supply chain disruptions constantly threaten stability. Internally, aging infrastructure and human skill gaps create operational bottlenecks. Left unchecked, these risks compound, leading to severe SLA penalties, loss of market share, and critical reputational damage.

The Chief Risk Officer (CRO) requires a holistic, bird's-eye view of the entire corporate risk landscape to effectively allocate the annual mitigation budget and prioritize interventions.

This project was initiated with a broad exploratory objective: to systematically map out Hataphar's entire risk portfolio using strategic business frameworks (PESTLE, 5 Forces, Value Chain). However, the ultimate goal was not just to list risks qualitatively, but to identify the most critical operational bottleneck that could be optimized using data-driven, quantitative simulation.

---

## 🛠️ Preparation <a name="preparation"></a>

To ensure the project aligns perfectly with business objectives rather than just being a coding exercise, I adopted a **Bottom-Up Approach**:

1. **Defining the Output First:** The end goal was clearly defined: a future risk forecast using Monte Carlo simulation, a machine age impact forecast (ML discovery), and a standardized Risk Heatmap to rank and prioritize risks.
2. **Strategic Data Collection:** Before writing any code, I conducted rigorous strategic data collection to build the Initial Risk Register. This involved:
   * **PESTLE Analysis:** To capture macro-environmental threats (Political, Economic, Social, Technological, Legal, Environmental).
   * **Porter’s 5 Forces:** To assess industry-level and market-driven risks.
   * **Value Chain Analysis:** To pinpoint internal vulnerabilities across primary and support activities. This systemic scan successfully highlighted the critical weakness in our Inbound Logistics and Operations, pointing directly to the Production Delay Risk.

---
## Implementation <a name="implementation"></a>

The project workflow is structured into 4 main phases based on modern ISO 31000 Risk Management standards, bridging qualitative strategy with quantitative Data Science.

![Risk Flow]([Ảnh màn hình 2026-02-15 lúc 09.56.45.png](https://github.com/pklinh29/Risk_Management_of_Hataphar_Project/blob/main/Ảnh%20màn%20hình%202026-02-15%20lúc%2009.56.45.png))
### Workflow Execution

#### Step 1: Identify Risks
Utilized strategic analysis tools to establish a **Comprehensive Risk Register**:
* **Organizational Fundamentals:** Reviewed Hataphar's Vision, Mission, and Core Values to align risk perspectives.
* **Risk Appetite:** Defined the enterprise's tolerance thresholds for various risk categories.
* **PESTLE & Porter's Five Forces:** Analyzed macro-environmental impacts and micro-level pharmaceutical industry dynamics.
* **Value Chain:** Mapped primary and support activities to pinpoint critical operational weaknesses.

#### Step 2: Analyze Risks and Select the Key Risk
This phase marks the transition from qualitative screening to quantitative deep dives:
* **Risk Scoping & Selection:** Filtered the comprehensive register down to **Critical Risks** via an Operational Drill-down. **OP1: Production Delay** was selected as the key quantitative target due to its high frequency and data availability.
* **Quantitative Risk Assessment (QRA):** The technical core of the project using Python:
  * *Historical Data Generation:* Processed and simulated historical manufacturing data using `NumPy` and `Pandas`.
  * *Machine Learning Root Cause Discovery:* Deployed `Scikit-Learn` (Regression) to mathematically discover the primary variables driving the delays (e.g., Machine Age, Worker Skill).
  * *Future Risk Simulation:* Ran a **Monte Carlo Simulation** (10,000 iterations) using `SciPy` and `NumPy` to forecast the precise probability of future SLA failures under an aging equipment scenario.

#### Step 3: Evaluate or Rank the Risk
* **Visualizing The Dashboard:** Translated the complex statistical outputs (like 1-CDF probabilities) into intuitive visual formats (`Matplotlib`/`Seaborn`). Plotted the dynamic quantitative risk alongside qualitative risks onto a unified Corporate Risk Heatmap to evaluate severity and likelihood.

#### Step 4: Treat or Address The Risk
Designed specific, actionable intervention measures:
* **Impact Assessment:** Evaluated the potential damage across financial, reputational, and operational dimensions.
* **Root Cause Analysis:** Utilized a Fishbone Diagram (4M/4P) to map out the exact origins of the bottlenecks.
* **Risk Treatment Plan (4T Strategy):**
  * **Tolerate:** Accept minor variances with buffer safety stocks.
  * **Terminate:** Refuse impossible deadlines exceeding current capacity.
  * **Transfer:** Outsource excess capacity to OEM (Original Equipment Manufacturer) partners during peak demand.
  * **Treat:** (Primary focus) Implement Predictive Maintenance and cross-training to directly mitigate the ML-discovered root causes.

#### Step 5: Monitor and Review The Risk
To ensure continuous improvement, the project established a post-treatment framework:
* **Monitor:** Designed a KRI (Key Risk Indicator) tracking mechanism focusing specifically on **Batch Release Time** on a daily and weekly basis.
* **Review:** Proposed a periodic evaluation system (running the simulation script every 6 months) to mathematically verify the effectiveness of the deployed solutions.

---
## Business Value Achievements <a name="business-value-achievements"></a>

This project delivers exactly what executive management expects from a robust Enterprise Risk Management (ERM) initiative:

1. **Holistic Portfolio Visibility:** The CRO receives a single, unified dashboard that seamlessly combines both qualitative strategic risks (Expert Judgment) and quantitative operational risks (AI Simulation), allowing for a complete view of the company's vulnerabilities.
2. **Eradicating "Gut-Feeling" Decisions:** Transitioned the core operational risk assessment from subjective guessing to a mathematically proven, data-driven approach. The root causes are backed by Regression Analysis, not assumptions.
3. **Optimized Capital Allocation (CapEx vs. OpEx):** By quantifying the exact impact of *Machine Age* vs. *Worker Skill*, the C-suite can mathematically justify whether to invest the annual budget in buying new machinery (CapEx) or funding intensive worker training programs (OpEx) to pull the risk back to the acceptable zone.
4. **Proactive Early Warning System:** The Monte Carlo simulation acts as a forward-looking radar, capturing the ~14% failure rate *before* the next fiscal year even starts, enabling proactive mitigation rather than reactive firefighting.

---

## Individual Achievements <a name="individual-achievements"></a>

Through the execution of this end-to-end project, I have developed a practical understanding of how data science can solve real-world operational challenges. Key takeaways include:

**1.Bridging Strategic Frameworks with Data Science:** Learned how to transition from high-level qualitative business analysis (PESTLE, Porter’s 5 Forces, Value Chain) into actionable quantitative models, realizing that data science is most powerful when guided by business context.

**2.Deepening Proficiency in Simulation & Machine Learning:** Gained hands-on experience in using Python libraries to decode operational bottlenecks:

  - Utilized NumPy and Pandas to process and simulate complex historical data environments.
  
  - Applied Scikit-Learn (Linear Regression) not just for basic forecasting, but specifically for Root Cause Discovery to identify hidden relationships between variables (e.g., Machine Age vs. Delay Time).
  
  - Employed SciPy and NumPy to run Monte Carlo simulations (10,000 iterations), shifting my analytical perspective from deterministic ("what happened") to probabilistic ("what is the likelihood of failure").

**3.Cultivating a Strong Risk Management Mindset**: Adopted the comprehensive ISO 31000 framework, understanding that Risk Management is an iterative cycle (Identify → Analyze → Evaluate → Treat → Monitor), rather than a one-time calculation.

**4.Refining Executive Communication via Data Visualization:** Improved my ability to translate complex statistical outputs (such as 1-CDF probabilities) into intuitive, standard corporate formats (1-5 Likert scales). I practiced using Matplotlib and Seaborn to design a unified Risk Portfolio Heatmap that communicates severity clearly to non-technical stakeholders (e.g., the C-suite).

---
