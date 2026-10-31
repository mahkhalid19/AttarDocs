---
title: Effects and campaigns
description: Control ATTAR's incense smoke and note ribbon store-wide, and dress your store for Ramadan, Eid and national days.
---

Two groups in Theme settings control ATTAR's signature effects and seasonal looks for the whole store: **Effects** and **Campaign**. To open them, go to Online Store › Themes › **Edit theme** and select the **Theme settings** icon in the editor sidebar.

Section settings keep working alongside them. When a section and Theme settings disagree, the stricter choice wins: for example, smoke that's off in a section stays off even when Theme settings › **Effects** › **Smoke** is **Full**.

## Smoke

Theme settings › **Effects** › **Smoke** controls the slow incense smoke that drifts over parts of the store.

| Option | What it does |
|---|---|
| **Off** | Removes the smoke everywhere. The store doesn't load the smoke's files at all. |
| **Subtle** (default) | Shows the smoke lighter than each section's density (60% of it). |
| **Full** | Uses each section's density as set. |

Where the smoke appears, and the section setting that controls it there:

| Place | Section setting | Default |
|---|---|---|
| Home page hero | **Hero** › **Show smoke**, **Smoke density**, **Smoke color** | On |
| Password page | **Password** › **Show smoke**, **Smoke density**, **Smoke color** | On |
| Mobile menu | **Header** › **Smoke behind the mobile menu**, **Smoke color** | On |
| Page not found | **404 page** › **Show a trace of smoke**, **Smoke color** | Off |
| Search page, before a search and when nothing matches | **Search** › **Show a trace of smoke**, **Smoke color** | Off |

Leave **Smoke color** blank to follow the color scheme. The smoke pauses when it's off screen, and stays still for visitors who've asked their device to reduce motion.

## Note display

Theme settings › **Effects** › **Note display** chooses how scent notes appear across the store.

| Option | What it does |
|---|---|
| **Note ribbon** (default) | Draws how each scent changes over time, on product pages and as a thin strip on product cards. Products need note ribbon data: see [Set up the note ribbon]({{ site.baseurl }}/product-pages/#set-up-the-note-ribbon). For products without it, the **Scent pyramid** card shows the notes list, and the **Note ribbon** block and product cards show nothing. |
| **Classic notes list** | Shows the top, heart and base notes wherever the ribbon would appear on the product page, and hides the strips on product cards. |
| **Off** | Shows no ribbon and no strips. The **Scent pyramid** card on the product page still lists the notes. |

Under **Note ribbon**, section settings still apply:

- **Show note ribbon on cards** in the **Collection**, **Featured products** and **Product recommendations** sections;
- **Notes display** in the **Scent pyramid** block of **Product highlights**;
- whether the **Product** section has a **Note ribbon** block.

## Campaigns

Theme settings › **Campaign** dresses the store for a season. No offers, discounts or countdowns are added: campaigns change the look and add a greeting, nothing more. Add offers yourself if you run them.

| Setting | Default | What it does |
|---|---|---|
| **Campaign** | **None** | **Ramadan**, **Eid**, **Saudi National Day** or **UAE National Day**. |
| **End date** | Blank | Optional. The last day of the campaign, as `YYYY-MM-DD` (for example `2027-03-20`) in your store's time zone. Western or Arabic-Indic digits both work. The campaign switches itself off after that day. Leave blank to keep it on until you change it. |

Shopify caches pages, so the switch-off can take a little while to show everywhere. A date in any other format is ignored and the campaign keeps running, so check the format when you type it.

### What changes while a campaign runs

- **Announcement bar**: if its **Text** is blank, the bar shows the campaign greeting, for example "Ramadan Kareem. Wishing you a blessed month." Text you type always wins. To hide the bar, turn off **Show announcement**.
- **Home page hero**: if its **Accent line** is blank, it shows the greeting in the other script, like the accent line itself: Arabic on English pages (for example رمضان كريم) and English on Arabic pages. The hero's accent line has text by default, so clear it to show the greeting.
- **Accent color**: buttons, links and highlights take a seasonal color (below).
- **Smoke**: warm gold for Ramadan, gold rose for Eid and a faint green for the national days. A **Smoke color** you picked in a section still wins there.

With no campaign, a blank announcement bar shows "Welcome to our store", or your free-shipping line on its own if you've set **Free-shipping threshold** in the bar.

To change the greetings, go to Online Store › **Themes**, select **…** next to ATTAR, then select **Edit default theme content** and search for "campaign". Translate them in the Translate & Adapt app.

### Seasonal accent colors

Each campaign has one accent for dark color schemes and one for light ones. A scheme counts as dark when its background is less than 50% bright.

| Campaign | Dark schemes | Light schemes |
|---|---|---|
| Ramadan (lantern gold) | `#E2B04A` | `#7E5A12` |
| Eid (gold rose) | `#E9A88A` | `#97493A` |
| Saudi National Day (green) | `#3DBF78` | `#006C35` |
| UAE National Day (red, with green smoke) | `#FF6B6B` | `#B3122B` |

The accent is used for text on the page background and as a button color. Every value meets the WCAG AA contrast ratio (4.5:1) against the background, surface and raised surface of the four color schemes that come with every [preset]({{ site.baseurl }}/presets/). If you've changed a scheme to a mid-tone background of your own, check the accent's contrast in the editor while the campaign is on.
