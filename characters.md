---
layout: default
title: Characters
permalink: Characters
---
{% assign row = site.data.characters[0] %}
{% for row in site.data.characters %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}