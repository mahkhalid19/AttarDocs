---
title: Collections and search
description: Set up ATTAR's collection pages, filters and sorting, quick add, express order, the compare teaser, collection FAQs, the collection list page and search.
---

## Collection page

The collection template has four sections, in this order:

| Section | What it shows |
|---|---|
| **Collection banner** | The collection's image, title, description and product count. |
| **Collection** | Occasion chips, filters, sorting and the product grid. |
| **Compare teaser** | Cards that lead to the compare page and the scent quiz. |
| **FAQ** | Questions and answers about the collection. |

To edit them, go to Online Store › Themes › **Edit theme**, then choose Collections › Default collection from the page selector at the top of the editor. Changes apply to every collection that uses this template.

### Collection banner

Online Store › Themes › **Edit theme** › Collections › Default collection › **Collection banner** section.

| Setting | Default | What it does |
|---|---|---|
| **Use the collection image** | On | Shows the image you set on each collection in Shopify admin (Products › Collections › your collection). |
| **Image** | Blank | Replaces the collection image on every collection that uses this template. |
| **Accent line** | Blank | A short line in the other script above the title, for example العود on the English store. Leave blank to use the collection's `attar.accent_line` metafield. |
| **Title when there is no collection** | Blank | Shown only in the theme editor preview. |
| **Show breadcrumbs** | On | Home › collection. |
| **Show collection description** | On | The description from Shopify admin. |
| **Show product count** | On | For example "24 scents". |

To set a different accent line per collection, create a collection metafield:

1. In Shopify admin, go to Settings › **Metafields and metaobjects** › **Collections** and select **Add definition**.
2. Name it "Accent line", set **Namespace and key** to `attar.accent_line` and choose **Single line text**.
3. Save, then fill it in on each collection and translate it in the Translate & Adapt app.

### Collection grid settings

Online Store › Themes › **Edit theme** › Collections › Default collection › **Collection** section.

| Setting | Default | What it does |
|---|---|---|
| **Layout** | **Grid with filter sidebar** | Filters in a column beside the products from 990 px wide, and in a drawer on smaller screens. **Grid with filter drawer** puts filters in a drawer at every width, with a wider grid. |
| **Product card** | **Responsive (sizes on mobile, overlay on desktop)** | See [Quick add](#quick-add). |
| **Products per page** | 12 | 8 to 48. |
| **Loading more products** | **Show more button** | Or **Page numbers**. See [Pagination and Show more](#pagination-and-show-more). |
| **Show Compare toggle on cards** | Off | Adds a "Compare" toggle to each card. See [Compare](#compare-teaser). |
| **Show note ribbon on cards** | On | A thin strip of each product's notes over time, for products with note ribbon data. Needs Theme settings › **Effects** › **Note display** set to **Note ribbon**. See [Product pages]({{ site.baseurl }}/product-pages/#set-up-the-note-ribbon). |
| **Show filters** | On | Shows the filters you set up in Search & Discovery. |
| **Show sorting** | On | Shows the sort menu. |
| **Show occasion chips** | On | See [Occasion chips](#occasion-chips). |

### Filters

Filters come from the free Shopify Search & Discovery app. The theme shows whatever filters you set up there: availability, price, product type, vendor, tags, variant options such as Size, and product metafields such as scent family.

To set up filters:

1. Install **Shopify Search & Discovery** from the Shopify App Store, if you don't have it.
2. In Shopify admin, go to Apps › **Search & Discovery** › **Filters** and select **Add filter**.
3. Choose a source, for example **Price**, **Availability**, the **Size** option, or the **Scent family** metafield (`attar.family`, see [Product data]({{ site.baseurl }}/product-pages/#product-data-metafields)).
4. Optional: rename the filter or group its values, then save.
5. Drag the filters into the order you want shoppers to see them.

What shoppers see:

- Each filter is a group of checkboxes; price is a "From" and "To" range.
- Options with [color swatches]({{ site.baseurl }}/product-pages/#color-swatches) show the color beside each value. Image swatches aren't shown in filters.
- Selected filters appear as removable chips above the grid, with "Clear all".
- In the drawer, the button reads "Show 12 scents" with the current number of matches.
- Results update in place, without reloading the page.

If a collection has no filters (or **Show filters** is off), the filter button and sidebar are hidden. In Arabic the drawer opens from the right and counts use your numeral setting. See [Languages and right-to-left]({{ site.baseurl }}/languages-and-rtl/).

### Sorting

The sort menu offers "Featured", "Best selling", "Name: A to Z", "Name: Z to A", "Price: low to high", "Price: high to low", "Oldest" and "Newest". "Featured" is the order you arrange by hand in Shopify admin. The menu starts on the collection's own sort order, which you choose in Products › Collections › your collection › **Sort**.

### Occasion chips

A row of chips above the grid, such as "Evening", "Wedding" and "Eid". Each chip shows the products with a matching tag.

To set them up:

1. Tag your products in Shopify admin, for example `Evening` or `Eid`.
2. In Search & Discovery, add a **Tags** filter (Apps › **Search & Discovery** › **Filters** › **Add filter** › **Tags**). Chips then combine with the other filters.
3. Optional: in the **Collection** section, add an **Occasion chip** block for each chip you want, in the order you want. Set **Product tag** to the exact tag, and **Label** to the text shoppers see.

With no **Occasion chip** blocks, the chips list up to 12 values of the Tags filter. The tags `evening`, `wedding`, `eid` and `office` show a translated label ("Evening", "Wedding" and so on); other tags show as typed. On **Occasion chip** blocks with **Label** left blank, `gift` and `daily` get a translated label too ("Gifts", "Everyday").

The first chip, "All", clears the occasion.

### Quick add

Product cards let shoppers add a product without opening it. **Product card** chooses how:

| Option | What shoppers see |
|---|---|
| **Responsive (sizes on mobile, overlay on desktop)** | Size choices and an add button on phones and tablets, and a "Quick add" button over the photo from 990 px wide. |
| **Quick add (sizes)** | Size choices and an add button at every width. |
| **Overlay quick add** | A "Quick add" button over the photo at every width. It adds the first available size. |

Cards also show the product's badge (`attar.badge`), a "Save 20%" tag when the price is below the compare-at price, the price per ml and, for products with several prices, "From" and the lowest price. Cards with size choices show the selected size's price, with "From" only while the cheapest size is selected. Sold-out cards read "Sold out". When WhatsApp is set up (Theme settings › **Floating widgets**), they read "Sold out · notify me on WhatsApp" and open a chat asking to be told when the product is back.

After adding, the cart drawer opens. See [Cart and checkout]({{ site.baseurl }}/cart-and-checkout/).

### Pagination and Show more

With **Show more button**, the grid shows "12 of 48 scents" and a "Show 12 more" button that adds the next page under the current one. The button is a link to the next page, so search engines can follow it. If the browser blocks scripts, page links also show under the grid from page 2 on.

With **Page numbers**, shoppers move between pages with numbered links and "Previous page" and "Next page" arrows. There's no "Show more" button in this mode.

### Empty collections

A collection with no products reads "This collection is being restocked. Explore our other scents in the meantime." When filters leave nothing, the grid reads "No scents match these filters."

### Compare teaser

Online Store › Themes › **Edit theme** › Collections › Default collection › **Compare teaser** section. Up to three cards under the grid, each with a heading, a line of text and a button. On phones the first card shows as a compact row; from 750 px the cards sit side by side.

Each **Card** block has:

| Setting | What it does |
|---|---|
| **Content** | **Compare scents**, **Scent quiz** or **Custom**. The first two come with translated copy ("Torn between two?", "Not sure where to begin?"); **Custom** has no default copy. |
| **Style** | **Outline** or **Accent**. |
| **Heading**, **Text**, **Button label** | Leave blank to use the content's default copy in each language. |
| **Button link** | Where the button goes. A card shows a button only when it has both a link and a button label. |

The **Compare scents** card is the way into the compare page: with **Button link** left blank, it links to your page with the handle `compare` once that page exists. When **Show Compare toggle on cards** is on in the **Collection** section, the button carries the shopper's picks to the page. To create the compare page, see [Product pages]({{ site.baseurl }}/product-pages/#compare-page).

For the **Scent quiz** card, set **Button link** to your scent finder page.

### Collection FAQ

Online Store › Themes › **Edit theme** › Collections › Default collection › **FAQ** section. Questions that open to show their answers. You can add this section to other templates too.

| Setting | Default | What it does |
|---|---|---|
| **Heading** | Blank | Leave blank for "Questions about [collection]". |
| **Open the first question** | On | Starts with the first answer showing. |
| **Add FAQ structured data** | On | Describes the questions to search engines. See [SEO and sharing]({{ site.baseurl }}/seo-and-sharing/). |

Add up to 12 **Question** blocks. Each has a **Topic**:

- **Extrait or oil** comes with a translated question and answer.
- **Authenticity**, **Returns** and **Samples** come with a translated question. Write your own **Answer**. Until you do, **Returns** links to your refund policy and the others are hidden.
- **Custom**: write both **Question** and **Answer**.

A question with no answer is hidden on your store.

## Express order

Express order is a second collection layout for reorders and trade customers: every product and size of a collection in one table, with a quantity for each size and one "Add all to bag" button. A summary shows the units, the subtotal and, if you set them up, quantity tiers.

To use it:

- For one collection: in Shopify admin, open Products › Collections › your collection and set **Theme template** to **express**.
- For any collection, without changing its template: link to the collection address with `?view=express` added, for example `/collections/oud?view=express`. That page shows a "Grid view" and "Express order" switch.

Settings: Online Store › Themes › **Edit theme** › Collections › **express** › **Express order** section.

| Setting | Default | What it does |
|---|---|---|
| **Intro line** | Blank | Leave blank for the default line in the store's language. |
| **Show grid / express view switch** | On | Shown on collections opened with `?view=express`. Collections assigned the express template have no grid view, so the switch is hidden there. |
| **Products per page** | 24 | 6 to 48. |
| **Show product images** | On | |
| **Show SKU** | On | |
| **Low stock alert at** | 5 | Shows "Only 3 left" for tracked sizes at or below this quantity. 0 turns it off. |
| **After adding to bag** | **Open the cart drawer (cart page if there is no drawer)** | Or **Go to the cart page**. |
| **Tier 1: minimum units**, **Tier 1: discount** | 6 units, 0% | See below. |
| **Tier 2: minimum units**, **Tier 2: discount** | 12 units, 0% | See below. |
| **Note under the summary** | Blank | For example trade account or payment terms. Promise only what your store offers. |

Sold-out sizes read "Sold out", and sizes that keep selling when out of stock read "Ships when restocked".

### Quantity tiers

Tiers are off while both discounts are 0. The theme only shows tier progress ("Add 2 more units for 10% off") and an estimated saving. It doesn't apply a discount. For each tier:

1. In Shopify admin, go to Discounts › **Create discount** › **Amount off products**.
2. Under **Method**, select **Automatic discount**, enter the percentage, and under **Minimum purchase requirements** choose **Minimum quantity of items** with the tier's units.
3. Save, then enter the same units and percentage in the **Express order** section.

## Collection list page

The page at `/collections` lists every collection with its image, title and product count. A collection without an image uses its first product's image, or a placeholder.

Online Store › Themes › **Edit theme** › Collections list › **Collections list** section:

| Setting | Default |
|---|---|
| **Collections per page** | 24 (8 to 48) |
| **Image ratio** | **Square** (or **Portrait**, **Landscape**) |
| **Show product count** | On |
| **Show collection description** | Off |

## Search page

Online Store › Themes › **Edit theme** › Search › **Search** section.

Search results use the same grid, filters, sorting, product cards and Show more button as collections. Matching blog articles and pages appear in the same grid as text cards, labeled "Article" or "Page", with a short excerpt. Filters come from Search & Discovery, as on collections.

| Setting | Default | What it does |
|---|---|---|
| **Layout** | **Grid with filter sidebar** | As on collections. |
| **Product card** | **Responsive (sizes on mobile, overlay on desktop)** | As on collections. |
| **Results per page** | 12 | 8 to 48. |
| **Loading more products** | **Show more button** | Or **Page numbers**. |
| **Show filters** | On | |
| **Show sorting** | On | |

### Before a search and when nothing matches

Before a search, and when a search finds nothing, the page offers ways forward instead of a dead end: popular searches, your scent families and a WhatsApp row. When a search finds nothing, it also shows the shopper's words ("Nothing matches “saffron”") and a help line.

| Setting | Default | What it does |
|---|---|---|
| **Help text** | Blank | Leave blank to use the default line for each language. |
| **Show a trace of smoke** | Off | Two faint wisps of smoke behind the message. Theme settings › **Effects** › **Smoke** can turn it off store-wide. |
| **Smoke color** | Blank | Leave blank to follow the color scheme. |
| **Popular searches** | Blank | Searches shown as chips, separated by commas. Leave blank for the default list in each language. Translate yours in Translate & Adapt. |
| **Family collections** | Blank | Collections shown as tiles under "Or browse by family". |
| **Browse menu** | Main menu | Used when no collections are chosen above. Shows the menu's top-level links. |
| **Show WhatsApp help row** | On | Uses the number in Theme settings › **Floating widgets**. |

You can also add up to four suggestion blocks, shown only when a search finds nothing: **Suggested collection**, **Suggested product** and **Suggested search**. Each has a **Note beside the suggestion**; leave it blank for the product count, the product's subtitle or a note about the other language. The default template has one **Suggested search** that, left blank, offers a search for oud in the other script: عود on English pages, oud on Arabic pages.

## Search suggestions while typing

When shoppers type in the search field in the header or the mobile menu, suggestions appear under it: suggested searches, products (with image, subtitle and price), collections and pages. Shoppers can browse them with the arrow keys and open one with Enter.

To turn them on or off: Online Store › Themes › **Edit theme** › **Header** section › **Show search suggestions while typing**. **Show search** must be on.

Shopify's suggestions don't support every language. On Arabic pages, the theme suggests matching products from a regular search instead, without suggested searches, collections or pages. See [Languages and right-to-left]({{ site.baseurl }}/languages-and-rtl/).
