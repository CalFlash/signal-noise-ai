#  Signal/Noise

> *An LLM-powered anomaly intelligence platform. We don't chase headlines — we classify them.*

Built on the day the Pentagon dropped 162 UAP files (May 7, 2026) and the CDC 
began monitoring a live hantavirus cruise ship event. Signal/Noise treats both 
streams the same way an intelligence analyst would: sourced, structured, and 
rated by confidence.

---

## The Problem

When something anomalous happens — a government disclosure, a disease cluster, 
an unexplained event — the information environment immediately splits into three 
layers:

- **Official data**: what agencies actually confirmed
- **News reporting**: what journalists said about it
- **Unverified signal**: what spread before anyone checked

Most people — and most AI tools — treat all three the same. Signal/Noise doesn't.

---

## What This Builds

A structured intelligence dashboard with four components:

| Panel | What It Does |
|---|---|
|  **Event Feed** | Scrolling stream of classified events, color-coded by source type |
|  **Cluster Map** | U.S. geographic view of hantavirus case density and UAP disclosure locations |
|  **LLM Briefing Box** | Auto-generated analyst note: "What changed? What is verified? What is noise?" |
|  **Confidence Ledger** | Running tally of official vs. news vs. unverified claims across all events |

Every event in the system is a structured record — not a raw article dump.

---

## Data Sources

All primary. All public. All cited.

- **[war.gov/ufo](https://www.war.gov/ufo)** — The Pentagon's official UAP disclosure portal, launched May 7, 2026. 162 files: PDFs, infrared video, and military memos from the FBI, DoW, NASA, and State Department. New tranches are released on a rolling basis.
- **[CDC Open Data Portal](https://data.cdc.gov)** — Hantavirus weekly surveillance, notifiable disease counts by state, and national case feeds. All public via API.
- **[CDC Hantavirus Case History](https://www.cdc.gov/hantavirus/data-research/cases/index.html)** — 890 confirmed U.S. cases since 1993 through 2023. Broken down by state. Historical baseline for cluster detection.
- **[NWS Weather API](https://www.weather.gov/documentation/services-web-api)** — Geographic and environmental context layered over case locations. Rodent habitat ranges correlate with hantavirus risk zones.

---

## What Makes This Different

**The `contradicted_by` field.**

Every event record has a field that explicitly flags when a news claim diverges 
from official data. Most AI summarizers collapse all sources into one voice. 
This platform surfaces the gap — and lets you see exactly where the story 
broke from the evidence.

That distinction is the product.

---

## Event Schema

Every data point in Signal/Noise is a structured intelligence record:

```json
{
  "event_id": "unique identifier",
  "event_type": "UAP | HEALTH | ENVIRONMENTAL",
  "title": "short title",
  "date": "YYYY-MM-DD",
  "location": {
    "country": "",
    "state": "",
    "region": ""
  },
  "source_type": "official | news | unverified",
  "source_url": "",
  "source_name": "",
  "summary": "150-word LLM-generated briefing",
  "confidence": "high | medium | low",
  "contradicted_by": [],
  "tags": []
}

