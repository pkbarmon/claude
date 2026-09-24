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

## Selected Vecteezy photos (non-AI filter on, picked 2026-09-24)

The Vecteezy non-AI library has almost no real luau or hula photos, so some picks are the closest honest match. The alt text below describes what each photo **actually shows**, and replaces the draft alt text above.

| Filename | Vecteezy ID | Actual alt text |
|---|---|---|
| blog-luau-cost-buffet.jpg | 11925389 | Guest serving herself from a resort dinner buffet |
| blog-cheapest-luau-sunset-lawn.jpg | 28627069 | Person silhouetted on a Hawaiʻi beach at sunset with palm trees on the point |
| blog-luau-start-time-sunset-palms.jpg | 1240675 | Palm trees silhouetted against a Hawaiian sunset over the ocean |
| blog-luau-seating-tables.jpg | 12828058 | Long outdoor dinner table set by the ocean with hanging candle jars |
| blog-open-bar-mai-tai.jpg | 8345296 | Layered red and orange tropical cocktail on a green leaf |
| blog-luau-rain-tropical-leaves.jpg | 6893469 | Raindrops on a green banana leaf |
| blog-luau-drive-coastal-highway.jpg | 1271685 | Aerial view of a coastal highway winding above a rocky shoreline |
| blog-luau-worth-it-hula.jpg | 1310198 | Palm trees and a fire pit at a beachfront resort at dusk |
| blog-luau-vegetarian-fruit.jpg | 79107079 | Platter of fresh pineapple, kiwi, oranges and grapes |
| blog-myths-vs-huakai-polynesian-dance.jpg | 2304987 | Fire performer spinning flames on a beach at night |
| blog-book-luau-calendar.jpg | 5205615 | Calendar with vacation dates circled in red |
| blog-luau-discounts-budget.jpg | 3492749 | Travel savings jar with coins on a world map |
| blog-best-time-maui-beach.jpg | 17535305 | Waves breaking on a sunny Maui beach |
| blog-luau-etiquette-lei.jpg | 1307626 | Rows of colorful Hawaiian flower leis |
| blog-what-to-wear-aloha-shirt.jpg | 11916247 | Couple in casual summer clothes walking on a tropical beach |
| blog-imu-kalua-pig.jpg | 14537447 | Whole roasted pig on a spit, similar to the kalua pig served at a luau |
| blog-wailea-beach-sunset.jpg | 1226104 | Sunset over Mākena Beach in South Maui, next to Wailea |
| blog-kaanapali-beach-sunset.jpg | 3370718 | Sunset over the ocean from West Maui, with palm trees in the foreground |
| blog-kaanapali-fire-knife-dancer.jpg | 7353623 | Fire spinner reflected in water among palm trees at night |
| blog-grand-wailea-premium-seating.jpg | 56315425 | Oceanfront table set for two with wine and flowers |
| blog-maui-vs-oahu.jpg | 3540094 | View from Diamond Head across Oʻahu's green hills to the ocean |
| blog-first-timer-luau-guests.jpg | 10203766 | Hand holding a pineapple wearing heart sunglasses on a beach |
| blog-luau-food-poi-plate.jpg | 5225826 | Hawaiian poke bowl with salmon, rice and vegetables |
