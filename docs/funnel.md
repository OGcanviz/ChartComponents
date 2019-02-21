# Solid Gauge

![Sample Solid Gauge Chart](images/funnel.png)

### Data

```javascript
{
    legends: ["Test 1", "Test 1"],
    labels: ["Label 1","Label 2","Label 3","Label 4","Label 5"],
    table: Table(
        {key:"values", values:[90, 20, 40, 80, 50]}
    )
}
```

### Options

| Key                            | Remark                                                       |
| ------------------------------ | ------------------------------------------------------------ |
| funnel.mode                    | The funnel chart has 3 modes, **ladder**<br />, **rectangle** and **pyramid**. The default value is `ladder`.<br />`ladder`<br />![Funnel Chart in Ladder Mode](C:/Users/admin/Documents/GitHub/ChartComponents/docs/images/funnel-ladder.png)<br />`rectangle`:<br />![Funnel Chart in Rectangle Mode](C:/Users/admin/Documents/GitHub/ChartComponents/docs/images/funnel-rectangle.png)<br />`pyramid`:<br />![Funnel Chart in Pyramid Mode](C:/Users/admin/Documents/GitHub/ChartComponents/docs/images/funnel-pyramid.png)<br />In pyramid mode, the area(**not height**) of parts are calculated from input values. |
| funnel.sort                    | You can sort input values. The direction can be **none**, **ascending** and **descending**. The default value is `none`.<br />For example, sort in descending direction looks like this:<br />![Funnel Chart in Descending Mode](C:/Users/admin/Documents/GitHub/ChartComponents/docs/images/funnel-descending.png) |
| funnel.orientation             | You can display the chart in different orientations. Can be **vertical** and **horizontal**. The default value is `vertical`.<br /> For example, horizontal mode looks like this:<br />![Funnel Chart in Horizontal Mode](images/funnel-horizontal.png) |
| funnel.align                   | You can also align all bars aside. In horizontal mode, can be **top**, **middle** and **bottom**. In vertical mode, can be **left**, **center** and **right**. The default value is `center`.<br />  For example, align to left looks like this:<br />![Funnel Chart in Left Mode](C:/Users/admin/Documents/GitHub/ChartComponents/docs/images/funnel-left.png) |
| funnel.maxBarLength            | You can change the max bar length of the chart. Can be **0~1**. The default value is `1`. |
| funnel.itemGap                 | You can change gap between two bars. The default value is `10`. |
| funnel.connectorColor          | You can change the color of the gap. The default value is data color. |
| funnel.connectorOpacity        | You can also change the opacity of the gap fill. The default value is `0.3`. |


| Key                            | Key                                  | Key                                       | Remark                                                       |
| ------------------------------ | ------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| funnel.labels                  | funnel.labels.value.                 | funnel.labels.percentage.                 | Should display labels or not. Can be **true** or **false**. The default value is `false`.<br />![Funnel Labels](images/funnel-labels.png) |
|                                | funnel.labels.value.dx               | funnel.labels.percentage.dx               | X Offset of labels                                           |
|                                | funnel.labels.value.dy               | funnel.labels.percentage.dy               | X Offset of labels                                           |
|                                |                                      | funnel.labels.percentage.mode             | How to calculate the percentage value. Available values:<br />`sum`: value / sum of all values<br />`max`: value / max value<br />`last`: value / value of last data |
| funnel.labels.align            | funnel.labels.value.align            | funnel.labels.percentage.align            | Alignment of the labels. Can be **left**, **center** and **right**. The default value is `center`. |
| funnel.labels.verticalAlign    | funnel.labels.value.verticalAlign    | funnel.labels.percentage.verticalAlign    | Vertical Alignment of the labels. Can be **top**, **middle** and **bottom**. The default value is `middle`. |
| funnel.labels.fontSize         | funnel.labels.value.fontSize         | funnel.labels.percentage.fontSize         | Font size of labels. The default value is `20                |
| funnel.labels.fontFamily       | funnel.labels.value.fontFamily       | funnel.labels.percentage.fontFamily       | Font family of labels                                        |
| funnel.labels.fontWeight       | funnel.labels.value.fontWeight       | funnel.labels.percentage.fontWeight       | Font weight of labels, can be CSS font weight values.        |
| funnel.labels.fontStyle        | funnel.labels.value.fontStyle        | funnel.labels.percentage.fontStyle        | Font style of labels, can be CSS font style values.          |
| funnel.labels.color            | funnel.labels.value.color            | funnel.labels.percentage.color            | Color of labels. The default value is `#ffffff`.             |
| funnel.labels.additionalStyles | funnel.labels.value.additionalStyles | funnel.labels.percentage.additionalStyles | You can add other CSS style rules here.                      |
