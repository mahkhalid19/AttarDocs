---
title: Cart and checkout
description: Set up ATTAR's cart drawer and cart page, order notes, free-shipping progress, gifting, payment notes and accelerated checkout, and see what the theme can't change.
---

ATTAR has two views of the same cart, which it calls the bag:

- **Cart drawer**: opens over any page when a shopper adds a product or taps the bag icon. On phones it slides up from the bottom; on larger screens it opens as a panel from the side (the left in Arabic, the right in English).
- **Cart page**: the full page at `/cart`. Shoppers reach it from the bag icon when their browser blocks scripts, and you can link to it.

Both show the same content and have the same settings, so set them up the same way. The cart page comes with a **Gift toggle** and an **Empty state** block; the drawer starts with no blocks, so add them there too if you want them.

## Where to find the settings

| View | Path |
|---|---|
| Cart drawer | Online Store › Themes › **Edit theme**, open any page except the cart, then select **Cart drawer** in the sidebar. It's part of the theme layout, so its settings apply on every page. |
| Cart page | Online Store › Themes › **Edit theme** › choose Cart from the page selector › **Cart** section. |

## What the bag shows

From top to bottom:

1. The heading "Your bag" with the number of items.
2. Free-shipping progress, if you set a threshold.
3. The items: image, name, size, price (with the regular price struck through when it's discounted), any discount applied to the item, and quantity buttons with a remove button. Gifts show their gift panel (see [Gifting]({{ site.baseurl }}/gifting/)).
4. The "This is a gift" row, if you add the **Gift toggle** block.
5. An upsell suggestion, if you choose a collection.
6. "Add a note to your order", if the order note is on.
7. The summary: subtotal and order discounts (when there are any), the total, and "VAT included" or "Taxes and shipping are calculated at checkout."
8. The cash-on-delivery and pay-later line, if you turn it on.
9. The "Checkout" button, the accelerated checkout buttons, "Continue shopping" and your payment icons.

Prices, quantities and counts follow Theme settings › **Numerals** › **Numeral system**. See [Languages and right-to-left]({{ site.baseurl }}/languages-and-rtl/).

If a shopper raises a quantity above your stock, Shopify keeps what's available and the bag shows Shopify's message at the top.

## Settings

These settings are the same in the **Cart drawer** and the **Cart** section.

| Setting | Default | What it does |
|---|---|---|
| **Free-shipping threshold** | 0 | The order amount for free shipping, in your store currency, for example 300. Shows a progress bar ("50 away from free shipping", then "You've unlocked free shipping"). 0 hides it. |
| **Gift-wrap product** | Blank | Your gift-wrap product, whose variants are the wrap choices. See [Gifting]({{ site.baseurl }}/gifting/). |
| **Upsell collection** | Blank | Suggests available products from this collection that aren't in the bag yet, under "Complete the ritual". |
| **Products to suggest** | 1 | 1 to 3. |
| **Show order note** | On | Adds "Add a note to your order". |
| **Show accelerated checkout buttons** | On | Shop Pay, Apple Pay and the other express methods turned on in your payment settings. |
| **Show cash on delivery and pay-later notes** | Off | Adds "Cash on delivery available" and an estimated pay-later installment line. See [Payment notes](#payment-notes). |

The free-shipping threshold can't be converted into other currencies. Shoppers paying in another currency see "Free shipping on qualifying orders" instead of the bar. Set the threshold to the same amount as your free-shipping rate in Settings › **Shipping and delivery**: the theme only displays it.

When an upsell product would bring the order over the free-shipping threshold, it's marked "Unlocks free shipping".

## Order notes

With **Show order note** on, shoppers can open "Add a note to your order" and type delivery instructions or anything else. The note is saved on the order: you see it under **Notes** on the order page in Shopify admin. Shoppers can write in Arabic or English.

## Discounts

The bag shows discounts that already apply: automatic discounts, and a code applied through a discount link. Item discounts show under the item; order discounts show under the subtotal, with their names.

There's no discount code field in the bag. Shoppers enter codes at checkout. To apply a code before checkout, share its discount link: in Shopify admin, go to Discounts, open the code, select **Promote**, then **Get a shareable link**.

## Gift wrap and message

The bag supports two gift features: a gift on a single item (added from the product page) and a message card and wrapping for the whole order. To show the "This is a gift" row:

1. Create the gift page and choose the wrap product, as described in [Gifting]({{ site.baseurl }}/gifting/#set-up).
2. In the **Cart drawer** (and the **Cart** section), add a **Gift toggle** block.
3. Set **Gift step page** to your gift page. The row is hidden until you choose one.
4. Optional: change **Label**. Leave it blank for "This is a gift — add wrapping and a card".

In the drawer the row opens the gift step in place, with a "Back to bag" link. On the cart page it opens the gift page.

## Empty bag

Add an **Empty state** block to control what an empty bag shows. Without one, the bag shows "Empty… for now." and a "Continue shopping" button.

| Setting | What it does |
|---|---|
| **Heading**, **Text** | Leave blank for "Empty… for now." and "Browse the collection, or let the scent finder choose for you." |
| **Button label**, **Button link** | The main button. Defaults to "Shop most wanted" linking to all products. |
| **Second button label**, **Second button link** | For example your scent finder page. Leave the link blank to hide the button. |
| **Collection**, **Heading**, **Products to show** | A row of first-bottle picks from a collection, under "Popular first bottles". Products to show: 0, 3 or 6. |
| **Show the WhatsApp line** | "Undecided? Ask a scent question on WhatsApp." Uses the number in Theme settings › **Floating widgets**. |

## Payment notes

With **Show cash on delivery and pay-later notes** on, the summary can show:

- "Cash on delivery available", to shoppers in the countries listed in Theme settings › **Payments** › **Cash-on-delivery markets** (country codes separated by commas, for example `AE,SA,EG`);
- "Or 4 payments of about [amount] with [providers] at checkout, if you're eligible": one line naming every pay-later provider you've turned on in Theme settings › **Payments** that serves the shopper's country. Tabby serves the UAE, Saudi Arabia, Kuwait, Bahrain and Qatar; Tamara serves Saudi Arabia, the UAE and Kuwait; valU serves Egypt.

The amount is a quarter of the total. The theme doesn't check eligibility or fees, and it doesn't add these payment methods to your checkout. Turn them on only if you offer them at checkout.

## Accelerated checkout

Accelerated checkout buttons (Shop Pay, Apple Pay, Google Pay, PayPal and others) let shoppers skip the checkout form. They're on by default on the product page and in the bag, and show the methods you've turned on in Shopify admin under Settings › **Payments**.

- Product page: **Show dynamic checkout buttons** in the **Buy buttons** block. See [Product pages]({{ site.baseurl }}/product-pages/#buy-buttons).
- Bag: **Show accelerated checkout buttons** in the **Cart drawer** and **Cart** section.

On the product page, the buttons are hidden on sold-out variants, on gift card products while the recipient form shows, and while a shopper has chosen paid gift wrapping (the buttons can't add the wrap).

## Payment icons

The bag and the footer show icons for the payment methods you've turned on in Settings › **Payments**, so they never show a method you don't accept. The footer shows them on desktop only, while **Show payment badges** is on in the **Footer** section.

Regional methods that Shopify may not list can be added as text badges in Theme settings › **Payments**: **mada**, **Tabby**, **Tamara** and **valU**. All are off by default. Each shows only in its markets (mada in Saudi Arabia, valU in Egypt, Tabby and Tamara as listed above). The mada badge is also skipped when Shopify already shows the mada icon.

## Payment and delivery strip

The **Payment and delivery** section shows tiles for cash on delivery, split payments, delivery and authenticity, plus the payment icons. You can add it to the cart page, the home page or any other template. Tiles follow the shopper's market, and the delivery and authenticity tiles show only once you write their titles. See [Sections]({{ site.baseurl }}/sections/).

## What the theme can't change

Some parts of the buying journey are run by Shopify, not the theme. Change them in Shopify admin:

| Part | Where to change it |
|---|---|
| Checkout pages (contact, delivery, payment) | Settings › **Checkout**. Select **Edit** next to your checkout configuration to match your logo, colors and fonts. |
| Order status and thank-you pages | Settings › **Checkout**, then **Edit** next to your checkout configuration. |
| Shipping rates and free-shipping rules | Settings › **Shipping and delivery**. The theme's free-shipping bar only displays your threshold. |
| Taxes and duties | Settings › **Taxes and duties**. |
| Discounts | **Discounts**. The theme shows discounts but never creates or applies them. |
| Payment methods | Settings › **Payments**. |
| Packing slips | Settings › **Shipping and delivery**, then **Packing slip template** in the **Documents** section. Shopify's packing slips never show prices. To print each item's gift message and wrap, paste the snippet from [Gifting]({{ site.baseurl }}/gifting/#packing-slip-snippet). |
| Order and shipping emails | Settings › **Notifications**. |

Shopify's checkout shows in the shopper's language, including Arabic, when that language is published on your store.
