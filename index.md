---
title: "OPE Loss Categories — General Assembly Standard Families"
description: "Docs site index optimized for crawlers. Single-page version."
last_updated: "2025-10-24"
---

# OPE Loss Categories — General Assembly

Plain-text reference for **General Assembly OPE Losses (Standard Families)**.

## Canonical Definitions

**Energy / IT** — Losses due to energy utilities or IT systems provided by services external to the shop (Stellantis or external).  
**Missing Body** — No cars enter GA due to upstream shortage.  
**Missing Part — Supplier** — Parts not supplied on time by *external supplier*.  
**Missing Part — Internal Logistics** — Parts not supplied on time by *internal supply chain*.  
**Stops — Kitting** — Losses specifically due to the kitting process.  
**Stops — Production Line** — Manual/operational line stops.  
**Breakdown Time** — Equipment technical issues (breakdowns + micro-stops).  
**Saturation** — Downstream congestion blocks the line; nowhere to send vehicle/carrier.  
**Launching** — Losses related to car/equipment launch activities.  
**Product / Process (incl. short-shift)** — Short-shift conditions penalizing the plant for a short work week.

---

## Category Reference

### Energy / IT
- **Definition:** Energy or IT service failures external to the shop responsibility.  
- **Examples:** lack of electricity, compressed air, steam, cooling water; IT/MES outage impacting flow/quality/production level.

### Missing Body
- **Definition:** Cars lost at end of shop due to **lack of bodies** entering from upstream.  
- **Examples:** bodyshop or paintshop breakdown causing no incoming bodies.

### Missing Part — Supplier
- **Definition:** External supplier failed to deliver parts on time.  
- **Examples:** component shortage, late truck/delivery.

### Missing Part — Internal Logistics
- **Definition:** Internal supply chain failed to deliver parts on time.  
- **Examples:** line starved due to internal logistics; kits not delivered to point of use.

### Stops — Kitting
- **Definition:** Losses due to **kitting** process.  
- **Examples:** kit introduction/exit issues; kit AGV problem.

### Stops — Production Line
- **Definition:** Manual/operational stops of the line.  
- **Examples:** Andon, waiting operator, training stops; speed reduction due to absenteeism; backup operation; quality rework.

### Breakdown Time
- **Definition:** Equipment technical issues; breakdowns and micro-stops.  
- **Examples:** automatic screwing issues; sealing/gluing/glazing faults; AGV breakdowns; “marriage” station problems; any machine condition that meets downtime rules.

### Saturation
- **Definition:** Line blocked due to a **downstream** issue; no “place” to send carrier/vehicle to next step.  
- **Examples:** downstream saturation; carrier/hanger/trolley evacuation blocked.

### Launching
- **Definition:** Losses specific to **launch** of cars/equipment.  
- **Examples:** training, quality variation, bad part design; equipment fine-tuning; cycle-time issues; breakdowns during ramp.

### Product / Process (incl. short-shift)
- **Definition:** Any **short-shift** condition that penalizes the plant within the short work week boundary.  
- **Examples:** plant reduces runtime below short-week threshold; time is added to OPE but loss is categorized here.

---

## Synonyms

- **Energy / IT:** utilities outage, compressed air loss, cooling water loss, IT/MES outage, network down.  
- **Missing Body:** upstream shortage, no bodies from bodyshop/paintshop.  
- **Missing Part:** supplier shortage, internal logistics miss, line starvation.  
- **Stops:** Andon, waiting operator, training stop, backup mode, rework.  
- **Breakdown:** micro-stops, equipment failure, AGV fault, marriage-station issue.  
- **Saturation:** downstream block, carrier jam, evacuation issue.  
- **Launching:** SOP ramp, PPAP issues, fine-tuning, cycle-time tuning.  
- **Product / Process:** short-shift, short work week, planned runtime reduction.

---

## Machine-Readable JSON
```json
{
  "domain": "General Assembly",
  "version": "1.0",
  "standard_families": [
    {
      "slug": "energy-it",
      "name": "Energy / IT",
      "definition": "Energy or IT service failures supplied by services external to the shop.",
      "examples": ["Lack of electricity", "Loss of compressed air/steam/cooling water", "IT/MES outages impacting flow/quality"]
    },
    {
      "slug": "missing-body",
      "name": "Missing Body",
      "definition": "No bodies arriving from upstream shop causing end-of-shop car losses.",
      "examples": ["Paintshop/bodyshop breakdowns resulting in zero bodies"]
    },
    {
      "slug": "missing-part-supplier",
      "name": "Missing Part — Supplier",
      "definition": "External supplier fails to deliver parts on time.",
      "examples": ["Component shortage", "Late truck"]
    },
    {
      "slug": "missing-part-internal",
      "name": "Missing Part — Internal Logistics",
      "definition": "Internal supply chain fails to deliver parts on time.",
      "examples": ["Line starved by internal logistics", "Kitting not delivered to point of use"]
    },
    {
      "slug": "stops-kitting",
      "name": "Stops — Kitting",
      "definition": "Losses due to kitting process problems.",
      "examples": ["Kit introduction/exit issues", "Kit AGV problems"]
    },
    {
      "slug": "stops-production-line",
      "name": "Stops — Production Line",
      "definition": "Manual or operational stops of the production line.",
      "examples": ["Andon", "Waiting operator", "Training", "Backup operation", "Quality rework", "Speed reduction due to absenteeism"]
    },
    {
      "slug": "breakdown-time",
      "name": "Breakdown Time",
      "definition": "Equipment technical issues, including breakdowns and micro-stops.",
      "examples": ["Automatic screwing issues", "Sealing/gluing/glazing issues", "AGV breakdowns", "Marriage station issues"]
    },
    {
      "slug": "saturation",
      "name": "Saturation",
      "definition": "Downstream congestion blocking carrier/vehicle exit to next step.",
      "examples": ["Downstream saturation", "Carrier/hanger/trolley evacuation issue"]
    },
    {
      "slug": "launching",
      "name": "Launching",
      "definition": "Losses specific to new product/equipment launch.",
      "examples": ["Training", "Quality variation", "Bad design", "Fine tuning", "Cycle-time issues"]
    },
    {
      "slug": "product-process-shortshift",
      "name": "Product / Process (incl. short-shift)",
      "definition": "Short-shift conditions penalizing the plant for short work week.",
      "examples": ["Runtime reduced below short-week threshold; loss still counted in OPE"]
    }
  ]
}
```

