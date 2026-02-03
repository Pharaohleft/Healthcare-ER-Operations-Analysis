# Healthcare-ER-Operations-Analysis

## 1. Executive Summary

### Purpose
Evaluate emergency room operational performance, patient flow, and service distribution for a single monthly snapshot.
Emergency departments operate under competing constraints: patient access, wait times, satisfaction, and admissions. While dashboards provide visibility into metrics, leadership decisions require structured evidence to determine:

- Whether performance is improving or deteriorating year-over-year
- Which metrics are structurally stable vs operationally volatile
- Whether monthly fluctuations meaningfully diverge from overall baselines

---

## Analytical Objective

Evaluate emergency room performance using a controlled, month-by-month analysis, then benchmark findings against a consolidated baseline — without inferring causality or introducing assumptions not supported by visible data.

### Scope & Data Context
- **Source:** Hospital Emergency Room Dashboard
- **View:** Monthly View
- **Filter state:** Month & Year = Jan 2024 (default selection as shown)
- All results are derived strictly from visible KPIs, tables, and charts in this view.

### Reader Orientation
This analysis is structured around a front-loaded “Questions Answered” section, allowing stakeholders to determine relevance before reviewing results.

---

## 2. Questions Answered (Questions Only)

- What was the total emergency room patient volume for the month?
- What was the average patient wait time?
- What level of patient satisfaction was recorded?
- How many patients were referred out of the emergency room?
- What proportion of patients were admitted versus not admitted?
- What percentage of patients were seen within the 30-minute target?
- How did patient volume vary by day of week and hour of day?
- Which age groups accounted for the highest number of visits?
- What was the gender distribution of patients?
- What were the most common department referral outcomes?
- How did patient volume vary by race category?

---

## 3. KPIs (Baseline — Default View)

| KPI | Value | Traceability |
|----|------|--------------|
| No. of Patients | 513 | KPI tile: “No. of Patients” |
| Avg. Wait Time | 36.3 minutes | KPI tile: “Avg. Wait Time” |
| Patient Satisfaction Score | 4.96 | KPI tile: “Patient Satisfaction Score” |
| No. of Patients Referred | Visible KPI tile (sparkline shown) | KPI tile: “No of Patients Referred” |
<img width="1188" height="721" alt="1" src="https://github.com/user-attachments/assets/2c7a6de4-01f7-435c-9927-408b2a1ab691" />
## Temporal Distribution — Day & Hour

- **Highest single day total:** Monday (95 patients)
- **Lowest single day total:** Friday (59 patients)

Hourly distribution shows visible variation across:
- Early morning (00–02 to 06–08)
- Midday (11–14)
- Evening (17–20)

**Source:** “No of Patients by Day & Hour” heatmap

---

## 5. Business Implications (Interpretation Only)

- Over half of emergency visits resulted in admission, indicating the ER is functioning as a significant intake channel rather than primarily a triage/filtering layer.

- With 38.4% of patients missing the 30-minute target, throughput constraints are present despite an average wait time of 36.3 minutes.

- Patient volume is not evenly distributed by day, with Mondays carrying materially higher load than Fridays, suggesting staffing and capacity planning implications.

- A large share of visits (289 patients) resulted in no department referral, indicating either resolution within ER or potential under-routing to downstream services.

- Patient demand spans age groups broadly, with no single age cohort dominating, reinforcing the need for generalist ER capability rather than age-specific optimization.
<img width="1178" height="715" alt="2" src="https://github.com/user-attachments/assets/6ce75040-ed4f-40be-b310-086036c8b42b" />

## Scope & Data Context

- **Source:** Hospital Emergency Room Dashboard
- **View:** Consolidated View
- **Date range:** 01/04/2023 to 30/10/2024 (as displayed on the dashboard)
- All results are derived strictly from visible KPIs, tables, and charts in this view.

Hourly heatmap shows consistently elevated volumes across:
- Morning (07–10)
- Afternoon (13–16)
- Evening (19–22)

**Source:** “No of Patients by Day & Hour” heatmap

---

## 5. Business Implications (Interpretation Only)

- Admission outcomes are nearly evenly split, indicating the ER functions both as an intake channel and a treatment-and-release environment across the consolidated period.

- Approximately 40% of patients miss the 30-minute target, suggesting persistent throughput constraints that are not isolated to short-term fluctuations.

- Patient volume is distributed relatively evenly across days of the week, with weekends showing comparable or higher demand than weekdays.

- A majority of visits (5,400 cases) result in no department referral, indicating substantial resolution within the ER itself.

- Age distribution is highly uniform across cohorts, implying demand is not concentrated in a narrow demographic segment.
## Scope & Data Context

- **Source:** Hospital Emergency Room Dashboard
- **View:** Consolidated View
- **Filter state:** date range 01/04/2023 → 30/10/2024 (top-right)
- **Outputs used:** KPI tiles + visible charts/tables on the consolidated page.

### Reference to Questions Answered
See the front-loaded Questions Answered section below.

---

## 2. Questions Answered (Questions Only)

- What was the total ER patient volume over the selected range?
- What was the average wait time over the selected range?
- What was the patient satisfaction score over the selected range?
- How many patients were referred over the selected range?
- What proportion of patients were admitted vs not admitted?
- How many patients met the 30-minute target vs missed it?
- What was total volume by day of week?
- What was total volume by age group?
- What was total volume by gender?
- What was total volume by department referral?
- What was total volume by race?
## Business Implications (Interpretation Only)

The consolidated baseline indicates near-even admission outcomes (~50/50) and a majority of patients within the 30-minute target (counts show 5K within target vs 4K missed).

The weekly pattern shows Saturday as the highest total-day volume among days shown.

Referrals are dominated by “None” and “General Practice” in absolute volume.

---

## Cross-Analysis Synthesis

*(Artifact 1: Monthly states captured) + (Artifact 2: Consolidated baseline)*

---

## A. Synthesis — Results Only

### A1) Same-month YoY KPI deltas (Monthly View)

Using the captured month pairs (Apr–Oct, 2023 vs 2024):

**Apr (2023 → 2024)**
- Patients: 479 → 469
- Avg wait: 34.9 → 35.0
- Satisfaction: 5.30 → 4.63
- Referred: 216 → 185
- Seen within 30 min (%): 56.99% → 57.14%
- Admitted (%): 49.48% → 46.27%

**May (2023 → 2024)**
- Patients: 480 → 519
- Avg wait: 34.4 → 35.8
- Satisfaction: 5.16 → 5.15
- Referred: 189 → 206
- Admitted (%): 47.71% → 51.25%

**Jun (2023 → 2024)**
- Patients: 506 → 485
- Avg wait: 35.6 → 35.5
- Satisfaction: 5.18 → 4.71
- Referred: 201 → 194
- Admitted (%): 49.80% → 48.45%

**Jul (2023 → 2024)**
- Patients: 464 → 488
- Avg wait: 34.7 → 35.2
- Satisfaction: 4.99 → 4.79
- Referred: 184 → 198
- Seen within 30 min (%): 57.54% → (percent not fully visible; count shown 288 / missed 200)
- Admitted (%): 50.86% → 54.51%

**Aug (2023 → 2024)**
- Patients: 494 → 530
- Avg wait: 36.4 → 35.1
- Satisfaction: 5.06 → 5.18
- Referred: 191 → 223
- Admitted (%): 47.37% → 45.66%

**Sep (2023 → 2024)**
- Patients: 469 → 466
- Avg wait: 34.3 → 35.1
- Satisfaction: 4.98 → 4.91
- Referred: 209 → 193
- Seen within 30 min (%): 54.8% → (percent not fully visible; count shown 278 / missed 188)
- Admitted (%): 53.09% → 50.64%

**Oct (2023 → 2024)**
- Patients: 493 → 471
- Avg wait: 34.9 → 34.1
- Satisfaction: 4.74 → 5.31
- Referred: 211 → 205
- Seen within 30 min (%): 57.0% → 55.63%
- Admitted (%): 48.48% → 52.44%

---

### A2) Consolidated baseline (for context)

- Total patients: 9,216
- Avg wait: 35.3 min
- Satisfaction: 4.99
- Referred: 3,816
- Admitted vs not admitted: 4,612 (50.04%) vs 4,604 (49.96%)
- 30-min target: Within target 5K vs Missed 4K (40.68%)
- Day totals highest among shown: Sat 1,377

*(All above are direct reads from Consolidated View visuals.)*

---

## B. Synthesis — Business Implications (Interpretation Only)

Across Apr–Oct YoY pairs, the 2024 months show mixed volume direction (e.g., May/Jul/Aug up YoY; Apr/Sep/Oct down YoY), indicating month-to-month variability rather than a uniform shift.

Patient satisfaction exhibits non-uniform YoY movement: notable decreases in Apr/Jun/Jul/Sep (within the captured set) and a notable increase in Oct.

Admission share crosses above/below 50% depending on month; this aligns with the Consolidated View showing admissions near parity (50.04% admitted overall).

For access performance, some months show exact target-hit rates (e.g., Apr 2024 = 57.14%, Oct 2024 = 55.63%) while some months only show counts clearly; the Consolidated View indicates more within-target counts (5K) than missed (4K), with missed explicitly 40.68%.
<img width="782" height="479" alt="image" src="https://github.com/user-attachments/assets/f0120b21-c91e-47e0-8c63-18247b0f9d23" />
## Key findings at a high level

- Patient volume exhibits month-specific volatility, not a uniform YoY trend.

- Admission rates remain structurally near parity (~50%), both monthly and in aggregate.

- Access performance (% seen within 30 minutes) improves in some YoY months but not consistently.

- Patient satisfaction shows non-linear behavior, declining in several mid-year months before rebounding sharply in Oct 2024.

- Consolidated averages mask meaningful month-level deviations observable only through controlled slicing.
## Results — Monthly YoY Evidence (Apr–Oct)

### 5.1 Directional Summary (YoY)

| Month | Patients | Avg Wait | Satisfaction | % ≤30 Min | Admitted % | Referrals |
|------|----------|----------|--------------|-----------|------------|-----------|
| Apr | ↓ | ↑ | ↓ | ↑ | ↓ | ↓ |
| May | ↑ | ↑ | → | — | ↑ | ↑ |
| Jun | ↓ | → | ↓ | → | ↓ | ↓ |
| Jul | ↑ | ↑ | ↓ | ↑ | ↑ | ↑ |
| Aug | ↑ | ↓ | ↑ | ↓ | ↓ | ↑ |
| Sep | ↓ | ↑ | ↓ | ↑ | ↓ | ↓ |
| Oct | ↓ | ↓ | ↑ | ↓ | ↑ |  |
## Key structural patterns

- Admissions consistently near 50%
- Majority of patients meet access target
- Saturday shows highest aggregate daily volume

---

## 7. Cross-Analysis Synthesis — Results Only

- Monthly patient volume fluctuates in both directions YoY, despite a stable consolidated total.
- Admission share oscillates monthly but converges near parity in aggregate.
- Satisfaction does not move linearly with wait time or access performance.
- Some months outperform consolidated averages while others materially underperform.

---

## 8. Business Implications (Interpretation Only)

- Monthly analysis is essential: consolidated averages obscure operational variability.
- Admission parity suggests system-level constraints, not month-specific anomalies.
- Access improvements are inconsistent, indicating localized operational effects rather than sustained improvement.
- Satisfaction rebounds in Oct 2024, signaling possible qualitative changes not observable in metrics alone.
## Key Areas of Insight and Evaluation

### Operational Volatility vs. Structural Stability

While consolidated metrics suggest stable performance, month-level analysis reveals significant volatility in patient volume, access performance, and satisfaction that is obscured by averages. This creates a false sense of operational control when viewed only at the aggregate level.

---

### Access Performance Inconsistency

Across same-month year-over-year comparisons, the percentage of patients seen within 30 minutes fluctuates meaningfully, with some months improving while others regress — despite similar average wait times. This highlights access performance as a localized operational issue, not a uniformly improving system metric.

---

### Admission Parity as a System Constraint

Admissions consistently hover near a 50/50 split across months and in the consolidated view, suggesting a structural capacity constraint rather than discretionary variation. Month-to-month swings rarely break this equilibrium, indicating limited elasticity in downstream flow.

---

### Satisfaction Non-Linearity

Patient satisfaction does not move in lockstep with wait time or access metrics. Several months show declining satisfaction despite stable or improving access performance, while others exhibit sharp satisfaction rebounds without corresponding wait time reductions — signaling qualitative factors not captured in standard KPIs.

---

### Temporal Pressure Points

Day-of-week and hour-of-day patterns reveal repeatable pressure points, particularly on weekends and specific weekday blocks, which are masked when viewed only through monthly totals. These patterns suggest opportunities for targeted operational adjustments rather than broad system changes.

## Key Metrics (KPIs)

- **Total ER Visits:** 9,216
- **Average Wait Time:** 35.3 minutes (consolidated)
- **Patients Seen ≤30 Minutes:** ~59–65% monthly range; **40.68% miss target**
- **Admission Rate:** ~50.04% (monthly range: 46%–54%)
- **Patient Satisfaction:** 4.63 (low) to 5.31 (high)

---

## Key Insights & Trends

### 1. Consolidated Averages Mask Operational Volatility
While aggregate metrics suggest stability, same-month year-over-year analysis shows meaningful swings in patient volume, access performance, and satisfaction. Several months diverge materially from the consolidated baseline, indicating that averages understate operational risk.

### 2. Access Performance Is Episodic, Not Improving
The share of patients seen within 30 minutes varies widely by month (≈54.8% to ≈65.7%) with no sustained upward trend across the period. Improvements occur in isolated months and reverse in others, undermining assumptions of steady access gains.

### 3. Admissions Are a Structural Constraint
Admission rates consistently cluster around 50% across months and in aggregate. Month-to-month movement is limited (±3–4 percentage points), signaling downstream capacity constraints rather than discretionary admission behavior.

### 4. Satisfaction Is Not Explained by Wait Time Alone
Comparable wait times produce sharply different satisfaction outcomes. For example, a <1-minute improvement in average wait coincides with a +0.57 increase in satisfaction between two observed months. This indicates non-quantified drivers of experience beyond throughput metrics.

### 5. Persistent Access Failures
Approximately 40.68% of patients miss the 30-minute target in the consolidated view. This miss rate persists even in lower-volume months, indicating a systemic access issue rather than a demand-driven one.

---

## Areas of Concern

- High and persistent access target miss rate (~2 in 5 patients)
- Volatile patient satisfaction, reducing reliability of experience outcomes
- Overreliance on consolidated KPIs, which obscure month-specific breakdowns
- Limited flexibility in admissions, constraining operational response

---

## Actionable Recommendations

### 1. Institutionalize Month-Level Performance Reviews
Require same-month YoY tracking for access and satisfaction to prevent consolidated averages from masking operational failures.

### 2. Broaden the Patient Experience Measurement Set
Supplement wait time with additional experience indicators (e.g., communication, handoffs, discharge clarity) to better explain satisfaction variability.

### 3. Target Access Interventions to Exception Months
Prioritize operational reviews for months where ≤30-minute performance falls below ~58%, treating these as exception states requiring focused remediation rather than normal variation.

---

## Bottom Line

The ER system is structurally constrained but operationally volatile. Leadership decisions based solely on consolidated dashboards risk underestimating access failures and misdiagnosing patient experience drivers. A shift to disciplined month-level monitoring is required to surface and address true performance gaps.
