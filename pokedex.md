---
layout: default
title: PokeDex
permalink: PokeDex
---
{% assign row = site.data.pokemon[0] %}
{% for row in site.data.pokemon %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}|
{% for pair in row %}|:-:{% endfor %}|{% endif %}
|{% for pair in row %}{{ pair[1] }}|{% endfor %}{% endfor %}
