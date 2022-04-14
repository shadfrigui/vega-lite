## UK Population Pyramid
A population pyramid for the UK in 2020 along with 2030 projections. This graphic was originally created by The Economist Data Team in January 2022, and I recreated it as part of the [#30DayChartChallenge](https://30daychartchallenge.org/about/) 2022 edition. I used UK data.

<p align="center">
  <img src="https://github.com/shadfrigui/vega-lite/blob/dbcee34118a220f93ef455cb21d8d88b8e5f3676/uk-population-2020/community-example/images/uk-population-pyramid.png" />
</p>
<br />

```json
{
  "$schema": "https://vega.github.io/schema/vega-lite/v5.json",
  "data": {
    "url": "https://raw.githubusercontent.com/shadfrigui/vega-lite/main/uk-population-2020/uk-population-2020-data.json"
  },
  "vconcat": [
    {
      "layer": [
        {
          "mark": {
            "type": "rect",
            "width": 470,
            "height": 2,
            "xOffset": 201,
            "yOffset": 10,
            "color": "#EB111A"
          }
        },
        {
          "mark": {
            "type": "rect",
            "width": 35,
            "height": 10,
            "xOffset": -16,
            "yOffset": 15,
            "color": "#EB111A"
          }
        },
        {
          "title": {
            "text": "Boomer bust",
            "font": "Segoe UI",
            "fontSize": 25,
            "subtitle": "UK, demographics",
            "dy": 85
          },
          "mark": "text"
        },
        {
          "mark": {
            "type": "rect",
            "width": 25,
            "height": 1,
            "xOffset": -21,
            "yOffset": 120,
            "color": "black"
          }
        }
      ]
    },
    {
      "height": 50,
      "title": {
        "text": "Population age structure, '000",
        "fontSize": 19,
        "dx": -14,
        "dy": 27
      },
      "mark": "text"
    },
    {
      "concat": [
        {
          "width": 200,
          "height": 450,
          "transform": [{"filter": {"field": "Gender", "equal": "Male"}}],
          "layer": [
            {
              "mark": {"type": "bar", "color": "#31C0D0"},
              "encoding": {
                "x": {
                  "field": "Population 2020",
                  "type": "quantitative",
                  "sort": "descending"
                },
                "y": {
                  "field": "Age",
                  "type": "ordinal",
                  "sort": {"field": "Age ID", "order": "descending"},
                  "scale": {"paddingInner": 0.35},
                  "axis": {"orient": "right"}
                }
              }
            },
            {
              "mark": {"type": "line", "color": "#006CA2"},
              "encoding": {
                "x": {
                  "field": "Projection 2030",
                  "type": "quantitative",
                  "sort": "descending"
                },
                "y": {
                  "field": "Age",
                  "type": "ordinal",
                  "sort": {"field": "Age ID", "order": "descending"},
                  "axis": null
                }
              }
            },
            {
              "mark": {
                "type": "rect",
                "width": 85,
                "height": 25,
                "color": "#31C0D0"
              },
              "encoding": {"x": {"value": 120}, "y": {"value": 253}}
            },
            {
              "data": {"values": [{}]},
              "mark": {"type": "text", "text": "2020 male", "color": "white"},
              "encoding": {"x": {"value": 120}, "y": {"value": 253}}
            },
            {
              "mark": {
                "type": "rect",
                "width": 95,
                "height": 45,
                "color": "white"
              },
              "encoding": {"x": {"value": 60}, "y": {"value": 55}}
            },
            {
              "data": {"values": [{}]},
              "mark": {
                "type": "text",
                "text": ["2030 male", "projection"],
                "color": "#006CA2"
              },
              "encoding": {"x": {"value": 60}, "y": {"value": 45}}
            }
          ],
          "resolve": {"scale": {"y": "independent"}}
        },
        {
          "width": 200,
          "height": 450,
          "title": "",
          "transform": [{"filter": {"field": "Gender", "equal": "Female"}}],
          "layer": [
            {
              "mark": {"type": "bar", "color": "#77CCC4"},
              "encoding": {
                "x": {"field": "Population 2020", "type": "quantitative"},
                "y": {
                  "field": "Age",
                  "type": "ordinal",
                  "sort": {"field": "Age ID", "order": "descending"},
                  "scale": {"paddingInner": 0.35},
                  "axis": {"labels": false}
                }
              }
            },
            {
              "mark": {"type": "line", "color": "#00949A"},
              "encoding": {
                "x": {"field": "Projection 2030", "type": "quantitative"},
                "y": {
                  "field": "Age",
                  "type": "ordinal",
                  "sort": {"field": "Age ID", "order": "descending"},
                  "axis": null
                }
              }
            },
            {
              "mark": {
                "type": "rect",
                "width": 100,
                "height": 25,
                "color": "#77CCC4"
              },
              "encoding": {"x": {"value": 80}, "y": {"value": 253}}
            },
            {
              "data": {"values": [{}]},
              "mark": {"type": "text", "text": "2020 female", "color": "white"},
              "encoding": {"x": {"value": 80}, "y": {"value": 253}}
            },
            {
              "mark": {
                "type": "rect",
                "width": 95,
                "height": 45,
                "color": "white"
              },
              "encoding": {"x": {"value": 140}, "y": {"value": 55}}
            },
            {
              "data": {"values": [{}]},
              "mark": {
                "type": "text",
                "text": ["2030 female", "projection"],
                "color": "#00949A"
              },
              "encoding": {"x": {"value": 140}, "y": {"value": 45}}
            }
          ],
          "resolve": {"scale": {"y": "independent"}}
        }
      ]
    },
    {
      "title": {
        "text": "Source: Office for National Statistics",
        "fontSize": 13,
        "fontWeight": "lighter",
        "lineHeight": 20,
        "dy": 50
      },
      "mark": "text"
    }
  ],
  "config": {
    "padding": {"top": 10, "bottom": 10, "left": 20, "right": 20},
    "view": {"stroke": null},
    "font": "Segoe UI Light",
    "axis": {
      "domainColor": "#595959",
      "labelFont": "Segoe UI",
      "labelFontSize": 18,
      "labelColor": "#333333",
      "title": null
    },
    "axisXQuantitative": {
      "orient": "top",
      "domain": false,
      "gridColor": {"expr": "(datum.value % 100000) == 0 ? '#D5DDE0' : ''"},
      "tickCount": 4,
      "ticks": false,
      "labelPadding": 5,
      "labelFlush": false,
      "labelExpr": "datum.value == 0 ? datum.value : truncate(datum.value, 3  ,'right', '')"
    },
    "axisYDiscrete": {
      "tickSize": 4,
      "tickColor": {"expr": "(datum.value % 10) == 0 ? '#595959' : ''"},
      "labelPadding": {
        "expr": "datum.value == 100 ? 2 : datum.value == 0 ? 12 : 7"
      },
      "labelOffset": -2,
      "labelFontSize": {"expr": "datum.value == '105+' ? 5 : 18"},
      "labelColor": {"expr": "(datum.value % 10) == 0 ? '#333333' : ''"},
      "zindex": 1
    },
    "line": {"interpolate": "step-before", "strokeWidth": 3},
    "text": {"fontSize": 19, "fontWeight": "bolder"},
    "title": {
      "anchor": "start",
      "subtitlePadding": 10,
      "subtitleFontSize": 19,
      "subtitleFontWeight": "bolder"
    },
    "concat": {"spacing": -5}
  }
}
```