# DC-09 "Aloha Luaus": orphan and weakly linked blog posts (2026-09-26)

Source: a read-only link-graph script run in the Lovable sandbox (commit `760072c`) over all of `src/`. It covers 24 posts: 19 standalone routes plus 6 from `BLOG_POSTS`. Sitemap, JSON-LD, canonical and self-links are not counted. Links from the `/blog` index are shown separately.

## Orphans

| Post | From other posts | From non-blog pages | Blog index | Status |
|---|---:|---:|:-:|---|
| myths-of-maui-vs-huakai-luau | 0 | 0 | yes | **Orphan: only the /blog index links to it.** It gets real GSC clicks (4 clicks, 108 impressions) |

## Weak: only 2–3 links, all from other blog posts (no hub, venue or home links)

| Post | Inbound from | Total |
|---|---|---:|
| is-a-maui-luau-worth-it | cheapest-maui-luaus, maui-luau-discounts | 2 |
| kaanapali-luaus-compared | maui-hotels-with-a-luau, wailea-luaus-compared | 2 |
| wailea-luaus-compared | maui-hotels-with-a-luau, maui-luau-discounts | 2 |
| maui-luau-vegetarian-vegan-gluten-free | is-a-maui-luau-worth-it, myths-of-maui-vs-huakai-luau (itself an orphan) | 2 |
| maui-hotels-with-a-luau | kaanapali, wailea, discounts posts | 3 |
| maui-luau-discounts | kaanapali, wailea, hotels posts | 3 |

The 2026-09-24 posts (Kaanapali, Wailea, hotels, discounts) only link to each other, so they form a closed loop with no way in from the site's hub pages.

## No links from any non-blog page (blog-to-blog only)
cheapest-maui-luaus (5), maui-luau-seating-guide (6), maui-luaus-with-open-bar (4), maui-luau-tips-first-timers (~2 real; counts from `blog.$slug.tsx` run high). None of these are linked from a hub, venue or home page, even though the seating and open-bar posts are among the top GSC pages.

## Other findings
- Broken `/blog/` links: none. The only hit is a code comment in `page-dates.ts`.
- `blog.kaanapali-luaus-compared.tsx` "Keep planning" links **"Compare Wailea luaus"** to `/maui-luau-locations/wailea`, not `/blog/wailea-luaus-compared`. It also links "See which Maui resorts host a luau" to `/luau-companies`, not `/blog/maui-hotels-with-a-luau`.
- The location hubs (`/maui-luau-locations/kaanapali`, `/wailea`) don't link to the comparison posts. The gap report had asked for these links to prevent cannibalization.

## Recommended links to add
| Target post | Add a link from |
|---|---|
| myths-of-maui-vs-huakai-luau | kaanapali-luaus-compared (Myths and Huaka'i sections), luau-companies/myths-of-maui-royal-lahaina, the Huaka'i venue page, cheapest-maui-luaus, best-maui-luaus |
| kaanapali-luaus-compared | maui-luau-locations/kaanapali + /west-maui, venue pages for Hyatt, Westin, Sheraton, Maui Nui and Myths of Maui, best-maui-luaus |
| wailea-luaus-compared | maui-luau-locations/wailea + /kihei, venue pages for Grand Wailea, Andaz and Honua'ula, grand-wailea premium-vs-standard post; fix the Kaanapali post's "Compare Wailea luaus" link |
| maui-hotels-with-a-luau | /luau-companies index, the Hilton venue page, plan-your-maui-luau; fix the Kaanapali post's resorts link |
| maui-luau-discounts | myths-of-maui-luau-discounts-and-promo-codes, cheapest-maui-luaus, how-much-does-a-maui-luau-cost |
| is-a-maui-luau-worth-it | homepage, plan-your-maui-luau, best-maui-luaus, maui-luau-tips-first-timers |
| maui-luau-vegetarian-vegan-gluten-free | maui-luau-food-guide, venue-page "Keep planning", best-for-kids / best-for-families experience pages |
| maui-luau-seating-guide, maui-luaus-with-open-bar, cheapest-maui-luaus | venue-page "Keep planning" block, best-maui-luaus |
