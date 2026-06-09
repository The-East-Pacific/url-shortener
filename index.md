---
layout: default
---

> ⚠️ **Heads up:** These short links are out of date and are currently being updated. Some destinations may change.

{% assign redirects = site.urls | where_exp: "item", "item.redirect_to != nil" %}

{% for page in redirects %}
  [{{ page.url }}]({{ page.url | relative_url }}) `{{ page.redirect_to }}`

  ---
{% endfor %}
