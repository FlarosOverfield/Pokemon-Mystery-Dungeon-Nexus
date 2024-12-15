---
layout: default
title: MoveDex
permalink: MoveDex
---
{% assign row = site.data.moves[0] %}
{% for row in site.data.moves %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}