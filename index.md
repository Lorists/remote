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
      type: select
      ref: attribute
    loose:
      type: select
      ref: attribute
---
{% include widgets/form.html form=page.attribute %}
{% include widgets/table.html file=attribute.csv %}
{% include widgets/form.html form=page.race %}
{% include widgets/table.html file=race.csv %}
