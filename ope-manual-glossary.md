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