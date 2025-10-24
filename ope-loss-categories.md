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

### Notes
- This is a faithful, manual transcription meant for indexing. If you have the original text source, replace/append for 100% fidelity.
- Keep file name stable for agents: `ope-loss-categories.md`.
