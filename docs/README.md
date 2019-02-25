# Quick Start

In this guide, we will show you how to import chart components and add a pie chart to a canvas app.

### Create a Canvas App

Navigate to https://web.powerapps.com,  then click **Canvas app from blank**:

![Create PowerApps](images/quickstart-create-app.png)

Input a name, and select a format. Then click **Create**.

![](images/quickstart-create-app-02.png)

### Enable Components Feature

Canvas components are now available as an experimental feature. Follow the steps below to enable it.

1. Click **File**.
2. Click **App settings** > **Advanced settings**.
3. Turn on **Components** in Experimental features.

![](images/quickstart-enabled-components.png)

Click the back arrow at the top left to navigate back to PowerApps Studio.

### Import Chart Components

Click **Insert**, then click **Components** > **Import component**.

![](images/quickstart-import-components.png)

On the popup dialog, select **Chart Components V2.msapp**, then click Open.

Wait for a while, chart components will be loaded to the **Components** tab.

![](images/quickstart-components-tab.png)

### Add a Pie Chart

Click **Screens**, then click **Insert** > **Components** > **Chart**.

![](images/quickstart-insert-chart.png)

Select the newly added chart component, then configure its properties:

![](images/quickstart-chart-properties.png)

* **Size**: 360 × 360

* **Type**: Input "Pie".

* **Title**: This is a record property. Let's edit its field values in the formula bar. Update the text to "Favorite Types of Movies".

  ![](images/quickstart-chart-title.png)

* **Subtitle**: This is also a record property. Set its text to empty to hide it.

  ```javascript
  {
      text: "",
      ...
  }
  ```

* **Options**: Update its value to

  ```javascript
  Table(
      { key:"pie.innerRadius", value:"0.7" }
  )
  ```

* **Data**: Update its value to

  ```javascript
  {
      labels: ["Comedy","Action","Romance", "Drama"],
      table: Table(
          { key:"values", values: [4, 5, 6, 1] }
      )
  }
  ```

Then we will get a chart like below:

![](images/quickstart-pie.png)

### Add a Gantt Chart

Click **Screens**, then click **Insert** > **Components** > **Chart**.

![](D:/GitHub/ChartComponents/docs/images/quickstart-insert-ganttchart.png)

Select the newly added chart component, then configure its properties:

![](D:/GitHub/ChartComponents/docs/images/quickstart-ganttchart-properties.png)

- **Size**: 1150 × 640

- **Title**: This is a record property. Let's edit its field values in the formula bar. Update the text to "Favorite Types of Movies".

  ![](D:/GitHub/ChartComponents/docs/images/quickstart-chart-title.png)

- **Subtitle**: This is also a record property. Set its text to empty to hide it.

  ```javascript
  {
      text: "",
      ...
  }
  ```

- **Options**: Update its value to

  ```javascript
  Table(
      {key:"gantt.type", value:"month"},
      {key:"gantt.step", value:"3"},
      {key:"gantt.startDate", value:"01/18/2018"},
      {key:"gantt.endDate", value:"06/25/2018"},
  
      {key:"gantt.lineColor", value:"#5a5252"},
      {key:"gantt.fontColor", value:"#5a5252"},
  
      {key:"gantt.rowHeaderFontSize", value:"15"},
      {key:"gantt.columnHeaderFontSize", value:"12"},
  
      {key:"gantt.barHeight", value:"20"},
      {key:"gantt.rowHeight", value:"50"}
  )
  ```

- **Data**: Update its value to

  ```javascript
  {
      legends: ["Label1","Label2","Label3","Label4","Label5"],
      clabels: ["Process 1","Process 2","Process 3","Process 4","Process 5"],
      intervals: Table(
          {start:"01/10/2018",end:"02/01/2018",colorindex:1,process:1},        		           {start:"03/10/2018",end:"05/01/2018",colorindex:5,process:2}
      )
  }
  ```

Then we will get a chart like below:<br>![](images/quickstart-gantt.png)

