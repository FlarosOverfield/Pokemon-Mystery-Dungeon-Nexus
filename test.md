---
layout: default
title: test
permalink: test
---
{% assign row = site.data.test[0] %}
{% for row in site.data.test %}{% if forloop.first %}{% for pair in row %}|{{ pair[0] }}{% endfor %}{% endif %}|
{% for pair in row %}|{{ pair[1] }}{% endfor %}{% endfor %}|
