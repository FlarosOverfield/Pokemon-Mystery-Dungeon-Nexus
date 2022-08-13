---
title: Table test
---

{% assign row = site.data.authors[0] %}
{{ row | inspect }}

* * *

{% assign row = site.data.test[0] %}
{% for pair in row %}
  {{ pair | inspect }}
{% endfor %}

* * *

<ul>
{% for row in site.data.test %}
  <li>{{ pair[0] }}-{{ pair[1] }}</li>
{% endfor %}
</ul>

* * *

<table>
  <thead>
  {% for row in site.data.test %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
  </thead>

* * *

  <tbody>
    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
  </tbody>
</table>

* * *

<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>The table body</td>
            <td>with two columns</td>
        </tr>
    </tbody>
</table>