---
layout: default
---

# Test data parsing and generation

## Overall description: {{ site.data.testdata.description }}

{% for section in site.data.testdata.sections %}
### Section: {{ section.description }}
{% for item in section.list %}
Item:  
* field1: {{ item.field1 }}
* field2: {{ item.field2 }}
* field3: {{ item.field3 }}
{% endfor %}

{% endfor %}

## Test table output

{% for section in site.data.testdata.sections %}
### Section: {{ section.description }}

<table>
  <tr>
    <th scope="col">Field 1</th>
    <th scope="col">Field 2</th>
    <th scope="col">Field 3</th>
  </tr>
{% for item in section.list %}
  <tr>
    <td>{{ item.field1 }}</td>
    <td>{{ item.field2 }}</td>
    <td>{{ item.field3 }}</td>
  </tr>
{% endfor %}
</table>

{% endfor %}
