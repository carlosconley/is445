---
name: Crash severity in poor conditions
tools: [Python, HTML, vega-lite, altair]
image: assets/pngs/chicago_flag.png
description: Submission page for homework 8
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Poor driving conditions can increase car crash severity

It's often said that 

## The Data!
<vegachart schema-url="{{ site.baseurl }}/assets/json/crashes_chart.json" style="width: 100%"></vegachart>

## Analysis


## The Raw Data and & Methodology


<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/carlosconley/carlosconley.github.io/main/python_notebooks/chicago_crash_2023.csv" text="My processed data"%}
</div>
<div class="left">
{% include elements/button.html link="https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if" text="The Raw Data"%}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/carlosconley/carlosconley.github.io/blob/main/python_notebooks/homework_7_workbook.ipynb" text="The Analysis" %}