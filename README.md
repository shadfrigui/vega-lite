## Intro
The Vega-Lite [ecosystem](https://vega.github.io/vega-lite/ecosystem.html) is huge, and there are many integrations, applications, and extensions of the Vega-Lite language and compiler. Here's a quick overview of *some* of the tools that you can use to write Vega-Lite specifications: 
- You can use the [online editor](https://vega.github.io/editor/#/custom/vega-lite) to replicate graphics from the [example gallery](https://vega.github.io/vega-lite/examples/) and make small changes. It's very useful for learning and experimenting without the need to install anything. Including data [inline](https://vega.github.io/vega-lite/docs/data.html#inline) in the online editor is okay for small datasets; but if your data is large, the editor would have to do a lot more work slowing everything down. Uploading data somewhere and accessing it via a [URL](https://vega.github.io/vega-lite/docs/data.html#url) is another option but can be slower for large datasets, and you will not want to make your sensitive data publicly available.
- To overcome the limitations of the online editor, you can use VS Code + the [Vega Viewer extension](https://github.com/RandomFractals/vscode-vega-viewer) to work on Vega-Lite projects locally. The Vega Viewer extension provides language support and Interactive Preview of Vega/Vega-Lite graphs and allows you to work with local files (more details [here](https://github.com/RandomFractals/vscode-vega-viewer)). Additionally, you get all VS Code features.
- If you're authoring Power BI reports, you can use the Power BI custom visual, [Deneb](https://deneb-viz.github.io/), to write Vega-Lite specs in Power BI and benefit from the power of both tools. One Deneb-only feature I like is the ability to use zoom controls to zoom in and out in the preview area. This is very useful when working with large graphs.
- If you prefer working with Python instead of the JSON-based Vega-Lite language, you can use [Altair](https://altair-viz.github.io/), which is a declarative statistical visualization library for Python. Altair provides a friendly Python API that generates Vega-Lite specifications in JSON format. Environments such as Jupyter Notebooks, JupyterLab, and Colab can then take this specification and render it directly in the web browser.


I’ll try to add 3 JSON files (if possible) for each visual: one for just copying the code in the online editor (```filename-online-editor.json```), another one to import it as a Deneb template (```filename-deneb.json```), and the last one for working with VS Code locally (```filename.vl.json```).

#### Note
~~I'm currently not configuring visualizations' themes *separately* in the [Config](https://vega.github.io/vega-lite/docs/config.html) object. I'll revisit the code to do that.~~
I updated all the files to separate theme customizations in the Config object. I added copies of Deneb templates to a separate directory for quick access.

<br />
<br />
<br />

## W.E.B Du Bois Challenge 2022 - Graph 3
My first Vega-Lite exploration was recreating a W.E.B Du Bois [graphic](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022/challenge03), which is part of the [Du Bois Visualization Challenge: 2022](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022). I used VS Code as I can't add TOPOJSON files to the Power BI custom visual, Deneb. There are workarounds, but I prefer working with VS Code for [geoshape](https://vega.github.io/vega-lite/docs/geoshape.html)-based, Vega-Lite experimentations as it is quicker to pass in local files.
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/du-bois-challenge-2022/resized-graphs/graph-3-original-resized.jpg" />   <img src="https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/du-bois-challenge-2022/resized-graphs/graph-3-recreated-resized.png" />
</p>
<br />
<br />
<br />

## Black American Population in the U.S.
I wanted to experiment more with Vega-Lite's geoshape mark and decided to do a choropleth map with a dark background. Choropleth maps are great for showing the big picture and helping readers recognize patterns in the data. You can easily see that the highest concentration of Black Americans (alone) population is in the South. I added tooltips to help readers access exact values for each county. I used VS Code.
<br />
<br />
![](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/2020-us-black-population/2020-us-black-population.png)
<br />
##### Note
In 2015, Shannon County, South Dakota (FIPS 46113) was renamed Oglala Lakota County (FIPS 46102). The [2020-us-black-population-data](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/2020-us-black-population/2020-us-black-population-data.csv) has this change reflected whereas the TOPOJSON file, [us-10m.json](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/2020-us-black-population/us-10m.json), has not. I replaced the FIPS code 46102 with the old one, 46113, in the population data.
<br />
<br />
<br />

## Premier League 2021-22 Current vs Predicted End-of-Seasons-Positions
I used Deneb + Power BI. Here's the graphic that you get if you paste the [code](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/premier-league-predictions/premier-league-predictions-online-editor.json) in the [online editor](https://vega.github.io/editor/#/custom/vega-lite):
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/premier-league-predictions/premier-league-predictions-online-editor.png" />
</p>
<br />
<br />

I increased the ```labelPadding``` property for the ```x``` axis to make room for a Power BI matrix visual. Here's the final graphic:

<br />
<br />

![](https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/premier-league-predictions/premier-league-predictions-power-bi.png)
<br />
<br />
<br />

## W.E.B Du Bois Challenge 2022 - Graph 7
Since I started exploring Vega-Lite, I quickly realized that recreating visuals is the best way to learn. So I decided to recreate W.E.B Du Bois Challenge's [N°7](https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022/challenge07).
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/du-bois-challenge-2022/resized-graphs/graph-7-original-resized.jpg" />   <img src="https://github.com/shadfrigui/vega-lite/blob/b7cb5cd2d4ccffe43612b2485d80965b7d231f31/du-bois-challenge-2022/resized-graphs/graph-7-recreated-resized.png" />
</p>
<br />
<br />
<br />

## Monthly Variance Analysis
The following graphic shows monthly actuals and forecasts in a lipstick column chart along with the variance in a column chart. The code is optimized to show millions/billions in the Y-axis as well as in the tooltip. Cross-filtering is also enabled.
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/0f799574ec0d86ac9a16887fea5685e25caa1ee4/monthly-variance-analysis/monthly-variance-analysis.png" />
</p>
<br />
<br />

I added different versions of the code to work in the online editor, VS Code, or in Power BI. [Auto-size is not supported for composed views](https://vega.github.io/vega-lite/docs/size.html#limitations). Be aware of that if you're importing the composed graphic above (```monthly-variance-analysis-deneb.json``` Deneb template). You have to resize the visual manually by changing the ```width``` and ```height``` properties in the Config tab. 

If you just want a visual that auto-resize without looking at the code, I got you covered. I created separate templates for the following graphics with autosize enabled:

- Actuals vs Forecasts Lipstick Column Chart
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/0f799574ec0d86ac9a16887fea5685e25caa1ee4/monthly-variance-analysis/actuals-vs-forecasts-lipstick-column-chart.png" />
</p>
<br />
<br />

- Actuals vs Forecasts Bullet-like Chart
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/0f799574ec0d86ac9a16887fea5685e25caa1ee4/monthly-variance-analysis/actuals-vs-forecasts-bullet-like-chart.png" />
</p>
<br />
<br />

- Variance Column Chart
<br />
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/0f799574ec0d86ac9a16887fea5685e25caa1ee4/monthly-variance-analysis/variance-column-chart.png" />
</p>
<br />
<br />

#### Note
If your data is spanning multiple years, add a **single select** Year slicer to show the correct results for each year.
