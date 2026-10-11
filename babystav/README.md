# Baby Stav – Monthly Meta Campaign Process

Public banner hosting for Baby Stav Meta ads, plus the monthly runbook.
Folder per month: `babystav/<month>-<year>/` (e.g. `october-2026`).

## File naming (per month folder)
`<product-slug>-feed.png` (square, ~1254×1254) and `<product-slug>-reel.png` (9:16, 1080×1920).
Raw URL pattern used by Meta:
`https://raw.githubusercontent.com/omerbrod-lab/ad-assets/main/babystav/<month>-<year>/<file>`

## Fixed account details
| Item | Value |
|---|---|
| Ad account | 24064050 (USD) |
| Facebook page | Baby Stav בייבי סתיו – 103997756319943 |
| Instagram | babystav (not visible to the connector yet – set manually) |
| Pixel / event | 170738550118263 / PURCHASE |
| Source sheet | Google Sheet "Baby Stav – Meta Campaigns" (1TIzDsIQPZaAwDP2wFyQsJu0CTrb4hFUc_VVm_AxQ3dM) |

## Monthly steps
1. **Sheet** – new tab per month. Columns: A product name, B client note, C post text, D product link, E notes, F banner links (FEED + REEL, Drive).
2. **Copy** – September style: product name / seasonal opener / 3 ✅ bullets / 📢 price line "X ₪ במקום Y ₪!" / "לפרטים ורכישה 👇". No link inside the text.
3. **Prices** – verify current + strikethrough price on babystav.co.il for every product (pages render prices via JS – use the browser, then close it).
4. **Banners** – download from Drive, verify each PNG opens fully, push to this repo.
5. **Campaign** – OUTCOME_SALES, AUCTION, ad-set budgets (ABO), copy settings from the previous month's campaign.
6. **Ad sets** – one per product, name = product name. Settings below.
7. **Budget** – monthly ILS budget ÷ current USD/ILS rate ÷ remaining days = total daily USD. Fixed amounts first (e.g. i-Spin $60/day), the rest split equally. End time = last day of month 23:59.
8. **Ads** – name = product name, square banner, text from column C, headline "לפרטים ורכישה >>", CTA Shop Now, link from column D. No AI disclosure. Build one example first, approve, then the rest.
9. **Manual in Ads Manager** – per ad: Instagram identity = babystav; Stories/Status/Reels → upload the 9:16 banner.
10. **Launch** – turn on ads (and any paused ad sets).

## Ad set template (October 2026)
- Optimization: Purchase (pixel above), Highest volume, billing Impressions
- Attribution: 7-day click, 1-day view, 1-day engaged view
- Audience: women, hard min age 25, Advantage+ audience with age suggestion 25–40
- Location: Israel (people living in / recently in), exclusions: Eilat 25 mi + 12 southern custom points (copy from previous ad set)
- Placements (manual): Facebook Feed/Stories/Reels, Instagram Feed/Stories/Reels, WhatsApp Status; mobile + desktop

## Known connector limits (as of Oct 2026)
- Two sizes in one ad (Placement Customization) – blocked for this account → 9:16 added manually.
- Uploading to the image library – blocked → ads pull images from raw GitHub URLs.
- Instagram account not exposed (Page↔IG connection needs "Review this connection" in Ads Manager).
- Reading Ads Manager drafts – blocked → publish a draft before Claude can read it.
- New ad sets get "frequently in" added to location types by Meta automatically.
