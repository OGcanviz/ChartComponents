# Radar

### Sample

![Sample Radar Chart](images/radar.png)

The following property values create the sample chart pictured above.

**Title**

```javascript
{
    text: "Test Title 1",
    ...
}
```

**Subtitle**

```javascript
{
    text: "",
    ...
}
```

**Legend**

```javascript
{
	enabled: true,
    source: "legends",
    ...
}
```

**Options**

```javascript
Table(
    { key: "radar.lineWidth", value: "1" }
)
```

**Data**

```javascript
{
    legends: ["Test 1", "Test 2", "Test 3"],
    labels: ["Label 1",  "Label 2",  "Label 3",  "Label 4",  "Label 5",  "Label 6",  "Label 7",  "Label 8"],
    table: Table(
        { key:"1.y", values: [500, 500, 500, 500, 500, 500, 500, 500] },
        { key:"2.y", values: [400, 400, 400, 400, 400, 400, 400, 400] },
        { key:"3.y", values: [300, 300, 300, 300, 300, 300, 300, 310] }
    )
}
```

Records `1.y`, `2.y` and `3.y` are the data for the first, second and third legend items.

### Options

| Key                  | Remark                                                       |
| -------------------- | ------------------------------------------------------------ |
| radar.labelsColor    | Color of labels of radar angles. The default value is `#000000`. |
| radar.lineWidth      | Line width of the radar chart. The default value is `1`.     |
| radar.plotLineColor  | Color of the plot lines. The default value is `#cccccc`.     |
| radar.plotLineWidth  | Line width of the plot lines. The default value is `0.5`.    |
| radar.backgroundOdd  | Background of the odd plot area. The default value is `#FFFFFF`. |
| radar.backgroundEven | Background of the even plot area. The default value is `#FAF4FB`. |

You can also change the style of [Y Axis](axes.md) of the chart by using the following options.

| Options of Y Axis | Default Value |
|:-|:-:|
| y.min | `0` |
| y.max | `0` |
| y.step | `0` |
| y.labels.color | `#000000` |
