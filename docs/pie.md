# Pie

Here are options to pie chart.

```javascript
{
    type:"pie",
    data:Table(
        {key:"", values:[]},
        {key:"labels", values:["Label 1","Label 2","Label 3","Label 4","Label 5"]},
        {key:"values", values:["100","200","300","400","500"]}
    ),
    options:Table(
        {key:"",value:""},
        {key:"title", value:"Test Title 1"},
        {key:"legend", value:"true"},
        {key:"legend.source", value:"labels"},
        {key:"pie.innerRadius", value:"0.5"}
    )
}
```
![Sample Pie Chart](images/pie.png)

## pie.radius

The outer radius of the pie chart. The value is the ratio of the max available radius. Can be `0 ~ 1`. For example, `0.5` means 50% of the chart area.

> The default value is `1`.

## pie.startAngle

The start angle of the pie chart.

## pie.innerRadius

The inner radius of the pie chart. The value is the ratio of the radius. For example, `0.5` means 50% of the radius.

## pie.semoCircle

Show pie chart in semi circle. Can be **true** or **false**.

## pie.roseType

Display pie chart in rose mode. Can be **none**, **radius** and **area**.

> The default value is `none`.

* The `radius` mode looks like this:

![Rose Type Radius](images/pie-radius.png)

* The `area` mode looks like this:

![Rose Type Area](images/pie-area.png)