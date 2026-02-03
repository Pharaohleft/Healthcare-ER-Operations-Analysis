# Healthcare-ER-Operations-Analysis

## 1. Executive Summary

### Purpose
Evaluate emergency room operational performance, patient flow, and service distribution for a single monthly snapshot.
Emergency departments operate under competing constraints: patient access, wait times, satisfaction, and admissions. While dashboards provide visibility into metrics, leadership decisions require structured evidence to determine:

- Whether performance is improving or deteriorating year-over-year
- Which metrics are structurally stable vs operationally volatile
- Whether monthly fluctuations meaningfully diverge from overall baselines

---
# Problem Context (Non-Technical)

-- Emergency departments face competing pressures: access, satisfaction, throughput, and admissions.

-- Leadership needs to understand whether operational performance is improving or deteriorating year-over-year, and which months materially deviate from baseline.

-- Dashboards alone show what, but not structured evidence.

## Analytical Objective

Evaluate emergency room performance using a controlled, month-by-month analysis, then benchmark findings against a consolidated baseline — without inferring causality or introducing assumptions not supported by visible data.

Purpose
Establish an all-period baseline across the full selected range for volume, access, satisfaction, admissions, and patient mix.

See the front-loaded Questions Answered section below.

### Scope & Data Context
- **Source:** Hospital Emergency Room Dashboard
- **View:** Consolidated View
- **Filter state:** date range 01/04/2023 → 30/10/2024 (top-right)
- All results are derived strictly from visible KPIs, tables, and charts in this view.

---

## 2. Questions Answered 

- What was the average patient wait time?
- What level of patient satisfaction was recorded?
- What proportion of patients were admitted versus not admitted?
- What percentage of patients were seen within the 30-minute target?
- How did patient volume vary by day of week and hour of day?
- Which age groups accounted for the highest number of visits?

# . Problem Context & Analytical Objective

-- Emergency departments operate under competing constraints: patient access, wait times, satisfaction, and admissions. While dashboards provide visibility into metrics, leadership decisions require structured evidence to determine:

-- Whether performance is improving or deteriorating year-over-year

-- Which metrics are structurally stable vs operationally volatile

-- Whether monthly fluctuations meaningfully diverge from overall baselines

## Analytical Objective

-- Evaluate emergency room performance using a controlled, month-by-month analysis, then benchmark findings against a consolidated baseline — without inferring causality or introducing assumptions not supported by visible data.

# 2. Executive Summary

This analysis evaluates emergency room performance across individual monthly states (Apr–Oct, 2023 vs 2024) and a consolidated baseline (Apr 2023–Oct 2024).

-- Key findings at a high level:

-- Patient volume exhibits month-specific volatility, not a uniform YoY trend.

-- Admission rates remain structurally near parity (~50%), both monthly and in aggregate.

-- Access performance (% seen within 30 minutes) improves in some YoY months but not consistently.

-- Patient satisfaction shows non-linear behavior, declining in several mid-year months before rebounding sharply in Oct 2024.

-- Consolidated averages mask meaningful month-level deviations observable only through controlled slicing.

-- All conclusions are grounded strictly in visible dashboard outputs.

# 3. Questions Answered (Decision-Oriented)

-- Is emergency room volume increasing or decreasing year-over-year?

-- Are wait times improving consistently?

-- Does patient satisfaction trend align with access performance?

-- Is admission share structurally stable?

-- How much variability exists month to month versus the consolidated baseline?

-- Which months diverge meaningfully from the overall average?

-- Do operational patterns differ by age, gender, referral type, or race?

-- (Answers intentionally follow later; this section enables executive triage.)

# 4. Methodology & Analytical Controls

-- One slicer at a time: Month & Year only

-- All other filters fixed

-- Each month treated as a standalone analytical state

-- YoY comparisons restricted to same-calendar months

-- Consolidated View treated as a separate system

-- No row-level reconciliation

-- No inferred or estimated values

-- Results and implications explicitly separated

-- This structure mirrors consulting-style case rigor and production analytics workflows


---
<img width="1188" height="721" alt="1" src="https://github.com/user-attachments/assets/c199f624-542d-4cd5-87f9-f44f05cd4b84" />
-- Over half of emergency visits resulted in admission, indicating the ER is functioning as a significant intake channel rather than primarily a triage/filtering layer.

-- With 38.4% of patients missing the 30-minute target, throughput constraints are present despite an average wait time of 36.3 minutes.

-- Patient volume is not evenly distributed by day, with Mondays carrying materially higher load than Fridays, suggesting staffing and capacity planning implications.

-- A large share of visits (289 patients) resulted in no department referral, indicating either resolution within ER or potential under-routing to downstream services.

-- Patient demand spans age groups broadly, with no single age cohort dominating, reinforcing the need for generalist ER capability rather than age-specific optimization.

<img width="1178" height="715" alt="2" src="https://github.com/user-attachments/assets/80810afe-8b45-4682-a23a-225d46e04b0e" />
-- Admission outcomes are nearly evenly split, indicating the ER functions both as an intake channel and a treatment-and-release environment across the consolidated period.

-- Approximately 40% of patients miss the 30-minute target, suggesting persistent throughput constraints that are not isolated to short-term fluctuations.

-- Patient volume is distributed relatively evenly across days of the week, with weekends showing comparable or higher demand than weekdays.

-- A majority of visits (5,400 cases) result in no department referral, indicating substantial resolution within the ER itself.

-- Age distribution is highly uniform across cohorts, implying demand is not concentrated in a narrow demographic segment.

<img width="1182" height="714" alt="3" src="https://github.com/user-attachments/assets/e4a7f177-e7ca-4dcd-9755-aa2279bbe62d" />
Feb 2024 shows lower total patient volume than Jan 2024, alongside a slightly higher average wait time.

Despite longer waits on average, a higher proportion of patients met the 30-minute target.

Patient satisfaction declined relative to Jan 2024.

Admission share remained close to parity, with no structural shift in admit vs non-admit mix.

Referral volume decreased in line with lower overall patient volume.

<img width="1188" height="720" alt="4" src="https://github.com/user-attachments/assets/7b05b27b-1cbd-425e-84a0-74dc73158eb3" />

Apr 2023 shows lower patient volume and lower average wait time relative to the immediately prior captured state.

A smaller share of patients met the 30-minute target.

Admission outcomes remained near parity, with a slight tilt toward non-admission.

Referral volume increased despite lower overall patient volume.

Patient satisfaction remained above 5.0 but slightly below the prior captured state.

<img width="1182" height="720" alt="5" src="https://github.com/user-attachments/assets/a78be89c-c613-4acc-82c4-0d2f51f6832f" />
Sep 2023 shows lower patient volume and lower average wait time than the immediately prior captured state.

Patient satisfaction declined relative to the prior captured state.

A smaller share of patients met the 30-minute target.

Admission share increased above 50%.

Referral volume declined in absolute terms.

# KPIs (Baseline — Consolidated View)

KPI | Value | Traceability  
No. of Patients | 9,216 | KPI tile: “No. of Patients”  
Avg. Wait Time | 35.3 min | KPI tile: “Avg. Wait Time”  
Patient Satisfaction Score | 4.99 | KPI tile: “Patient Satisfaction Score”  
No of Patients Referred | 3,816 | KPI tile: “No of Patients Referred”  

# 4. Analysis — Results Only

## 4.1 Admission Outcomes

Admission Status | Patients | % of Total  
Admitted | 4,612 | 50.04%  
Not Admitted | 4,604 | 49.96%  

-- Source: Patient Admission Status table

## 4.2 Service Timeliness (30-Minute Target)

-- Target Missed: 4K (40.68%)

-- Within Target: 5K (percent not fully visible on the chart)

-- Source: “% of Patients Seen Within 30 Mins” donut chart
The consolidated baseline indicates near-even admission outcomes (~50/50) and a majority of patients within the 30-minute target (counts show 5K within target vs 4K missed).

The weekly pattern shows Saturday as the highest total-day volume among days shown.

Referrals are dominated by “None” and “General Practice” in absolute volume.

# Cross-Analysis Synthesis

(Artifact 1: Monthly states captured) + (Artifact 2: Consolidated baseline)

## A. Synthesis — Results Only

### A1) Same-month YoY KPI deltas (Monthly View)

Using the captured month pairs (Apr–Oct, 2023 vs 2024):

#### Apr (2023 → 2024)

-- Patients: 479 → 469  
-- Avg wait: 34.9 → 35.0  
-- Satisfaction: 5.30 → 4.63  
-- Referred: 216 → 185  
-- Seen within 30 min (%): 56.99% → 57.14%  
-- Admitted (%): 49.48% → 46.27%  

#### May (2023 → 2024)

-- Patients: 480 → 519  
-- Avg wait: 34.4 → 35.8  
-- Satisfaction: 5.16 → 5.15  
-- Referred: 189 → 206  
-- Admitted (%): 47.71% → 51.25%  

#### Jun (2023 → 2024)

-- Patients: 506 → 485  
-- Avg wait: 35.6 → 35.5  
-- Satisfaction: 5.18 → 4.71  
-- Referred: 201 → 194  
-- Admitted (%): 49.80% → 48.45%  

#### Jul (2023 → 2024)

-- Patients: 464 → 488  
-- Avg wait: 34.7 → 35.2  
-- Satisfaction: 4.99 → 4.79  
-- Referred: 184 → 198  
-- Seen within 30 min (%): 57.54% → (percent not fully visible; count shown 288 / missed 200)  
-- Admitted (%): 50.86% → 54.51%  

#### Aug (2023 → 2024)

-- Patients: 494 → 530  
-- Avg wait: 36.4 → 35.1  
-- Satisfaction: 5.06 → 5.18  
-- Referred: 191 → 223  
-- Admitted (%): 47.37% → 45.66%  

#### Sep (2023 → 2024)

-- Patients: 469 → 466  
-- Avg wait: 34.3 → 35.1  
-- Satisfaction: 4.98 → 4.91  
-- Referred: 209 → 193  
-- Seen within 30 min (%): 54.8% → (percent not fully visible; count shown 278 / missed 188)  
-- Admitted (%): 53.09% → 50.64%  

#### Oct (2023 → 2024)

-- Patients: 493 → 471  
-- Avg wait: 34.9 → 34.1  
-- Satisfaction: 4.74 → 5.31  
-- Referred: 211 → 205  
-- Seen within 30 min (%): 57.0% → 55.63%  
-- Admitted (%): 48.48% → 52.44%  

### A2) Consolidated baseline (for context)

-- Total patients: 9,216  
-- Avg wait: 35.3 min  
-- Satisfaction: 4.99  
-- Referred: 3,816  
-- Admitted vs not admitted: 4,612 (50.04%) vs 4,604 (49.96%)  
-- 30-min target: Within target 5K vs Missed 4K (40.68%)  
-- Day totals highest among shown: Sat 1,377  

-- (All above are direct reads from Consolidated View visuals.)

## B. Synthesis — Business Implications (Interpretation Only)

-- Across Apr–Oct YoY pairs, the 2024 months show mixed volume direction (e.g., May/Jul/Aug up YoY; Apr/Sep/Oct down YoY), indicating month-to-month variability rather than a uniform shift.

-- Patient satisfaction exhibits non-uniform YoY movement: notable decreases in Apr/Jun/Jul/Sep (within the captured set) and a notable increase in Oct.

-- Admission share crosses above/below 50% depending on month; this aligns with the Consolidated View showing admissions near parity (50.04% admitted overall).

-- For access performance, some months show exact target-hit rates (e.g., Apr 2024 = 57.14%, Oct 2024 = 55.63%) while some months only show counts clearly; the Consolidated View indicates more within-target counts (5K) than missed (4K), with missed explicitly 40.68%.

# Results — Monthly YoY Evidence (Apr–Oct)

## 5.1 Directional Summary (YoY)

Month | Patients | Avg Wait | Satisfaction | % ≤30 Min | Admitted % | Referrals  
Apr | ↓ | ↑ | ↓ | ↑ | ↓ | ↓  
May | ↑ | ↑ | → | — | ↑ | ↑  
Jun | ↓ | → | ↓ | → | ↓ | ↓  
Jul | ↑ | ↑ | ↓ | ↑ | ↑ | ↑  
Aug | ↑ | ↓ | ↑ | ↓ | ↓ | ↑  
Sep | ↓ | ↑ | ↓ | ↑ | ↓ | ↓  
Oct | ↓ | ↓ | ↑ | ↓ | ↑ | ↓  

-- (Arrows indicate direction only; values traceable to monthly artifacts.)

# 6. Results — Consolidated Baseline (Apr 2023–Oct 2024)

-- Total patients: 9,216

-- Avg wait time: 35.3 minutes

-- Patient satisfaction: 4.99

-- Admitted: 4,612 (50.04%)

-- Not admitted: 4,604 (49.96%)

-- Within 30 min: ~5K

-- Missed target: ~4K (40.68%)

## Key structural patterns:

-- Admissions consistently near 50%

-- Majority of patients meet access target

-- Saturday shows highest aggregate daily volume

# 7. Cross-Analysis Synthesis — Results Only

-- Monthly patient volume fluctuates in both directions YoY, despite a stable consolidated total.

-- Admission share oscillates monthly but converges near parity in aggregate.

-- Satisfaction does not move linearly with wait time or access performance.

-- Some months outperform consolidated averages while others materially underperform.

# 8. Business Implications (Interpretation Only)

-- Monthly analysis is essential: consolidated averages obscure operational variability.

-- Admission parity suggests system-level constraints, not month-specific anomalies.

-- Access improvements are inconsistent, indicating localized operational effects rather than sustained improvement.

-- Satisfaction rebounds in Oct 2024, signaling possible qualitative changes not observable in metrics alone.

-- These implications are bounded strictly by observed evidence.

# 9. Limitations & Explicit Non-Claims

-- This analysis does not:

-- Infer causality between wait time and satisfaction

-- Assume staffing, acuity, or seasonality effects

-- Recommend operational interventions

-- Perform patient-level reconciliation

-- Replace clinical or operational review


## Bottom Line

The ER system is structurally constrained but operationally volatile. Leadership decisions based solely on consolidated dashboards risk underestimating access failures and misdiagnosing patient experience drivers. A shift to disciplined month-level monitoring is required to surface and address true performance gaps.
