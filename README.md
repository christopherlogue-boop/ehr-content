# SE Field Intel

Structured data repo that powers the SE TechGuide app — contains EHR integration specs, competitive intelligence, and field reference data for Commure's SE team.

## What it does

This repo is the **single source of truth** for EHR-specific integration details and competitive positioning. The [se-techguide](https://github.com/christopherlogue-boop/se-techguide) app pulls from these files at runtime (via raw GitHub URLs), so updating a CSV here instantly updates what SEs see in the tool.

## How to update

- **EHR data:** Edit `ehr-master.csv` and commit to `main`. Changes go live immediately in SE TechGuide.
- **Competitive intel:** Edit `competitive-ehr-ref.md` (human-readable) or `competitive-ehr-ref.json` (machine-readable). Keep both in sync.

No build step. No deploy. Commit = live.

## Key files

| File | What it is |
|---|---|
| `ehr-master.csv` | Master EHR reference — integration status, timelines, field mappings, blockers, pivot paths, and SE guidance for every supported EHR |
| `competitive-ehr-ref.md` | Competitive intel doc — Abridge, Ambience, Dragon Copilot, Suki, Nabla, plus EHR-native threats and coverage matrix |
| `competitive-ehr-ref.json` | Same competitive intel in JSON format for programmatic consumption by SE TechGuide |
