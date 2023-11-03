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

My first visualization displayed the same plot as the starboard homework, so I'll quote the original description and note any differences:

"For my first visualization, I created a scatter plot that compares the usages of buildings with when they were built in the Champaign and Normal city areas. I also use colors to emphasize any differences that could be found in the use and build year of buildings in each city. I chose to restrict to Champaign and Normal because my partner is from Normal, IL, and I thought it could be fun to compare the age and uses of buildings in her area versus mine. I also added a tooltip to show whether or not the building was still in use/in the process of being built to give the viewer some context. If the building is decommissioned, then its use is less relevant than a building still in use."  Here the only difference was trying to use a jitter, which I couldn't get working in vega-lite. It worked in the jupyter notebook, but when exporting to jekyll, it appeared the same as in starboard. One major change was that I didn't read from a url anymore, I read in the data first into a pandas dataframe and then passed that into Altair.

"I decided to use individual markers instead of grouping them so each data point could be individually viewed and investigated if the user desired. I added tooltips and scrolling to let users navigate the data and make connections that I maybe hadn’t anticipated finding when first creating the plot. I also added custom colors to the markers which signified which town they were a part of, making use of the color association many people will have between Normal → ISU → Red and Champaign → UIUC → Blue to make it more natural to understand which marker belonged to which city. I also filtered out any data that had the year 0, as this data was not valid." I also filtered the cities to just Champaign and Normal using pandas in this version before creating the viz to improve how long it took to render the data.

For my encoding types, I also need to note that I used nominal for the useage descriptions since they are unordered categorical data. I wanted to use a datetime format for Construction Year, but when doing so no years befoer 1970 would show up, so I had to use Quantitative instead, like my original plots. I realized that I could encode them as timestamps and try to play around with the datatype in Altair, but I only have years (which are discrete values) so the datetime format isn't necessary for the clarity of the chart. The City (Champaign vs Normal) is also nominal for the same reasons as usage.

## Plot 2
Drag for interactivity!
<vegachart schema-url="{{ site.baseurl }}/assets/json/cook_sizes.json" style="width: 100%"></vegachart>

For this visualization I also chose the same plot, except with a linked histogram on the bottom to complement it. Differences will be noted after each quote from hw 7:

"For my second visualization, I created a scatter plot that compares the total floors versus square footage of every building in Cook County. I wanted to know if there was a positive correlation between square footage and total floors in buildings like I suspected, and was curious to know about these buildings in the Cook County area since I am from Chicago. I also wanted to investigate if buildings with greater floors or large square footage tended to have certain uses over others." I also added a linked histogram which displays the total number of buildings with each usage type in the selection area, or across all buildings in the chart if no selection. With the histogram, it is easier to find trends in the usage of buildings with their square footage and floor count.

"I made each building its own data point for the same reason as the previous plot, to allow users to investigate individual building’s properties and those similar to it around it in the plot. I also colored the points based on their usage to possibly identify trends in how many floors or how large a building is and what it is used for. I also added panning, zooming, and tooltip interactions to let users better investigate areas of markers or individual markers to identify patterns in the data. The tooltips contain the agency that owns the building, the city, usage, and location name to better connect these buildings to real world places. This was users can look up these buildings to investigate them further if they wish. I ended up using a log scale for the square footage because there were a lot of large outliers, and the log scales better visually balanced the plot, while keeping the correlation between the two features.  I also filtered out any buildings with 0 square footage or floors, as this cannot exist and would break the logarithmic scales used for square footage." This plot was different because I did not have panning and zooming, since the interaction I included was a linked histogram controlled by an interval selection. While this makes it more difficult to individually select and look at a building, the benefit of the interactive histogram is worth it. I believe that the histogram gives the user an easier was to identify trends between building size and usage. I kept the same filters as I did in vega-lite, except I did them using the pandas dataframe.

I was also unable to get the width filling behavior like with the first plot because the linked charts are wrapped in a container, which doesn't have variable width functionality. 

I also used the default color scheme since it had enough colors that were all distinct, which worked perfectly for the unordered categorical data it is representing. For the encoding types, I encoded the x and y variables as quantitative because they were ordered numerical values, whereas I kept the usages as nominal like the previous visualization.

## Search The Data & Methods

Links to data and analysis code:

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data"%}
</div>
<div class="right">
{% include elements/button.html link="https://github.com/carlosconley/carlosconley.github.io/blob/main/python_notebooks/homework_7_workbook.ipynb" text="The Analysis" %}