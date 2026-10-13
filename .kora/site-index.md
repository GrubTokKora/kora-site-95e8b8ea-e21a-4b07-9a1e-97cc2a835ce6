# Site index · format 2
Structure and the names of what each page offers. Values that change often — prices, hours, phone,
address — and body copy are deliberately not recorded here; read the page itself for those.

## index.html → /
title: Bedford Thai — Authentic Thai Curry, Soup & Salads in Stamford
purpose: The whole site — a one-page restaurant site carrying the full menu, hours, location, gallery, reviews and FAQ.
sections:
- `#heroMedia` — hero image, restaurant name, tagline and the order-online call to action
- `#about` "About Bedford Thai" — the restaurant's story and cooking approach
- `#menu` "Explore Our Flavors" — the full menu, split into the eleven category blocks below
- `#appetizer` "Appetizer" — 15 priced items: Edamame, Vegetable Spring Roll, Chicken Cashew Wrap, Roti Canai, Crab Rangoon, Curry Puff, Po Pia Sod, Shrimp Summer Roll, Táo Hoo Tord, Dumpling, Chicken Satay, Chicken Wing, Lime Chili Shrimp, Crispy Calamari, Kong Tod
- `#soup` "Soup" — 4 priced items: Tom Yum Goong, Tom Kha Gai, Sweet Corn Soup, Vegetable Soup
- `#salad` "Salad" — 6 priced items: Thai Salad, Somtum, Larb, Nua Nam Tok, Duck Salad, Yum Woon Sen
- `#chef-special` "Chef Special" — 14 priced items: Sizzling Pancake, Seafood Delight, Pla Rad Prik, Pla Sam Rod, Salmon Mango Curry, Steamed Ginger Fish, Pineapple Duck Curry, Duck Choo Chee, Duck Ga Prow, Peanut Shrimp Curry, Pra Raam Chicken, Shaking Beef, Laksa Shrimp, Garlic Eggplant Asparagus
- `#noodle-rice` "Noodle Plate or Rice Plate" — a lunch/dinner price table by protein, then 9 dishes: Pad Thai, Drunken Noodles, Pad See Ew, Pad Woon Sen, Mee Goreng, House Fried Rice, Spicy Fried Rice, Pineapple Fried Rice, Nasi Goreng
- `#noodle-soup` "Noodle Soup" — a lunch/dinner price table by protein, then 2 dishes: Noodle Soup, Sour and Spicy Noodle Soup
- `#wok` "From the Wok" — a lunch/dinner price table by protein, then 7 preparations: Basil, Cashew Nut, Ginger, Garlic, Sambal, Sweet and Sour, Broccoli
- `#curry` "Curry" — a lunch/dinner price table by protein, then 9 curries: Rendang, Red Curry, Green Curry, Penang Curry, Mango Curry, Yellow Curry, Masaman Curry, Jungle Curry, Pineapple Curry
- `#side` "Side Dishes" — 9 priced items: Fried Egg, Jasmine Rice, Add Tofu, Thai Sticky Rice, Steamed Vegetables, Brown Rice, Peanut Sauce, Prik Nam Pla, Roti
- `#desserts` "Desserts" — 3 priced items: Mango Sticky Rice, Fried Banana, Coconut Pudding
- `#beverages` "Beverages" — 8 priced items: Thai Ice Tea, Coke, Diet Coke, Sprite, Ginger Ale, Perrier, Mango Juice, Lychee Juice
- `#hours` "Opening Hours" — the weekly opening hours, one row per day
- `#location` "Find Us" — street address and a directions link
- `#gallery` "A Taste of Thailand" — photographs of the restaurant and its dishes, opened in a lightbox
- `#reviews` "What Our Customers Say" — customer review quotes
- `#faq` "Frequently Asked Questions" — an accordion covering: reservations, vegetarian or vegan options, parking
also: Every FAQ question and answer is written twice — once in the visible accordion and once inside a JSON-LD FAQPage block. Changing one and not the other leaves the page and its structured data disagreeing, and nothing on screen shows it.
also: Each side dish additionally carries its own id of the form side-dishes-<slug>, so a side dish can be linked to directly; renaming one leaves that id pointing at the old name.
also: Menu rows repeat the same markup per dish, so a change to one row's structure has to be made to every row in that category.

## support files
Files that are not pages. A line marked [content] holds words or data a visitor reads, so a
change to the site's content can land there; the rest only make the site work or look right.
- `robots.txt` — crawler rules and the sitemap link — derived from the site by the deploy, not written by hand
- `sitemap.xml` — the list of page URLs — derived from the site by the deploy, not written by hand

## shared (every page)
The header, navigation, mobile menu and footer are propagated from index.html to every other page by
`shell_propagation`. A change to any of them is made on index.html alone and copied automatically.
