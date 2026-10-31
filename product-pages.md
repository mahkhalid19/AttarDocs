---
title: Product pages
description: Set up ATTAR's product page, its blocks, media gallery, scent notes and note ribbon, reviews, recommendations and the compare page.
---

The product page is built from four sections that you edit in the theme editor:

| Section | What it shows |
|---|---|
| **Product** | The media gallery and the buy column: title, price, size and option pickers, buy buttons and the other blocks below. |
| **Product highlights** | Cards below the gallery and buy column: scent pyramid, pairs well with, discovery set and trust badges. |
| **Product reviews** | Your rating summary and review quotes, or your review app's block. |
| **Product recommendations** | A row of related or complementary products. |

To edit them, go to Online Store › Themes › **Edit theme**, then choose Products › Default product from the page selector at the top of the editor. Changes apply to every product that uses this template. To give some products a different layout, create another product template from the same menu and assign it to those products in Shopify admin (the product's **Theme template** field).

Most text the theme shows on its own (headings such as "You may also like") is translated for English and Arabic. Where a block has a **Heading** or **Text** setting, leave it blank to keep the translated default in every language.

## Product section settings

Online Store › Themes › **Edit theme** › Products › Default product › **Product** section.

| Setting | Default | What it does |
|---|---|---|
| **Show breadcrumbs** | On | Shows Home › collection › product above the gallery. The collection is the one the shopper came from; otherwise the collection that matches the product's scent family; otherwise the product's first collection. |
| **Mobile layout** | **Swipe carousel with dots** | Or **Stacked images**. |
| **Desktop layout** | **Large image with thumbnails** | Or **Stacked images**. |
| **Show sticky add-to-bag bar on mobile** | On | See [Sticky add-to-bag bar](#sticky-add-to-bag-bar). |

## Blocks in the buy column

Add, remove and reorder blocks inside the **Product** section. The default template has, in order: **Title and rating**, **Price**, **Description**, **Variant picker**, **Gift option**, **Buy buttons**, **WhatsApp order**, **Two-size bundle**, **Stock line**, two **Collapsible tab** blocks and **Complementary products**. Blocks marked "one per section" below can be added only once.

### Title and rating

One per section. Shows the product title as the page heading, with:

- above it, the scent family (product metafield `attar.family`) and, when **Show SKU** is on, the selected variant's SKU;
- below it, when **Show subtitle (metafield attar.title_alt, else attar.subtitle)** is on, the product's name in the other script (`attar.title_alt`) or, if that's empty, its subtitle (`attar.subtitle`);
- the star rating and review count, when a review app has filled in the standard rating metafields. The rating links to the **Product reviews** section.

### Price

One per section. Shows the selected variant's price, its compare-at price (struck through) when it's higher, the price per ml, and "VAT included" when your prices include tax.

The price per ml uses Shopify's unit price when you've set one on the variant in Shopify admin. Otherwise it's worked out from the variant metafield `attar.volume_ml`. With neither, no unit price shows. See [Product data](#product-data-metafields).

### Description

One per section. **Text** chooses the source:

- **Story (metafield attar.story), else description** (default): the short editorial paragraph in `attar.story`, or the product description when the story is empty.
- **Product description**: always the description from Shopify admin.

### Variant picker

One per section. Shows one group of choices per product option. Products with a single variant don't show it.

- An option whose name contains "size" or "volume" (or the Arabic حجم or سعة) shows each size as a tile with its price and price per ml. When two or more available sizes have different `attar.volume_ml` values, the group heading adds "Best price per ml:" and the size with the lowest price per ml.
- **"What's the difference?" link**: a page link shown beside every option that isn't a size, for example a guide to concentrations.
- **Show swatches**: shows the color or image swatch you set for an option value in Shopify admin. Values without a swatch keep the plain label. Turn it off to show text labels only. See [Color swatches](#color-swatches).

Choosing an option updates the price, SKU, stock line, pickup availability and the page address (so a shared link opens the same variant), and moves the gallery to that variant's image.

In Arabic, sizes and prices follow your numeral setting (Theme settings › **Numerals** › **Numeral system**) and stay readable in right-to-left text. See [Languages and right-to-left]({{ site.baseurl }}/languages-and-rtl/).

### Buy buttons

One per section. The "Add to bag" button (with the price), plus:

| Setting | Default | What it does |
|---|---|---|
| **Show quantity selector** | On | Minus and plus buttons around a quantity field. |
| **Show dynamic checkout buttons** | On | Shop Pay, Apple Pay, Google Pay and the other express methods you've turned on in Settings › Payments. |
| **Show recipient form for gift cards** | On | On gift card products, lets the shopper send the card to someone by email with an optional message and send date. Dynamic checkout buttons are hidden on gift card products while the form shows. |
| **Show pickup availability** | On | See [Pickup availability](#pickup-availability). |

When you've turned on Shop Pay Installments, its message shows above the buttons in this block.

If a shopper asks for more than you have in stock, Shopify adds only what's available and shows its message about the available quantity next to the button.

### Gift option

One per section. A "This is a gift" switch with a gift message, gift wrapping and a "Leave prices out of the parcel" choice, saved on the item. Setup and what you see on the order are on [Gifting]({{ site.baseurl }}/gifting/).

### WhatsApp order

One per section. A WhatsApp row ("Looking for something specific?") that opens a chat with the product title filled in as the message. It uses the number in Theme settings › **Floating widgets** › **WhatsApp number** and shows only while **Show WhatsApp** is on there.

### Two-size bundle

One per section. Adds the product's first two available variants to the bag together, for example "Buy 50 ml + 100 ml". It shows only when at least two variants are in stock.

The theme doesn't apply a discount. To offer a saving, create an automatic discount in Shopify admin (Discounts › **Create discount**) and describe it in the block's **Heading** and **Text**.

### Stock line

One per section. Shows "In stock" for an available variant, followed by your **Delivery note** (for example a same-day delivery promise). A sold-out variant shows "Sold out for now", and an option combination that doesn't exist shows "Unavailable".

### Pay in installments

One per section, not in the default template. Shows an estimated installment amount (a quarter of the price) for Tabby or Tamara when you've turned them on in Theme settings › **Payments** and the shopper is in one of their markets: Tabby in the UAE, Saudi Arabia, Kuwait, Bahrain and Qatar; Tamara in Saudi Arabia, the UAE and Kuwait. The theme doesn't check eligibility or fees, so turn a provider on only if it's offered at your checkout.

### Prepaid nudge

One per section, not in the default template. Encourages prepaid orders, for example "Pay now and save 5%". Set **Prepaid saving** above 0 to show it (0 hides it).

It shows to shoppers in the countries listed in Theme settings › **Payments** › **Cash-on-delivery markets**. If that list is empty, it shows in every market. The theme doesn't apply the saving: create the matching discount in Shopify admin first.

### Collapsible tab

Add as many as you need. Each is a heading that opens to show its content.

| Setting | What it does |
|---|---|
| **Topic** | **Authenticity and returns**, **Shipping** or **Custom**. The first two come with a translated heading and, until you write your own **Content**, link to your refund or shipping policy (Settings › Policies). |
| **Heading** | Replaces the topic's heading. Required for **Custom**. |
| **Content** | Your text. |
| **Open by default** | Starts the tab open. |

A tab with no content (and no policy to link to) is hidden on your store. In the theme editor it shows a reminder instead.

### Trust badges

One per section, not in the default template. Up to three short promises, each with a **Badge 1 heading** and **Badge 1 text** (and so on for 2 and 3). A badge shows only when you fill in its heading or text. Promise only what your store offers.

### Note ribbon

One per section, not in the default template. Draws how the scent changes from the first spray to 14 hours. It needs note ribbon data on the product: see [Set up the note ribbon](#set-up-the-note-ribbon). Products without it don't show the block.

### Complementary products

One per section. A short list of products that pair well with this one, each with an "Add" button. Choose them per product in the Shopify Search & Discovery app:

1. In Shopify admin, go to Apps › **Search & Discovery** and select **Product recommendations**.
2. Select **Add recommendations**, select the product, then add products under **Complementary products**.
3. Save.

**Products to show** sets the maximum (1 to 6). The block is hidden on products with no complementary products.

### Custom Liquid

Add as many as you need. Paste Liquid or HTML, such as an app snippet or a small embed. See [Custom code]({{ site.baseurl }}/custom-code/).

### App blocks

Apps that offer theme blocks (reviews, size guides, back-in-stock alerts and so on) appear under **Apps** when you add a block to the **Product** section. Add the app's block and drag it where you want it.

## Pickup availability

When a location offers local pickup for the selected variant, the **Buy buttons** block shows "Pickup available at [location]" with its pickup time, or "Pickup currently unavailable at [location]" when that location has no stock. Below it, a "Check availability at other stores" link ("View store information" when you have one pickup location) opens a list of your pickup locations with stock status, address and phone. It updates when the shopper changes the variant.

To turn on local pickup:

1. In Shopify admin, go to Settings › **Shipping and delivery**.
2. In the **Additional delivery methods** section, select **Pickup in store**, then select the location.
3. Turn on **Let customers pick up orders directly at this location**.
4. Set the pickup time and instructions, then save.

Nothing shows when no location offers pickup for the variant. To hide the line everywhere, turn off **Show pickup availability** in the **Buy buttons** block.

## Sticky add-to-bag bar

On phones and tablets, a bar with the product name, the selected size, the price and an "Add to bag" button appears once the main button scrolls out of view. The WhatsApp and back-to-top buttons move above it so nothing overlaps. On desktop the buy column stays in view instead, so the bar isn't needed.

To hide it, turn off **Show sticky add-to-bag bar on mobile** in the **Product** section.

## When stock runs out or a combination doesn't exist

| Situation | What shoppers see |
|---|---|
| The selected variant is sold out | The button reads "Sold out" and can't be pressed. The dynamic checkout buttons, the installment line and the prepaid nudge are hidden. The stock line reads "Sold out for now". |
| A size or option value is sold out in the current combination | Its tile or pill is dashed and its label struck through. Shoppers can still select it to see the price. |
| The chosen combination doesn't exist (for example a 100 ml oil you don't make) | The button and stock line read "Unavailable". The price, SKU and installment line are hidden, and the page address drops the variant. |
| The whole product is sold out | On product cards, the card reads "Sold out". When WhatsApp is set up, it reads "Sold out · notify me on WhatsApp" and opens a chat asking to be told when the product is back. |
| A shopper adds more than you have | Shopify adds what's left and its message shows next to the button. |

Shopify's "Continue selling when out of stock" setting on a variant keeps it available, so the theme treats it as in stock.

## Media gallery

The gallery shows every image, video and 3D model you add under Products › your product › **Media**. The selected variant's image comes first. Each image's alt text comes from the media's alt text in Shopify admin, or the product title when it's empty.

| Media | How it shows |
|---|---|
| Images | Swipe on phones (with dots) or select the thumbnails on desktop, depending on the layout settings. |
| Videos you upload | Play with controls when the shopper presses play. They never autoplay. |
| YouTube and Vimeo videos | Show the preview image with a "Play video" button. The player loads only when pressed. |
| 3D models | Show the preview image with a "View in 3D" button that loads the 3D viewer. A "View in your space" button also appears on phones and tablets that support augmented reality. |

To add media:

1. In Shopify admin, open Products and select the product.
2. Under **Media**, select **Upload new** to upload images, videos or 3D models. To add a YouTube or Vimeo video, select **Select existing**, then **Add from URL**, and paste the link.
3. To link an image to a variant, select the variant under **Variants** and choose its image. Selecting that variant on the product page then moves the gallery to it.

More notes:

- With more than 10 media items, phones show a "1 / 26" counter instead of dots.
- A product with no media shows a placeholder so the layout stays the same.
- The product's badge (metafield `attar.badge`, for example "Bestseller") shows on the first image.
- In Arabic the carousel starts at the right edge and swipes in reading direction. See [Languages and right-to-left]({{ site.baseurl }}/languages-and-rtl/).

## Color swatches

Swatches come from Shopify's option swatches: a color or image attached to an option value through a category metafield. The theme shows them inside the option pills when **Show swatches** is on in the **Variant picker** block.

To add swatches:

1. In Shopify admin, open Products and select the product.
2. Under **Category**, choose a product category that includes the option you need (for example one with **Color**).
3. Under **Variants**, add an option and pick the suggested linked option (for example **Color**). Choose existing values or create new ones, and give each a color or an image.
4. Save.

To change a swatch later, go to Content › **Metaobjects**, open the entry type (for example **Color**) and edit its color or image. Values without a swatch keep the text label, so you can mix both in one option. Shopify's guide: [Using category metafields](https://help.shopify.com/manual/custom-data/metafields/category-metafields/using-category-metafields).

Color swatches also appear in collection filters when you add a filter for that option in Search & Discovery. Image swatches show only on the product page; filters show the value's name instead. See [Collections and search]({{ site.baseurl }}/collections-and-search/).

## Product highlights

Online Store › Themes › **Edit theme** › Products › Default product › **Product highlights** section. Each block reads the product's own data and hides itself when that data is missing, so no product shows an empty card.

### Scent pyramid

One per section. Shows the top, heart and base notes, with longevity and sillage meters, from the metafields `attar.notes_top`, `attar.notes_heart`, `attar.notes_base`, `attar.longevity`, `attar.sillage` and their scores. The first base note is marked as the key note. Hidden when the product has none of these.

- **Notes display**: **Note ribbon** (default) shows the note ribbon for products that have note ribbon data, and the notes list for the rest. **Notes list** always shows the list.
- **Heading** and **Text**: leave blank for "Scent pyramid" and "From the first spray to the last trace on fabric."

Theme settings › **Effects** › **Note display** decides first: with **Classic notes list** or **Off**, the card always shows the list. See [Effects and campaigns]({{ site.baseurl }}/effects-and-campaigns/).

### Pairs well with

One per section. Shows the product in the metafield `attar.pairs_with` (for example a matching bakhoor) with an "Add both" button and the combined price. Hidden when the metafield is empty. When either product is sold out, the card shows the paired product without the combined price and the "Add both" button.

### Discovery set

One per section. A card that points to your sample or discovery set. It shows only once you set **Button link**, and it's hidden on the product page that link points to. Leave **Eyebrow**, **Heading**, **Text** and **Button label** blank for the translated defaults: "Discovery set", "Try before you decide", "Try a sample first, then choose your full bottle." and "Build your set".

### Trust badges

One per section. Up to three badges, shown on phones and tablets only (on desktop the collapsible tabs cover the same ground). Each badge shows only when you fill in its heading or text.

## Product data (metafields)

The theme reads these product and variant metafields. None are required: each part of the page hides when its data is empty. Create the definitions once, then fill them in on each product.

To create a definition:

1. In Shopify admin, go to Settings › **Metafields and metaobjects** › **Products** (or **Variants** for `volume_ml`).
2. Select **Add definition**.
3. Enter a name, set **Namespace and key** exactly as in the table (for example `attar.subtitle`), and choose the type.
4. Save. The field then appears under **Metafields** on every product.

| Namespace and key | Type | Where it shows |
|---|---|---|
| `attar.subtitle` | Single line text | Under the title (when there's no `title_alt`) and on product cards, for example "Oud · Extrait" |
| `attar.title_alt` | Single line text | Under the title: the product's name in the other script |
| `attar.badge` | Single line text | On the first image and on product cards, for example "Bestseller" |
| `attar.family` | Single line text | Above the title, breadcrumbs, compare table, filters |
| `attar.concentration` | Single line text | Sticky bar, compare table, search engine data |
| `attar.notes_top`, `attar.notes_heart`, `attar.notes_base` | Single line text (list of values) | Scent pyramid, compare table |
| `attar.note_ribbon` | JSON | Note ribbon (see below) |
| `attar.longevity`, `attar.sillage` | Single line text | Scent pyramid meters, for example "14 hours" or "Strong" |
| `attar.longevity_score`, `attar.sillage_score` | Integer (0 to 100) | How full each meter is |
| `attar.story` | Multi-line text | **Description** block |
| `attar.pairs_with` | Product reference | **Pairs well with** block |
| `attar.volume_ml` (variant) | Integer | Price per ml, for example 50 for a 50 ml bottle |

The star rating reads Shopify's standard `reviews.rating` and `reviews.rating_count` metafields, which review apps fill in for you.

Text metafields are translatable: translate them in the Translate & Adapt app so Arabic pages show Arabic notes and subtitles.

## Set up the note ribbon

The note ribbon draws a scent from the spray to 14 hours: one colored band per note, its height showing how strong that note is over time. Shoppers can tap the time marks (Spray, 1 h, 3 h, 8 h, 14 h) to read which notes lead at each stage. It appears in the **Note ribbon** block, the **Scent pyramid** card and, as a thin strip, on product cards.

It uses two pieces of data:

- a **Note** library (a metaobject), where each note's name is translated once and its color chosen once;
- one JSON metafield per product, `attar.note_ribbon`, that lists the product's notes and how each behaves.

### 1. Create the Note metaobject

1. In Shopify admin, go to Settings › **Metafields and metaobjects** › **Metaobjects** and select **Add definition**.
2. Name it "Note" and set its **Type** to exactly `attar_note`.
3. Add three fields:

   | Field key | Type | Notes |
   |---|---|---|
   | `name` | Single line text, required | The note's name, for example "Taif rose" |
   | `color` | Color, required | The band color, used on dark color schemes (and on light ones without `color_light`) |
   | `color_light` | Color, optional | A darker shade for light color schemes, so pale notes such as musk keep contrast |

4. Turn on **Storefronts** access so the theme can read the entries, and turn on **Translations** so you can translate the names.
5. Save.

### 2. Add your notes

1. Go to Content › **Metaobjects** › **Note** and select **Add entry**.
2. Fill in the name and colors, and check the entry's handle (for example `taif-rose`). You'll use the handle in the product data.
3. If the definition has a status option, set each entry to **Active**.
4. Translate the names in Translate & Adapt.

### 3. Create the product metafield

1. Go to Settings › **Metafields and metaobjects** › **Products** and select **Add definition**.
2. Name it "Note ribbon", set **Namespace and key** to `attar.note_ribbon` and choose **JSON**.
3. Optional: paste the schema below so Shopify rejects values with mistakes.
4. Save.

```json
{"type":"array","maxItems":12,"items":{"type":"object","required":["note","level","w","peak","sl","sr"],"properties":{"note":{"type":"string","minLength":1},"level":{"type":"integer","enum":[0,1,2]},"w":{"type":"number","minimum":0,"maximum":1},"peak":{"type":"number","minimum":0,"maximum":14},"sl":{"type":"number","exclusiveMinimum":0},"sr":{"type":"number","exclusiveMinimum":0}}}}
```

### 4. Fill in each product

Open the product, find **Note ribbon** under **Metafields** and paste a list of up to 12 notes, in the order you want them listed:

| Key | Value | Meaning |
|---|---|---|
| `note` | Text | The handle of a Note entry, for example `taif-rose` |
| `level` | 0, 1 or 2 | Top, heart or base |
| `w` | 0 to 1 | How strong the note is at its peak |
| `peak` | Hours, 0 to 14 | When the note is strongest |
| `sl` | Hours, above 0 | How quickly it rises before the peak |
| `sr` | Hours, above 0 | How long it lasts after the peak |

Example:

```json
[
  { "note": "bergamot", "level": 0, "w": 0.55, "peak": 0.1, "sl": 0.2, "sr": 0.5 },
  { "note": "saffron", "level": 0, "w": 0.85, "peak": 0.25, "sl": 0.45, "sr": 0.9 },
  { "note": "taif-rose", "level": 1, "w": 0.9, "peak": 2, "sl": 1.2, "sr": 2.6 },
  { "note": "omani-frankincense", "level": 1, "w": 0.6, "peak": 2.6, "sl": 1.4, "sr": 3.2 },
  { "note": "cambodian-oud", "level": 2, "w": 1, "peak": 6.5, "sl": 4, "sr": 9 },
  { "note": "white-musk", "level": 2, "w": 0.55, "peak": 9.5, "sl": 5, "sr": 7 }
]
```

Rules of thumb: top notes peak in the first half hour (`sr` about 0.5 to 1), heart notes around 2 to 3 hours (`sr` about 2.5 to 3), and base notes at 6 to 10 hours (`sl` about 4, `sr` about 7 to 9). Scale the base values down for lighter scents. Use your perfumer's data where you have it.

Entries whose note doesn't exist (or has no color), whose `w`, `sl` or `sr` is 0 or less, or whose `peak` is below 0 are skipped. With no valid entries, the **Scent pyramid** card shows the notes list, the **Note ribbon** block is hidden and cards show no strip.

### 5. Show it

- Product page: add the **Note ribbon** block to the **Product** section, or leave the **Scent pyramid** card's **Notes display** on **Note ribbon**.
- Product cards: **Show note ribbon on cards** in the **Collection**, **Featured products** and **Product recommendations** sections.
- Store-wide: Theme settings › **Effects** › **Note display** must be **Note ribbon**. See [Effects and campaigns]({{ site.baseurl }}/effects-and-campaigns/).

## Product reviews

Online Store › Themes › **Edit theme** › Products › Default product › **Product reviews** section.

The rating summary comes from the `reviews.rating` and `reviews.rating_count` metafields that review apps fill in. The theme never invents a rating or a review. The section is hidden on products with no rating and no review blocks.

| Setting | What it does |
|---|---|
| **Heading** | Leave blank for "Reviews". |
| **Show language filter** | When your quotes are in both Arabic and English, shows "All", "العربية" and "English" chips that filter them. |
| **"All reviews" link** | Optional link to a page with all your reviews. |

Add reviews in one of two ways:

- **Your review app's block**: add it from **Apps** inside this section.
- **Review** blocks: one per real customer review, with **Review**, **Name and city**, **Variant bought**, **Rating**, **Review language** and **Verified purchase**. Tick **Verified purchase** only when you've matched the review to an order. Publish real customer reviews only.

## Product recommendations

Online Store › Themes › **Edit theme** › Products › Default product › **Product recommendations** section. Shopify picks the products automatically from sales and product details.

| Setting | Default | What it does |
|---|---|---|
| **Heading** | Blank | Leave blank for "You may also like" (or "Pairs well with" for complementary products). |
| **Recommendation type** | **Related products** | Or **Complementary products**, the products you choose per product in the Search & Discovery app. Complementary rows have no fallback and stay hidden until Shopify returns products. |
| **Products to show** | 4 | 2 to 8. |
| **Fallback collection** | Blank | Shown while recommendations load, or when Shopify has none yet for a new product. Left blank, the product's scent-family collection (or its first collection) is used. |
| **Show note ribbon on cards** | On | A thin strip of each product's notes over time. |

## Compare page

Shoppers can compare up to four fragrances side by side: price, rating, concentration, scent family, notes, longevity, sillage, sizes and a buy button. Rows that are empty for every product are hidden. On phones the table scrolls sideways with the row labels pinned.

To set it up:

1. In Shopify admin, go to Online Store › **Pages** › **Add page**. Title it, for example, "Compare", and check that its handle is `compare`.
2. Under **Theme template**, choose **compare** and save.
3. In the theme editor, open the page and select the **Compare** section:
   - **Heading** and **Intro text**: leave blank to use the page title and content.
   - **Default fragrances**: shown until a shopper builds a list of their own.
   - **Collection for "Add a fragrance"**: where the "Add a fragrance" button and the empty state lead. Leave blank for all products.
4. To let shoppers pick products, turn on **Show Compare toggle on cards** in the **Collection** section, and keep the **Compare teaser** section on your collection template. Its "Compare" button opens the page with the shopper's picks. See [Collections and search]({{ site.baseurl }}/collections-and-search/).

The shopper's list is kept in their browser. You can also share a comparison as a link: add `?ids=` and product handles to the page address, for example `/pages/compare?ids=royal-oud,white-musk`.
