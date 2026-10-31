---
title: SEO and sharing
description: How ATTAR presents your store to search engines, social apps and AI shopping assistants, and what you fill in to help it.
---

ATTAR takes care of the technical side of search engine optimization (SEO): page titles, descriptions, canonical page addresses, link previews and structured data. It works in every language and market you publish. Your part is the content: good titles, descriptions, images and alt text.

## What the theme does for you

- **Page titles** use each item's search engine title, followed by your store name if you choose.
- **Descriptions** use each item's search engine description. If it's empty, the theme uses the start of the product, collection, page or article text, and then your store's description.
- **Link previews** on WhatsApp, X, Facebook and other apps show the page's title, description and image. Product pages also share their price with apps that show it.
- **Duplicate pages are kept out of search results.** Filtered and sorted collection pages point search engines to the main collection page. Search results, the cart, customer account pages and the password page are always hidden from search engines.
- **Languages:** Shopify tells search engines about each published language and market version of a page. Each language uses its own titles and descriptions.
- **Structured data** describes your store, products and articles in a format Google and AI assistants read. See [Structured data](#structured-data).

## Titles and descriptions

Write a search engine title and description for each product, collection, page and blog post:

1. Open the item in Shopify admin.
2. Scroll to **Search engine listing** and select **Edit**.
3. Enter a **Page title** (about 60 characters or fewer) and a **Meta description** (about 155 characters or fewer). Check the **URL handle**.
4. Save.

For the home page, set the title and description in Online Store › **Preferences**.

### In each language

Translate the search engine title, description and URL handle of each item in Shopify's **Translate & Adapt** app. Arabic shoppers then see Arabic results with Arabic page addresses.

Write the Arabic title and description fresh rather than translating word for word. Use the words your customers type, such as «دهن عود» or «عطر مسك».

### Title settings

Go to Online Store › Themes › **Edit theme** › Theme settings › **SEO and sharing**:

- **Title separator**: the symbol between the page name, page number and store name, for example "Royal Oud \| ATTAR". Choose from a vertical bar, dash, long dash, middle dot or slash.
- **Add store name to page titles**: adds your store name to the end of every title. It's skipped when the title already contains it.

## Social sharing image

When someone shares a link, the preview uses the page's own image: the product photo, the article's featured image or the collection image. For pages without one, the theme uses:

1. the **Default share image** in Theme settings › **SEO and sharing**, then
2. the **Brand logo** in the same settings.

Use an image of 1200 × 630 px for the **Default share image**. For the home page, you can set a different image in Online Store › **Preferences** › **Social sharing image**.

Fill in **X (Twitter) username**, for example `@yourstore`, to show your account on X link previews.

Apps cache previews. After you change an image, it can take a while for WhatsApp, X or Facebook to show the new one.

## Brand logo and social profiles

- **Brand logo** (Theme settings › **SEO and sharing**): a square or wide logo on a plain background, at least 112 × 112 px. Google can show it next to your store in search results. It's also shown on the gift card page.
- **Social media links** (Theme settings › **Social media**): your profile addresses tell search engines which accounts belong to your store.

## Alt text

Alt text describes an image for people using screen readers, and it helps search engines understand your images. Link previews reuse it too.

- **Product images:** in the product's **Media**, select an image, then add alt text.
- **Section images:** many sections have an **Image description (alt text)** or **Image description** field next to the image. If you leave it empty, the theme uses the alt text saved with the image in **Content** › **Files**.
- **Blog posts:** add alt text to each post's featured image.

Describe what's in the image in a few words, for example "50 ml bottle of Royal Oud on a wooden tray". Translate alt text in Translate & Adapt.

## Hiding pages from search results

### Tag pages and later pages

In Theme settings › **SEO and sharing**:

- **Hide tag pages from search results**: turn on if your tag pages repeat their collections. Leave off if you use tags as landing pages, for example occasion shelves.
- **Hide page 2 and later from search results**: usually best left off, so search engines can still reach products deeper in long collections.

### A single page or product

To hide one item, such as a thank-you page or a private price list:

1. In Settings › **Metafields and metaobjects**, choose the type of item (Products, Collections, Pages, Blog posts or Blogs).
2. Add a definition with the namespace and key `seo.hidden` and the type **Integer**.
3. Open the item and set the value to `1`.

The theme asks search engines not to list the item.

## Structured data

Structured data is information in your pages that search engines and AI shopping assistants read directly. It helps Google show prices, stock and star ratings, and helps assistants describe your scents accurately.

ATTAR adds:

| Type | Pages | What it includes |
|---|---|---|
| Organization | Home page | Store name, logo and social profiles |
| Website and search | Home page | Store name and your search page |
| Breadcrumbs | Products, collections, pages, blogs and articles | The path to the page, such as Home › Oud › Royal Oud |
| Products | Product pages | Each variant's price, stock, SKU, barcode, size and price per ml, plus fragrance notes and ratings when filled in |
| Blog articles | Articles | Headline, image, dates and author |

Each type has a checkbox in Theme settings › **SEO and sharing** › **Structured data**. Leave them all on unless an app, such as a reviews or SEO app, already adds the same type. Two copies of the same product information confuse search engines.

### Fragrance details

Products give richer results when you fill in a few extra details. Create these metafield definitions once in Settings › **Metafields and metaobjects**, then fill them in on each product or variant:

| Where | Name | Namespace and key | Type |
|---|---|---|---|
| Product | Top notes | `attar.notes_top` | Single line text (list of values) |
| Product | Heart notes | `attar.notes_heart` | Single line text (list of values) |
| Product | Base notes | `attar.notes_base` | Single line text (list of values) |
| Product | Concentration | `attar.concentration` | Single line text |
| Product | Longevity | `attar.longevity` | Single line text |
| Product | Sillage | `attar.sillage` | Single line text |
| Variant | Volume (ml) | `attar.volume_ml` | Integer |

Also fill in:

- **Barcode** on each variant (the GTIN, EAN or UPC number), if your products have one.
- **Vendor** on each product, which is used as the brand.
- **Category** on each product.

**Ratings** come from your reviews app. Many review apps save them to Shopify's standard rating metafields; check your app's settings. Google shows stars only when the reviews are also visible on the product page.

See [Product pages]({{ site.baseurl }}/product-pages/#product-data-metafields) for how these details also appear on your product pages.

## Check your setup

- **Google's Rich Results Test** (search.google.com/test/rich-results): paste a product page address, in each language. You should see product and breadcrumb results without errors.
- **Google Search Console**: add your store, then submit your sitemap at `https://your-domain/sitemap.xml`. Shopify's sitemap includes every published language. In the **Pages** report, filtered and sorted collection pages listed as excluded by a "noindex" tag are expected.
- **Link previews**: paste a link into WhatsApp, or use Facebook's Sharing Debugger.

## robots.txt

Your store uses Shopify's standard robots.txt, which already keeps search engines away from the cart, checkout, account and search pages. ATTAR doesn't change it. Adding custom rules requires editing theme code; see [Custom code and apps]({{ site.baseurl }}/custom-code/) before you do.
