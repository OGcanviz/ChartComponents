# Solid Gauge

Here are options to solid gauge chart.

```javascript
{
    type:"solidGauge",
    data:Table(
        {key:"", values:[""]},
        {key:"labels", values:["Label 1","Label 2","Label 3","Label 4"]},
        {key:"values", values:["50", "60", "70", "80"]}
    ),
    options:Table(
        {key:"",value:""},
        {key:"title", value:"Test Title 1"}
    )
}
```
![Sample Solid Gauge Chart](images/solidGauge.png)

You can also change the style of [X Axis](axes.md?id=x-axis) and [Y Axis](axes.md?id=y-axis) of the chart by following options.

| Options of Axes | Default Value |
|:-|:-:|
| x.labels.fontSize | `12` |
| x.labels.fontFamily |  |
| x.labels.fontWeight | `bold` |
| x.labels.fontStyle | `normal` |
| x.labels.color |  |
| x.labels.additionalStyles |  |
| y.labels | `true` |
| y.labels.fontSize | `12` |
| y.labels.fontFamily |  |
| y.labels.fontWeight | `bold` |
| y.labels.fontStyle | `normal` |
| y.labels.color | `#333333` |
| y.labels.additionalStyles |  |

## solidGauge.itemGap

Gap between 2 items

> The default value is `5`.

## solidGauge.minRadius

Min radius of the solid gauge chart

> The default value is `0.3`.