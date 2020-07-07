Extracting and Transforming Data
================================

>   Estimated Time to complete: 60 min

Exercise 1: Accessing Data
--------------------------

#### Scenario 

>   In this lab exercise you will gather some data from the Internet and learn
>   how to shape and transform that data to support additional exploration and
>   analysis.

>   The main tasks for this exercise are as follows:

-   Import data using Get & Transform.

-   Transform and cleanse data

-   Source additional data to create a *data mashup*.

-   Create a relationship manually.

-   Create a visualisation to test the model.

####  Task 1: Import data from the Internet 

>   First, we will start by exploring a website to obtain data. An important
>   consideration when accessing data from the internet is that websites do
>   change, and this could provide unique challenges if you wish to maintain the
>   ability to refresh data from these sources. It is always a good idea to
>   obtain data from rather static sources, many of which are provided by
>   government, academia and large corporations. Also, another factor to be
>   aware of is that some sites will not allow PowerBI to scrape the HTML and/or
>   extract data.

1.  Start your browser and open a page to <http://www.motogp.com>

2.  Scroll down the page slightly to find the link, **RESULTS**.

3.  When you click this link the site takes you to the results section for the
    current season. Copy this URL, we will use it soon.

4.  Scroll down the page and note the areas containing tables of data.

5.  Start the **PowerBI Desktop** and from the splash screen, click the **Get
    Data** link.

6.  From the **Get Data** dialog, click **Other**, make sure **Web** is selected
    then click **Connect**.

7.  In the **From Web** dialog, paste the URL and add the number 2017 as shown:

![](media/f33de8fdb891750c3de5301e01daaeeb.png)

1.  Click **OK**.

2.  PowerBI will now go to the site and examine the structure of the page at
    that location. A list of available data table(s) will be shown as follows:

![](media/5cc83ca0e05641da81f419b5055d4750.png)

1.  You can click on the names of the tables to preview the data or select the
    checkbox to download the data from that table.

![](media/c76ca917ff8764793af9c43716a9cc9c.png)

>   **Note:** You can also select multiple tables. The name of the table becomes
>   the name of the query, this can be renamed as necessary.

1.  Select the checkbox next to the last table **MotoGP World Standing 2017** in
    the list, then click **Edit**.

2.  This will open the **Query Editor** Window. You may find this window will
    appear behind the main Power BI Desktop window, bring it to the foreground
    and maximise the window.

3.  Your query editor window will look like the following:

![](media/a2411a0f1fa6d9aa2e89a0dfa21dae9d.png)

1.  Explore some of the commands available on the various ribbons by examining
    their tooltips and asking your instructor if you want more detailed
    explanations.

2.  This data seems to be in good shape, so no edits are required at this point.
    Change the query name however to simply **MotoGP Results**, then in the top
    left, click the **Close & Apply** button.

>   *Power BI will download the latest data from the MotoGP site, close the
>   Query Editor and return you to the Power BI Desktop report view. You will
>   notice a list of fields on the right of the PowerBI desktop. These are the
>   columns provided by the MotoGP data. Notice that the numeric fields have a ∑
>   to the left, indicating that these are numeric fields and the default
>   aggregation is to sum these values.*

![](media/9380829f956584178ce7a7bda5d86d41.png)

1.  If necessary, switch to **Report View** by clicking the button on the left
    of the Power BI Desktop as shown.

![](media/e2710b268fd92c03230d5bf0c3aa8cd8.png)

1.  Select the check box next to **Points**

2.  Select the check box next to **Nation**.

3.  This will create a default column chart on the design surface (canvas).

4.  Take note of where the fields have been added to the visualisation,
    **Points** is in the **Value** section and **Nation** is on the **Axis**.

![](media/6d0491adc5d2461f154064dd2e79fe0a.png)

>   *Experiment with these (and other) fields by selecting and un-selecting
>   different combinations and sequences. If you remove all checkboxes the
>   visualisation is deleted (and there is an undo!). You can also drag and drop
>   field names into the different sections in the visualisations pane. If you
>   use drag and drop, you will discover that multiple fields can be placed on
>   the Axis. This enables what is referred to as a “drill down” and can be used
>   to expose various levels of detailed data. You will use this feature later
>   in this lab exercise. Once you have explored this function a little, return
>   to the original chart with Points for the Value and Nation for the Axis*

1.  Resize the column chart to view the data. Your chart should look like this:

![](media/5ba1c74d8188f77fe432ba727bab7f36.png)

1.  Experiment with some of the available visualisations and explore the
    available actions on the chart, e.g. sorting.

2.  Save the Power BI Desktop file to Documents with the name
    **MotoGP_Results.pbix**

3.  Keep the file open for the next exercise.

End of Exercise

>   **Results**: After this exercise, you will have obtained some data from the
>   internet and created a visualisation.  
>   

Exercise 2: Combining Data
--------------------------

#### Scenario 

>   In this exercise you will access additional information from the web in
>   order to satisfy the requirements for geocoding and allow the data to be
>   accurately visualised on a map.

>   The main tasks for this exercise are as follows:

-   Create a new query.

-   Transform and cleanse data

-   Create a relationship

![](media/c76ca917ff8764793af9c43716a9cc9c.png)

>   **Note:** *If you obtain the country data from a site that is different to
>   the one given, you will need to use the appropriate functions to cleanse the
>   data from your source. Ask your instructor for assistance. This exercise is
>   constructed to show you what transformations may be required on real world
>   data, to make it clean, consistent and trustworthy.*

####  Task 1: Import Additional Data

1.  Use your browser to search for the following: **3 letter country codes**

2.  Select the search result for “**Country Codes List - Nations Online
    Project**”.  
    *The URL for this site is:*
    <https://www.nationsonline.org/oneworld/country_code_list.htm>

3.  Examine the page and its structure. The data we require is located further
    down the page.

![](media/71a545deabc30fc7a493df04ff96de8a.png)

1.  Copy the URL from the location bar in the browser.

2.  Switch to the Power BI Desktop and choose **Get Data** -\> **Web**

3.  Paste the URL in the **From** web dialog and click OK.

4.  In the **Navigator** select Table 1 as shown (or the table the gives the
    required data):

![](media/5afbe3907716db6f5896a413d77ae583.png)

>   *As you can see this data will require a little cleaning up. Can you think
>   of a way to remove the rows containing single letters?*

####  Task 2: Apply transformations to the data

1.  Click the **Transform Data** button to open the query editor.

![](media/19597b43c29804abc22358d86304ac5e.png)

1.  Remove the first row by clicking the **Remove rows** button, then **Remove
    Top Rows**

![](media/9cccbc3d64b5175572280b5cc6c41674.png)

1.  Enter 1 as the number of rows to remove.

2.  Double click the Column Header and rename Column2 to **Country** and Column4
    to **Code** as follows:

![](media/4b484a010862379bc22f489fd8e4f7f5.png)

1.  Click the **Choose Columns** button

![](media/d85c100e8971face57f20c9f7c762067.png)

1.  In the Choose Columns dialog, clear the **(Select All Columns)** checkbox
    and select Only the **Country** and **Code** columns as shown:

![](media/9e23accefc2764f4a52c86897ee242b9.png)

1.  Click **OK** to remove the unnecessary columns.

2.  On the right-hand side of the query editor, locate the **Name** under the
    properties section:

![](media/5b5e633bf484097b0a629ad5e5bd4678.png)

1.  Rename the query **Countries**

2.  Click **Close and Apply**, wait for the query changes to be applied.

3.  Examine the Fields pane and notice the inclusion of a new table named
    **Countries**.

![](media/96c3302a8f6d11b22c5d9843476586fb.png)

1.  Save the Power BI Desktop file.

2.  Click to select the column chart **Points by Nation**, which you created in
    the previous exercise.

3.  Remove the **Nation** field from the axis by clicking the x located on the
    right of the field name.

![](media/e54f5fd3f597834ceac7e1992c674fdf.png)

1.  In the list of fields under **Countries** add the **Country** field to the
    axis of the column chart. (Either drag and drop or click the checkbox to the
    left of the field name).

2.  This will result in the following:

![](media/d0a1df97db25ed9544c21531270fe92f.png)

>   *The repeating values are typically a sign of a missing relationship in the
>   data. We will fix this in the next task*

####  Task 3: Create a Relationship

1.  Switch to the modelling view in the Power BI Desktop.

![](media/28281450e7d9e67ec0b50cb7d21120ab.png)

1.  If necessary, resize and move the tables around to clearly see all the
    fields as shown above:

2.  Click **Code** in the Countries table and then drag this to the MotoGP table
    and drop it on the **Nation** field.

3.  The following dialog displays indicating that there are duplicates on the 1
    side of the relationship:

![](media/be83eb38397f4bcf18346c65a901dce2.png)

1.  We will remove these duplicates by returning to the Power Query editor.

2.  Click **Cancel** to the create relationship dialog.

3.  On the home ribbon, click **Transform Data.**

4.  Select the **Countries** query from the list of queries on the left.

5.  Click the down arrow to the right of the column name **Code**

6.  Clear the checkbox for **(blank)**

![](media/400c005eac0575cd648c4d995cc25e3f.png)

1.  Click **OK** to filter dialog.

2.  **Close and Apply** the query

3.  Return to the Model view

4.  Drag the name **Code** from the **Countries** table and drop it on the
    **Nation** column in the **MotoGP Results Table**

5.  This will now create the 1 – M relationship for you and results in the
    following changes to your data model:

![](media/c40fc23b714b3b3b194d26f6e0116a24.png)

1.  Switch back to the Report view and examine the changes in the chart. You
    should now see that the data is displayed correctly:

![](media/aed5c9f83e37b43ebfdc2efcc4cf60e3.png)

![](media/c76ca917ff8764793af9c43716a9cc9c.png)

>   **Note**: *You will notice a large column value for (Blank). Although we
>   have created the relationship correctly, the blanks typically indicate that
>   there is some unmatched data. Investigating the data further you discover
>   that the codes used by the MotoGP in the Nation column are not the standard
>   internationally recpgnised codes we obtained. An example here is Spain, the
>   official code is ESP, whereas MotoGP uses SPA instead. There are several
>   ways this can be addressed, we will use the search and replace technique.*

1.  Click the **Transform Data** Button to return to the Power Query editor

2.  In the query Editor window, Locate the **MotoGP Results** Query, then right
    click on the **Nation** Column.

3.  Choose **Replace Values…** as shown:

![](media/30095ff0663da77f6bc32f8425262f45.png)

1.  In the Replace Values dialog enter the value to find as **SPA** and the
    value to replace with as **ESP**

![](media/c76ca917ff8764793af9c43716a9cc9c.png)

>   **Note**: *These values are case sensitive*

1.  Click **Close and Apply** to return to the report view

>   *Examine the chart, you will now notice that the data displays correctly for
>   Spain, however, there is still a (Blank) visible, indicating further
>   unmatched data. Can you see where and how to fix this?*

![](media/8c77dd35983722321dea4ee9d3a68439.png)

End of Exercise

>   **Results**: After this exercise, you will have created a model that uses
>   data from different sources on the internet and created a relationship to
>   correctly visualise that data.

Exercise 3: Working with multiple files
---------------------------------------

#### Scenario 

>   In this exercise you will work with some publicly available data from the
>   Australian Federal Government Department of Industry and Science. The way
>   the data is provided is via comma separated value files (csv) for each
>   quarter of the fiscal year. You can examine (and download) this data from
>   the department of Industry by searching the web for Australian Department of
>   Industry Grants Reporting. The direct URL is:
>   <https://www.industry.gov.au/about-us/finance-reporting/grants-reporting->

>   We have previously downloaded all the files from the 2013/14 financial year
>   (as this data has now been archived) and placed them in the
>   **C:\\Labfiles\\Data\\GrantsReporting** folder. These files contain the data
>   posted for each quarter of the financial year.

>   The main tasks for this exercise are as follows:

-   Combine multiple data files.

-   Transform and cleanse data

-   Visualise data

####  Task 1: Use Get & Transform to access multiple data files

.

1.  Start a new instance of the Power BI Desktop, close the splash screen and
    then save the file as **GrantsReporting.pbix**

2.  From the **Get Data** drop down list choose **All** then select **Folder**
    in the Get Data Dialog as shown:

![](media/e2d0bc099a048f92555bb96eb48ec671.png)

1.  Click **Connect**

2.  In the folder dialog box, click **Browse**

3.  Navigate to the **C:\\Labfiles\\Data\\GrantsReporting** folder, then click
    **OK**

4.  You will be presented with the following dialog:

![](media/e388a7d4e37c96cfd87cff717c67b885.png)

1.  Click the **Edit** button to start the query editor.

2.  The **Query Editor** window opens and displays a result set as follows:  
    

    ![](media/644ac11c8bc0a17cce26602f5d9c9793.png)

3.  Click either of the **Combine Files** buttons, located in the header row or
    in the **Combine** section of the **Home** ribbon:  
    

    ![](media/9bb92560bc34f6172228dcc909728b96.png)

4.  This will prompt you with the following dialog:

![](media/939a6a9ea9d4c75b99f0f9098dfb8f9d.png)

1.  Click the **OK** button to continue.

2.  **Power Query** will now open all the files in the folder and combine their
    contents, expanding all the data contained in these individual source files
    into a single result set.

3.  When the import data process is complete, save your work. When prompted
    about pending query changes select **Apply Later** to save the file
    immediately.

4.  Save the file to the **Documents** folder as **GrantsReporting.pbix**

####  Task 2: Sort and Filter the data

1.  If necessary, switch to the query editor window.

2.  Your Query Editor window will show the contents of all 4 files in the data
    preview window – for performance, only a small number of rows are imported,
    when the query is refreshed, all rows will be imported.

![](media/b320607aafb108dbcb1b4b852b1b9e7d.png)

1.  The first step required in this data transformation is to filter for only
    those rows related to **Industry**.

2.  Click the down arrow next to the agency column and examine the follow
    dialog:

![](media/48b9c8347247f68d18800e13671d7f4f.png)

1.  As you can see, not all the data is loaded into cache, to ensure we get all
    the Department of Industry rows, click the link **Load more**.

2.  Clear the **Select All** check box, then select only the **Industry**
    checkbox *(you may have to scroll the list)*

3.  Click **OK**.

4.  Examine the **Value (GST incl.)** column. Notice the \$ symbol on the left
    of the field name:

![](media/22897ff3437d09191398aa28ea6680c5.png)

>   *This indicates that a datatype of Fixed decimal number (currency) has been
>   assigned to this column. You can also change the datatype from this list.
>   Note there is an option to use a Locale – this becomes important when
>   working with dates.*

>   *Selecting the correct data type is important for when you use various
>   functions to create custom measures (calculations) in your model.*

####  Task 3: Shaping Data

1.  Use the Choose Columns button to remove columns from your results set so
    only the following remain:

    -   Grant Recipient

    -   Value (GST incl.)

    -   Grant Commencement Date

    -   Grant End Date

    -   Grant Funding Location

    -   Postcode

2.  The Query editor view of this table will look like the following:

![](media/0cac10991c569e6bb1dd17197002a88e.png)

>   *Looking at this data, you can see we would have a challenge creating a
>   chart and plotting this by state, or city (Grant Funding Location). Get &
>   Transform allows us to easily fix this. We will begin by splitting the
>   column into State and City, then renaming and cleaning up blank spaces.*

1.  Select the **Grant Funding Location** column

2.  Select the **Transform** ribbon

3.  Click the **Split Column** Button**,** then choose **By Delimiter**.

![](media/0284c6b41e2589c8b697d1a2c09bbbf7.png)

1.  Accept the default comma as the delimiter and choose to split at the **Each
    occurrence of the delimiter** as shown:  
    

    ![](media/a287398a09d758f2de682d5f202f76e8.png)

2.  Click the **OK** button to continue

3.  Rename the column **Grant Funding Location.1** to **City**, and **Grant
    Funding Location.2** to **State** by double clicking on the column names

4.  Right click the **State** column and Select **Transform Trim** as shown:  
    

    ![](media/0ec96c88a185754eaeea3745ac95ddbf.png)

      
    **Note**: *This removes the leading space remaining from the split
    transformation. To remove the space in the same split transform, you could
    have split on a custom delimiter and entered a comma and a space. Clean will
    remove any none printable characters that may be present in the column. When
    you click Trim, you will notice all the values shift to the left after the
    space is removed*.

5.  Filter the result set to exclude rows where the State value is null, click
    the down arrow on the right of the field name as shown, and clear the (null)
    and (blank) checkboxes:

![](media/b6c827eb5cea4a2a31eca61612d0b562.png)

>   *As you can see there are several issues with the data, remember it is also
>   Case Sensitive.*

1.  Click **Close and Apply** to return to the report view of the Power BI
    Desktop.

2.  In the list of fields, select **Value (GST incl.)**, this will create a
    single column chart as shown:

![](media/c3082c876c95149ab8de89a878ad3dfb.png)

1.  Next, while the visualisation is still selected, click the checkbox for
    **State**, this will expand the chart to show the grant value by state:

![](media/cbb5850a155808731f6d07fa91b10e63.png)

*As we saw in the data there is still a bit of work to do.*

1.  With the chart is still selected, click the map icon to change the
    visualisation.

2.  Expand the map to show all the data. You should have something like the
    following:

![](media/1f90d1548dbca7324b23ce8d6f28a5dd.png)

1.  Click the **Edit Queries** button to return to the query editor.

2.  Right Click the **State** Column and select Replace Values …

3.  Complete the Replace Values dialog Replacing **Kangaroo Island** with
    **SA**.

4.  Click **OK**

5.  Click **Close and Apply** and return to report view.

>   *Notice how the map updates automatically and removes Kangaroo Island from
>   somewhere in Washington, USA. (The Kangaroo Inn at Orcas Island, WA). You
>   will still notice however that WA and NT are incorrectly placed in the
>   American continent, Washington state and the Northern Territories of Canada.
>   Again, we can fix this using the power of Get & Transform by creating a more
>   accurate geocode column. Firstly, we will make the data consistent by
>   capitalising the state code and examining the impact on the map.*  
>   

1.  Switch to the **Query Editor Window**. If you have closed it, click the
    **Edit Queries** button to open.

2.  Right click the **State** column and select **Transform UPPERCASE.**

3.  Click **Close and Apply** to return to the report.

>   *There is no discernible difference on the map, lets change back to a column
>   chart to see what this impact is.*

1.  In the Visualizations section select the stacked Column chart (Top 2nd
    left). Your chart should appear as follows:

![](media/d5eb486eb50d9d10026ec2cf8edd4a49.png)

>   *Complete the data cleansing process by replacing the remaining full state
>   names by their 3 letter abbreviations. After fixing the data your chart will
>   look like this:*

![](media/2bca9e54f0cc737144b150eba4bd89c8.png)

1.  Save your work.

####  Task 3: Mapping Data

1.  Click **Edit Queries** to open the query editor

2.  From the Add Column ribbon, choose **Custom Column**.

3.  Name the Column **Location**, then enter the following formula after the =
    in the Custom column formula box:

>   [State] & “, AU”

1.  Your Custom Column Dialog should appear as follows:

    ![](media/f5c09e9403f34124ab80a032a2a901ab.png)

2.  Click **OK**

3.  Click **Close and Apply** to return to report view.

4.  Click the **+** next to Page 1 at the bottom left of the screen to create a
    new report page.

![](media/c6e4bc7ec1ab037cdcefee3bee4ec548.png)

1.  On Page 2, click the map visualisation. This will appear as the following on
    the design surface:

![](media/cf73d19bf0aafe0812d3cf839a2d8c8d.png)

1.  While the map is selected, drag the **Location** field to location on the
    map visual.

2.  Drag **Value (GST incl.)** to the size field of the map visual.

3.  The map should appear like the following. (Resize as appropriate to clearly
    show the data points).

![](media/eb31bff3854cc8e878c8a2fb8af6be32.png)

1.  Save and Close Power BI Desktop.

End of Exercise

>   **Results**: After this exercise, you will have a data model built from data
>   across several files located in a folder and plotted the results on a map.
