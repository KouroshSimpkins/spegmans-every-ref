
<div class="ref-index" markdown="1">
{% if include.group %}

{% for page in site.content |sort "title" %}

{% unless page.relative_path contains "index" %}
{% if page.relative_path contains include.group %}
- [{{page.title}}]({{page.url}})
{% endif %}
{% endunless %}
{% endfor %}

{% else %}
{% for page in site.content |sort "title" %}
{% if page.relative_path contains "index" %}
{% assign urllist = page.url | split: "/" %}
{% assign cat = urllist[1] %}
- ## [{{page.title}}]({{page.url |remove: "/index"}})
{% for page2 in site.content |sort_natural "title" %}
{% unless page2.relative_path contains "index" %}
{% if page2.url contains cat %}

  - [{{page2.title}}]({{page2.url}})
{% endif %}
{% endunless %}
{% endfor %}

{% endif %}
{% endfor %}
{% endif %}

</div>

<hr />

