Modelling Data
==============

Exercise 1: Creating a Data Model 
----------------------------------

>   Estimated Time to complete: 60 min

#### Scenario 

>   In this lab exercise you will use Power BI Desktop to create a data model
>   from an Azure SQL data warehouse.

>   The main tasks for this exercise are as follows:

-   Import data to create a data model

-   Append new data

-   Create columns

-   Create a hierarchy

-   Hide tables and fields to reduce complexity

####  Task 1: Import data into a Power BI Desktop Model 

>   A data warehouse is often provided as a single point of truth for business
>   data. Usually meaning that the data has been checked for quality and
>   accuracy. The process to access this data is the same, whether the server is
>   in the cloud or on premise, essentially the only difference is in the name
>   of the server. However, there can be very large volumes of data in a data
>   warehouse and you must be careful to select only the required data for your
>   analysis, particularly if bandwidth is limited.

>   Use the information in the table below to connect to your server.

|                |                                    |
|----------------|------------------------------------|
| Server Name    | sqlazuredw001.database.windows.net |
| Database Name  | AdventureWorksDW                   |
| Authentication | Database                           |
| User name      | Student                            |
| Password       | Pa55w.rd                           |

1.  Start a new instance of the **Power BI Desktop**.

2.  Close the splash screen if necessary

3.  Select **Get Data** then choose **SQL Server**.

>   *If you are connecting to an Azure SQL database, you are required to enter
>   the name of the database. Once you click connect you will be presented with
>   an authentication dialog. For an on‑premise server, the default is usually
>   Windows Authentication, in this case we must choose the Database option*

1.  Choose **Database** on the left of the dialog as shown and enter the
    credentials given above:

    ![](media/988cd5ff1d1b35a79254070999d6951a.png)

2.  Click **Connect**

3.  Once the Navigator is displayed, scroll the list of tables to see what data
    is available.

4.  Click a table name to preview the data.

5.  Scroll to find the table named **FactInternetSales**, examine the column
    names and data. *(Do not select the check box for this table)*

6.  Scroll to find the table name **FactResellerSales**, examine the columns
    names and data. *(Do not select the check box for this table)*

>   The data you see here is has been processed within the data warehouse to
>   provide for two different types of sales. Our analysis is concerned with the
>   total sales from both channels, Internet and Reseller. We will use a custom
>   view stored in the database to access these tables.

1.  Scroll to the top of the list and select **vTotalSales** as shown:

    ![](media/23d81f50c528e4ed0eb63f861bd0c759.png)

2.  Click the **Load** button to load the data into Power BI desktop.

3.  In report view notice the field names to right.

4.  Rename the table (query) to **Sales** by right clicking the name
    **vTotalSales** and choosing **Rename**. *(This saves having to re-open the
    Query editor to do a trivial change).*

####  Task 2: Add Product Information

1.  Click the down arrow under recent sources in the external data section of
    the Home ribbon of the Power BI Desktop.

2.  Select the most recent source (your database connection,
    **sqlazuredw001.database.windows.net**).

3.  From the Navigator, select the three product tables as shown:

![](media/1e8759398621e99389add91472f80d82.png)

1.  Choose **Edit** to open the query editor

2.  When you are prompted with the Connection settings dialog, click **OK** to
    continue *(ensuring that the Import option is selected)*.

![](media/90e1fc8c1131c315149704fae3f6986e.png)

1.  Use the **Choose columns** button in the Query Editor to remove columns from
    the tables until only the following remain:

| **DimProduct**            | ProductKey                    |
|---------------------------|-------------------------------|
|                           | ProductSubCategoryKey         |
|                           | English ProductName           |
|                           | Color                         |
|                           | EnglishDescription            |
| **DimProductSubcategory** | ProductSubCategoryKey         |
|                           | EnglishProductSubCategoryName |
|                           | ProdcutCategoryKey            |
| **DimProductCategory**    | ProductCategoryKey            |
|                           | EnglishProductCategoryName    |

>   *Your table columns should appear as follows in the query editor:*

>   *DimProduct*

![](media/6c540d9fb4d358934af7455e3d0fb1b1.png)

>   *DimProductSubCategory*

![](media/374739b3ead109b6e1439582c5cd4db4.png)

>   *DimProductCategory*

![](media/55df0f0f95c0dacdd4e5ccc76445048c.png)

1.  Rename the tables as follows:

| DimProduct            | Product       |
|-----------------------|---------------|
| DimProductCategory    | Categories    |
| DimProductSubcategory | SubCategories |

![](media/f5405333724adfbef182cc6c55645bc8.png)

>   **Note** You should consider renaming all columns that you expect to use in
>   your data analysis for clarity. This also provides context for the Q&A
>   feature.

1.  Click **Close and Apply** to save the changes to the query.

2.  Save the Power BI desktop file as **AdventureWorks Sales.pbix** to the
    Documents folder.

3.  In the report view click the checkbox to the left of the **SalesAmount**

4.  Expand the **Categories** table and select **EnglishProductCategoryName**.

![](media/0911c2429a78ddf627897d5b29ece85b.png)

1.  Experiment with some of the other fields available, save your work when
    done.

####  Task 3: Add a Date Dimension

1.  Open the connection to the data warehouse from recent sources. (when
    prompted for connection settings ensure **Import** is selected then choose
    **OK**).

2.  Select the **DimDate** table and choose **Edit**.

3.  In the Query Editor window, remove all columns except those shown below:

![](media/c5d4364f77c1d194cdce9f1272ec5f41.png)

1.  Rename the **FullDateAlternateKey** column to **Date** (double click the
    column name or right click and choose Rename).

2.  Rename the **EnglishMonthName** column to **Month**

3.  Rename the query to **Order Date**

4.  **Close and Apply** the changes to save the query.

5.  Save your work

####  Task 4: Create Visualisations

1.  Switch to the report view

2.  Add a new report page.

3.  Expand the **Order Date** table in the Fields section

4.  Select the **CalendarYear** column. A Stacked Column Chart will display on
    the report canvas as shown:

![](media/eb0368f8e434936c50c62e64091b5c63.png)

>   *The reason for this is that the CalendarYear has been detected as a number
>   and the default behaviour is to sum numbers. This “auto summarisation” is
>   indicated by the following symbol next the column name:*

![](media/d87a18057f7f203e57222e216cedcbe4.png)

>   *This is incorrect so we will adjust the properties that control this
>   behaviour.*

1.  Select the **CalendarYear** column in the list of fields for the **Order
    Date** table by clicking on the column name as shown (a blue border will
    appear indicating the column is selected):

![](media/4f697ae47abeef571245e385ff5b50f4.png)

1.  On the Modelling Ribbon, under the Properties section, select the down arrow
    next to **Sum**

![](media/385605cb55ed9e751e1f0ea48b23e7a9.png)

1.  Choose **Don’t summarize**

2.  Note the visual changes to **Sum of CalendarYear**. Delete the visual.

3.  Note that the sum symbol has been removed from the **CalendarYear** column.

4.  Select the **CalendarYear** Column to create a new visualisation.

5.  Notice now the **CalendarYear** is now chosen to be on the axis.

6.  If necessary, expand the sales table and select **SalesAmount**

7.  Note the repeated values in the data, this is a sign of a missing
    relationship.

8.  Switch to model view

9.  Locate the **DateKey** Field in the Order Date table, then drag and drop on
    to the **OrderDateKey** column of the sales table

10. Switch back to report view

11. Notice how the visualisation has changed.

####  Task 5: Create Custom Columns 

1.  Switch to **Model View** and examine the relationships between **Products**,
    **SubCategory** and **Category**.  
    

    ![](media/412dab6d3f68e84f1638b3c28f049c54.png)

2.  In the Power BI desktop, switch to the **Data View**.

3.  Select the **Product** table.

4.  From the Modelling ribbon choose New Column to add a new Column called
    **SubCategory** to the **Product** table. In the formula bar, type the
    following Data Analysis Expressions (DAX) formula, and then press Enter:

>   **SubCategory = RELATED(SubCategories[EnglishProductSubcategoryName])**

>   *As you start typing expressions in the formula bar, Power BI will give you
>   a list of suggested formulae, just like Excel does, you can use the tab and
>   arrow keys to select the required function and continue typing your
>   expression. An example of this behaviour is shown here:*

![](media/638cf0814a0e818edc83d8d1a0aca7b8.png)

1.  Not all rows in the **Products** table have a value for the **Subcategory**
    column. Use the scroll bar to scroll down the **Subcategory** column until
    you see the rows that have a value for **Subcategory**.

2.  Click the **Add Custom Column** button again, to create the **Category**
    column, use the following formula and then press Enter:

>   **Category = RELATED(Categories[EnglishProductCategoryName])**

####  Task 6: Using more complex column expressions

>   You can use a more complex expression to determine if category values are
>   present for a product. If not, you can make a new category for the empty
>   values and call it, for example *Uncategorised*.

>   We will use the IF function to create a new uncategorised value to our list
>   of categories to account for those products without categories, this will
>   ensure that there are no blanks in our data.

>   The first step is to determine if the Category name is blank, the
>   **ISBLANK** function will return a true or false based on the input value,
>   so this is the one to use. The result of this expression is then used in the
>   IF function test. If it returns true we place our custom text there,
>   otherwise use the actual value for the related category name.

1.  Select the expression for the **Category** column in the formula bar.

2.  Change the expression for the **Category** column to the following:

>     
>   **Category = IF(ISBLANK(RELATED(Categories[EnglishProductCategoryName])),**  
>   **"Uncategorised",**  
>   **RELATED(Categories[EnglishProductCategoryName]))**  
>   

1.  Line breaks are included for clarity but are not necessary in the formula
    bar. Use Shift+Enter to add a line break and expand the formula bar if
    necessary.

2.  Change the expression for the Subcategory column to use the value “NA” when
    the category is Uncategorised.

3.  Your formula should appear like the following.

>     
>   **SubCategory =**  
>   **IF([Category]="Uncategorised",**  
>   **"NA",**  
>   **RELATED(SubCategories[EnglishProductSubcategoryName]))**  
>   

1.  Make sure the expressions work correctly then save the Power BI Desktop
    file.

![](media/e788d99b9ea45c68bfd41a16281d7e20.png)

>   **Note:** *These DAX expressions create calculated columns in the Product
>   table that use the RELATED function to bring the data in the Category and
>   Subcategory tables into the Product table. As the required information is
>   now placed in the correct location, the source tables can be hidden from
>   view. These functions are just a few of hundreds available in DAX, to learn
>   more about DAX functions refer to the Online DAX Function Reference,
>   available from Microsoft.*  
>   

####  Task 7: Create a Hierarchy

1.  Switch to Report View in the power BI Desktop.

2.  In the **Product** table, right-click the **Category** field and choose
    **New hierarchy**

![](media/7c270c30974ed67227c43e0fe0f4b8c3.png)

1.  Rename the hierarchy to **Product Categories** by right clicking the
    hierarchy name and selecting **Rename**.

2.  Drag **SubCategory** from the **Product** table onto the **Product
    Categories** hierarchy, wait for the yellow border to appear around the
    hierarchy name before releasing the button.

>   You can use the new **Categories** hierarchy in a visualisation by dragging
>   the Hierarchy name to the available fields list, or just simply clicking the
>   checkbox next to the name. Note that when you place a hierarchy on a chart
>   axes, it activates drill down mode on the visualisation, you might want to
>   explore this further. Not all charts support drill down.

####  Task 8: Hide tables and fields from client tools 

1.  Switch back to the Data View window if necessary.

2.  Right-click the **Category** table and choose **Hide in Report View**.

3.  Right-click the **Subcategory** table and choose **Hide in Report View.**

4.  In the **Product** table, hide the newly **Category** and **SubCategory**
    columns which are now contained in the Hierarchy.

5.  As the Fields **ProductKey** and **ProductSubcategoryKey** are used to
    define relationships in the model, they are not necessary to be seen in the
    visualisations. Right click these fields and select **Hide in report view**.

6.  The fields in data view will appear like the following:

![](media/e7f4bcff8c1681a84582a63a6639324b.png)

1.  Hide any other fields that are not used for analysis. You may also want to
    experiment with additional hierarchies, for example colour by category.

2.  After you have finished exploring the data, **Save** your work and close the
    Power BI Desktop.

End of Exercise

>   **Results**: After this exercise, you will have created and saved a Power BI
>   data model based on the AdventureWorks Data Warehouse.  
>   

Exercise 2: Creating Measures
-----------------------------

#### Scenario 

>   In this exercise you will continue to explore the capabilities of the
>   modelling features of Power BI. Here you will create various custom
>   calculations to aid in your analysis.

>   The main tasks for this exercise are as follows:

-   Create measures.

-   Use Time Intelligence.

-   Create visualisations.

####  Task 1: Visualising Measures

1.  Open **C:\\Labfiles\\Lab3\\Starter\\Creating Measures.pbix**.

2.  Create a visualisation by clicking the checkbox to the left of
    **SalesAmount** in the Sales table, then **Year** from the **Order Date**
    Table. You should have a column chart like this:

![](media/6e21e2e26c6e80fbf8f8c2bd5b5d64b5.png)

>   *The name Sum of SalesAmount is descriptive, however it can be difficult to
>   work with, Revenue is a better term. We will simplify the model by creating
>   a new measure and hiding those implicitly created measures.*

####  Task 2: Create a Measure 

1.  Switch to Report View.

2.  From the **Modelling Ribbon** click the **New Measure** button

![](media/2e939b8a7fa95a5f1181411965406b59.png)

1.  Type over the highlighted text with the following formula, then press Enter
    when finished.

>   Revenue = SUM('Sales'[SalesAmount])

1.  Switch to Data View, right click on the **SalesAmount** field and choose
    **Hide in Report View**. The **SalesAmount** field appears dim.

2.  Right Click again anywhere in the list of fields under the **Sales** table.

3.  Choose **New measure**

4.  In the formula bar type:

>   Cost = SUM(Sales[TotalProductCost])

1.  Create another new measure for the total number of units sold:

>   Units = SUM(Sales[OrderQuantity])

1.  Create a measure for Profit

>   Profit = [Revenue] – [Cost]

>   To calculate profit margin, you must divide the profit by the revenue. In
>   certain cases, the revenue could be 0, and this would cause an error. DAX
>   has many functions that can be used to ensure that errors are minimised. The
>   division by zero error is well known and DAX provides a safe DIVIDE function
>   to allow for the odd case where the denominator of an expression evaluates
>   to 0.

1.  Create a **Profit Margin** measure using the safe **DIVIDE** function

>   Profit Margin = DIVIDE([Profit],[Revenue])

####  Task 3: Create a measure using Time Intelligence 

>   Examine the year by year sales report. We need to plot the previous year
>   revenue next to the current year. We will create a new measure named
>   “**Revenue LY**” to represent the sales of the previous year:

1.  Create a new measure with the following formula:

>   Revenue LY = CALCULATE([Revenue],SAMEPERIODLASTYEAR('Order Date'[Date]))

1.  Add the **Revenue LY** measure to the Revenue by Year chart

>   *No data is displayed. The reason for this is that the time intelligence
>   functions require the use of dates and times. The relationship defined
>   between the date dimension and the sales data must be of the type date or
>   datetime*  
>   

1.  Switch to **Model** view and delete the relationship between the **Sales**
    table and the **Order Date** table. This relationship was based on a
    surrogate key, an integer field.

2.  Drag the **Date** field in the **Order Date** table to the **OrderDate**
    field in the **Sales** table, this creates a relationship based on a
    datetime datatype – which is required for Time Intelligence.

3.  Switch back to report view and examine the change in the column chart.

4.  Add the **Quarter** field to the chart and enable drilldown

5.  Click on the chart to drill down into the data

6.  Drill up in the chart and see how the revenue switches back to the year
    context.

End of Exercise

>   **Results**: After this exercise, you will have created a series of measures
>   used for data analysis.
