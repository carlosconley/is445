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

We learn in driver's education that rain and snow can increase our likelihood for crashes. The same is said for driving at elevated speeds and at night. However, does this mean that the severity of crashes increases under these conditions? Using a subset of car crashes recorded in Chicago's surrounding downtown area, we can see trends that are applicable to similar urban areas.

Have a go at poking around the data to some trends for yourself! You can drag and scroll on the plot of daily crashes to filter the data and double click to clear your filter.

## The Data!
<vegachart schema-url="{{ site.baseurl }}/assets/json/crashes_chart.json" style="width: 100%"></vegachart>

## Analysis


## Methodologies

How I created the plots and what data I used!

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/carlosconley/carlosconley.github.io/main/python_notebooks/chicago_crash_2023.csv" text="My processed data"%}
</div>
<div class="right">
{% include elements/button.html link="https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if" text="The Raw Data"%}
</div>


<div class="left">
{% include elements/button.html link="https://github.com/carlosconley/carlosconley.github.io/blob/main/python_notebooks/chicago_crashes.ipynb" text="The Notebook" %}