---
title: OPE Manual
description: Authoritative, crawl‑friendly reference for Copilot agents.
last_updated: 2025-10-24
permalink: /
---

# OPE Manual

> **TL;DR:** How to measure and improve **Overall Production Efficiency (OPE%)**: the ratio of **good units actually produced** to the **maximum potential units** (Gross JPH × Line running time). This guide standardizes data sources, accounting rules (pilots, short‑work‑week, cancellations, PM), and loss categories so every plant can diagnose bottlenecks and act consistently.

- **Key facts:**
  - **OPE% = Actual good units ÷ (Gross JPH × Line running time).**
  - **Units:** PC1/PFS at Flat Top/Framer/Sealer by center. **Runtime:** `JPH Runtime Validation.xlsx` (GA) or FIS scheduler (BIW/Paint). **Gross JPH:** measured by **IE** at the measurement point.
  - **Pilots not counted in PC1:** subtract **1 cycle at net JPH per pilot unit** from runtime.
  - **Short Work Week:** OPE uses **paid hours**; add **80% of the gap to 40h** (incl. paid 5‑min breaks/hour) when applicable.
  - **Cancelled before start:** exclude from OPE and **do not** treat as SWW. **Planned maintenance** can avoid SWW if strict criteria are met.
  - **Loss categories:** Energy/IT, Missing Body, Missing Part (Supplier/Internal), Stops—Kit, Stops—Line, Breakdown Time, Saturation, Product/Process (incl. launch/short‑week).
- **Scope:** GA / BIW / Paint; daily → weekly/monthly roll‑ups; US & Canada SWW rules noted.
- **Version:** v1.0 (imported from PDF; last_updated: 2025‑10‑24)

---

## Table of Contents
- [1) Why are we here?](#why-are-we-here)
- [2) OPE Loss Categories and Definitions](#ope-loss-categories-and-definitions)
  - [A. OPE Definition and Formula](#ope-definition-and-formula)
  - [B. OPE Loss Stratification](#ope-loss-stratification)
  - [C. OPE reporting process](#ope-reporting-process)
  - [D. Maintenance Domain Website](#maintenance-domain-website)
- [3) OPE Management Processes](#ope-management-processes)
  - [A. OPE Best Practices](#ope-best-practices)
  - [B. Orange Room Standard](#orange-room-standard)
  - [C. Breakdown Escalation Process](#breakdown-escalation-process)
  - [D. Top 20 Machine Process](#top-20-machine-process)
- [4) OPE Analysis Tools](#ope-analysis-tools)
  - [A. Factory Information Systems (FIS)](#factory-information-systems-fis)
  - [B. eWall (Bottleneck Identification)](#ewall-bottleneck-identification)
  - [C. Business Intelligence Applications (Data Mining)](#business-intelligence-applications-data-mining)
- [5) How to improve OPE by attacking loss scenarios](#how-to-improve-ope-by-attacking-loss-scenarios)
  - [A. Cycle Time](#cycle-time)
  - [B. Stops Production Line](#stops-production-line)
  - [C. Shift Specific Downtime](#shift-specific-downtime)
  - [D. Internal / External Material](#internal-external-material)
  - [E. Breakdown / Microstops](#breakdown-microstops)
  - [F. Reoccurring Issue](#reoccurring-issue)
  - [G. FIS Scheduler Issue](#fis-scheduler-issue)
  - [H. Shift Differential](#shift-differential)
  - [I. Data issue](#data-issue)

---

## 1) Why are we here? {#why-are-we-here}

### Overview
- This manual explains how to **understand, measure, and improve Overall Production Efficiency (OPE)** in each plant area.
- By identifying the main contributors that affect **OPE%**, teams can **prioritize limited resources** on problems with the largest impact.

### What is OPE?
- **Overall Production Efficiency (OPE)** is a **key performance indicator** that measures how effectively a plant uses resources to produce vehicles.
- **Meaning of OPE%:** the number of vehicles **actually produced** compared to the **maximum number** that could have been produced **without losses**. See the formal definition and formula in [§2A](#ope-definition-and-formula).
- Applying the OPE methodology strengthens **standard conformance**, supports **continuous improvement**, and ensures **best use of manpower and assets**.

### Why is a formal process needed?
- Ensures **consistent measurement** across all plants.
- Standardized metrics enable **accurate comparisons** and **faster anomaly detection**.
- Provides a **repeatable foundation** for targeted problem‑solving.

### Why stratify our losses into categories?
- Not all production losses are the same; each type needs a tailored approach. Grouping losses into clear categories enables teams to:
  - **Apply the right tools** to the right problems.
  - **Focus resources** where they matter most.
  - **Implement timely and permanent countermeasures**.
  - **Sustain efficient problem‑solving** over time.

### Why are E‑Wall and Business Intelligence applications needed?
- Effective OPE management requires **robust data analysis tools**.
- **E‑Wall:** enables drill‑down analysis to identify **shifting bottlenecks**; continuous monitoring **improves data accuracy**.
- **Business Intelligence applications:** provide data for rapid **root‑cause analysis**, **trend visualization**, and **shift‑to‑shift comparisons** that are not obvious by manual review.
- Together these tools **accelerate decision‑making** and **improve resource deployment**. Instead of reacting only to top losses, teams analyze data across systems to reveal **common root causes** and address multiple issues **proactively and in parallel**, driving **long‑term efficiency gains**.

### Key Outcomes {#why-outcomes}
- Shared purpose and common language for OPE across plants and centers.
- Clear link between OPE%, loss categories, and day‑to‑day actions.
- Data‑driven workflows (E‑Wall + BI) that surface bottlenecks and quantify impact.
- Repeatable processes that sustain improvements and reduce recurrence.
---

## 2) OPE Loss Categories and Definitions {#ope-loss-categories-and-definitions}

### A. OPE Definition and Formula {#ope-definition-and-formula}

**Overall Production Efficiency (OPE%)** is a KPI used to drive efficiency of manpower and asset utilization.

#### Formula
```
OPE% = (Actual number of good units produced) / (Maximum potential units)

Maximum potential units = Gross JPH at measurement point × Line running time
```

**Variable notes**
- **Gross JPH** = gross jobs per hour (line speed with no losses) at the defined measurement point.
- **Line running time** = available production time for the defined period (shift/day/week/month/year).

#### Worked Example
- Equipment capability: **100 JPH** (Gross JPH = 100).
- Planned production duration: **1 hour** (Line running time = 1 hour).
- **Maximum Achievable Production** = 100 JPH × 1 hour = **100 units**.
- Actual output in that hour: **80 units**.
- **OPE%** = 80 ÷ (100 × 1) = **0.80 = 80%**.

#### Scope and definitions
- **Actual good production units**: units produced during the defined time period **excluding scrap**. Units requiring rework **before moving to the next process step** are counted as good production.
- **Maximum potential units**: units that **could** be produced during the period **with no losses**. Computed as **gross line speed (units/hour) × line running time** for the chosen time base (shift/day/week/month/year).
- **Line running time**: the **available production time** of the area. **Planned stops** within scheduled production time (e.g., Planned TPM, social breaks, team briefings) are **deducted** from line running time. **Unplanned losses** (e.g., breakdowns, Andon, labor shortages, Covid cleaning, material shortages, blocked/starved by upstream or downstream processes) **remain within available time**—they do not reduce line running time and therefore reduce OPE when they lower actual output.

### B. OPE Loss Stratification {#ope-loss-stratification}

**General Assembly OPE Losses — Standard Families**

| Category | Definition (normalized) | Typical examples |
|---|---|---|
| **Energy / IT** {#loss-energy-it} | Losses due to utilities or IT services external to the shop (Stellantis services or external providers) that impact production capability. | Electricity, compressed air, steam, cooling water outages; MES/IT system failures affecting production management, flow, or quality; network/server incidents. |
| **Missing Body** {#loss-missing-body} | Car lost at end of shop due to lack of a body entering the shop from upstream. | Upstream paint shop or body shop breakdowns/starvation; no body on carrier at entry. |
| **Missing Part – Supplier** {#loss-missing-part-supplier} | Cars lost due to parts not supplied **in time** by an external supplier. | Component shortage, late truck/transport delays. |
| **Missing Part – Internal Logistics** {#loss-missing-part-internal} | Cars lost due to parts not supplied **in time** by the internal supply chain team. | Parts not delivered to line due to internal logistics issues (stores, lineside delivery). |
| **Stops – Production Kit** {#loss-stops-kit} | Losses specifically caused by kitting issues. | Problems introducing/removing kits; kits AGV issues; kit mismatch/availability. |
| **Stops – Production Line (Manual stop)** {#loss-stops-line} | Manual stop of the production line unrelated to equipment failure. | Andon/waiting operator stops; training stops; line speed reduction due to absenteeism; backup operation/mode; quality rework holds. |
| **Breakdown Time** {#loss-breakdown} | Stops due to equipment or technical issues, including **breakdowns and microstops**. | Machine/robot/PLC faults; automatic screwing/sealing/glazing/gluing issues; AGV breakdowns; “marriage” station issues. |
| **Saturation (Downstream blocked)** {#loss-saturation} | Line blocked by downstream area; no place to exit the car/carrier to the next step. | Downstream saturation; carrier/hanger/trolley evacuation jam or blockage. |
| **Product / Process (Launch & process changes)** {#loss-product-process} | Losses tied to vehicle/equipment/facility **launching** or process/product changes. | **Car launch:** stops due to training, quality, workstation issues, part design; **Equipment launch:** fine‑tuning, design issues, breakdowns, cycle‑time tuning. **Short‑week/short‑shift condition:** deliberate runtime reduction below short‑week threshold; time remains in OPE but loss is classified here. |

**One‑line category glossary (for search/aliases)**
- **Energy/IT:** utilities outage, power loss, compressed air, chilled water, MES/SCADA/network down.
- **Missing Body:** upstream starvation, no body at entry, bodyshop/paintshop down.
- **Missing Part – Supplier:** supplier shortage, late delivery, truck delay.
- **Missing Part – Internal:** internal logistics shortage, stores issue, lineside replenishment delay, kitting supply miss.
- **Stops – Kit:** kitting fault, kit AGV jam, kit not introduced/removed.
- **Stops – Line:** Andon/manual stop, training stop, speed reduction, backup mode, rework hold.
- **Breakdown Time:** BDT, equipment breakdown, microstop, machine fault, robot fault, PLC fault, marriage station.
- **Saturation:** downstream jam, accumulation full, unload blocked, no place available, trolley/hanger/carrier jam.
- **Product/Process:** launch ramp‑up, fine tuning, design change, process change, cycle‑time tuning, short‑week.

### C. OPE reporting process {#ope-reporting-process}

**System:** Qlik Sense — **App:** *JPH Trends* (daily OPE by plant and center).

#### Navigation & filters
- Use the sheet dropdown to switch views (e.g., **Overall Production Efficiency**, **OPE Tracker**, **OPE Range**, **VA**, **Lead Time Tracker**).
- Global filters (linked across sheets): **Year**, **Plant**, **Center**, **Month**, **Date**.  
  *Default Center:* **GA** (General Assembly).
- Filter selections persist when moving between sheets (e.g., selections in *Overall Production Efficiency* remain active in *OPE Tracker*).

#### Exporting data
1. Right‑click on a table or visualization.
2. Select **Export** → **Export data** to download the underlying table for the current selections.

#### Viewing details
- Click the **full‑screen** icon on any plant chart to view its **OPE Trend** in detail.
- Use the **full‑screen** icon on the detail table to open **OPE Detail Data** for the active filters.
- In **OPE Detail Data**, the **top bolded row** is the **actual OPE%** and input for the current filter context; the table lists **OPE by day** detail.

#### On‑screen formula (for reference)
- The Qlik sheet displays:  
  `Overall Production Efficiency % = PC1 Actual / (Runtime × Gross)`  
  This is equivalent to the formal definition in [§2A](#ope-definition-and-formula) when **PC1 Actual** equals the actual number of good units produced at the measurement point and **Gross** equals **Gross JPH**.

#### Source Data
**Units Produced**
- **GA:** PC1 database, measured at **Flat Top**.
- **BIW:** PFS database, measured at **Framer**.
- **Paint:** PFS database, measured at **Sealer**.

**Runtime**
- **GA:** `JPH Runtime Validation.xlsx` — runtime hours **entered by plants**.
- **BIW:** FIS at **Framer** based on **FIS scheduler**.
- **Paint:** FIS at **Sealer** based on **FIS scheduler**.

**Gross JPH** (measured by **Industrial Engineering (IE)**)
- **GA:** **Flat Top** gross JPH.
- **BIW:** **Framer** gross JPH.
- **Paint:** **Sealer** gross JPH.

**Governance note**
- To **change Gross JPH** used for OPE reporting, submit a **work order** to the **Throughput team** with **evidence that the rate has been validated by IE**.

#### Accounting rules & adjustments

##### Pilot units (do **not** count toward PC1) {#pilot-units-adjustment}
- Log pilot units on the **“GA Pilot Units Input Sheet”** in `JPH Runtime Validation.xlsx`.
- For **each pilot unit that does not count toward PC1**, **reduce runtime by one cycle** calculated at **net JPH** for the period.
- If pilot units **do** count toward PC1, **no action** is required.

**Formula**
```
runtime_adjustment_hours = pilot_units_not_counted / net_JPH
adjusted_runtime_hours   = original_runtime_hours - runtime_adjustment_hours
```

##### Short Shifting & Short Work Week (US/Canada) {#short-work-week}
- OPE uses **runtime based on paid hours**, **not** strictly hours worked.
- Under the 2023 UAW Automatic Short Week Benefit, when an eligible employee works **< 40 hours** in a week, they are paid **80% of the gap** between hours worked and **40 hours**.
- Paid breaks (e.g., **5 minutes per runtime hour**) are included in paid hours.

**Computation (weekly)**
Let `H_rt` = actual runtime hours; `b` = paid break minutes per hour ÷ 60 (typically **5/60**).
```
paid_hours_from_runtime = H_rt × (1 + b)
short_week_extra_paid   = 0.8 × max(0, 40 − paid_hours_from_runtime)
OPE_runtime_hours       = paid_hours_from_runtime + short_week_extra_paid
SWW_penalty_hours_for_OPE = short_week_extra_paid
```
- Apply the calculation at the **plant/week** aggregation used for OPE.
- Record resulting hours in `JPH Runtime Validation.xlsx` so they flow into Qlik Sense OPE reporting.

##### Cancelled shifts {#cancelled-shifts}
- If a shift is **cancelled before it starts**, **exclude** it from OPE calculation.
- **Do not** treat cancelled hours as part of **Short Work Week** calculations.  
  *Example:* If Mon–Wed run 8h, Thu short‑shifts by 2h, and Fri is cancelled, the SWW runtime adjustment is **80% of the 2h short‑shift only**, **not** 80% of the 10h gap to 40.

##### Planned Maintenance (avoiding runtime adjustment) {#planned-maintenance-adjustment}
Short‑shifting due to **planned maintenance (PM)** may **avoid** the SWW runtime adjustment **if all** of the following are met:
- Short‑shift occurs **at the end of the shift** (**PFS** must **not** show cars built during the short‑shift period).
- PM is **performed and bought‑off the same day** as the short‑shift.
- PM is **static** with a frequency **≥ monthly**.
- A **work order** is submitted to the **SPW Maintenance Domain** with details of completed PMs **and** a **screenshot** of the completed work including **trade comments**.
- The **work ticket** is submitted **during the same week** the short‑shift occurs, **before** reporting is published.
- **PM man‑hours** must **exceed** the **time short‑shifted**.
- **Launch pull‑ahead** work can also qualify **if documented** with a **WT in TMS**.

##### Other exclusions {#other-exclusions}
- **Make‑up shifts with PC1 plan = 0** are **excluded** from OPE.  
  For 3‑shift plants running a **Sunday make‑up shift**, the **first 4 hours of Monday (midnight shift)** are also excluded (PC1 system day rollover at **02:00**).
- **New product launch:** Plants in a **new launch** are **excluded from division OPE** for up to **3 months after Job 1**.

### D. Maintenance Domain Website {#maintenance-domain-website}
<!-- Provide URL, access, what to find there; summarize critical pages. -->

- _TBD_

---

## 3) OPE Management Processes {#ope-management-processes}

### A. OPE Best Practices {#ope-best-practices}
- _TBD_

### B. Orange Room Standard {#orange-room-standard}
- _TBD_

### C. Breakdown Escalation Process {#breakdown-escalation-process}
<!-- Use a decision tree expressed as bullets with IF/THEN and timing SLAs. -->
- _TBD_

### D. Top 20 Machine Process {#top-20-machine-process}
- _TBD_

---

## 4) OPE Analysis Tools {#ope-analysis-tools}

### A. Factory Information Systems (FIS) {#factory-information-systems-fis}
- _TBD_

### B. eWall (Bottleneck Identification) {#ewall-bottleneck-identification}
- _TBD_

### C. Business Intelligence Applications (Data Mining) {#business-intelligence-applications-data-mining}
- _TBD_

---

## 5) How to improve OPE by attacking loss scenarios {#how-to-improve-ope-by-attacking-loss-scenarios}

> Each scenario gets **Symptoms → Diagnosis → Actions → Owner → KPI impact**.

### A. Cycle Time {#cycle-time}
- _Symptoms:_ _TBD_
- _Diagnosis:_ _TBD_
- _Actions:_ _TBD_

### B. Stops Production Line {#stops-production-line}
- _Symptoms:_ _TBD_
- _Diagnosis:_ _TBD_
- _Actions:_ _TBD_

### C. Shift Specific Downtime {#shift-specific-downtime}
- _TBD_

### D. Internal / External Material {#internal-external-material}
- _TBD_

### E. Breakdown / Microstops {#breakdown-microstops}
- _TBD_

### F. Reoccurring Issue {#reoccurring-issue}
- _TBD_

### G. FIS Scheduler Issue {#fis-scheduler-issue}
- _TBD_

### H. Shift Differential {#shift-differential}
- _TBD_

### I. Data issue {#data-issue}
- _TBD_

---

## Glossary & Synonyms {#glossary}
<!-- Expand acronyms on first use and collect synonyms to aid retrieval. -->
- **OPE — Overall Production Efficiency:** _TBD official definition_

## FAQs {#faqs}
**Q:** What is the OPE formula?  
**A:** `OPE% = Actual good units produced ÷ (Gross JPH × Line running time)` where **Gross JPH** is the gross line speed at the measurement point and **Line running time** is available production time after deducting planned stops. See [§2A](#ope-definition-and-formula).

**Q:** What data sources feed OPE?  
**A:** **Units:** PC1/PFS by center (Flat Top/Framer/Sealer). **Runtime:** GA uses `JPH Runtime Validation.xlsx`; BIW/Paint use FIS scheduler. **Gross JPH:** measured by **IE** at the measurement point. See [Source Data](#ope-reporting-process).

**Q:** How do pilot units affect OPE?  
**A:** Pilot units **not counted in PC1** reduce runtime by **one net‑JPH cycle per pilot unit**; log them in the **GA Pilot Units Input Sheet** within `JPH Runtime Validation.xlsx`. See [§2C](#pilot-units-adjustment).

**Q:** How is Short Work Week applied?  
**A:** OPE uses **paid hours** (runtime × (1 + paid‑break factor)) plus **80% of the gap to 40 hours**. The added hours are the **SWW penalty hours for OPE**. See [§2C](#short-work-week).

**Q:** Are cancelled shifts included?  
**A:** If a shift is cancelled **before it starts**, it is **excluded** from OPE and **not** included in SWW. See [§2C](#cancelled-shifts).

**Q:** When can planned maintenance avoid SWW adjustment?  
**A:** Only when all criteria in [§2C](#planned-maintenance-adjustment) are met (end‑of‑shift, same‑day buy‑off, frequency ≥ monthly, WO + screenshots, submitted during the same week, PM man‑hours exceed short‑shift time; launch pull‑ahead with WT in TMS can qualify).

**Q:** What are the OPE loss categories?  
**A:** Energy/IT; Missing Body; Missing Part—Supplier; Missing Part—Internal Logistics; Stops—Production Kit; Stops—Production Line (manual); Breakdown Time (incl. microstops); Saturation; Product/Process (launch/short‑week). See [§2B](#ope-loss-stratification).

---

> Source PDF: `/assets/OPEManual.pdf` (to be added to the repo)

