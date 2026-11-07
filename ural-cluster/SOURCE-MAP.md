# Source map — the `notebook_sources_urls` Google Sheet, read 8 November 2026

This file answers one question: **the URL inventory behind the notebook's `[cite: n]` markers — was it used, and what did it change?**

Sheet: `notebook_sources_urls` · `spreadsheet_id` `1-vQGtAjSqPtQPYc8nim_qsRKFeIGZ2OdvBGM_2PwhHA` · tab `notebook_sources_urls.csv` (sheet id `1763950496`).

## What the sheet actually contains

- **40 data rows, 20 unique URLs.** Every URL appears exactly twice; the second copy is suffixed `(Duplicate Source)`.
  That 1:2 duplication is the origin of the doubled `[cite: n]` markers in the Drive drafts — the same page was cited twice per claim.
- Two columns only: `Title`, `URL`. No claim text, no snapshot date, no quotation. It is a *reading list*, not a citation ledger.
- The used range ends at row 41; the remaining rows of the 998-row grid are empty.
- **Zero of the 20 URLs are a Saudi government or mosque-authority domain.** The official pages the articles rely on
  (`haj.gov.sa`, `nusuk.sa`, `sar.hhr.sa`, `sar.com.sa`, `saptco.com.sa`, `prh.gov.sa`, `visitsaudi.com`) are not in the sheet at all.
- Mix by class: 6 hotel-booking platform pages (hotels.com, Kayak, Trip.com ×2, Expedia ×2, Agoda, Booking.com),
  3 Haramain-train pages (2 resellers, 1 editorial), 9 agency/content blogs, 1 official operator (SAT), 1 transport comparison.

So the sheet cannot by itself verify anything. What it can do is (a) show where each draft's claims came from, and
(b) supply independent pages that either corroborate or contradict a band the draft asserted. That is how it was used below.

## The 20 URLs mapped to the eight articles

| # | Source (as titled in the sheet) | Class | Article | What I did | Result |
|---|---|---|---|---|---|
| 1 | hotels.com — 10 Best Cheap Hotels in Makkah | OTA filter page | 4, 2 | not fetched | Commercial filter; prices change hourly and nothing on it is verifiable evidence. Not cited. |
| 2 | Kayak — 16 Best Hotels in Medina | OTA filter page | 3 | not fetched | Same class. Not cited. |
| 3 | Trip.com — Best Makkah Hotels with Shuttle | OTA filter page | 4 | not fetched | Shuttle "facts" on these pages are platform metadata, not operator timetables. Not cited. |
| 4 | **haramainrailway.com** | reseller (12Go affiliate front-end) | 5 | **fetched** | Sells tickets; not the operator and not an authority. Its route table (Makkah→Madinah 2h 20m, "from SAR 150+") is consistent with the article, but it is not cited — citing a reseller for the operator's own timetable would be misleading. |
| 5 | Expedia — Cheap Hotels in Makkah | OTA filter page | 4, 2 | not fetched | As #1. |
| 6 | haramain-train.com | reseller | 5 | not fetched | Same class as #4. |
| 7 | **ZiyaraGo — Haramain High-Speed Train guide** | independent editorial, compiled from the operator's public pages, dated 16 Oct 2026 | 5 | **fetched, cited** | Gave two checkable operational facts the article now states: ticket offices close **20 minutes** before departure, boarding gates **10 minutes** before, no-show forfeits the ticket. Also independently restates the operator's luggage rule (one bag ≤25 kg, ≤65 × 55 × 35 cm + one hand item) and notes two wheelchair spaces per train in the business car. |
| 8 | Noor Umrah Travels — Hotels near Masjid Nabawi 3–5 star | agency blog | 3 | not fetched | Agency inventory pitch. Not cited. |
| 9 | Agoda — Hotels near Al Masjid an Nabawi | OTA | 3 | not fetched | As #1. |
| 10 | **Booking.com — Hotels near Masjid Al Haram** | OTA | 7 (also 2) | **fetched, cited** | The one place an OTA page is genuinely useful: it publishes its own measurements. It lists the **Clock Royal Tower at ~900 ft** and **Swissotel Al Maqam at ~700 ft** from the mosque — straight map distances to the mosque boundary, exactly the number article 7 argues tells you least. Now used as the worked example in that paragraph. |
| 11 | **Package Umrah — How to use the Nusuk app in 2026** | agency guide (UK) | 1 | **fetched, cited** | Corroborates the permit chain for a foreign pilgrim: both permits **free**, Rawdah limited to **one permit per 365 days**, QR scanned before entry, arrive at the waiting area **20–30 minutes** early. Adds the gate-side timing the article previously left implicit. |
| 12 | flymoreme.com — Madinah Hotels, walking distance 2026 | commercial inventory (330 properties, 3 tiers) | 3 | **fetched**, not cited | Its tier thresholds (`under 750 m = 9–10 minute walk`) are the same map-distance arithmetic article 7 warns about, sold as a proximity guarantee. Useful as a warning example; not evidence, so it is not in any reference list. |
| 13 | ae.trip.com — "Madinah's Top 10 Hotels with FREE Shuttle" (moments) | user-generated post | 3, 4 | not fetched | Weakest class in the sheet. Not cited. |
| 14 | **LoveUmrah — Makkah to Madinah Transport 2026** | independent editorial | 5 | **fetched, cited** | The most useful page in the sheet. It publishes bands that overlap mine but reach higher, which forced three corrections (below). Also confirms 2h 20m on the rails and 3.5–5 h door to door. |
| 15 | BookMyUmrahTrip — Haramain railway transit guide | agency blog | 5 | not fetched | Duplicates #7 and #14 at lower precision. Not cited. |
| 16 | **Wego Travel Blog — Nusuk App 2026** | OTA blog citing the ministry and Arab News | 1 | **fetched, cited** | Independent statement of the "no booking, no visa" chain: hotel reference covering the **full stay** plus a transport reference for **at minimum a one-way airport transfer**. This is the claim article 1 is built on and it previously rested on ministry pages that describe the services rather than the pairing. |
| 17 | **SAT — Saudi Arabia Transport** | **official licensed intercity operator** | 5 | **fetched, cited** (root; the sheet's `/news/...` path returns an error) | Confirms the operator sells **STANDARD and VIP** ticket tiers on its own site and app — so "VIP coach" is a ticket tier sold by more than one operator, not a single brand. This is why the article's "standard SAPTCO" paragraph is now "standard coach services" covering both operators. |
| 18 | Expedia — Madinah hotels with shuttle | OTA filter page | 4 | not fetched | As #3. |
| 19 | MyPeaceTrip — Top 10 hotels near Masjid al-Haram | content blog | 2 | not fetched | Listicle; the "Top 10" phrasing the drafts repeated came from titles like this one. Not cited. |
| 20 | HotelsInMakkah — Top 10 hotels for every budget | content blog | 2 | not fetched | As #19. |

**8 of 20 fetched. 5 cited** (ZiyaraGo, Booking.com, Package Umrah, LoveUmrah, Wego) **plus 1 official operator** (SAT).
Twelve not fetched because their class makes them unusable as evidence; that judgement is recorded per row rather than hidden.

## What changed in the articles because of the sheet

**Article 5, Makkah–Madinah transport (the fare bands were the risk).**

| Claim | Before | After | Why |
|---|---|---|---|
| Train, economy | SAR 119–172 | **SAR 120–200, higher on peak dates** | LoveUmrah publishes economy at ~120–200; my lower ceiling was too tight for peak dates. |
| Train, business | SAR 210–350 | unchanged | 210–350 brackets both sources. |
| Coach, standard | SAPTCO, SAR 69–85 | **SAPTCO SAR 69–85; SAT standard SAR 85–130**; VIP SAR 100–170 | SAT is an official operator selling a STANDARD tier (sheet #17); LoveUmrah prices standard coaches at 85–130 (sheet #14). The old paragraph implied one operator. |
| Private car | sedan SAR 400–600 → van SAR 700–900 | **sedan SAR 400–800 → family van SAR 650–1,100** | My band sat inside LoveUmrah's, so the ceilings were understated for peak season. |
| Station deadlines | not stated | **ticket offices close 20 min before departure, gates 10 min, no-show forfeits the ticket** | ZiyaraGo (sheet #7), compiled from the operator's pages. |
| Luggage dimension, Bengali | missing | **65 × 55 × 35 cm added** | The English twin had it; the Bengali one did not. Fixed. |

**Article 7, walking time vs map distance.** The "listing distance is the number that tells you least" paragraph now carries a concrete
example with numbers: one major platform lists the Clock Royal Tower at ~900 ft and Swissotel Al Maqam at ~700 ft from the mosque.
Previously the point was argued abstractly; now it is shown, and the source is the platform itself.

**Article 1, Nusuk hotel BRN.** One sentence added to the booking-chain section: two independent 2026 guides describe the same
pair (hotel reference covering the whole stay + at least a one-way arrival transfer, both readable by the visa system), and the door
routine they describe matches the ministry's — QR scanned before entry, arrive 20–30 minutes early. These are now references [7] and [8].

**Articles 2, 3, 4, 6 and the pillar: unchanged.** The sheet holds no page that can verify a sector boundary, a gate number or a
shuttle timetable. Adding a hotels.com filter page to a reference list would have looked like sourcing without being sourcing, so it
was not done. Those articles continue to lean on the authority pages listed in `VERIFICATION-LEDGER.md`, with property distances
carried as documented rather than verified.

## What this does and does not settle

- It **settles provenance**: every substantive claim in the drafts traces to one of these 20 pages or to the authority pages now cited.
- It **found three real errors** in the drafts' numbers (economy-ceiling too low, coach operators conflated, car ceilings too low) and
  **two gaps** (station cut-off times, Bengali luggage dimensions).
- It **cannot** verify property-level facts. No page in the sheet is the hotel, the operator, or the mosque authority. Distances,
  gate numbers and queue minutes stay labelled as documented rather than verified, as recorded in the ledger.
- Prices remain **indicative bands, not quotes**, checked 8 November 2026 — the standing instruction for this cluster.
