---
layout: default
---

# Test data parsing and generation

## Overall description: {{ site.data.testdata.description }}

{% for section in site.data.testdata.sections %}
### Section: {{ section.description }}
{% for item in section.list %}
  field1: {{ item.field1 }}
  field2: {{ item.field2 }}
{% endfor %}

{% endfor %}
