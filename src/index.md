---
layout: index.njk
title: Vinny's Eatery
description: "Located in Melbourne’s Docklands, Vinny's Eatery is known for fresh banh mi, hearty pho, and flavourful Vietnamese-style breakfast and lunch dishes in a relaxed setting."
permalink: "/"
---

{{description}}

<br>

# Menu
Explore our delicious Vietnamese dishes, from classic pho to fresh salads and bánh mì.

{% set icon = "fork-knife" %}
{% set url = "/menu" %}
{% set text = "View Menu" %}
{% set style = "primary" %}
{% set align = "start" %}
{% include "partials/btn.njk" %}

<br>
<br>


## Opening Hours

**Monday to Saturday** :   
7am to 6pm

**Sunday** :   
Closed




<br>

### {{site.title}}
{% set mapAddress = "Vinny's Eatery Docklands Melbourne" %}
{% include "partials/google-map.njk" %}
