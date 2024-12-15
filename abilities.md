---
layout: default
title: AbilityDex
permalink: AbilityDex
---
{% assign row = site.data.abilities[0] %}
{% for row in site.data.abilities %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}