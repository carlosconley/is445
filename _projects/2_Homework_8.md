---
name: Homework 8 
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: Submission page for homework 8
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Homework 8

## Plot 1
<vegachart schema-url="{{ site.baseurl }}/assets/json/ch_no_years.json" style="width: 100%"></vegachart>




## Plot 2
<vegachart schema-url="{{ site.baseurl }}/assets/json/cook_sizes.json" style="width: 100%"></vegachart>


## Search The Data & Methods

Links to data and analysis code:

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data"%}
</div>
<div class="right">
{% include elements/button.html link="https://github.com/carlosconley/carlosconley.github.io/blob/main/python_notebooks/homework_7_workbook.ipynb" text="The Analysis" %}