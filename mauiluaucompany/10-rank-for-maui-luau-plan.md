# Plan: rank mauiluaucompany.com for "maui luau" (US Google)

**Where we are:** "maui luau" averages position 67.9 (320 impressions, 0 clicks, Sept 2026 GSC export). Close variants: "luau maui" 49.6, "maui luaus" 68.7, "luau in maui" 41.1, "best luau in maui" 52.5. The domain went live in June 2026, so it's about 4 months old.

**Who's on page 1** (US results, Oct 2026): first-hand review blogs (thehawaiivacationguide.com, campfiresandconcierges.com, scenicandsavvy.com), official operator sites (oldlahainaluau.com, sheratonmauiluau.com, **huakailuau.com**, which is your own show), and OTAs (Travelocity, Expedia). Google treats "maui luau" as a mixed review-and-booking search, so it rewards first-hand experience and trusted domains.

---

## Why we're stuck at 60+ (from the GSC export and the live code)

| # | Problem | Evidence | Impact |
|---|---|---|---|
| 1 | **The www and non-www versions are both indexed separately.** | GSC lists the same pages twice, e.g. `mauiluaucompany.com/` (pos 28, 457 impr) and `www.mauiluaucompany.com/` (pos 32, 647 impr), and both versions of `/best-maui-luaus`, `/activities` and the Sugar Beach page. Both A records point at Lovable, so the apex domain isn't redirecting. | Ranking signals and links are split in half across every page. |
| 2 | **Three pages compete for the same query.** | Home title: "Best Maui Luaus 2026: Reviews, Prices & Booking". `/best-maui-luaus`: "Best Maui Luaus 2026: Compared, Ranked, Booking Tips". Plus `/best-maui-luaus/2026-rankings`. | Google can't tell which page should rank, so none of them do. |
| 3 | **No page targets the exact head term "Maui Luau".** | Every title leads with "Best Maui Luaus". The homepage H1 doesn't lead with "Maui Luau". | The exact head term is weaker than the "best" variant. |
| 4 | **Weak authority: a new domain with few backlinks.** | The domain is about 4 months old. Page 1 competitors have years of links. | This is the biggest gap. On-page fixes alone won't reach the top 10. |
| 5 | **Trust problems on the page.** | Future "updated" dates (`LAST_UPDATED = "November 2026"`, blog cards dated 2026-11-01). Out-of-date prices (Old Lahaina $145 vs about $230 now). FAQs that contradict each other (best for families = Drums/Myths on one page, Huaka'i on others). No named reviewers or first-hand photos. | It hurts E-E-A-T (Google's experience-and-trust signals) against first-hand review blogs. |

---

## Fix plan in priority order

### Week 1: technical fixes (Lovable plus domain settings)
1. **Pick www as the one version and 301-redirect the apex domain to it.** In Lovable go to **Project → Settings → Domains** and set `www.mauiluaucompany.com` as **Primary**, so `mauiluaucompany.com` redirects to it. Check that `curl -I https://mauiluaucompany.com/best-maui-luaus` returns `301 → https://www.…`. In GSC, use the Domain property, and resubmit `https://www.mauiluaucompany.com/sitemap.xml`.
2. **Give each page one job:**
   - **Homepage → "maui luau"** (exact-match domain, and already the best-ranking page).
   - `/best-maui-luaus` → "best maui luau(s)" / "best luau in maui".
   - `/best-maui-luaus/2026-rankings` → 301 into `/best-maui-luaus`, then remove it from the sitemap and nav.
3. **Remove future dates.** Set `LAST_UPDATED` and every card date to the real edit date.

### Weeks 1–2: homepage on-page work for "maui luau"
- **Title (≤60 chars):** `Maui Luau 2026: Compare Prices & Book Every Luau on Maui`
- **Meta description:** `Every Maui luau compared in one place: Old Lahaina, Grand Wailea, Myths of Maui, Huakaʻi and more, from $100. Real 2026 prices, show times and live booking.`
- **H1:** `Maui Luau Guide 2026: Compare and Book Every Luau on Maui`
- **First 60 words (direct answer):** "A Maui luau is an evening Hawaiian feast and Polynesian show held at oceanfront resorts in Kāʻanapali, Lahaina, Wailea and Kīhei. In 2026 adult tickets run from $100 to about $360. Below we compare all 11 Maui luaus by price, setting, food and who each suits, with live availability for the ones we sell."
- **Sections to add or tighten on the homepage:**
  - one comparison table of **every** Maui luau (all 11: Old Lahaina, Grand Wailea, Myths of Maui, Huakaʻi, Drums of the Pacific, Wailele, Maui Nui, Te Au Moana, Feast at Mōkapu, Aloha Wailea, Sugar Beach; not only the ones the site sells)
  - "Maui luau by area" (links to the location pages)
  - "How much is a Maui luau" (short, linking to the cost post)
  - "When to book"
  - a 6–8 question FAQ
- **Schema:** `ItemList` of all luaus, `FAQPage`, and `Organization` with `sameAs` (social profiles once they exist).
- **Internal anchors:** change sitewide nav or footer text and blog links that point to the homepage to read **"Maui luau"** or **"Maui luau guide"**. Keep "best Maui luaus" anchors pointing to `/best-maui-luaus`.

### Weeks 2–6: experience and trust (E-E-A-T)
- **Name the reviewers.** Add an author box with a real name, photo and "attended N Maui luaus" on the homepage, `/best-maui-luaus` and the venue pages, plus an `/about` page with the team's Hawaiʻi credentials.
- **Use first-hand photos and notes.** Attend or re-attend the top 4–5 luaus, shoot your own photos (seating view, food, show), and add a dated "We went: [date]" paragraph to each venue page. This is what page-1 blogs have that the site lacks.
- **Fix the data errors** listed in `00-content-gap-analysis.md`: Old Lahaina price and format, Te Au Moana's name and price, Feast at Mōkapu price, Hilton page, Myths location and length, and the family-pick contradictions.
- **Keep the Huakaʻi disclosure.** It's an honest trust signal.

### Months 1–6: authority (backlinks), the biggest lever
Aim for 15–30 relevant, editorial referring domains over 3–6 months:
1. **Your own network, used sparingly:**
   - a contextual link from **huakailuau.com** (already on page 1), e.g. "Compare all Maui luaus"
   - a link from hawaiian-activities.com's Maui luau guide
   - no sitewide links
2. **Operator and partner pages:** ask the luaus you sell (Sugar Beach Events, Royal Lahaina, Grand Wailea) for a mention or link on their "where to buy tickets" or partner page.
3. **Hawaiʻi and Maui travel blogs:** pitch a guest post or data piece. For example, a "2026 Maui luau price index" that tracks every show's price, which bloggers like to cite and link.
4. **Digital PR and HARO-style requests** (Connectively, Qwoted, Featured): answer travel journalists' questions about luaus and Maui as the expert.
5. **Local citations:** Maui Visitors Bureau/GoHawaii listings if eligible, Hawaiʻi business directories, Google Business Profile (if allowed for an affiliate/ticket seller), Yelp.
6. **Avoid** bought link packages and PBNs. A 4-month-old domain is easily hit by link penalties.

### Ongoing: supporting content
Keep publishing pages that link back to the homepage with "Maui luau" anchors, such as the comparison posts, the hotel and discount posts, and the Luau Finder copy, then merge or redirect thin pages that overlap. Refresh the homepage table monthly, because recent updates with real dates help on travel queries.

---

## What to expect
- **Weeks 2–6 after the redirect and consolidation:** "maui luau" should move from about 68 to the 30–40 range as split signals combine. That's the typical effect, not a guarantee.
- **Months 3–6 with steady links and E-E-A-T work:** page 2, and the long tail ("luau in maui", "maui luau tickets", "luau maui kaanapali") reaches page 1 first.
- **The top 10 for "maui luau"** realistically takes 6–12 months, mainly depending on links. The page-1 competitors are older domains.

## Measuring progress
Each week in GSC, filter the Query to exactly `maui luau`, compare against the Page `https://www.mauiluaucompany.com/`, and track average position, impressions and CTR. Also watch whether the non-www URLs drop out of the Pages report, which confirms the redirect worked.

Sources: [The Hawaii Vacation Guide](https://thehawaiivacationguide.com/activities/best-luaus-maui/), [Campfires & Concierges](https://www.campfiresandconcierges.com/maui-luau/), [Scenic and Savvy](https://www.scenicandsavvy.com/old-lahaina-best-luau-in-maui-review/), [Old Lahaina Luau](https://oldlahainaluau.com/), [Maui Nui Luau](https://www.sheratonmauiluau.com/), [Huakaʻi Lūʻau](https://huakailuau.com/)
