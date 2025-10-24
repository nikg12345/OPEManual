---
title: OPE Manual Glossary (Pages 1–10)
description: Definitions, formulas, and reporting rules distilled from the OPE Process Manual, pages 1–10.
---

# OPE Manual — Glossary & Rules (pp. 1–10)

> This page condenses the first 10 pages of the **OPE Process Manual** into an indexed glossary with short, precise definitions and the key reporting rules. Use the search in your browser (Ctrl/Cmd+F) or the links below.

## Contents
- [Overall Production Efficiency (OPE)](#overall-production-efficiency-ope)
- [Formula & Worked Example](#formula--worked-example)
- [Key Terms](#key-terms)
- [Scope Clarifications](#scope-clarifications)
- [Reporting Process (What sources to use)](#reporting-process-what-sources-to-use)
- [Special Rules](#special-rules)
- [Acronyms (quick pick)](#acronyms-quick-pick)

---

## Overall Production Efficiency (OPE)

**Definition.** A Stellantis KPI that measures **how effectively a plant converts available runtime and line capacity into actual good units**. In short: *actual good units* ÷ *maximum potential units* for a defined period (shift/day/week/month/year).

**Intent.** Provide a consistent measure to compare performance across plants/centers, strengthen standard conformance, and focus problem‑solving on the largest losses.

---

## Formula & Worked Example

**Core formula**

\[ OPE\% = \frac{\text{Actual good units}}{\text{Gross JPH} \times \text{Runtime (hours)}} \times 100 \]

**Example (manual p.5):** If Gross JPH = 100 and planned Runtime = 1 hour (so **Maximum Achievable Production** = 100 units) and **Actual good units** = 80, then **OPE% = 80 / 100 = 80%**.

---

## Key Terms

### Gross JPH
Line’s **gross design speed** in Jobs Per Hour for the measurement point (per IE). Used to compute maximum potential units.

### Runtime (Line running time)
**Available production time** during the defined period. Time lost to breakdowns, operational issues (e.g., Andon, labor shortages), material shortages, or blocked/starved conditions **still counts as available runtime**. **Planned stops** (e.g., planned TPM, social breaks, team briefings) are **deducted** from runtime.

### Maximum Achievable Production
The theoretical units that could be built with **no losses** during the period: **Gross JPH × Runtime (hours)**.

### Actual good units
Units produced during the period **excluding scrap**. Units needing rework **before** moving to the next process **still count as good**.

---

## Scope Clarifications

- **Timebase:** OPE can be computed at shift, day, week, month, or year granularity, but the **measurement point’s** gross JPH and runtime must match that period.
- **Measurement point by Center (examples from pp. 8–9):**
  - **GA:** Units from **PC1** at **Flat Top**; runtime from **“JPH Runtime Validation.xlsx”** (plant-entered).
  - **BIW:** Units from **PFS** at **Framer**; runtime from **FIS scheduler** (Framer).
  - **Paint:** Units from **PFS** at **Sealer**; runtime from **FIS scheduler** (Sealer).
- **Gross JPH ownership:** Measured/validated by **Industrial Engineering (IE)** for each center’s measurement point. Rate changes for OPE reporting require a **Throughput work order** with IE validation evidence.

> Note: The specific SharePoint/Qlik links referenced in the manual require internal access. Keep the business logic here independent of those URLs so your public site remains accessible.

---

## Reporting Process (What sources to use)

When assembling weekly/monthly OPE for a plant/center, use the following inputs:

**Units Produced**
- GA: **PC1** at Flat Top
- BIW: **PFS** at Framer
- Paint: **PFS** at Sealer

**Runtime**
- GA: **“JPH Runtime Validation.xlsx”** (plant‑entered hours)
- BIW: **FIS scheduler** at Framer
- Paint: **FIS scheduler** at Sealer

**Gross JPH**
- GA/BIW/Paint: **Measured by IE** at the respective measurement points

---

## Special Rules

### Pilot units (p.9)
- **Pilot units not counted in PC1**: For each such pilot built, **reduce runtime** by **one cycle at Net JPH**. Pilots that **do** count toward PC1: **no adjustment**.

### Short shifting & short work week (p.9)
- OPE **uses paid hours** for runtime (per labor agreements). **Adjust runtime up** by **80% of the gap** between paid hours and hours worked when employees work < 40 hours (US/Canada), **unless** short‑shifting is due to **Planned Maintenance** (see below).

### Canceled shifts (p.10)
- Shifts canceled **before** they start are **excluded** from OPE (no runtime). Example: If Friday is canceled, there’s **no** short‑work‑week runtime adjustment for that day.

### Planned Maintenance exemption (p.10)
To **avoid** the short‑work‑week runtime uplift, the maintenance must:
1) Occur at **end of shift** (no cars built during the PM window in PFS),
2) Be **static and ≥ monthly** frequency, completed and **bought‑off the same day**,
3) Have a **work order** submitted to the SPW Maintenance Domain **that week** with evidence/comments,
4) **PM man‑hours exceed** the time short‑shifted.  
Launch pull‑ahead work can also qualify when documented with a **WT** in TMS.

### Other exclusions (p.10)
- **Make‑up only shifts** with **PC1 plan = 0** are **excluded**.
- For **3‑shift** plants running a make‑up shift on **Sunday**, the **first 4 hours of Monday midnight shift** are excluded (PC1 day boundary at 2 a.m.).
- **New product launch**: Plants can be **excluded from division OPE** for up to **3 months after Job 1**.

---

## Acronyms (quick pick)

**BIW** (Body in White), **FIS** (Factory Information System), **GA** (General Assembly), **IE** (Industrial Engineering), **JPH** (Jobs per Hour), **KPI** (Key Performance Indicator), **OPE** (Overall Production Efficiency), **PC1** (Production count database), **PFS** (Production tracking DB), **PM** (Planned Maintenance), **TMS** (Ticketing/maintenance system), **WT** (Work Ticket).

> For the full acronym list, see Appendix A of the manual.

---

## Provenance

This page summarizes **pages 1–10** of the OPE Process Manual provided by the requester. It is intended to be a concise, public, crawl‑friendly reference for Copilot Studio.

---
title: "OPE Loss Categories — General Assembly Standard Families"
description: "Plain‑text reference for OPE loss categories with short definitions and examples, transcribed from slide. Optimized for retrieval agents and web crawling."
tags: [OPE, losses, manufacturing, general-assembly, downtime, categories, definitions]
last_updated: "2025-10-24"
---

# OPE Loss Categories (General Assembly)

Authoritative, crawlable reference of **General Assembly OPE Losses — Standard Families**.  
Each section includes a precise definition and short, bullet examples.

> Source: Transcribed from the provided 'OPE Loss Categories' slide (Stellantis branding).

---

## Quick Index

- [Energy / IT](#energy--it)
- [Missing Body](#missing-body)
- [Missing Part — Supplier](#missing-part--supplier)
- [Missing Part — Internal Logistics](#missing-part--internal-logistics)
- [Stops — Kitting](#stops--kitting)
- [Stops — Production Line](#stops--production-line)
- [Breakdown Time](#breakdown-time)
- [Saturation](#saturation)
- [Launching](#launching)
- [Product / Process (incl. short‑shift)](#product--process-incl-shortshift)

---

## Normalized Table

| Category | Definition (short) | Example cues |
|---|---|---|
| **Energy / IT** | Losses caused by energy utilities or IT systems under services external to the shop. | Lack of electricity, compressed air, steam, cooling water; IT system outages affecting production flow/quality. |
| **Missing Body** | No car enters GA due to upstream shortage. | Upstream bodyshop/paintshop breakdown leading to no bodies. |
| **Missing Part — Supplier** | Parts not supplied on time by external supplier. | Component shortage, late truck. |
| **Missing Part — Internal Logistics** | Parts not supplied on time by internal supply chain team. | Line starved due to internal logistics issue. |
| **Stops — Kitting** | Losses specifically due to kitting process. | Kit introduction/exit issues; AGV for kits causing misses. |
| **Stops — Production Line** | Manual/operational stops of the line. | Andon, waiting operator, training stops, backup/quality rework; speed reductions due to absenteeism. |
| **Breakdown Time** | Equipment technical issues (breakdowns + micro‑stops). | Automatic screwing, sealing/gluing issues, AGV breakdowns, “marriage” station issues. |
| **Saturation** | Downstream congestion blocks the line (no place to send vehicle/carrier). | Carrier/hanger/trolley evacuation blocked; downstream station saturated. |
| **Launching** | Losses specific to new product/equipment launch activities. | Training, quality variation, bad part design; fine‑tuning, cycle‑time issues during equipment launch. |
| **Product / Process (incl. short‑shift)** | Any short‑shift condition penalizing the plant within the short‑work‑week boundary. | Plant reduces runtime below short‑week threshold; loss counted in OPE but categorized here. |

---

## Energy / IT
**Definition.** Energy breakdowns supplied by services external to the shop (STELLANTIS or external company). IT failures under responsibility of services external to the shop.  
**Examples.**
- Lack of electricity, compressed air, steam, cooling water.
- Lack of IT systems for production management/flow/quality affecting production level.

---

## Missing Body
**Definition.** Cars lost at the end of the shop due to lack of cars entering GA from the upstream shop.  
**Examples.**
- Shortage due to breakdown in paintshop or bodyshop.

---

## Missing Part — Supplier
**Definition.** Cars lost at the end of the shop due to parts not supplied in time **by supplier**.  
**Examples.**
- Lack of component, late truck/delivery.

---

## Missing Part — Internal Logistics
**Definition.** Cars lost at the end of the shop due to parts not supplied in time **by internal supply chain/logistics**.  
**Examples.**
- Kits/parts not delivered to line on time due to internal logistics issue.

---

## Stops — Kitting
**Definition.** Specific focus on losses due to **kitting**.  
**Examples.**
- Issues introducing or exiting kits from the line.
- Cars lost due to **kit AGV** problems.

---

## Stops — Production Line
**Definition.** Manual/operational stops of the production line.  
**Examples.**
- **Andon** stops; waiting-operator stops; training stops.
- Reduced line speed due to **absenteeism**.
- Stops due to **backup operation / backup mode**.
- **Quality rework** impacts.

---

## Breakdown Time
**Definition.** Stops due to equipment technical issues, including **breakdowns and micro‑stops**.  
**Examples.**
- Equipment breakdowns (e.g., automatic screwing).
- Sealing/gluing/glazing issues.
- **AGV** breakdowns.
- “**Marriage**” station issues.
- Machine conditions causing downtime regardless of whether they exceed a threshold.

---

## Saturation
**Definition.** Line blocked due to a **downstream** area issue (no place to send the car/carrier to next step).  
**Examples.**
- Downstream saturation.
- Carrier/hanger/trolley **evacuation** blocked.

---

## Launching
**Definition.** Losses specific to **launch** of cars/equipment.  
**Examples.**
- **Car launching:** training, quality variation, bad part design.
- **Equipment launching:** fine tuning, bad design, breakdowns, **cycle time** issues.

---

## Product / Process (incl. short‑shift)
**Definition.** Any **short‑shift** condition that penalizes the plant for a short work week.  
**Examples.**
- Plant decides to reduce runtime below the **short‑work‑week** threshold; the short‑week time is included in OPE but categorized here.

---

## Synonyms & Search Hints (for retrieval)
- **Energy / IT:** utilities outage, compressed air, steam, cooling water, IT downtime, MES outage.
- **Missing Body:** upstream shortage, no-bodies, bodyshop/paintshop gap.
- **Missing Part:** supplier shortage, internal logistics miss, kitting starvation.
- **Stops:** andon, waiting operator, training stop, backup mode, rework.
- **Breakdown:** micro-stops, equipment failure, AGV fault, marriage station.
- **Saturation:** downstream block, carrier jam, evacuation issue.
- **Launching:** SOP ramp, PPAP issues, fine-tuning, cycle-time.
- **Product / Process:** short-shift, short work week, planned runtime reduction.

---

## Machine‑Readable (JSON)
```json
{
  "domain": "General Assembly",
  "standard_families": [
    {
      "category": "Energy / IT",
      "definition": "Energy or IT service failures supplied by services external to the shop.",
      "examples": ["Lack of electricity", "Lack of compressed air/steam/cooling water", "IT outages impacting flow/quality"]
    },
    {
      "category": "Missing Body",
      "definition": "No bodies arriving from upstream shop causing end-of-shop car losses.",
      "examples": ["Paintshop/bodyshop breakdowns leading to zero bodies"]
    },
    {
      "category": "Missing Part — Supplier",
      "definition": "External supplier fails to deliver parts on time.",
      "examples": ["Component shortage", "Late truck"]
    },
    {
      "category": "Missing Part — Internal Logistics",
      "definition": "Internal supply chain fails to deliver parts on time.",
      "examples": ["Line starved by internal logistics", "Kitting not delivered"]
    },
    {
      "category": "Stops — Kitting",
      "definition": "Losses due to kitting process problems.",
      "examples": ["Kit introduction/exit issues", "Kit AGV problems"]
    },
    {
      "category": "Stops — Production Line",
      "definition": "Manual or operational stops of the production line.",
      "examples": ["Andon", "Waiting operator", "Training", "Backup mode", "Quality rework", "Speed reduction due to absenteeism"]
    },
    {
      "category": "Breakdown Time",
      "definition": "Equipment technical issues, including breakdowns and micro-stops.",
      "examples": ["Automatic screwing issues", "Sealing/gluing/glazing issues", "AGV breakdowns", "Marriage station issues"]
    },
    {
      "category": "Saturation",
      "definition": "Downstream congestion blocking carrier/vehicle exit to next step.",
      "examples": ["Downstream saturation", "Carrier/hanger/trolley evacuation issue"]
    },
    {
      "category": "Launching",
      "definition": "Losses specific to new product/equipment launch.",
      "examples": ["Training", "Quality variation", "Bad design", "Fine tuning", "Cycle-time issues"]
    },
    {
      "category": "Product / Process (incl. short-shift)",
      "definition": "Short-shift conditions penalizing the plant for short work week.",
      "examples": ["Runtime reduced below short-week threshold; loss still counted in OPE"]
    }
  ]
}
```

---
