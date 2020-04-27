---
layout: default
---

<div class="page">
    <h1 class="page-title">{{ page.title }}</h1>

    {% assign path = page.url |split: "/" %}
    {% assign category = path[1] %}

    {% capture index %}{% include content-index.md group=category %}{% endcapture %}
    {{ index | markdownify }}
</div>

{{ content }}