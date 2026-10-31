---
title: Custom code and apps
description: Add your own Liquid, HTML and CSS to ATTAR, use app blocks and app embeds, and keep your changes through theme updates.
---

Most stores never need custom code: ATTAR's sections, blocks and settings cover the common needs, and apps add their features through app blocks. When you do need something extra, ATTAR gives you places to add code without editing the theme's files.

## Before you add custom code

- **Duplicate your theme first.** In Online Store › **Themes**, select **…** next to ATTAR, then select **Duplicate**. Make your changes on the copy, check them, then publish it. If something breaks, you can go back to the original.
- **Custom code isn't covered by theme support.** We support ATTAR's own features and settings. We can't write, review or fix custom code, code added by apps, or problems caused by edits to the theme's files. If you contact support, tell us about any custom code so we can rule it out.
- **Consider hiring an expert.** For custom work, we recommend hiring a [Shopify Partner](https://www.shopify.com/partners/directory) who works with themes.

## Custom Liquid section

The **Custom Liquid** section adds your own Liquid, HTML, CSS or JavaScript to any page, including the header and footer areas. Use it for an app's embed code, a third-party widget or a small piece of custom content.

1. In Online Store › Themes › **Edit theme**, open the page where you want the code.
2. Select **Add section**, then choose **Custom Liquid**.
3. Paste your code into the **Custom Liquid** field.
4. Select **Save**.

| Setting | What it does |
|---|---|
| **Custom Liquid** | Your code. |
| **Make section full width** | Lets the content use the full width of the screen instead of the page width. |
| **Background** | **Page background**, **Subtle** or **Dark**. |
| **Section spacing** | The space above and below the section: **None**, **Compact** or **Normal**. |

## Custom Liquid block

The **Product** section (product pages) and the **Featured product** section also have a **Custom Liquid** block. Use it to add code between the product's other blocks, for example a size guide link or an app snippet that needs to sit next to the buy buttons.

Select **Add block** in the section, choose **Custom Liquid**, paste your code, then drag the block into place. In the **Product** section, the code can use the product being shown, for example `{% raw %}{{ product.title }}{% endraw %}`. In **Featured product**, the code can't read the featured product, so use it for fixed content or app snippets.

## Custom Liquid in more than one language

Text in a **Custom Liquid** field is the same in every language, and Translate & Adapt can't translate it. To show different text per language, check the page's language in your code:

{% raw %}
```liquid
{% if request.locale.iso_code == 'ar' %}
  <p>توصيل مجاني داخل المدينة</p>
{% else %}
  <p>Free delivery within the city</p>
{% endif %}
```
{% endraw %}

If you write CSS, use properties that follow the reading direction, such as `margin-inline-start` and `text-align: start`, instead of `margin-left` and `text-align: left`. Your styles then work on both Arabic (right-to-left) and English (left-to-right) pages.

## Custom CSS

Shopify's theme editor has its own **Custom CSS** field for small style changes, both in Theme settings and at the bottom of each section's settings. Section CSS applies only to that section. Test your CSS on Arabic and English pages, on a phone and on a computer.

## App blocks

Many apps add their features as app blocks, which you place like any other block. No code is needed.

These sections accept app blocks:

- **Product** (product pages), for example for reviews, size advice or subscriptions.
- **Featured product**.
- **Product reviews**, for your reviews app's review list.

To add one, select **Add block** in the section, then choose the app's block under **Apps**. Drag it into place and fill in its settings. Some apps also offer whole sections, which you add with **Add section**.

When you uninstall an app, its app blocks disappear from your theme automatically.

## App embeds

Apps that add something to every page, such as chat, analytics or a cookie banner, use app embeds. Turn them on or off in the theme editor under **App embeds** in the sidebar.

ATTAR keeps one floating area on the page for its WhatsApp and back-to-top buttons. If an app adds a bar pinned to the bottom of the screen, go to Theme settings › **Floating widgets** and increase **Raise widgets by** so ATTAR's buttons sit above it. See [Theme settings]({{ site.baseurl }}/theme-settings/#floating-widgets).

## Editing theme code

You can edit ATTAR's files in Online Store › **Themes**: select **…** next to ATTAR, then select **Edit code**. This is for experienced developers only. Before you do:

- Duplicate the theme and edit the copy.
- Keep a note of every change, so you or a developer can repeat it later.
- Remember that edited code isn't covered by theme support.

Each file in the code editor keeps older versions, so you can compare or restore a file after a change.

## Theme updates and your customizations

When a new version of ATTAR is released, a notice replaces the version number in Online Store › **Themes**. Select **Add to draft themes** to add an updated copy to the **Draft themes** section, and you choose when to publish it.

What carries over to the updated theme:

- **Carries over:** your theme editor customizations: theme settings, sections, blocks, their content, and the code you've pasted into **Custom Liquid** sections and blocks and **Custom CSS** fields.
- **Carries over only without conflicts:** changes made in **Edit code**. Code edits are included when they don't conflict with the update; if they can't be included, the theme card says so, and you or your developer need to make them again on the updated theme. Save a copy of any code edits before updating.

This is one more reason to use the **Custom Liquid** section and block, **Custom CSS** and app blocks rather than editing the theme's files: your changes always carry over when you update.

Before publishing an updated theme, preview it in Arabic and English and check any custom code still works with the new version.
