# Verification ledger — the Drive documents, what they proved, and what changed

Answering two questions: *"are the Drive source files any use for verification?"* and
*"did you publish them as they were, with no change?"*

**Documents read (all nine, full text, 7–8 Nov 2026):** 01 Nusuk, 02 Makkah proximity,
03 Madinah Markazia, 04 15–75 budget/shuttles, 05 transit blueprint, 06 family & elderly,
07 walking times vs map distance, 08 the pillar, plus the source-inventory document.

## 1. Are the documents usable for verification? Partly — and precisely where

They are an excellent **editorial** source: they carry the argument, the sector models, the
named properties, the gate guidance, the shuttle protocols, the transit stages and the FAQ
intent. That is what the articles are built on, and none of it was invented by me.

They are a weak **citation** source for two reasons:

1. **They contain almost no URLs.** Full-text export of all nine documents yields exactly two
   live links: `https://services.nusuk.sa/` and `https://www.sar.com.sa/`. Every other claim
   arrives with `[cite: n]` markers pointing at an internal notebook index, not at a public page.
2. **The underlying sources are secondary.** The inventory lists 21 titles — Booking.com,
   Expedia, Trip.com, KAYAK, Agoda, LoveUmrah, ZiyaraGo, Wego, Noor Umrah Travels, FlyMoreME,
   BookMyUmrahTrip, agency and blog pages. Those are useful for *what travellers report*, not
   for a citation list.

So verification ran the other way round: the documents supplied the claims, and each testable
claim was checked against the authority that owns it.

### Claims I verified against a primary source (and re-checked while writing this ledger)

| Claim | Source (fetched, live) | Status |
|---|---|---|
| Rawdah Sharif permit: free, Nusuk app + website, 5 steps via Nafath, date + slot, "Immediate", visa-based target groups | `haj.gov.sa/en/E-Services/Permit-to-Visit-Al-Rawdah-Al-Sharifiyah-for-Men-Women` (page updated 19 Oct 2026) | ✔ verified 7 Nov |
| Umrah permit: free, Nusuk app/website, Nafath login, 5 steps, target group visitor/GCC citizen/citizen/resident, "Immediate" | `haj.gov.sa/en/E-Services/Umrah-Permit-Application` (updated 19 Oct 2026) | ✔ verified 8 Nov |
| The permit service is executed through `services.nusuk.sa` — the one URL in the documents | same page, "Execute Service" target + document 08 | ✔ verified |
| SAR operates the Haramain High-Speed Railway Makkah–Madinah | `sar.com.sa` homepage ("SAR operates … the Haramain High-Speed Railway between Makkah and Madinah") | ✔ verified 8 Nov |
| Haramain luggage: **one** bag, max **25 kg**, max **65 × 55 × 35 cm**, plus one hand item, security scan before boarding | `sar.hhr.sa/travel/guidelines/baggage` (official HHR portal) | ✔ verified 8 Nov — **upgraded** while writing this ledger: the dimension limit was added to the article and the page added to its references |
| Makkah–Madinah rail journey ≈ 2 h 20 min | Not stated on the SAR page; corroborated by several independent 2026 sources quoting the operator | ◐ carried, phrased as "about 2 hours 20 minutes" |
| Tourist and other visit visas allow Umrah, with conditions that change | `visitsaudi.com/en/plan-your-trip/visa-regulations` — the official FAQ carries the question "Can I perform Umrah or Hajj with the tourist visa?" | ✔ page verified; article tells the reader to check the current rule for their passport |
| Gate names and numbers (Makkah King Fahad 79/94 side, Ajyad 84–90, King Abdulaziz 1; Madinah 24/25/37 for women) | No primary page isolates these; the Presidency for the Two Holy Mosques (`prh.gov.sa`) is cited for the institution, not for a gate table | ◐ carried as documented, and every article tells the reader to confirm the current gate with the property or on arrival |

### Claims carried as documented, deliberately not dressed up as facts

Property-by-property distances and walking minutes (Oberoi, Dar Al Taqwa, Hilton, Pullman
Zamzam, Dallah Taibah, Dar Al Tawhid, Conrad, Jumeirah, Ibis Styles, voco, Al Kiswah),
the three-tier distance model, the Kudai/Jarwal terminal geography, the shuttle suspension
window, the lift-bank behaviour in the Clock Tower towers, and the quad-versus-rollaway room
distinction. All of it survives as *guidance with an action attached* ("ask which gate, ask
how many permanent beds, ask what the shuttle does on Ramadan's last ten nights") rather than
as numbers a reader could hold us to.

### Claims I could not stand behind, and what I did with them

| Document says | Why it could not ship as written | What the article says |
|---|---|---|
| "20 to 45 minutes" lift queues; "90-second" room-to-carpet; "15–20 minute plaza trek" | no source, and highly variable by tower, floor and hour | the mechanism, the trade-off, and a departure-time rule — no invented minutes |
| "235,000 m² plaza", "43 °C", "1.2 km walk" | unsourced precision | dropped; "an enormous paved plaza", "summer heat", "a long perimeter walk" |
| "saves $1,200+ per week" | arithmetic on undated OTA rates | kept as a comparison of vectors, with the arithmetic left to the reader's own dates |
| "Shuttles stop 30–45 minutes before the adhan" | plausible, but no municipal source found | kept as the operating rule the documents describe, with "treat 50–60 minutes before the adhan as the latest sensible boarding time" |
| "Gates 24/25/37 = women" | consistent across sources, not from an authority | kept as orientation with an explicit "confirm current assignment" |
| Nightly rate bands ($15–$75, $393–$580, etc.) | undated, no primary source | **kept, per your decision**, every band labelled "indicative … checked 8 November 2026", never as a quote |
| "Ultimate", "Truth", "definitive", "Top 10" | banned by the house voice rules | titles rewritten; boilerplate "Top 10 Hotels in Makkah for Every Budget" lines removed (they appeared 20+ times inside the documents) |

## 2. Did the articles come through unchanged? No — and here is exactly what changed

**Preserved (substance):** every section of every document, in order — the mapping illusion and
the four-stage transit sum, the three Makkah zones with Abraj Al-Bait / Jabal Omar / shuttle
zones, the Madinah four-sector model and the northern-gate logic, the three-tier distance model,
the budget-and-shuttle operating rules with Kudai and Jarwal, the Haramain-vs-VIP-coach-vs-van
transit breakdown with classes, luggage and booking windows, the family/elderly ground-access
analysis, the quad-room and hidden-fee sections, the Nusuk/BRN chain, and every named property
and example the documents use.

**Changed (container and unverifiable precision):**

| In the documents | In the published article |
|---|---|
| HTML (`<article>`, `<section>`, `<table border="1">`, inline styles) | markdown headings, paragraphs, bullets |
| ASCII / box-drawing diagrams | prose or bullets (plus one real generated figure where a picture carries the point) |
| `[cite: 1, 3]` markers | removed; a real reference list of live https authority pages |
| "SEO METADATA BLOCK", "Suggested URL Slug", "Meta Title" | deleted; real frontmatter (`seoTitle`, `seoDescription`, `snippet`, `summary`) |
| `<h3>Q: …</h3>` FAQ | numbered FAQ block that matches the `FAQPage` schema |
| "Image of: … Feature Image" placeholders | eight generated covers |
| repeated boilerplate lines | deleted |
| invented precision and superlatives | softened or dropped, as tabulated above |

**Added that was never in the documents:** the full Bengali twin of each article (written by me,
not machine-pasted), the Reference block, the curated internal links, the "checked 8 November
2026" line, cover alt text in both languages, and the affiliate CTA slot the template requires.

**Net effect:** you are reading your own material — same structure, same advice, same property
names, same examples — in a different container, with the numbers either sourced or clearly
marked as indicative. If you would rather have a specific softened passage restored to its
original wording, name it and I will put it back (and note the exception in the PR).

## 3. Per-article notes

1. **Nusuk / BRN / Rawdah** — the permit chain is the best-sourced piece in the set: both service
   pages fetched, free of charge, five steps, Nafath, immediate, plus the `services.nusuk.sa`
   execution target from your own documents.
2. **Makkah sectors** — structure and property names from doc 02; lift-queue minutes removed;
   the "ask which tower, which floor, which lift bank" questions added.
3. **Madinah** — doc 03's four sectors, three tiers and property shortlist kept; the women's Rawdah
   gate logic kept as orientation; rate bands flagged.
4. **Budget + shuttles** — doc 04's operating rules and the Kudai/Jarwal routing kept; the weekly
   savings claim turned into a comparison you can run on your own dates.
5. **Transit** — doc 05's door-to-door stage table turned into prose; the 25 kg rule now carries the
   official 65 × 55 × 35 cm limit and the HHR baggage page as a reference.
6. **Family / elderly** — doc 06's incline, gate and lift analysis kept; room-area and bed-count
   guidance kept; per-person fee bands flagged.
7. **Walking time vs map distance** — doc 07's four-stage sum and the tower-vs-podium contrast kept;
   the "90-second" and "15–24 minute" totals replaced with the mechanism.
8. **Pillar** — doc 08's holistic frame and booking lead times kept; the "Top 10" repeats and the
   five invented internal URLs remapped to the seven real cluster routes.

## 4. What could still be verified, if you want it done

Ask and I will chase a source for any of these: the Madinah women's gate numbering from an official
or mosque-authority page; the pre-adhan road-closure window from a Makkah traffic announcement;
per-property distances from the properties' own pages; and the 21 inventory titles, each fetched and
confirmed before it goes anywhere near a reference list.
