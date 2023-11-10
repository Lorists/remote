---
title: Remote
team:
  file: team.json
  fields:
    name: true
    color_1:
      type: color
    color_2:
      type: color
    race:
      type: ref
      csv: races
races:
  file: races.csv
  fields:
    name: true
---
**Race form**

{% include widgets/form.html form=page.races class='unfork' %}

**Team form**

{% include widgets/form.html form=page.team %}
