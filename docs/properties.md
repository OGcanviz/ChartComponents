# Chart Properties

In the [Quick Start](/), you learned how to update some of the chart component properties and how to create and customize a Pie chart.

In this guide, you will learn more details about the properties you can use to configure the charts.

### Type

The Type property determines the kind of chart to display. We have implemented the following types of charts so far.  Would you like to add another to the library?  That would be awesome!  Please send us a Pull Request!

* Pie
* Solid Gauge
* Funnel
* Line
* Bar
* Radar
* Scatter
* Candle

> **Note**: The Gantt chart uses different data payload schema and we created a separate component for it.  [Learn more and create a](gantt.md) Gannt chart.  

### Colors

The property accepts a series of colors:

```javascript
["#31825d", "#30a667", "#5ec16c", "#f6c790", "#f7c772", "#f7b45b", "#f68f64", "#d46068", "#946eb0", "#769acc", "#60c5ea"]
```

They are used by the various labels and legends. 

[All CSS color values](https://www.w3schools.com/colors/default.asp) are allowed. For examples: `Blue`, `#808080`. 

> **Note**: This also applies to other color fields, such as title color, line color, etc.

### Title

This record property controls the title text and style. It accepts the following fields:

| Name             | Remark                                                       |
| ---------------- | ------------------------------------------------------------ |
| text             | Text of the title.<br />You may set it to empty to hide the title. |
| height           | Height of the title.                                         |
| align            | Alignment of the title.<br />Available values: left, center and right. |
| paddingTop       | Padding top of the title.                                     |
| fontSize         | Font size of the title.                                      |
| fontFamily       | Font family of the title.                                    |
| fontWeight       | Font weight of the title.<br />Available values: normal and bold. |
| fontStyle        | Font style of the title.<br />Available values: normal and italic. |
| color            | Color of the title.                                          |
| additionalStyles |                                                              |

> **Note**: the available values for align, font weight and font style also apply to the same types of fields in other properties.

### Subtitle

This record property controls the text and styles of the subtitle. It has the same fields as the title property.

### Legend

This record property controls the styles of the legend. 

| Name       | Remark                                                       |
| ---------- | ------------------------------------------------------------ |
| enable     | Show or hide the legend. Available values: true and false.   |
| source     | Data source of the legend. Available values:<br />labels: get items from the Data property's labels field<br />legends: get items from the Data property's legends field |
| placement  | Position of the legend. Available values: top, right, left and bottom. |
| width      | Width of the legend. Effective when placement is set to left or right. |
| height     | Height of the legend. Effective when placement is set to top or bottom. |
| itemGap    | Gap between legend items.                                    |
| fontSize   | Font size of the legend.                                     |
| fontFamily | Font family of the legend.                                   |
| fontWeight | Font weight of the legend.                                   |
| fontStyle  | Font style of the legend.                                    |
| color      | Color of the legend.                                         |
| align      | Align of the legend.                                         |

### Options

This property allows you to control even more details of the chart:

* X and Y Axes:

  ```javascript
  Table(
      { key:"x.labels.color", value:"#336699" }
      { key:"y.labels.fontWeight", value:"bold" }
  )
  ```

  For more details, please check [Axes](axes.md).

* Chart special settings:

  ```javascript
  Table(
      { key:"pie.radius", value:"0.95" },
      { key:"pie.innerRadius", value:"0.75" }
  )
  ```

  For more details, please check the documentation for each chart type.

### Data

Legends, labels and values are set via this property. Below is sample data for radar chart.  The data, just like all the properties, may be passed in dynamically at run time.

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

  For more details, please check the documentation for each chart type.

> **Known Issue**: 
> By default, the Canviz Power Apps Chart Components support a maximum of 100 points. If you wish to modify the code to support more points, for example 400, then add the following record to a charts Options property:
>
> ```javascript
> { key: "indexes", value: "1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20" }
> ```
>
> The value contains 20 continuous numbers starting at 1, and separated by commas. 20 × 20 = 400
