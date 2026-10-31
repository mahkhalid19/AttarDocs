---
title: Pages and templates
description: Create Our story, Boutiques, Compare, Scent finder, Lookbook, Contact and gift pages with ATTAR's templates, and set up the blog, 404, password, account and gift card pages.
---

ATTAR comes with ready-made templates for the pages a fragrance store usually needs. A template decides which sections a page shows. You write the page in Shopify admin, assign the template, then fill in the sections in the theme editor.

## Create a page with a template

1. Go to Online Store › **Pages** and select **Add page**.
2. Enter a **Title**, for example "Our story". Add content if the template uses it (each template below says so).
3. Under **Theme template**, choose the template, for example **story**.
4. Select **Save**.
5. Add the page to a menu in Online Store › **Navigation** so customers can find it.

To fill in the sections, go to Online Store › Themes › **Edit theme**. Use the page selector at the top of the editor, choose **Pages**, then the template. Changes to a template apply to every page that uses it.

To have two pages with the same kind of layout but different content, for example two lookbooks, create a second template: in the editor's page selector, choose **Pages** › **Create template**, base it on the existing one, and assign it to the second page.

## Page templates

| Template | Use it for |
|---|---|
| **story** | Our story: your brand's history and values. |
| **boutiques** | A list of your physical shops. |
| **compare** | A side-by-side comparison of up to four fragrances. |
| **scent-finder** | A short quiz that recommends a fragrance. |
| **lookbook** | Shoppable photos. |
| **contact** | A contact form. |
| **gift** | The gift wrap and message step. |
| Default page | Any other page, such as FAQs or delivery information. |

### Our story (story)

**Admin:** write your story as the page content. It's shown by the **Story text** section and translated with the page.

**Theme editor:** the template has five sections:

- **Story hero**: a **Photo** with an **Eyebrow**, **Heading** and **Text**. **Layout** puts the text on a panel over the photo or beside it. An empty **Heading** uses the page title.
- **Story text**: shows the page content. Set **Content** to **Custom text** to write it in the editor instead.
- **Story chapters**: a timeline. Each **Chapter** block has a **Marker** (a year, a date or a word), a **Title**, **Text** and an optional **Photo**. The four starting chapters use **Starter text**: sample copy in Arabic and English that you replace by typing your own.
- **Story values**: what your brand stands for. Each **Value** block has an **Icon**, a **Title** and **Text**, and can also use **Starter text**.
- **Story image with text**: a photo beside text and a button. An empty **Button link** goes to all products.

Replace the starter text before you publish, so the story is truly yours.

### Boutiques (boutiques)

**Admin:** name the page, for example "Our boutiques". Page content isn't shown.

**Theme editor:** the **Boutiques** section has an **Eyebrow**, **Heading** and **Text**, and one **Boutique** block per shop (up to 40). For each boutique, fill in:

- **Name** and **City**. Boutiques in the same city share a city filter; the filter appears when you have boutiques in two or more cities and **Show city filter** is on.
- **Address**, **Opening hours** (one line per day or range of days) and an optional **Note**, such as where to park.
- **Phone** and **WhatsApp number**, with the country code. Turn on **Use the store WhatsApp number** to use the number from Theme settings › **Floating widgets** when the boutique's own **WhatsApp number** is empty.
- **Photo** and its **Image description (alt text)**.
- **Maps link**: paste the share link from Google Maps or Apple Maps. Without one, the card's map link searches for the address.

The template starts with two sample boutiques. Replace them with your own, or remove them.

### Compare (compare)

**Admin:** name the page "Compare", so its web address ends in `/pages/compare`. The **Compare teaser** section on collection pages links to a page with this address when its **Button link** is empty. If you use another name, set the teaser's **Button link** yourself. Page content is shown as the intro when **Intro text** is empty.

**Theme editor:** the **Compare** section has:

- **Heading** (empty uses the page title) and **Intro text**.
- **Default fragrances**: the products shown until a shopper builds their own list.
- **Collection for "Add a fragrance"**: where the **Add a fragrance** button leads. Empty uses all products.

Shoppers add products from collection pages. Turn on **Show Compare toggle on cards** in the **Collection** section, and shoppers can tick up to four products. The table shows price, rating, concentration, scent family, notes, longevity, sillage, sizes and a buy button, and hides any row that's empty for every product. Shoppers can share the comparison by copying the page's link.

### Scent finder (scent-finder)

**Admin:** name the page, for example "Find your scent". Page content isn't shown.

**Theme editor:** the **Scent finder** section asks up to four questions and recommends a product. It runs in the shopper's browser; no app is needed.

- **Question** blocks: each has a **Question**, a **Hint** and four options. Choose **Ready-made copy** for a translated question, such as **Who is it for?** or **Heavy or light?**, or type your own.
- **Question that picks the result**: the question whose answer decides the recommendation. By default it's question 3 (**Heavy or light?**).
- **Result** blocks: each links one **Answer** of that question to a **Product**, with **Why it suits them** and **Tags**. **Ready-made copy** fills the text with translated descriptions.
- **Result when that question is skipped**: the answer to use when a shopper skips the deciding question.
- **Sample note title** and **Sample note text**: an optional note, for example a sample offer. Only promise what your store actually offers.
- **Discovery set button** and **Discovery set collection**: an optional link to your discovery sets.

The template starts with four questions and four results. Choose a **Product** for each result; the ready-made result copy names example scents, so replace it with your own description.

To link to the finder from the home page, set **Button link** in the **Scent finder teaser** section. The teaser's button shows only when it has a link.

### Lookbook (lookbook)

**Admin:** name the page, for example "Lookbook". Page content isn't shown.

**Theme editor:** the **Lookbook** section is a grid of photos with product hotspots.

- **Frame** blocks are the photos. Set the **Image**, the **Shape** (**Wide** or **Tall**), a **Caption** or **Ready-made caption**, and an **Image description**.
- **Hotspot** blocks are the dots on a photo. A hotspot belongs to the frame just above it in the block list. Choose the **Product**, then set **Horizontal position** and **Vertical position**. The dot stays on the same spot on Arabic pages.
- **Layout**: **Editorial** (wide frames span two of three columns on desktop) or **2-up** (two columns at every size).
- **Show "Add the look"** shows a button that adds every in-stock hotspot product to the cart in one step, with the total price. It appears when the lookbook has at least two in-stock products.

The template starts with four frames, each with one hotspot. Choose a product for each hotspot. A frame without an image uses its first hotspot product's photo.

### Contact (contact)

**Admin:** name the page "Contact". Page content is shown above the form when **Show page content** is on.

**Theme editor:** the **Contact form** section has a **Heading** (empty uses the page title), **Text**, **Show phone number field**, **Alignment**, **Background** and **Section spacing**.

Messages are sent to your store's contact email, which you set in Settings › **General**. You can also add the **Contact form** section to other pages; set **Heading level** to **Section heading (H2)** when it sits below other content.

### Gift page (gift)

The gift page holds the order-level gift wrap and message step. Shoppers reach it from the "This is a gift" row in the cart.

1. Create a page, for example "Gift wrap and message", and choose the **gift** template.
2. In the theme editor, open the page and choose the **Gift-wrap product** in the **Gift wrap and message** section.
3. In the **Cart drawer** and **Cart** sections, add a **Gift toggle** block and choose your page as the **Gift step page**. The cart's gift row stays hidden until a page is chosen.

[Gifting]({{ site.baseurl }}/gifting/) explains the gift-wrap product, messages and packing slips.

## Collection template: Express order

The **express** collection template shows every product and variant of a collection in one table, with a quantity for each, so customers can order many items at once. It suits reorders, trade customers and corporate gift orders. Assign it in Products › **Collections** › your collection › **Theme template**. See [Collections and search]({{ site.baseurl }}/collections-and-search/).

## Blog and articles

**Admin:** write posts in Online Store › **Blog posts**. Add a featured image with alt text to each post. Turn comments on or off for each blog under **Manage blogs**.

**Theme editor:** open a blog with the page selector, **Blogs**. The **Blog** section sets **Articles per page** and whether to **Show featured image**, **Show date**, **Show author**, **Show comment count** and **Show tag filter**.

The article page has no settings. It shows the featured image, title, date and author, the post, and comments when the blog allows them. To show recent posts on another page, add the **Blog posts** section.

## 404 page

Customers see the 404 page when a link is broken. Open it by choosing **404 page** in the editor's page selector. The **404 page** section has:

- **Heading** and **Text**: leave them blank to use the theme's default copy in each language.
- **Show a trace of smoke** and **Smoke color**.
- **Products** or **Or a collection**: two products to suggest. Add a **Products heading** if you like.
- **Popular searches**: searches separated by commas. Blank uses a default list in each language.
- **Family collections** or **Browse menu**: links to help customers find their way.
- **Show WhatsApp help row**.

## Password page

The password page is shown while your store is password protected. Turn protection on or off in Online Store › **Preferences** › **Password protection**, and edit the page by choosing **Password** in the editor's page selector.

The **Password** section has two layouts: **Drop: countdown over the photo** and **Plain: form beside the photo**. Fill in:

- **Photo**, **Logo** or **Wordmark**, and the smoke settings.
- **Drop name**, **Name in the other script**, **Eyebrow** and **Description**. An empty **Description** uses the password message from Online Store › **Preferences**.
- **Launch date and time**, for example `2026-11-14T20:00:00+04:00`, to show a countdown. Leave it blank to hide the countdown.
- **Show waitlist form**: shoppers leave their email and are added to Customers with the **Customer tag** you choose. **Show "notify on WhatsApp" checkbox** adds the tag `whatsapp` when ticked.
- **Show Instagram handle**: uses the Instagram link from Theme settings › **Social media**.

The store password form opens from "Have a password? Enter" at the bottom of the page, so you and your team can still enter the store. It also has a "Store owner? Log in" link to your Shopify admin.

## Customer accounts

Choose how customers sign in at Settings › **Customer accounts**.

- **Customer accounts** (Shopify's current version): Shopify hosts the sign-in, orders and profile pages. The header's account icon opens Shopify's account menu. In the **Header** section, **Customer account menu** sets its links.
- **Legacy customer accounts**: the theme shows the sign-in, registration, account, order, addresses, activation and password reset pages. They have no settings; they use your colors, fonts and the theme's Arabic and English text.

## Gift card page

When a customer buys a gift card, Shopify emails a link to the gift card page. The page shows the balance and code, a QR code, an **Add to Apple Wallet** button, the expiry date, and the recipient's name and scheduled send date when the buyer set them.

The page shows your **Brand logo** from Theme settings › **SEO and sharing**. It has no other settings.
