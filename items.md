---
layout: default
title: ItemDex
permalink: ItemDex
---
# Items
{% assign row = site.data.items[0] %}
{% for row in site.data.items %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}

# Exclusive Items
{% assign row = site.data.itemsx[0] %}
{% for row in site.data.itemsx %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}