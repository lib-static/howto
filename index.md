---
layout: page
title: Lib-Static Howtos
---

{% for h in site.html_pages %}{% if h.layout == "howto" %}
- [{{ h.title }}]({{ h.url | relative_url }})
{% endif %}{% endfor %}