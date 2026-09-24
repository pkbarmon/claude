# mauiluaucompany.com: Content Gap Analysis (GSC, Sept 2026)

**Source data:** GSC Performance on Search export, Pages + Queries, pulled 2026-09-24.
**Site:** Lovable project "Aloha Luaus" (`5f078018-a623-4efc-b2cd-e2c54bad766c`), 21 blog posts, 11 venue pages, 5 location pages, 8 experience pages.

## How the gap was found

1. Grouped all 1,000 queries into topic clusters by regex pattern (script in session).
2. For each cluster: total impressions, clicks, impression-weighted average position.
3. Mapped each cluster against existing URLs in the Lovable codebase (`src/routes/*`, `BLOG_POSTS`, `VENUE_CATALOG`).
4. A **gap** is a cluster with real impressions, near-zero clicks, and either no page built for that intent or only a page built for a different intent. Example: a location hub ranking for "which is best" comparison searches.

## Cluster table

| Cluster | Queries | Impr. | Clicks | Avg pos | Existing coverage | Verdict |
|---|---:|---:|---:|---:|---|---|
| Kaanapali / Black Rock / resort luaus | 146 | 1,296 | 1 | 31.4 | Location hub + venue pages; no comparison | **GAP #1** |
| Wailea / South Maui | 118 | 1,047 | 4 | 50.3 | Location hub (pos 45), venue pages; no comparison | **GAP #2** |
| "Does [hotel] have a luau" | 103 | 478 | 1 | 34.8 | Scattered venue pages; Hilton page says Hilton has no luau (wrong, see below) | **GAP #3** |
| Discounts / deals / cheap | 84 | 442 | 2 | 31.5 | Myths-of-Maui-only promo post + cheapest post | **GAP #4** (all-venue) |
| Feast at Lele + Lahaina "is it open" | 32+ | 346 | 2 | 23.3 | Venue page `/luau-companies/feast-at-lele` | **GAP #5** (status/alternatives intent) |
| Old Lahaina Luau price/menu/tickets | 68 | 365 | 3 | 28.5 | Venue page (pos 10) | Update venue page, not new post |
| Cost / price | 53 | 305 | 2 | 49.0 | `how-much-does-a-maui-luau-cost` (pos 16–24) | Refresh existing |
| Food / menu | 51 | 258 | 1 | 40.8 | `maui-luau-food-guide` (only 3 thin sections) | Expand existing |
| Kihei / Sugar Beach | 32 | 233 | 16 | 29.2 | Sugar Beach activity page (best page on site) | Healthy; expand Kihei hub |
| Imu | 30 | 203 | 1 | 24.4 | `what-is-an-imu-ceremony` | Covered |
| Weddings / private / events | 20 | 187 | 0 | 51.1 | Experience page only | Next batch |

## The 5 posts in this batch

| # | File | Target slug | Primary keyword cluster | Why it wins |
|---|---|---|---|---|
| 1 | `01-kaanapali-luaus-compared.md` | `/blog/kaanapali-luaus-compared` | kaanapali luau, kaanapali beach luau, luau near kaanapali, best luau in kaanapali | 1,296 impressions and 1 click. People are comparing, and no page compares. |
| 2 | `02-wailea-luaus-compared.md` | `/blog/wailea-luaus-compared` | wailea luau, wailea resort luau, wailea marriott luau, luau near wailea | 1,047 impressions at position 50. The location hub can't rank for "best/compare" searches. |
| 3 | `03-maui-resorts-with-a-luau.md` | `/blog/maui-hotels-with-a-luau` | hilton luau maui, four seasons maui luau, hyatt/westin/sheraton/andaz luau | Yes/no questions like these are exactly what AI answer engines quote |
| 4 | `04-maui-luau-discounts.md` | `/blog/maui-luau-discounts` | royal lahaina luau discount, maui luau deals, costco, military, kamaaina, promo code | Covers every venue. The existing promo post covers Myths of Maui only. |
| 5 | `05-is-feast-at-lele-open.md` | `/blog/is-feast-at-lele-open` | feast at lele, feast at lele luau, is old lahaina luau open, lahaina luau | Many searchers still look for a closed venue, so this post redirects them to open luaus they can book |

## Cannibalization guards

- Posts 1 and 2 target **comparison** searches ("compared", "best", "which"). The location hubs keep **navigational** searches ("luau in kaanapali"). Each post links to its hub in the first 150 words, and each hub should link back with the anchor "Kaanapali luaus compared" or "Wailea luaus compared".
- Post 4 links to `myths-of-maui-luau-discounts-and-promo-codes` and `cheapest-maui-luaus` for the deep dives rather than repeating them.
- Post 5 targets status intent ("is it open", "closed"). The `/luau-companies/feast-at-lele` venue page should get a status banner that links to it.

## Data problems found in the site (fix before or with publishing)

These came up while fact-checking. Several are live on the site now.

1. **Old Lahaina Luau price and format.** `venue-catalog.ts` says $145–$170 with a buffet. Current 2026 third-party reports put it around **$230** with a **four-course family-style** dinner ([hawaiitravelwithkids.com](https://hawaiitravelwithkids.com/old-lahaina-luau/), [hawaii-guide.com](https://www.hawaii-guide.com/blog/visiting-lahaina-whats-open)). Verify on oldlahainaluau.com and update.
2. **Wailea Marriott luau name.** `venue-catalog.ts` calls it the "Honuaula Luau" and says Te Au Moana is the old name. The resort's official site still markets it as **Te Au Moana**, with a three-course tableside dinner ([teaumoana.com](https://www.teaumoana.com/)). Swap the primary name.
3. **"Hilton does not operate its own luau on Maui."** Wrong in spirit. Huaka'i Luau runs at **Hilton Vacation Club Ka'anapali Beach** (per your own `activities-data.ts`). The Grand Wailea is a Waldorf Astoria, which is also Hilton. Rewrite `/luau-companies/hilton-maui-luau`.
4. **Four Seasons Maui.** It runs a **Family Luau** (communal tables, coursed family-style menu, about 5 minutes' drive from the resort) ([fourseasons.com](https://www.fourseasons.com/maui/experiences/local-experiences/family-luau/)). The site has no page for it despite queries.
5. **Myths of Maui duration.** `activities-data.ts` says 2.5 hours and `venue-catalog.ts` says 5 hours. Pick one.
6. **Myths of Maui location.** Listed under Lahaina in the activity data. The Royal Lahaina Resort (2780 Kekaa Dr) is in **Ka'anapali**. That mismatch hurts the "kaanapali luau" cluster.
7. **Kaanapali Beach Hotel** is now **Outrigger Kā'anapali Beach Resort**. Queries for "kaanapali beach hotel luau / hula show" (23+ impressions) have no page.
8. `LAST_UPDATED = "November 2026"` in `venue-catalog.ts` is a future date (today is September 2026). Google and AI engines can treat future "updated" dates as a trust problem.

## Images (Vecteezy)

Vecteezy is blocked from this environment's network, so I couldn't download or license images. Each post has an **Image plan** table with the exact Vecteezy search term, a filename, and alt text. To stay non-AI on Vecteezy, turn on the **"Exclude AI-generated"** filter (Vecteezy labels AI content). Download with your account, then upload through Lovable.
