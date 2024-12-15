---
layout: default
title: StatusDex
permalink: StatusDex
---
{% assign row = site.data.status[0] %}
{% for row in site.data.status %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}