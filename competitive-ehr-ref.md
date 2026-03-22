# Competitive EHR Reference — v1.0

> **Source:** Ambient Competitive Research wiki (last updated March 7, 2026), Epic/MEDITECH integration guides, SOWs, EHR one-pagers from Google Drive.
> **Last compiled:** 2026-03-22
> **Rule:** Nothing inferred. If it's not documented, it's marked unknown.

---

## Table of Contents

1. [EHR Technical Reference](#ehr-technical-reference)
   - [Epic](#epic)
   - [MEDITECH](#meditech)
   - [eClinicalWorks (eCW)](#eclinicalworks-ecw)
   - [athenahealth (athenaOne)](#athenahealth-athenaone)
2. [Competitive Intelligence — Ambient AI](#competitive-intelligence--ambient-ai)
   - [Abridge](#abridge)
   - [Ambience Healthcare](#ambience-healthcare)
   - [Microsoft Dragon Copilot (Nuance DAX)](#microsoft-dragon-copilot-nuance-dax)
   - [Suki](#suki)
   - [Nabla](#nabla)
3. [EHR-Native Threats](#ehr-native-threats)
4. [Competitor × EHR Coverage Matrix](#competitor--ehr-coverage-matrix)
5. [Knowns vs Unknowns](#knowns-vs-unknowns)
6. [Market Share Ranking](#market-share-ranking)
7. [Commure Differentiators](#commure-differentiators)

---

## EHR Technical Reference

### Epic

| Field | Value |
|-------|-------|
| **Integration (mobile)** | Haiku FHIR R4 — native app launch, listed in Epic Toolbox as "Ambient Notes" |
| **Integration (workstation)** | Hyperspace via FDI record — two modes: embedded window (mic NOT accessible) or pop-up window (mic accessible) |
| **Note writeback** | SmartDataElements (SDE1) — 5 SmartSections max at go-live |
| **Scheduling inbound** | HL7 v2 SIU/ADT or FHIR |
| **Auth** | SMART on FHIR + OAuth2 |
| **Fallback** | HL7 v2 ADT/ORU for Epic 2018 or API-blocked sites |
| **Key limits** | No SmartForms, no Flowsheets; Epic 2018 adds ~2 weeks; Commure has no direct Epic env access — customer team does all builds; FDI build required for Hyperspace |
| **Timeline** | Scribe 6–8 wks; +RCM 12–16 wks total; high-complexity SMART on FHIR + Hyperspace iFrame: 10–14 wks |
| **RCM method** | Selenium + API |
| **Competitive exposure** | High — Abridge, Dragon Copilot; Epic now building its own native ambient tool with Microsoft (early 2026) |
| **Epic AI Charting (Art)** | Launched Feb 2025, 40x AI usage growth in 2025, built with Microsoft, usage-based pricing can become expensive, disjointed experience across product teams |

---

### MEDITECH

| Field | Value |
|-------|-------|
| **Integration (Expanse v2+)** | FHIR R4 |
| **Integration (older Expanse / Magic)** | HL7 v2 via integration bridge |
| **Note writeback** | Colossus DOM injection — less stable than native API, IT security may reject |
| **Kill shot qualifier** | Expanse vs Magic — Magic dramatically increases complexity |
| **Timeline** | Expanse FHIR 8–10 wks; Magic/HL7 bridge 12–16 wks |
| **RCM method** | Selenium |
| **Suki** | Confirmed native MEDITECH Expanse API integration — first to market |
| **Dragon Copilot** | Confirmed MEDITECH strategic development partnership |
| **Solventum (3M)** | Confirmed MEDITECH Accelerator partner as of Jan 2026 |

---

### eClinicalWorks (eCW)

| Field | Value |
|-------|-------|
| **Integration** | eCW API → SOAP Progress Note — 5 free-text fields max; HL7 SIU/ADT for scheduling |
| **Mobile** | Full validation on eCW Mobile iOS/Android |
| **RCM** | Selenium — no direct eCW API dependency |
| **Credentials** | 4 eCW service accounts required (eBO + appointment + chart read/write) |
| **Kill shot qualifier** | Cloud-hosted vs on-premise — on-prem = zero integration path, no workaround |
| **Timeline** | Scribe 4–6 wks (fastest in portfolio); full stack ~10–14 wks |
| **Sunoh** | Confirmed eCW-native scribe — built on top of eCW |
| **Abridge / Ambience** | No confirmed eCW integration |

---

### athenahealth (athenaOne)

| Field | Value |
|-------|-------|
| **Integration** | 100% REST API — no HL7 at all |
| **Note writeback** | Up to 8 free-text fields; templates 17292 and 17293 |
| **Scribe Macros** | Dot phrases supported — athena-specific feature |
| **Kill shot qualifier** | 2FA must be disabled on service account — non-negotiable |
| **API authorization** | 1–2 week processing lag |
| **Timeline** | Scribe 6–8 wks; +RCM 12–16 wks total |
| **Ambience** | Confirmed on athenahealth (Midi Health partnership) |
| **Suki** | Confirmed athenahealth Preferred Partner status |
| **EHR-native** | Athena Ambient Notes already live; athenaAmbient (next-gen) in user testing Feb 2026; marketplace includes Suki, iScribe, DAX Copilot |

---

## Competitive Intelligence — Ambient AI

### Abridge

| Field | Detail |
|-------|--------|
| **Funding** | Series E ~$5B valuation (Nov 2025), $450M+ total raised |
| **Headcount** | 560 employees |
| **Customers** | 200+ enterprise; former Epic preferred partner — Epic sold equity stake in 2025 |
| **Pricing** | ~$300–400/provider/month enterprise; ~$200/month individual |
| **EHR coverage** | Epic (deep, native Haiku embedding); athenahealth (confirmed); MEDITECH: 🔍 Unknown — not documented; eCW: 🔍 Unknown — not documented |
| **Key features** | Linked evidence (click note section → transcript source), pre-visit chart prep, HCC coding assist, prior auth (launched Aug 2025 w/ Highmark/AHN), nursing workflows (Mayo Clinic reference) |
| **Wins when** | Note quality, Epic shops, linked evidence for compliance, specialty workflows |
| **Loses when** | Price sensitivity, non-Epic EHRs, full workflow automation beyond notes |
| **Internal intel** | Lowering price recently; fast off-the-shelf deployment with no custom template work needed; "one main template and canned specialty features" vs Commure customization |
| **Watch out for** | Epic now building competing native ambient tool — Abridge and Epic are no longer aligned |

---

### Ambience Healthcare

| Field | Detail |
|-------|--------|
| **Funding** | Series C $243M at $1B valuation (July 2025), ~$345M total; backed by OpenAI, a16z, Kleiner Perkins, Optum |
| **Headcount** | 214 employees (Jan 2026) |
| **Notable win** | Cleveland Clinic (head-to-head evaluation) |
| **EHR coverage** | Epic (confirmed); athenahealth (confirmed — Midi Health partnership); MEDITECH: 🔍 Unknown — not documented; eCW: 🔍 Unknown — not documented |
| **Key features** | AutoScribe, Patient Recap (pre-visit), coding-aware documentation, orders/workflow execution, structured data extraction, inpatient care (launched Nov 2025) |
| **Pricing** | AutoScribe ~$2,800–3,200/provider/year; Full suite ~$4,000–5,000/provider/year |
| **Internal intel** | "Best product, highest price, colossus motion with integration when API not available, challenging to work with"; best note quality and specialty customization; coding accuracy strong |

---

### Microsoft Dragon Copilot (Nuance DAX)

| Field | Detail |
|-------|--------|
| **Scale** | 400+ healthcare organizations; 150+ hospitals with Epic integration |
| **EHR coverage** | Epic (deep, fully embedded — GA Jan 2024); MEDITECH (strategic development partnership confirmed); eCW (confirmed); athenahealth (confirmed); Cerner (deep) |
| **Epic AI role** | Building Epic's native ambient tool for early 2026 release |
| **Pricing** | ~$600/clinician/month (~$7,200/year); some resellers ~$369/month |
| **Key features** | Ambient + dictation (Dragon Medical One), order suggestions, clinical Q&A, voice commands/macros |
| **Wins when** | Microsoft/Azure enterprise footprint, dictation/macro lock-in, ortho/radiology specialties, broadest EHR coverage |
| **Loses when** | Cost, innovation pace, no RCM, no PXP |
| **Internal intel** | Industry-leading dictation and macros; deepest EHR integration footprint; "fastest innovation and modern AI platform approach" is Commure's counter |

---

### Suki

| Field | Detail |
|-------|--------|
| **Scale** | 400+ organizations, 140,000+ healthcare customers worldwide (2025) |
| **Notable** | 8 of 10 largest US health systems; 9 of top 10 US News-ranked hospitals |
| **Funding** | Series D $70M (Oct 2024), ~$165M total |
| **EHR coverage** | Epic (confirmed — "Suki Inside" natively embedded in Haiku and desktop); MEDITECH Expanse (confirmed — first company with direct native API integration); athenahealth (Preferred Partner); Oracle Health (confirmed); eCW: 🔍 Unknown — not documented |
| **Key features** | Ambient + dictation (first-class), pre-visit chart prep, HCC/ICD-10 coding, order staging, Zoom integration, nursing workflows, UpToDate integration (Wolters Kluwer) |
| **Pricing** | ~$199–399/month individual; enterprise custom |
| **Wins when** | Voice-first workflows, multi-EHR environments, athenahealth, mid-market |

---

### Nabla

| Field | Detail |
|-------|--------|
| **Funding** | Series C $70M (June 2025), $120M total; 3x ARR growth |
| **EHR coverage** | 150+ organizations via plug-and-play browser extension model; Greenway Next Gen, Navina (partnerships); Epic: 🔍 Unknown — not documented; MEDITECH: 🔍 Unknown — not documented; eCW: 🔍 Unknown — not documented; athenahealth: 🔍 Unknown — not documented |
| **Key features** | Ambient + dictation, patient briefs, ICD-10/HCC suggestions, Nabla Connect API platform |
| **Pricing** | Free tier (30 consults/month); ~$119/month unlimited |
| **Wins when** | Rapid deployment, price, SMB/mid-market |

---

## EHR-Native Threats

| Threat | Details |
|--------|---------|
| **Epic AI Charting (Art)** | Launched Feb 2025; 40x AI usage growth; usage-based pricing; built with Microsoft; disjointed multi-team product experience |
| **Athena Ambient Notes** | Live for athena customers; marketplace also offers Suki, iScribe, DAX Copilot; athenaAmbient (next-gen) in user testing Feb 2026 |
| **Oracle Clinical Digital Assistant (OCDA)** | Native Cerner; blocks third-party scribes in Cerner ecosystem; reportedly high pricing; struggles in ED/hospitalist; "we've never run into OCDA" |
| **Solventum Fluency Align** | MEDITECH Accelerator partner Jan 2026; strong CDI/coding heritage; #1 KLAS radiology speech 2025 |
| **Sunoh** | eCW-native, mobile-first, low-cost |
| **Amazon Health Connect** | Launched March 5–6, 2026; ambient docs + scheduling agent + billing codes; Veradigm EHR partner; internal intel: prior HealthScribe product considered a failure internally |

---

## Competitor × EHR Coverage Matrix

| Competitor | Epic | MEDITECH | eCW | athenahealth | Cerner/Oracle |
|-----------|------|----------|-----|--------------|---------------|
| **Abridge** | ✅ Deep (native Haiku) | 🔍 Unknown | 🔍 Unknown | ✅ Confirmed | 🔍 Unknown |
| **Ambience** | ✅ Confirmed | 🔍 Unknown | 🔍 Unknown | ✅ Confirmed (Midi Health) | 🔍 Unknown |
| **Dragon Copilot** | ✅ Deep (fully embedded) | ✅ Strategic partnership | ✅ Confirmed | ✅ Confirmed | ✅ Deep |
| **Suki** | ✅ "Suki Inside" (Haiku + desktop) | ✅ Expanse native API (first to market) | 🔍 Unknown | ✅ Preferred Partner | ✅ Oracle Health confirmed |
| **Nabla** | 🔍 Unknown | 🔍 Unknown | 🔍 Unknown | 🔍 Unknown | 🔍 Unknown |
| **Commure** | ✅ Haiku FHIR R4 + Hyperspace FDI | ✅ Expanse FHIR R4 / HL7 bridge | ✅ eCW API + HL7 | ✅ REST API | 🔍 See ehr-master.csv |

---

## Knowns vs Unknowns

### What We Know (Documented)

**EHR Integration — Commure:**
- ✅ Epic: Full integration path (Haiku, Hyperspace, SMART on FHIR, HL7 fallback), timelines, limits
- ✅ MEDITECH: Expanse FHIR R4, Magic HL7 bridge, Colossus DOM injection writeback, timelines
- ✅ eCW: API integration, mobile validation, on-prem kill shot, fastest timeline in portfolio
- ✅ athenahealth: 100% REST API, dot phrases, 2FA kill shot, API auth lag

**Competitor Positioning:**
- ✅ Abridge: pricing, Epic depth, linked evidence, recent price drops, Epic relationship fracture
- ✅ Ambience: pricing, Cleveland Clinic win, coding accuracy, "best product, highest price"
- ✅ Dragon Copilot: broadest EHR coverage, pricing, dictation lock-in, building Epic's native tool
- ✅ Suki: MEDITECH first-to-market, athena preferred partner, voice-first positioning
- ✅ Nabla: browser extension model, free tier, SMB focus

**Market Dynamics:**
- ✅ Epic building native ambient with Microsoft (early 2026)
- ✅ Amazon Health Connect launched March 2026
- ✅ Solventum is MEDITECH Accelerator partner
- ✅ Oracle OCDA blocks third-party scribes in Cerner ecosystem

### What We Don't Know (Gaps to Fill)

**Competitor EHR Coverage Gaps:**
- 🔍 Abridge on MEDITECH — not documented
- 🔍 Abridge on eCW — not documented
- 🔍 Abridge on Cerner/Oracle — not documented
- 🔍 Ambience on MEDITECH — not documented
- 🔍 Ambience on eCW — not documented
- 🔍 Ambience on Cerner/Oracle — not documented
- 🔍 Suki on eCW — not documented
- 🔍 Nabla on all major EHRs (Epic, MEDITECH, eCW, athena) — not documented

**Competitor Product Gaps:**
- 🔍 Abridge RCM capabilities — not documented (noted they lack "full workflow automation beyond notes")
- 🔍 Ambience RCM capabilities — not documented
- 🔍 Suki RCM capabilities — not documented
- 🔍 Nabla RCM capabilities — not documented
- 🔍 All competitors: PXP capabilities — not documented for any competitor

**Pricing Gaps:**
- 🔍 Suki enterprise pricing — listed as "custom"
- 🔍 Nabla enterprise pricing — not documented
- 🔍 Ambience enterprise discount tiers — not documented

**Market Intel Gaps:**
- 🔍 Dragon Copilot total customer count (beyond "400+ organizations") — not documented
- 🔍 Ambience total customer count — not documented
- 🔍 Nabla total customer count (beyond "150+ organizations") — not documented
- 🔍 Amazon Health Connect pricing — not documented
- 🔍 Epic AI Charting (Art) pricing details beyond "usage-based" — not documented

---

## Market Share Ranking

*Source: Internal intel, approximate*

| Rank | Competitor |
|------|-----------|
| 1 | Dragon Copilot |
| 2 | Abridge |
| 3 | Ambience |
| 4 | Suki / Nabla |
| 5 | PLG tier (Heidi, Freed) |
| 6–7 | Commure Ambient |

---

## Commure Differentiators

- **Only platform with Ambient + RCM + PXP in one layer** — no competitor offers all three
- 40M+ appointments at deployment scale
- HCA + Tenet exclusive partnerships
- Augmedix acquisition — proven ambient scribe heritage
- EHR breadth: 60+ integrations
- Forward-deployed engineering model
- Revenue cycle differentiation: coding-aware documentation, denial-aware intelligence, CDI nudges tied to billing accuracy
