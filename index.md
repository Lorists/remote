---
title: Remote
attribute:
  file: attribute.csv
  fields:
    name: true
race:
  file: race.csv
  fields:
    name: true
    ma:
      type: number
    st:
      type: number
    ag:
      type: number
    skills:
      type: select
      multiple: true
      default: [Block, Catch, Dodge, Pass, Sure Hands]
---
{% include widgets/form.html form=page.attribute %}
{% include widgets/table.html file=attribute.csv %}
{% include widgets/form.html form=page.race %}
{% include widgets/table.html file=race.csv %}
