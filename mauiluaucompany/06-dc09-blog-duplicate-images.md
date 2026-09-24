# DC-09 "Aloha Luaus": duplicate blog images audit + Vecteezy download list

Project: `61984924-a48c-49ec-a27a-f2559f8dbb17` (workspace DC-09). Audited 2026-09-24.

## Findings: 22 blog posts share 4 images

| Image asset (current) | Posts using it | Count |
|---|---|---:|
| `hero-luau-sunset.png` (also the homepage hero) | open bar, rain, worth it, vegetarian, how far in advance, etiquette/tipping, imu ceremony, food guide, **wailea-luaus-compared**, **kaanapali-luaus-compared** | 10 |
| `best-time-maui-luau-featured.png` | cost, cheapest, what time, parking, best time to book | 5 |
| `hero-dancer.jpg` | seating guide, discounts/promo codes, what to wear, first-timer tips | 4 |
| `maui-vs-oahu-luau-featured.png` | Myths vs Huaka'i, Grand Wailea premium vs standard, Maui vs Oahu | 3 |

Other duplicates inside posts:
- `kaanapali-luaus-compared`: hero (`/img/hero-luau-sunset-1200.webp`) and inline "fire knife dancer" figure (`/hero-luau-sunset.webp`) are **the same sunset photo**, and the inline alt text describes a fire-knife dancer that isn't in the photo.
- `wailea-luaus-compared`: reuses the same homepage sunset for its hero and og:image.
- `blog.$slug.tsx`: the og:image for Maui vs Oahu and Best Time reuses the card images above. The other dynamic posts (imu, food guide, tips) have no og:image.
- Most standalone posts have no hero photo and no og:image (gradient header only). Social shares show no image.

## Vecteezy download list (one unique image per post)

On Vecteezy, turn on **"Exclude AI-generated"**, and download landscape images at least 1600px wide. Rename each file to the filename below, then upload them in the Lovable chat for the DC-09 project. The prompt already sent tells Lovable to wire them up by filename.

| # | Post slug | Vecteezy search | Filename | Alt text |
|---|---|---|---|---|
| 1 | how-much-does-a-maui-luau-cost | `hawaii luau buffet` | `blog-luau-cost-buffet.jpg` | Hawaiian luau buffet table with kalua pork and tropical sides |
| 2 | cheapest-maui-luaus | `maui beach sunset people` | `blog-cheapest-luau-sunset-lawn.jpg` | Guests on an oceanfront lawn at sunset in Kihei, Maui |
| 3 | what-time-do-maui-luaus-start | `maui sunset palm trees` | `blog-luau-start-time-sunset-palms.jpg` | Palm trees silhouetted against a Maui sunset before a luau |
| 4 | maui-luau-seating-guide | `luau tables ocean` | `blog-luau-seating-tables.jpg` | Rows of luau dinner tables facing the ocean and stage |
| 5 | maui-luaus-with-open-bar | `mai tai cocktail beach` | `blog-open-bar-mai-tai.jpg` | Mai tai cocktail with a pineapple garnish at a beach bar |
| 6 | do-maui-luaus-cancel-for-rain | `tropical rain leaves` | `blog-luau-rain-tropical-leaves.jpg` | Raindrops on tropical leaves during a passing Maui shower |
| 7 | maui-luau-parking-and-drive-times | `maui coastal highway` | `blog-luau-drive-coastal-highway.jpg` | Coastal highway along the West Maui shoreline |
| 8 | is-a-maui-luau-worth-it | `hula dancers stage` | `blog-luau-worth-it-hula.jpg` | Hula dancers performing on a luau stage |
| 9 | maui-luau-vegetarian-vegan-gluten-free | `tropical fruit platter` | `blog-luau-vegetarian-fruit.jpg` | Platter of fresh pineapple, papaya and tropical fruit |
| 10 | myths-of-maui-vs-huakai-luau | `polynesian dance performance` | `blog-myths-vs-huakai-polynesian-dance.jpg` | Polynesian dancers in traditional costume on an oceanfront stage |
| 11 | how-far-in-advance-to-book-a-maui-luau | `calendar travel planning` | `blog-book-luau-calendar.jpg` | Travel calendar and planner used to book a Maui luau |
| 12 | myths-of-maui-luau-discounts-and-promo-codes | `vacation budget money travel` | `blog-luau-discounts-budget.jpg` | Travel budget with cash and a notebook for a Hawaii trip |
| 13 | best-time-to-book-maui-luau | `maui beach summer` | `blog-best-time-maui-beach.jpg` | Sunny Maui beach in peak summer season |
| 14 | luau-etiquette-and-tipping-guide | `flower lei greeting` | `blog-luau-etiquette-lei.jpg` | Fresh flower lei offered as a luau welcome |
| 15 | what-to-wear-to-a-maui-luau | `aloha shirt hawaiian dress` | `blog-what-to-wear-aloha-shirt.jpg` | Aloha shirt and floral sundress laid out for a Maui luau |
| 16 | what-is-an-imu-ceremony | `kalua pig imu` or `hawaiian pig roast` | `blog-imu-kalua-pig.jpg` | Kalua pig being unearthed from a Hawaiian imu pit |
| 17 | wailea-luaus-compared | `wailea beach` | `blog-wailea-beach-sunset.jpg` | Sunset over Wailea Beach in South Maui |
| 18 | kaanapali-luaus-compared (hero) | `kaanapali beach` | `blog-kaanapali-beach-sunset.jpg` | Sunset over Ka'anapali Beach with Lāna'i on the horizon |
| 18b | kaanapali-luaus-compared (inline) | `fire knife dancer` | `blog-kaanapali-fire-knife-dancer.jpg` | Samoan fire knife dancer performing at dusk |
| 19 | grand-wailea-luau-premium-vs-standard-seating | `resort luau dinner table` | `blog-grand-wailea-premium-seating.jpg` | Front-row reserved luau table set for dinner near the stage |
| 20 | maui-luau-vs-oahu-luau | `oahu diamond head` + `maui coastline` (pick one) | `blog-maui-vs-oahu.jpg` | Hawaiian coastline comparing Maui and Oahu luau settings |
| 21 | maui-luau-tips-first-timers | `luau hawaii tourists` | `blog-first-timer-luau-guests.jpg` | First-time guests greeted with leis at a Maui luau |
| 22 | maui-luau-food-guide | `poi taro hawaiian food` | `blog-luau-food-poi-plate.jpg` | Plate of poi, lomi salmon and kalua pork at a Maui luau |
