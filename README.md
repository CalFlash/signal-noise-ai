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

## Stack

- **LLM**: OpenAI API — entity extraction and briefing generation
- **Data**: CDC Open Data, war.gov/ufo, NWS API
- **Frontend**: HTML / CSS / JS — no framework, fast and readable
- **Backend**: Node.js or Python — lightweight, no bloat
- **Map**: Leaflet.js — open-source, embeddable

---

## Project Status

-  Day 1 — Schema defined, seed data loaded, UI plan mapped
-  Day 2 — LLM pipeline, war.gov PDF parsing (in progress)
-  Day 3 — Live dashboard, public demo (upcoming)

---

## Why This Exists

The same week the U.S. government told the public to "draw their own conclusions" 
from 162 classified UAP files, the CDC was quietly monitoring travelers from a 
cruise ship for hantavirus exposure.

Two anomalous data streams. Zero tools to cross-reference them with rigor.

Signal/Noise exists because the gap between *what happened* and 
*what was reported* is where the actual story lives — and LLMs are now 
good enough to map that gap in real time.

---

## Author

**Michael Senno** — Writer, entrepreneur, and AI developer based in Hermosa Beach, CA.  
Author of *California Gothic*. Founder of Investing Buds.  
Building at the intersection of language models, public data, and high-signal events.

[GitHub](https://github.com/CalFlash) · [LinkedIn](#) · [Investing Buds](#)

---

*Signal/Noise is not a conspiracy platform. It is a source-classification engine 
built on public government data. Every claim in this system is traceable to a 
primary source.*



