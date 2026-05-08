## What This Is
Signal/Noise is an LLM-assisted anomaly intelligence platform that ingests 
official government disclosures and public health surveillance data, 
structures them into a unified event schema, and generates analyst-style 
briefings that separate verified claims from unverified ones.

## Why It Exists
The Pentagon released 162 UAP files on May 7, 2026 — the same week the CDC 
was actively monitoring hantavirus exposure from a cruise ship event. 
Signal/Noise was built to treat these emerging streams the same way an 
intelligence analyst would: sourced, structured, and labeled by confidence.

## What Makes It Different
Most AI apps summarize. This one classifies. Every event is tagged with 
source type (official/news/unverified), a confidence rating, and a 
contradicted_by field that catches when news claims diverge from official data.

## Stack
- Data: CDC Open Data, war.gov/ufo, NOAA/NWS API for geographic context
- LLM: OpenAI API for entity extraction and briefing generation
- Frontend: HTML/CSS/JS dashboard with cluster map and event feed
- Backend: Node.js or Python (lightweight, no framework required)

## Status
Day 1 — schema defined, seed data seeded, UI mockup in progress.


