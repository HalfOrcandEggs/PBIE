Visualising Data in Power BI
============================

Exercise 1: Creating Power BI Reports 
--------------------------------------

>   Estimated Time to complete: 45 min

#### Scenario 

>   In this exercise you will create various visualisations in the report view
>   of the Power BI Desktop. These visuals then form the basis of a Power BI
>   Dashboard.

>   The main tasks for this exercise are as follows:

-   Create a multipage report

-   Explore Power BI Visualisations

####  Task 1: Create a multipage Power BI report 

1.  Open **C:\\Labfiles\\Lab4\\Starter\\AdventureWorks Sales.pibx**

2.  From Report view click the **Employees** field in the **Sales** table

3.  Expand the fields in the **Order Date** table

4.  Expand the **Calendar Hierarchy**

5.  Select **Quarter** from the list of fields, (uncheck Year).

6.  Resize the chart until all the quarters appear on the axis as shown

![](media/da4e812cb3e5686a16b2b2a0eb61346d.png)

1.  While the chart is selected press **Ctrl+C** to copy, then press **Ctrl+V**
    to paste.

2.  Drag the new chart below the **Employees by Quarter** chart.

3.  With the new chart selected, clear the checkmark from the **Employees**
    field and replace it with **Customers**. The visualisation will change
    automatically.

![](media/6c016055e8e78ef7098f7f93f1cc929a.png)

1.  Copy and Paste the Employees by Quarter chart once more, this time place it
    to the right.

2.  Deselect **Employees** and select **Resellers**

3.  Select the **Units sold** measure to create a new visualisation.

4.  Expand the Calendar hierarchy and select the **Quarter** field.

5.  Clear the checkbox for **Year**.

6.  Switch to a line chart and examine the new visualisation.

7.  Select the various sorting options by using the menu on the top right of the
    visualisation. Use the Sort by Quarter option and resize the chart to appear
    as follows:

![](media/fdc2077303f08bd4d1e692b898f480c3.png)

1.  Move the Chart to the bottom right of the report page.

2.  Create a new line chart visualisation to compare the **Revenue** and
    **Cost** Measures.

![](media/222c2298e64df56dba21cdfe9a1f76a6.png)

1.  Resize the new chart to the same size as the **Units Sold by Quarter** chart
    and place it above this on the bottom right.

2.  Your report should look like the following

![](media/204da417301d2f24352324ee408a1a74.png)

1.  Rename the report to **Sales Volumes**

2.  Save your work

####  Task 2: Add a Card visualization 

1.  Add a **new** report page.

2.  Click the **Card** visualisation.

![](media/3fcbde63ccdeef49ab5219628bdb46c5.png)

1.  With the card selected, check the **Profit** measure from the Sales table.
    The card visualisation will change to the following:

![](media/5cace4b661a80c6b2b5cb6b3d0bf9d33.png)

1.  Resize the card and place it in the top left corner of the report page.

####  Task 3: Add a Slicer 

1.  Expand the list of fields in the **Order Date** table, then Expand the
    **Calendar hierarchy**

2.  Ensure no visuals are selected on the report page (we wish to create a new
    one, not add to an existing one).

3.  Select the **Year** field from the **Calendar hierarchy**

4.  Choose the Filter visualisation from the list as shown:

![](media/8f531da61ab1a80791f194eac5538a4d.png)

1.  Resize the slicer to fit underneath the Profit Card.

2.  Change to different years and examine the results.

3.  No data exists for 2010, so this we will filter this out.

4.  Click the report design surface to ensure no visualisation is selected.

5.  In the filters section of the report, drag the Year field from the **Order
    Date** table to the **Page level filters** section. As shown (if necessary
    switch to basic filtering by choosing it from the dropdown list):

![](media/bd0074f96b470aa719d196a4b6acb003.png)

1.  Place a checkmark in **Select All**, then clear the checkbox for 2010. Note
    the change in the Slicer.

2.  Save your work.

####  Task 4: Create a tabular Report 

1.  Insert a table visualisation:

![](media/37f86da382c0028057f534914d1086d8.png)

1.  Add the following fields: **Category, SubCategory, Revenue, Profit, Units
    Sold and Profit Margin**

2.  Resize the table so the data is displayed across all the columns.

3.  Place the table to the right of the Card and Slicer as shown:

![](media/66483c6f16a79ae2a6b34b8078a8b6c3.png)

1.  Create an additional slicer for the **Category** and explore the effect of
    changing different category values.

2.  Create a Column chart to compare the Revenue and Profit by Subcategory.
    Place this chart on the bottom left of the report page:

![](media/3d328acc6803a3815c190db012966919.png)

1.  Copy and paste the **Revenue and Profit by subcategory** chart. Move the
    copy to the bottom right of the report page.

2.  Remove **Revenue** and **Profit** from the value section of the field list
    and replace with **Profit Margin**

####  Task 5: Create a line chart 

1.  Click in the blank space of the report page.

2.  Select the **Units Sold** measure then select the **SubCategory** field from
    the **Product** table.

3.  Change to a line chart and resize to fit the space in the top right side of
    the report page.

4.  Rename the report to **Sales by Category**.

5.  Your report should appear like the following:

![](media/094db435092953b4d1a4c4c5cf5aef35.png)

1.  Experiment with the various slicers and filters and examine the
    cross-filtering behaviour of the all the visualisations on the page

End of Exercise

>   **Results**: After this exercise, you will have created several reports on
>   multiple pages using the Power BI Desktop Designer.

Exercise 2: Creating Interactive Visualisations 
------------------------------------------------

#### Scenario 

>   In this exercise you will create an animated visualisation in the Power BI
>   Desktop. This can be used to examine data over time.

>   The main tasks for this exercise are as follows:

-   Create a scatter chart

-   Explore the Power BI filtering features

####  Task 1: Create a scatter chart 

1.  Add a new report page and call it **Sales Over Time**

2.  Add a scatter chart visualisation and resize it to fill the report designer
    (alternatively you can use focus mode to maximise the viewing area).

3.  Add the fields as shown below:

![](media/547d1e9f15678c39b22b20b5ca972975.png)

1.  Add a visual level filter to display just the data for the **Clothing**
    category. (Alternatively, you can create a slicer to make the filtering by
    Category more flexible).

2.  Press the play button on the left to watch the data points move over time.

![](media/d1f4850cfb7644fc650e743ba0e21291.png)

1.  Select the data point representing **Jerseys** to highlight the changes over
    time.

2.  Explore the data with different filters and measures.

3.  Save and close the Power BI Desktop.

End of Exercise

>   **Results**: After this exercise, you will have created a scatter chart to
>   examine the changes in data over time.
