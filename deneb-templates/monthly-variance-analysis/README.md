## Monthly Variance Analysis
A multi-view layered visual showing monthly actuals and forecasts along with the variance percentage.
<br />
<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/f6f4fb5ced1a4d17b8d51b5b0c4dbb43affdd057/monthly-variance-analysis/images/monthly-variance-analysis.png" />
</p>
<br />

Here's how the template looks like when importing it to Deneb:
<br />

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/f6f4fb5ced1a4d17b8d51b5b0c4dbb43affdd057/deneb-templates/monthly-variance-analysis/images/monthly-variancee-analysis-ts.png" />
</p>
<br />

[Auto-size is not supported for composed views](https://vega.github.io/vega-lite/docs/size.html#limitations). Be aware of that if you're importing the composed graphic above. You have to resize the visual manually by changing the ```width``` and ```height``` properties. 

To overcome this limitatin, you can import the visuals separately, each as a standalone template, so you can resize them simply by dragging. You can use the [variance percentage column chart](https://github.com/shadfrigui/vega-lite/tree/main/deneb-templates/variance-percentage-column-chart) with either the [lipstick column chart](https://github.com/shadfrigui/vega-lite/tree/main/deneb-templates/actuals-vs-forecasts-lipstick-column-chart) or the ["bullet-like" chart](https://github.com/shadfrigui/vega-lite/tree/main/deneb-templates/actuals-vs-forecasts-bullet-like-chart).
<br />
<br />
