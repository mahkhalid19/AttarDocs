---
title: FAQ
description: Answers to common questions about setting up and using the ATTAR theme.
---

## Languages and Arabic

### Why does my store switch to right-to-left?

Pages in Arabic use a right-to-left layout automatically, and pages in left-to-right languages such as English use left-to-right. You don't need to change any setting. To add or publish a language, go to Settings › **Languages**. See [Languages and right-to-left]({{ site.baseurl }}/languages-and-rtl/).

### Can I upload my own Arabic font?

No. Themes in the Shopify Theme Store can only use fonts from Shopify's font library, and that library has no Arabic letters. Arabic text uses the fonts already on your visitor's device, which load instantly. You can choose a classic (Naskh) or modern (Sans) style in Theme settings › **Typography** › **Arabic headings** and **Arabic body text**. The **Headings** and **Body** fonts you pick apply to Latin text.

### How do I show Arabic-Indic numbers (٠١٢٣)?

Go to Theme settings › **Numerals** › **Numeral system** and choose **Arabic-Indic (٠١٢٣)**. Prices, quantities, sizes and timers across the store switch together, in every language.

### Some section text is still in English on my Arabic pages. Why?

Text you type into sections is saved in one language. Translate it with Shopify's free Translate & Adapt app: open the app, choose Arabic, then **Online Store** › **Theme**. Text that comes with the theme, such as buttons and labels, is already translated into Arabic and English.

### My logo is in Arabic. Can English pages show a Latin version?

Yes. In the theme editor, select the **Header** section and add a **Logo for other languages** image. If you use text instead of a logo, fill in **Latin wordmark**. Pages in Arabic keep the main logo.

## Products

### How do I add scent notes to a product?

Scent notes come from a metaobject (`attar_note`) that holds each note's name and color, and a product metafield (`attar.note_ribbon`) that lists each product's notes. Create your notes once, then list them by handle in each product's **Note ribbon** metafield. [Product pages]({{ site.baseurl }}/product-pages/#set-up-the-note-ribbon) has step-by-step setup. Theme settings › **Effects** › **Note display** chooses between the note ribbon, a classic list of top, heart and base notes, or neither.

### How do I show color swatches?

Swatches come from Shopify. Choose a product category that includes the option (for example Color), add the linked option under **Variants**, and give each value a color or an image. The theme shows the swatches automatically when **Show swatches** is on in the **Variant picker** block. See [Product pages]({{ site.baseurl }}/product-pages/#color-swatches).

### A shopper added more than I have in stock. What happens?

Shopify adds only what's available and shows its message about the available quantity next to the button. The cart updates to the real quantity. This applies when you track inventory and don't allow selling when out of stock.

### Why don't star ratings show on my products?

The theme shows ratings that a review app saves to your products (the standard `reviews.rating` and `reviews.rating_count` metafields). Install a review app that writes these metafields, then add the **Product reviews** section to the product template, or your app's own block. You can also add review quotes by hand as **Review** blocks; only publish real customer reviews.

## Collections and search

### Why don't filters show on my collection pages?

Filters come from Shopify's free Search & Discovery app. Install it, then add filters in the app under **Filters**. The collection and search pages show them automatically.

### Can shoppers compare fragrances?

Yes. In the **Collection** section, turn on **Show Compare toggle on cards**, then create a page that uses the compare template. The collection template also includes a **Compare teaser** section that links to it. See [Pages and templates]({{ site.baseurl }}/pages-and-templates/).

## Cart and checkout

### Why don't Apple Pay or Google Pay buttons show?

Accelerated checkout buttons appear only for payment methods you've turned on in Settings › **Payments**, and only on devices that support them. They're on by default in the theme. If you've turned them on and still don't see them, check **Show dynamic checkout buttons** in the product page's **Buy buttons** block and **Show accelerated checkout buttons** in the cart drawer and cart settings.

### Can I change the checkout or the packing slip?

Not from the theme. Shopify controls checkout. For packing slips, go to Settings › **Shipping and delivery** and select **Packing slip template** in the **Documents** section. Shopify's packing slips never show prices. [Gifting]({{ site.baseurl }}/gifting/#packing-slip-snippet) has a snippet that prints each item's gift message and wrap.

### The free-shipping amount in the announcement bar doesn't show in some markets.

The **Free-shipping threshold** is in your store's currency and isn't converted, so it's shown only to shoppers paying in that currency. This avoids showing a wrong amount after currency conversion.

### How do I show mada, Tabby, Tamara or valU?

Turn on each method you offer in Theme settings › **Payments**. Each badge is hidden in markets where that method isn't available.

## Look and feel

### How do I turn off the smoke effect?

Go to Theme settings › **Effects** › **Smoke** and choose **Off**. For visitors who've asked their device to reduce motion, the smoke holds still.

### How do I set up a Ramadan or Eid look?

Go to Theme settings › **Campaign**, choose the campaign, and optionally enter an **End date** (YYYY-MM-DD). The accent color and smoke take a seasonal tint, and the announcement bar shows a greeting while its text is blank. Campaigns never add discounts. See [Effects and campaigns]({{ site.baseurl }}/effects-and-campaigns/).

### Can visitors in light mode see a light version?

Yes. In Theme settings › **Colors**, turn on **Switch scheme for devices in light mode** and pick a **Light mode scheme**. Visitors whose device is set to light mode see that scheme.

### Where do the WhatsApp and back-to-top buttons come from?

They're in Theme settings › **Floating widgets**. Enter your **WhatsApp number** in international format (for example +971500000000), or turn **Show WhatsApp** off. If an app pins a bar to the bottom of the screen, raise the widgets with **Raise widgets by**.

## Updates and code

### How do I update the theme?

When an update is out, a notice replaces the version number in Online Store › **Themes**. Select **Add to draft themes** to add an updated copy with your theme editor customizations carried over. Code edits are included when they don't conflict with the update; if they can't be included, the theme card says so. Save a copy of any code edits before updating.

### Can I edit the theme code?

You can, but duplicate the theme first, and know that code changes aren't covered by theme support. For most changes, the **Custom Liquid** section and block are safer. See [Custom code and apps]({{ site.baseurl }}/custom-code/).

### My question isn't here.

[Contact support]({{ site.baseurl }}/support/). We reply within two business days.
