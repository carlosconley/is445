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

<vegachart schema-url="{{ site.baseurl }}/assets/json/crashes_chart.json" style="width: 100%"></vegachart>