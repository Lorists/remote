---
title: Remote
attribute:
  type: append
  class: admin
  file: attribute.csv
  fields:
    name: true
race:
  type: append
  file: race.csv
  class: admin
  fields:
    name: true
    win:
      type: ref
      csv: attribute
      property: name
    loose:
      type: ref
      csv: attribute
      property: name
---
{% include widgets/form.html form=page.attribute %}
{% include widgets/table.html file=attribute.csv %}
{% include widgets/form.html form=page.race %}
{% include widgets/table.html file=race.csv %}
