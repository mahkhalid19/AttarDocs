---
title: Gifting
description: Let shoppers mark items as gifts, add a message and gift wrapping, and ask for prices to be left out of the parcel, with no app.
---

Fragrance is often bought as a gift, so ATTAR lets shoppers mark an item as a gift on the product page, add a message and wrapping, and ask for prices to be left out of the parcel. Everything runs on Shopify's own cart and orders. No app is needed.

There are two gift features. You can use one or both:

| Feature | Where shoppers find it | What it covers |
|---|---|---|
| **Gift option** block | Product page, above the buy buttons | One item: a gift message, wrapping for that item, and the no-prices choice |
| **Gift wrap and message** step | The "This is a gift" row in the bag, or its own page | The whole order: a card with the recipient's name and a message, and one wrapping choice |

Gift cards have their own "send to someone by email" fields (recipient email, name, message and send date). That's Shopify's gift card recipient feature, turned on with **Show recipient form for gift cards** in the **Buy buttons** block. See [Product pages]({{ site.baseurl }}/product-pages/#buy-buttons).

## Set up

### 1. Optional: create a gift-wrap product

Create a product such as "Gift wrap" with one variant per wrap (for example Plain, Velvet and Majlis box) and a price on each. Leave it out of your collections, and don't track inventory unless you need to. A variant image is used as that wrap's picture in the gift step.

Without a wrap product, the gift option still offers the message and the no-prices choice, and you can offer free wrapping instead.

### 2. Product page: the Gift option block

Online Store › Themes › **Edit theme** › Products › Default product › **Gift option** block. It's in the default template, just above the buy buttons.

| Setting | Default | What it does |
|---|---|---|
| **Gift-wrap product** | Blank | Each variant becomes a wrap choice, added to the bag as its own line under the item. |
| **Offer free wrapping when no gift-wrap product is chosen** | Off | Shoppers can tick "Gift-wrap it (free)". You see the request on the order; nothing is charged. |
| **Message length limit (characters)** | 150 | 40 to 240. |
| **Show “Leave prices out of the parcel”** | On | Lets shoppers ask you to leave the invoice and any prices out of the parcel. Their request sets the `Gift receipt` cart attribute, shown on the order. |

### 3. Bag: the wrap product

In the **Cart drawer** and the **Cart** section, set **Gift-wrap product** to the same product. Shoppers can then change the wrap when they edit a gift in the bag. See [Cart and checkout]({{ site.baseurl }}/cart-and-checkout/#where-to-find-the-settings).

### 4. Optional: the Gift wrap and message step

1. In Shopify admin, go to Online Store › **Pages** › **Add page**. Title it, for example, "Gift wrap and message", set **Theme template** to **gift** and save.
2. In the theme editor, open that page and select the **Gift wrap and message** section:
   - **Gift-wrap product**: a product with up to three variants, one per wrap choice. It can be the same wrap product.
   - **Offer the large name option**: lets shoppers show the recipient's name in large heading type on the card.
   - **Name font**: **Automatic**, **Display font of the language** or **Accent font of the language**.
3. In the **Cart drawer** and the **Cart** section, add a **Gift toggle** block and set **Gift step page** to the page from step 1.

### 5. Packing slip

Optional: paste the [packing slip snippet](#packing-slip-snippet) into your packing slip template to print each item's gift message and wrap. Shopify doesn't let a theme change packing slips, so this step is yours.

## What the shopper sees

### Product page

A "This is a gift" switch. Switched on, it shows:

- a gift message box with a "Characters left" count (in your store's numerals);
- the wrap choices with their prices, and "No wrapping", when a wrap product is set; or "Gift-wrap it (free)" when free wrapping is on;
- "Leave prices out of the parcel", with the hint "For orders shipped straight to the recipient."

While a paid wrap is chosen, the accelerated checkout buttons (Shop Pay, Apple Pay and others) are hidden, because they can't add the wrap. "Add to bag" always works.

### Bag

The item gets a gift panel with its message and wrap, and two buttons:

- **Edit gift**: change the message or the wrap.
- **Remove gift**: the item stays in the bag; the gift details and the wrap go.

The wrap isn't listed as a separate item: it follows the item it belongs to. Changing the item's quantity changes the wrap's quantity, and removing the item removes the wrap. When any item is a gift, the bag also shows a "Leave prices out of the parcel" box for the whole order.

### Gift wrap and message step

Opened from the "This is a gift" row: in the drawer it opens in place, with "Back to bag"; on the cart page it opens the gift page. Shoppers:

1. choose a wrap, or "Card only, no wrapping";
2. type the recipient's name (up to 40 characters) and a message (up to 240 characters), in Arabic or English, or fill in a ready message for Eid, a wedding, a thank-you or "just because";
3. see a live preview of the card, then press "Save and continue".

The row then shows the wrap's price or "Card added · Edit".

## What you see on the order

### On the item

These appear as line item properties on the order, at checkout and in order emails:

| Property | Value |
|---|---|
| `Gift` | `Yes` |
| `Gift message` | The message, exactly as typed |
| `Gift wrap` | The wrap chosen, for example `Velvet` (or `Yes` for free wrapping) |

A paid wrap is a separate line of the same quantity, so it's charged and counted like any product. Two hidden properties tie the lines together; shoppers don't see them.

### On the order

These appear under **Additional details** on the order page:

| Attribute | Value |
|---|---|
| `Gift receipt` | `yes`: leave the invoice and any prices out of the parcel |
| `gift_to` | The recipient's name, from the gift step |
| `gift_message` | The card message, from the gift step |
| `gift_wrap` | The wrap chosen in the gift step |
| `gift_calligraphy` | Whether the shopper chose the large name |

Use `gift_to` and `gift_message` to prepare the card from the gift step; packing slips can't print these order details.

If a shopper's browser blocks scripts, the gift option still works, with two differences: the wrap is saved as the `Gift wrap` property only (no wrap line is added, so it isn't charged), and "Leave prices out of the parcel" is saved on the item as `Gift receipt: Yes`. In the bag, that item's gift panel then reads "No prices in the parcel".

## Packing slip snippet

Shopify's packing slips never show prices, so gift orders shipped to the recipient are already price-free. The snippet below prints each item's gift message and wrap on the packing slip. The card from the **Gift wrap and message** step and the order-level "Leave prices out of the parcel" choice can't be read there; find them under **Additional details** on the order.

To add it:

1. Go to Settings › **Shipping and delivery** and select **Packing slip template** in the **Documents** section.
2. Find the line items loop ({% raw %}`{% for line_item in line_items_in_shipment %}`{% endraw %}) and paste the snippet under the item's title.
3. Save, then print the packing slip of a recent gift order to check it.

{% raw %}
```liquid
{%- for p in line_item.properties -%}
  {%- assign first_char = p.first | slice: 0 -%}
  {%- if p.last != blank and first_char != '_' and p.first != 'Gift receipt' and p.first != 'Gift' -%}
    <p class="gift-detail">
      {%- if p.first == 'Gift message' -%}
        <strong>Gift message:</strong> “{{ p.last }}”
      {%- else -%}
        {{ p.first }}: {{ p.last }}
      {%- endif -%}
    </p>
  {%- endif -%}
{%- endfor -%}
```
{% endraw %}

The snippet prints every visible property of the item, so `Gift wrap` (and any other properties an app adds) shows too. It skips hidden properties and the `Gift` and `Gift receipt` flags.

The property names (`Gift message`, `Gift wrap` and so on) are fixed English keys. Shoppers see translated labels, but the order keeps these names in every language.
