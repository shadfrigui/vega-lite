# What Is Vega-Lite? And What Is Vega?
Vega and Vega-Lite are open-source data visualization tools that enable you to create and share interactive visualizations. Vega and Vega-Lite are known as *declarative* visualization grammars as they provide a declarative syntax to describe the visual appearance and interactive behavior of a visualization. Similar in spirit to how SQL provides a declarative language for expressing database queries, Vega and Vega-Lite provide declarative languages for describing visualizations in a JSON (JavaScript Object Notation) format. These descriptions are defined as Vega/Vega-Lite specifications.

Vega-Lite is built on top of Vega and provides a more concise visualization grammar to build a wide range of visualizations *quickly* while offering control to override defaults and customize various parts of a visualization. As Vega-Lite can compile its specifications to Vega specifications, users may use Vega-Lite as the *primary* visualization tool and transition to using the lower-level language, Vega, for advanced use cases if needed.

Vega-Lite specifications represent a high-level description of what you want the visualization to include, in terms of data, graphical marks (point, bar, line, etc.), and visual encoding channels (x-axis, y-axis, color, size, etc.). The key idea is that you declare links between data fields and encoding channels. The rest of the plot details are handled automatically. Axes, legends, and scales are all automatically generated by the Vega-Lite compiler based on a set of carefully designed rules. This approach is what makes Vega-Lite specifications to be concise and suitable for quick visualization authoring. 

Vega-Lite supports data analysis, data transformations (e.g., aggregation, binning), visual transformations (e.g., stacking, faceting), flexible combinations of charts, and interactions (e.g., zooming, selection).
<br />
<br />

# Vega-Lite Ecosysytem
The Vega-Lite [ecosystem](https://vega.github.io/vega-lite/ecosystem.html) is huge, and there are many integrations, applications, and extensions of the Vega-Lite language and compiler. Here's a quick overview of *some* of the tools that you can use to write Vega-Lite specifications: 
- You can use the [Vega online editor](https://vega.github.io/editor/#/custom/vega-lite) to replicate graphics from the [example gallery](https://vega.github.io/vega-lite/examples/) and make small changes. It's very useful for learning and experimenting without the need to install anything. Including data [inline](https://vega.github.io/vega-lite/docs/data.html#inline) in the online editor is okay for small datasets; but if your data is large, the editor would have to do a lot more work slowing everything down. Uploading data somewhere and accessing it via a [URL](https://vega.github.io/vega-lite/docs/data.html#url) is another option but can be slower for large datasets, and you will not want to make your sensitive data publicly available.
- To overcome the limitations of the online editor, you can use VS Code + the [Vega Viewer extension](https://github.com/RandomFractals/vscode-vega-viewer) to work on Vega-Lite projects locally. The Vega Viewer extension provides language support, interactive preview of Vega/Vega-Lite graphs, and allows you to work with local files (more details [here](https://github.com/RandomFractals/vscode-vega-viewer)). Additionally, you get all VS Code features.
- If you're authoring Power BI reports, you can use the Power BI custom visual, [Deneb](https://deneb-viz.github.io/), to write Vega-Lite specs in Power BI and benefit from the power of both tools. One Deneb-only feature I like is the ability to use zoom controls to zoom in and out in the preview area. This is very useful when working with large graphs.
- If you prefer working with Python instead of the JSON-based Vega-Lite language, you can use [Altair](https://altair-viz.github.io/), which is a declarative statistical visualization library for Python. Altair provides a friendly Python API that generates Vega-Lite specifications in JSON format. Environments such as Jupyter Notebooks, JupyterLab, and Colab can then take this specification and render it directly in the web browser.
<br />

# My Vega-Lite Experimentations
I use the online editor, VS Code, and Deneb. For each visualization, I'll add the following JSON files (if possible):
1. ```filename-online-editor.json``` for working in the online Vega editor.
2. ```filename.vl.json``` for working in VS Code locally. 
3. ```filename-deneb.json``` for working in Power BI. **This is not a Deneb template. Just copy the content of the file and paste it into Deneb's Specification tab. Make sure to delete everything in Deneb's Config tab because I already added the Config object within the specification.** I use Deneb for everything, including titles, subtitles, and footers. You can use Power BI's text boxes instead.

### Note
I use custom fonts in many of my visuals. If you see the Times New Roman font, then it is a sign that a custom font is used.
<br />
<br />


## Du Bois Visualization Challenge 2023 - Challenge 7
This was part of the [Du Bois Visualization Challenge 2023](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2023).

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/28974c8e1a9c90f84b265802789e5e77ab4e54a3/dubois-challenge-2023/images/dubois-challenge-07.png">
</p>

## FDA Inspections
This was part of [Makeover Monday 2022](https://www.makeovermonday.co.uk/data/data-sets-2022/) - Week 42.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/ae3abc1a586520368061be423b7d6d2f2a5e76d3/fda-inspections/images/fda-inspections.png">
</p>

## Warren Buffett's Top 5 Holdings
This was part of [Makeover Monday 2022](https://www.makeovermonday.co.uk/data/data-sets-2022/) - Week 37.
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/b92c848baf83e38e623f4832c7e7c741cb09fb75/buffet-top-5-holdings/images/buffet-top-5-holdings.png">
</p>
<br />

## Net Promoter Score Analysis

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/b92c848baf83e38e623f4832c7e7c741cb09fb75/nps-analysis/images/nps-analysis.png">
</p>
<br />

## Waterfall Pipeline
This chart was created as part of [Power BI Workout Wednesday 2022 - Week 38.](https://www.workout-wednesday.com/pbi-2022-w38/) 

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/19eceba68aa4cb731abf1babbc438a1969702a46/waterfall-pipeline/images/waterfall-pipeline.png" />
</p>

I also created a horizontal waterfall chart.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/19eceba68aa4cb731abf1babbc438a1969702a46/waterfall-pipeline/images/waterfall-pipeline-horizontal.png" />
</p>
<br />
<br />

## Droughts in Arizona

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/7c938b09333d51d90fecf96d746468e028d76787/arizona-droughts/images/arizona-droughts.png">
</p>
<br />

## Top 5 MENA Countries by Alcohol Consumption

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/mena-alcohol-consumption/images/mena-alcohol-consumption.png">
</p>
<br />

## Sales by State - Spike Map

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/sales-spike-map/images/sales-spike-map.png">
</p>
<br />

## Sales Performance

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/sales-performance/images/sales-performance.png">
</p>
<br />

## US Soil Colors - Tile Map
This is a re-creation of [@priyamisner](https://twitter.com/priyamisner)'s interesting graphic, which shows soil colors by state. [Here's her work on Observable](https://observablehq.com/@pmisner/state-soils). 

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/us-soil-colors/images/us-soil-colors.png">
</p>
<br />

## Abortion Appointment Wait Times - Hex Map
This is a re-creation of a [Financial Times' graphic](https://twitter.com/federicacocco/status/1523950924816916480). 

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/abortion-appointment-wait-times/images/abortion-appointment-wait-times.png">
</p>
<br />

## Daily Fulfillment Rate

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/daily-fulfillment-rate/images/daily-fulfillment-rate.png">
</p>
<br />

## Adolescent Birth Rate
This was part of the #30DayChartChallenge 2022 - Day 30.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/adolescent-birth-rate/images/adolescent-birth-rate.png">
</p>
<br />

## Africa vs Asia Population
This was part of the #30DayChartChallenge 2022 - Day 30.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/africa-vs-asia-population/images/africa-vs-asia-population.png">
</p>
<br />

## France Elections 2022
This is a re-creation of a [Financial Times' graphic](https://twitter.com/FinancialTimes/status/1518369203253825538/photo/2) and was part of the #30DayChartChallenge 2022 - Day 24. 

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/france-elections-2022/images/france-elections-2022.png">
</p>
<br />

## Cutting Russian Gas
This is a re-creation of a [Financial Times' graphic](https://twitter.com/ftdata/status/1516386687143886852) and was part of the #30DayChartChallenge 2022 - Day 24. I created this with Deneb as it makes it so easy to work with pattern fills. I used the "HTML Content" custom visual for the text on the left.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/cutting-russian-gas/images/cutting-russian-gas-deneb.png">
</p>
<br />

You can also use pattern fills in Observable or you can just use a simple color and render the chart in the Vega editor. Here's an example:

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fbade48be9ee150767657e7970a7a7df046f97fb/cutting-russian-gas/images/cutting-russian-gas.png">
</p>
<br />

## UK Demographics
Day 12  of the #30DayChartChallenge 2022 was about The Economist theme. So I decided to recreate the following graphic originally created by The Economist in January 2022. I used UK's data.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/fff31ae7ba56d1e390912627a50b6e034e73fb20/uk-population-2020/images/uk-population-2020-original.png" /> 
</p>

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/78ab3aea038744ac461a7e71d9b643be3e4cb0bd/uk-population-2020/images/uk-population-2020-recreated.png" />
</p>
<br />

## Box Office vs Gaming Revenues
This time, I decided to recreate a [Financial Times' graphic](https://twitter.com/ftdata/status/1484890343086637058).

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/57987450644a3ebf0cd55130d7ad9e50f909c4c7/box-office-vs-gaming-revenues/images/box-office-vs-gaming-revenues-original.png" />   <img src="https://github.com/shadfrigui/vega-lite/blob/57987450644a3ebf0cd55130d7ad9e50f909c4c7/box-office-vs-gaming-revenues/images/box-office-vs-gaming-revenues-recreated.png" />
</p>
<br />

## Monthly Variance Analysis
The following graphic shows monthly actuals and forecasts in a lipstick column chart along with the variance in a column chart.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/monthly-variance-analysis/images/monthly-variance-analysis.png" />
</p>
<br />
<br />

## Du Bois Visualization Challenge 2022 - Challenge 7
Since I started exploring Vega-Lite, I quickly realized that recreating visuals is the best way to learn. So I decided to recreate the Du Bois Challenge [N°7](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022/challenge07).

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/du-bois-challenge-2022/images/resized-graphs/graph-7-original-resized.jpg" />   <img src="https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/du-bois-challenge-2022/images/resized-graphs/graph-7-recreated-resized.png" />
</p>
<br />

## Premier League 2021-22 Current vs Predicted End-of-Seasons-Positions
The following graphic shows current vs predicted end-of-season Premier League positions.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/premier-league-predictions/images/premier-league-predictions-online-editor.png" />
</p>

I increased the ```labelPadding``` property for the X-axis to make room for a Power BI matrix visual. Here's the final graphic:

![](https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/premier-league-predictions/images/premier-league-predictions-power-bi.png)
<br />
<br />

## Black American Population in the U.S.
I wanted to experiment more with Vega-Lite's geoshape mark and decided to create a choropleth map with a dark background. I used VS Code.

![](https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/2020-us-black-population/images/2020-us-black-population.png)

##### Note
In 2015, Shannon County, South Dakota (FIPS 46113) was renamed Oglala Lakota County (FIPS 46102). The [2020-us-black-population-data](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/2020-us-black-population/2020-us-black-population-data.csv) has this change reflected whereas the TOPOJSON file, [us-10m.json](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/2020-us-black-population/us-10m.json), has not. I replaced the FIPS code 46102 with the old one, 46113, in the population data.
<br />
<br />

## Du Bois Visualization Challenge 2022 - Challenge 3
My first Vega-Lite exploration was recreating a [W.E.B Du Bois graphic](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022/challenge03), which was part of the [Du Bois Visualization Challenge 2022](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022). I prefer working with VS Code for [geoshape](https://vega.github.io/vega-lite/docs/geoshape.html)-based Vega-Lite experimentations as it is quicker to pass in local files.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/du-bois-challenge-2022/images/resized-graphs/graph-3-original-resized.jpg" />   <img src="https://github.com/shadfrigui/vega-lite/blob/4a7c8b59f3867361f84999853f971b5b8aeb629f/du-bois-challenge-2022/images/resized-graphs/graph-3-recreated-resized.png" />
</p>
<br />
