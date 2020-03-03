---
layout: page
title: Lib-Static Howtos
list-js: true
---

<div id="howtoList">
    <div class="form-inline">
        <label class="sr-only" for="howtoSearch">Search howtos</label>
        <input type="text" class="search form-control mb-2 mr-2" id="howtoSearch" placeholder=" Search">
        <button class="btn btn-secondary sort mb-2 mr-2" data-sort="title">Title</button>
        <button class="btn btn-secondary sort mb-2 mr-2" data-sort="tags">Tags</button>
    </div>
    <div class="listJs">
        {% for h in site.html_pages %}{% if h.layout == "howto" %}
        <div class="border rounded p-3 my-2">
            <a href="{{ h.url | relative_url }}"><span class="title h5">{{ h.title }}</span></a>
            <small>[ <span class="tags">{{ h.tags | split: ';' | join: ' '}}</span> ]</small>
        </div>
        {% endif %}{% endfor %}
    </div>
</div>
