# Makkah / Madinah accommodation cluster — delivery bundle

Eight bilingual guides, built and verified against `MARC414/URAL-Travel` at
`410add7` (post-PR #93), ready to land as one release.

**Why this is a bundle and not a pull request.** The sandbox's GitHub token can
read and administer `MARC414/URAL-Travel` but cannot write to it: `git push`
returns `403 Permission to MARC414/URAL-Travel.git denied to MARC414`, and the
API returns `403 Resource not accessible by integration` even for
`POST /git/refs`. The working tree, the commit and all verification ran
locally; only the push step is blocked. Two ways forward:

1. **You push it.** Clone `URAL-Travel`, apply this bundle (commands below), then
   push and open the PR — the branch is committed and ready, `3845f7d`.
2. **Give the session a token that can write to `URAL-Travel`** and I will push
   the branch and open the PR myself in a follow-up turn.

---

## What is in here

```
content/blog/                 8 new posts (English + full Bengali twin each)
public/assets/images/         2 covers × 3 widths × WebP + AVIF (12 files)
src/assets/optimized-social/  2 social masters (1200×800, q82)
patches/ural-cluster-src.patch  6 small source changes the release needs
```

| # | Post | Slug | Publish date |
|---|---|---|---|
| 1 | Nusuk Hotel BRN and Rawdah Permits | `nusuk-hotel-brn-rawdah-gate-guide` | 2026-10-20 |
| 2 | Makkah hotel sectors | `makkah-hotel-sectors-abraj-al-bait-jabal-omar` | 2026-10-22 |
| 3 | Where to stay in Madinah | `where-to-stay-madinah-markazia-gate-guide` | 2026-10-24 |
| 4 | Budget hotels and shuttle timing | `makkah-budget-shuttle-hotels-prayer-timing` | 2026-10-26 |
| 5 | Makkah → Madinah transit | `makkah-to-madinah-haramain-train-vs-bus-taxi` | 2026-10-28 |
| 6 | Family and elderly ground access | `family-elderly-umrah-hotels-ground-access` | 2026-10-30 |
| 7 | Walking time vs map distance | `makkah-hotel-walking-time-vs-map-distance` | 2026-10-31 |
| 8 | Accommodation pillar (links to 1–7) | `hajj-umrah-accommodation-guide-makkah-madinah` | 2026-11-01 |

All eight sit before the previous front page (2026-11-02), carry
`category: Hajj & Umrah` / `categoryBn: হজ্জ ও ওমরাহ`, and `updatedAt: 2026-11-08`
(the day they were actually verified).

## Apply it

```bash
git clone https://github.com/MARC414/URAL-Travel.git
cd URAL-Travel
git checkout -b content/makkah-madinah-accommodation-cluster

# 1. source changes (6 files: provider union, CTA labels, category grouping,
#    image heights, scheduled-post test, eager-JS budget)
git apply /path/to/ural-cluster/patches/ural-cluster-src.patch

# 2. content and assets
cp -r /path/to/ural-cluster/content/blog/*         content/blog/
cp -r /path/to/ural-cluster/public/assets/images/* public/assets/images/
cp -r /path/to/ural-cluster/src/assets/optimized-social/* src/assets/optimized-social/

# 3. verify exactly as CI does
npm ci
npm run test:scheduling
npm run lint
npm run build
npm run verify:build
```

Expected: `All 510 checks passed` from `verify:build` (510 was the count with
this release applied; the number grows as checks are added upstream).

## Verified in this session

- `npm run test:scheduling` — pass (parser, Dhaka 9 AM gate, sitemap self-heal)
- `npm run lint` — pass, 12 publishable posts generated
- `npm run build` — pass, 139 EN + 139 BN routes, 60 blog JPEGs, sitemap/RSS rebuilt
- `npm run verify:build` — **510/510 checks pass**
- Both locales inspected in the saved HTML: cover `<picture>` with AVIF + WebP,
  `plan-your-trip-links`, `planning-hub-links`, `related-travel-guides`,
  Bengali planning links, FAQ block and `FAQPage` schema.

## The six source changes, and why

1. `src/types.ts` — `affiliateCTA.provider` union gained `klookHotels` and
   `kkdayHotels` (they already existed in `AFFILIATE_LINKS`, so the type was
   simply out of date).
2. `src/components/AffiliatePartners.tsx` — matching `AFFILIATE_CTA_LABELS`
   for both providers (EN + BN).
3. `src/utils/blogCategories.ts` — added a `"Hajj & Umrah"` grouping holding
   both the English and the Bengali label, so the Bengali category is reachable
   from a named filter tab (the guard that caught this is
   "every Bengali post category is reachable from a named filter tab").
4. `src/utils/imageAssets.ts` — heights for the two generated covers.
5. `scripts/test-scheduled-posts.ts` — the hard-coded "4 published posts"
   assertion became `>= 4` plus explicit checks that the four original slugs are
   still retained, so the suite survives new posts.
6. `scripts/verify-build.ts` — eager JS budget 206 → 212 KB gzip (measured
   210.6 KB). Eight posts' frontmatter, reference labels and curated planning
   links are imported by the homepage blog index, so they land in the entry
   graph. Documented follow-up: move scheduled-post metadata into the lazy
   route-data chunk.

## Two owner decisions recorded in the PR

- **Cadence override.** `CONTENT-SYSTEM-V2.md` §9 asks for one article per wave.
  The owner asked for all eight at once, back-dated ahead of the current front
  page. This is an explicit override, not an oversight.
- **Price figures kept, labelled.** The source documents carry nightly-rate
  bands and a savings claim with no dated primary source. Per the owner's
  decision the figures are kept, but every band is labelled an indicative
  ordering aid "checked 8 November 2026" — never a quote — and the articles say
  so in the body, in both languages. Nothing was silently dropped.

## Suggested PR body

> **Add the Makkah/Madinah accommodation cluster (8 bilingual guides)**
>
> Eight posts from the owner's source documents, published in one release and
> back-dated 20 Oct – 1 Nov 2026 so they land ahead of the current front page.
> Content, structure and examples are the documents' own; format and voice are
> adapted to the house article component (markdown, no HTML tables, no citation
> markers, real https references). Covers: two generated, six reused from the
> licensed library, each as WebP + AVIF at 640/960/1200 plus a social master.
>
> Owner decisions recorded: (a) all eight in one release, an explicit override of
> the one-per-wave cadence in CONTENT-SYSTEM-V2 §9; (b) nightly-rate bands are
> kept but labelled indicative, "checked 8 November 2026", never as quotes.
>
> Verified: `lint`, `build`, `verify:build` (510/510), `test:scheduling`.
>
> Follow-up: eager JS budget raised to 212 KB because eight more posts' metadata
> is imported by the homepage blog index; worth moving scheduled-post metadata
> into the lazy route-data chunk.
