# Vinny’s Eatery 🍜

A simple static website for **Vinny’s Eatery** in Melbourne’s Docklands, showcasing the menu, opening hours, and location.

Built using the **SpaceClub Web Template** (Eleventy + Nunjucks).  
Template: https://github.com/SpaceClub-Web/template

---

## Pages

- **Home:** `index.md`
- **Menu:** `menu.md`
- **Navbar:** `src/_includes/partials/navbar.njk`

There are only two pages and one navbar for simplicity.

---

## Editing the Home Page

**File:** `index.md`

You can change:
- **Title & description** (used for SEO and page content):
```yaml
  title: Vinny's Eatery
  description: "Your description here"
````

* **Text content** directly in Markdown
* **Menu button** by editing the button variables:

```njk
{% set text = "View Menu" %}
{% set url = "/menu" %}
```
* **Google Maps location**:

```njk
{% set mapAddress = "Vinny's Eatery Docklands Melbourne" %}
```

---

## Editing the Menu Page

**File:** `menu.md`

* Menu items use Markdown headings (`###`) and paragraphs.
* Spacing between dishes is controlled by the `<style>` block at the top.
* The button at the bottom uses the same reusable button partial.

---

## Editing the Navbar

**File:** `src/_includes/partials/navbar.njk`

* Update links, labels, or order directly in this file.
* Changes apply to all pages automatically.

---

## Buttons

Buttons are reusable and use a partial.

**File:** `src/_includes/partials/btn.njk`

### How to use a button

Set the variables **before** including the partial:

```njk
{% set url = "/menu" %}
{% set text = "View Menu" %}
{% set icon = "fork-knife" %}
{% set style = "primary" %}
{% set align = "start" %}

{% include "partials/btn.njk" %}
```

---

## Adding a New Page

1. Create a new `.md` file (e.g. `about.md`)
2. Add front matter:

   ```yaml
   ---
   layout: base.njk
   title: About
   description: "About Vinny’s Eatery"
   permalink: "/about/"
   ---
   ```
3. Add content below the front matter.
4. Add a link to the navbar.

---

## Changing Colours

Colours are controlled via CSS (Bootstrap classes + custom styles).

* Button colours: change `style` (e.g. `primary`, `secondary`, `light`)
* Global colours: edit your main CSS file.

---

## Deployment

This site is ready to deploy on **Netlify** using the included configuration.

---

Simple, fast, and easy to update ✨
