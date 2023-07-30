---
title: Remote
team:
  file: team.csv
  fields:
    name: true
    slogan:
      type: textarea
    race:
      type: ref
      csv: race
      property: name
race:
  file: race.csv
  fields:
    name: true
    image: true
player:
  file: players.csv
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
{% include widgets/form.html form=page.team %}
{% include widgets/table.html file=team.csv %}
{% include widgets/form.html form=page.race %}
{% include widgets/table.html file=race.csv %}
