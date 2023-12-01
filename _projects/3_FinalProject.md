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

### Dashboard Analysis
The data above shows that as the driving conditions involved in a crash worse, the severity of the crash also worsens. In the this case, I am treating damage as levels of severity, but we can see in the hisogram on the right, this can be applied to the severity of injury.

We can see that among the 3 graphs on the bottom of the dashboard, damage increases as we get worse conditions. For the first graph, we can see that the ratio of high severity crashes increases slighty as we go from "Clear" to "Rain". This is a slight change, but still has some validity. As we continue onto "Blowing Snow," we see that there are no crashes of the lowest severity, and most crashes are high severity. "Snow" is an outlier here, with the ratios of the severity being similar to "Clear," however this is most likely a byproduct of driving slower in the downtown region when it is snowy.

We can also see in the next graph that when we have limited visibility, like "Darkness with Lighted Road," we see the highest severity is much more frequent.

Finally, we see a clear trend in the final graph with the posted speed limit increasing, and how severe crashes are. This indicates that the faster you are driving, the more severe the crash is likely to be.

### Contextual Visualizations
Source: https://crashstats.nhtsa.dot.gov/Api/Public/ViewPublication/813336

In 2020, the National Highway Traffic Safety Administration (NHTSA) conducted an analysis on the rate of fatality in traffic accidents compared to factors such as rural vs urban roads, age of the driver, time of day, etc. We can take a look at these graphs and see how the national data connects to our analysis of Chicago's local data.

![NHTSA graph of fatality rate when speeding](/assets/pngs/nhtsa_speeding_fatal.png)
From this graph here, can see that the national data also lines up with our findings. In our data set, we saw an increase in the severity when we were in poor lighting conditions. While this graph displays the fatality rate while speeding, we can come to the same conclusion that when driving on roads during the nighttime, or in low visibility areas, it is better to slow down and be alert to reduce the severity of a possible accident.

![NHTSA graph of fataility rate per state](/assets/pngs/nhtsa_nat_fatal.png)
While Chicago drivers may be discourage by the above data, fearing that their roads are unsafe, the NHTSA actually provides a hopeful graph of the Urban fatality rate in each state. We can see in the above graph that Illinois has one of the lowest Urban fatality rates in the country, despite being home to the 3rd largest city in the nation. We can see that although we need to be aware and think about how to drive safely on the roads, Illinois and Chicago's infrastructure and road safety provides it's citizens with a good foundation to reduce accidents on their roads.

### Conclusion






## Design Choices



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