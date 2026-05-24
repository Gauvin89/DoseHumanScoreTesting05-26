# Dose Human Score — Testing 05-26

Anonymized demo of the **Human Score** concept (0–100 composite across 6 tiers / 18 health dimensions) applied to live remote-patient-monitoring data.

Modeled on the [DoctorBodyguard](https://doctorbodyguard-v3.vercel.app/) "Your Human Score" framework — a single number summarizing every connected health signal, with a complementary Data Ensemble Score for source completeness.

## What's in this demo

A single self-contained HTML page (`raegen_deep_dive.html`) showing how the Human Score model surfaces clinical and behavioral insights from one anonymized patient's data:

1. **Daily Activity Log** — 20-day unified view (dispense time + adherence state + sleep + steps + HR + SpO2 per row)
2. **Day-by-Day Pattern Summary** — 5 derived behavioral patterns with proposed clinical alerting rules
3. **Cardiac & Respiratory Findings** — HR by hour of day, BP trend, SpO2 desaturation events
4. **Data Inventory** — what the platform has captured
5. **Human Score — Multi-Tier Model** — 6 tiers / 18 dimensions:
   - Tier 1: Passive sensors (Cardio, Sleep, Activity, HRV)
   - Tier 2: Patient-reported (PHQ-9, nutrition, body composition)
   - Tier 3: Clinical / EHR (labs, diagnoses, office vitals, medication history)
   - Tier 4: Continuous biomarkers (CGM, sleep architecture, SpO2, skin temp)
   - Tier 5: Genomic & predictive risk (**PGx CYP2D6/CYP2C19**, polygenic risk, family history)
   - Tier 6: Adherence & engagement
6. **AI Predictive Recommendations** — 30/60/90-day forecasts + ranked interventions with expected score lift
7. **Technical & Wearable Data Quality Recommendations** — data capture gaps (Watch off during sleep, dual-source dedup, etc.)
8. **Data to Scrape Next** — backlog ranked by impact (high: Apple Health Clinical Records / RHR / HRV)
9. **5 Standardized AI Briefing Bullets**
10. **Human Score Visual**

## How to view

```bash
open raegen_deep_dive.html
```

No build step, no dependencies — single HTML file with inline CSS.

## Anonymization

All patient-identifying information has been removed:

| Field | Status |
|---|---|
| Patient name | Replaced with "Patient R" |
| DOB | Removed (age 24 retained) |
| Phone, email | Redacted |
| ZIP code | Redacted (city/state retained) |
| Internal user IDs | `[REDACTED-UUID]` |
| Dispenser serial number | Last 5 chars masked (`GO-60224XXXX`) |
| Clinical staff names + emails | Anonymized |

Clinical content (medications, dose timing, adherence metrics, wearable readings, derived patterns) is preserved as-is — these drive the analytical demonstration.

## Generated

2026-05-24
