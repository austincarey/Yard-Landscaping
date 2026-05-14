---
Created: "2026-04-25"
tags: [landscaping, irrigation, rachio, planning]
---

# Irrigation Plan (Rachio Controller)

**System Overview:** Rachio Smart Controller (12 Zones)
**Soil Type:** Clay (Standard for Colorado - requires Cycle & Soak)

This document serves as the master configuration and planning guide for the yard's irrigation system. It will be updated once the precipitation rates (inches/hour) for each zone are measured (e.g., via a catch-cup test).

---

## 📅 Watering Philosophy (Colorado Climate)
1. **Deep and Infrequent:** The goal is to water deeply to encourage deep root growth, then let the soil dry out slightly before watering again. Shallow, daily watering creates weak roots.
2. **Cycle and Soak:** Because Colorado clay soil absorbs water slowly, Rachio's "Smart Cycle" is essential. It breaks a long watering cycle into smaller chunks (e.g., 3 cycles of 5 minutes instead of 1 cycle of 15 minutes) to prevent runoff.
3. **Hydrozoning:** Keep plants with similar water needs in the same zone. Do not mix turf grass with drought-tolerant native shrubs.

---

## 💧 Zone Configuration Matrix

*To be filled out once precipitation rate data is collected.*

| Zone | Area / Name | Sprinkler Type | Plant Type | Exposure (Sun/Shade) | Precip Rate (in/hr) | Target Duration (Mins) | Frequency |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | Front Parkway | Rotary | Lawn (Cool Season) | Full Sun | *TBD* | *TBD* | *TBD* |
| **2** | Front Lawn | Rotary | Lawn (Cool Season) | Full Sun | *TBD* | *TBD* | *TBD* |
| **3** | Front Planters | Drip | Perennials/Shrubs | Part Shade | *TBD* | *TBD* | *TBD* |
| **4** | West Planters | Drip | Shrubs/Vines | Afternoon Sun | *TBD* | *TBD* | *TBD* |
| **5** | Backyard Lawn 1 | Rotary | Lawn (Cool Season) | Full Sun | *TBD* | *TBD* | *TBD* |
| **6** | Backyard Lawn 2 | Rotary | Lawn (Cool Season) | Full Sun | *TBD* | *TBD* | *TBD* |
| **7** | Backyard Shrubs | Drip | Shrubs | Full Sun | *TBD* | *TBD* | *TBD* |
| **8** | Backyard Planter | Drip | Perennials/Shrubs | Part Shade | *TBD* | *TBD* | *TBD* |
| **9** | Wildflower Garden | Drip/Micro | Native Perennials | Full Sun | *TBD* | *TBD* | *TBD* |
| **10** | Vegetable Patch | Drip | Annual Crops | Full Sun | *TBD* | *TBD* | *TBD* |
| **11** | Trees (Drip Line) | Drip/Bubbler | Mature Trees | Sun/Shade | *TBD* | *TBD* | *TBD* |
| **12** | *Open/Unassigned* | *TBD* | *TBD* | *TBD* | *TBD* | *TBD* | *TBD* |

---

## 🧮 Calculating Duration and Frequency

Once you have your `in/hr` data for a zone, you can calculate your watering duration based on the plant's seasonal needs.

### 1. Cool Season Grass (Kentucky Bluegrass/Tall Fescue)
- **Target:** 1.5 to 2.0 inches of water per week during peak summer heat (July/August). 1.0 inch per week in spring/fall.
- **Frequency Goal:** 2 to 3 days per week (e.g., Sunday, Wednesday, Friday).
- **Calculation Example:** If a rotary zone outputs **0.5 in/hr**, and you need **1.5 inches a week** divided across **3 days**:
  - You need 0.5 inches *per watering event*.
  - At 0.5 in/hr, it takes **60 minutes** to drop 0.5 inches of water.
  - *Rachio will break this 60 minutes into multiple smaller "Cycle and Soak" intervals.*

### 2. Drip Systems (Shrubs, Perennials, Wildflowers)
- **Target:** Varies heavily by plant. Native wildflowers may only need watering once a week or every two weeks. Vegetable patches may need it every 1-2 days.
- **Frequency Goal:** Water deeply to penetrate 8-12 inches into the soil.
- **Drip Emitters:** Usually measured in Gallons Per Hour (GPH). Emitters must run significantly longer than rotary sprinklers to drop the same volume of water (often 30-60+ minutes per cycle depending on the GPH).

---

## ⚙️ Rachio Schedule Types
*Recommendations for configuring the app:*

- **Flex Daily (Recommended for Drip & Established Turf):** The controller uses localized weather data and soil moisture tracking to only water when the zone's "bucket" is empty. It automatically adjusts frequency based on rain and heat. *Requires highly accurate inputs for soil type and precip rate.*
- **Flex Monthly (Good for New Plantings/Vegetables):** Adjusts the duration and frequency every month based on historical averages, but keeps the schedule predictable.
- **Fixed (Good for Seeds/Pre-emergent):** Waters exactly when you tell it to. Use this when laying new grass seed or immediately after applying fertilizer/weed control.
