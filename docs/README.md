# Quick Start

In this guide, you will learn how to quickly use the Canviz Power Apps Chart Components in a Power App.  You will create a Canvas Power App, import the Canviz Power Apps Chart Components, and add a pie chart to the Canvas Power App.  You will also learn how to change the Pie chart to a different chart type.

> **Note:** The estimated time to complete these steps is 5-15 minutes.

When you are done your charts will look like this.

![](images/quickstart-pie.png)

![](images/quickstart-change-type.png)

### Create a Canvas Power App

Navigate to https://web.powerapps.com, then click **Canvas app from blank**:

![Create PowerApps](images/quickstart-create-app.png)

Enter an **App name**, select a **Format**, and click **Create**.

![](images/quickstart-create-app-02.png)

### Enable Components Feature

The Components feature should be enabled by default.  Double check it is enabled.

1. Click **File**.
2. Click **Settings** > **Advanced settings**.
3. Ensure the **Components** feature is turned on.

![](images/quickstart-enabled-components.png)

Click the back arrow at the top left to navigate back to Power Apps Studio.

### Import Chart Components

Download the **[Chart Components V2.msapp](https://github.com/OGcanviz/ChartComponents/blob/master/Chart%20Components%20V2.msapp)** file.  The **Chart Components V2.msapp** file contains the Canviz Power Apps Chart Components.  Remember where you save the **Chart Components V2.msapp** file.

Click **Insert**, then click **Components** > **Import component**.

![](images/quickstart-import-components.png)

Click **Upload file**, and select the **Chart Components V2.msapp** file you downloaded, then click **Open**.

Wait for a little bit and the Canviz Power Apps Chart Components will appear in the **Components** tab.

![](images/quickstart-components-tab.png)

### Add a Pie Chart

Click the **Screens** tab, then select **Screen1**.

![](images/quickstart-select-screen.png)

In the tree view, click **Insert**.

Expand the **Custom** section, then click **Chart**.

![](images/quickstart-insert-chart.png)

### Configure Chart Appearance

Select the newly added chart component, then configure the chart properties to adjust how it looks.

To make a Pie chart, enter Pie in the Type property.  Pie is the default Type property.
* **Type**: Pie

  ![](images/quickstart-chart-properties.png)
  
To change the size of the chart, click the Advanced tab and change the Height and Width properties.
* **Size**: 360 × 360

  ![](images/quickstart-size-properties.png)

* **Title**: To change the Title, edit the Title property.  The Title property is a record property.  Edit the value in the formula bar.  Update the value for the text field in the Title property to "Favorite Types of Movies".

  ![](images/quickstart-chart-title.png)

* **Subtitle**: The Subtitle is also a record property. Set its text field to empty to hide it.

  ```javascript
  {
      text: "",
      ...
  }
  ```
* **Options**: Options allow you to configure the look and feel of the chart to a large degree.  For example, to change the size of the inner radius for the pie chart, simply set the pie.InnerRadius property.  Update the Options property with the following code.  For more details about the various options properties, please see the dcoumentation page for each chart.

  ```javascript
  Table(
      { key:"pie.innerRadius", value:"0.7" }
  )
  ```

### Define Chart Data

* **Data**: Just like the name says, this property contains the data the chart renders.  Update the Data property with the following code.  Keep in mind, this property can be set at runtime so you can make these charts dynamic.

  ```javascript
  {
      labels: ["Comedy","Action","Romance", "Drama"],
      table: Table(
          { key:"values", values: [4, 5, 6, 1] }
      )
  }
  ```

> **Note:** To learn how to integrate dynamic data sources with your charts see [this article](data-integration.md).

To create a Gantt chart follow the [Gantt chart instructions](gantt.md).

Now take a look at your chart!

![](images/quickstart-pie.png)

## Other Chart Types

To implement other chart types simply change the **Type** property for the Chart component.  

The following Types are currently available.

- Pie
- Solid Gauge (SolidGauge)
- Funnel
- Line
- Bar
- Radar
- Scatter
- Candle Stick (Candle)

For example, to change the chart to a Solid Gauge chart, select the Chart component, then change the **Type** property to **Solid Gauge**.

![](images/quickstart-change-type.png)

> **Note:** The Gantt chart uses a seperate component.  To create a Gantt chart follow the [Gantt chart instructions](gantt.md).
