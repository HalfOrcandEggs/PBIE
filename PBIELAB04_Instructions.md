#Lab 4	Visualising Data in Power BI

##Exercise 1
## Creating Power BI Reports 
Estimated time to complete: 30 min

###Scenario 
In this exercise you will create various visualisations in the report view of the Power BI Desktop. These visuals then form the basis of a Power BI Dashboard.

The main tasks for this exercise are as follows: 

-	Create a Power BI reports
-	Explore Power BI Visualisations


####**Task 1: Create a multipage report**  

1.  [] Log on to the virtual machine
2.	[] Open **AdventureWorks Sales.pibx** from the starter folder of lab 4
3.	[] From Report view click the **Employees** field in the **Sales** table
4.	[] Expand the fields in the **Order Date** table
5.	[] Expand the **Calendar Hierarchy**
6.	[] Select **Quarter** from the list of fields, (uncheck Year).
7.	[] Resize the chart until all the quarters appear on the axis as shown
!IMAGE[khp7fkrf.jpg](khp7fkrf.jpg) 
8.	[] While the chart is selected press **Ctrl+C** to copy, then press **Ctrl+V** to paste.  
9.	[] Drag the new chart below the **Employees by Quarter** chart.
10.	[] With the new chart selected, clear the checkmark from the **Employees** field and replace it with **Customers**. The visualisation will change automatically.  
!IMAGE[fy26nhuq.jpg](fy26nhuq.jpg) 
11.	[] Copy and Paste the **Employees by Quarter** chart once more, this time place it to the right.
12.	[] Deselect **Employees** and select **Resellers**
13.	[] Select the **Units sold** measure to create a new visualisation.
14.	[] Expand the Calendar hierarchy and select the **Quarter** field. 
15.	[] Clear the checkbox for **Year**.
15.	[] Switch to a line chart and examine the  new visualisation.
16.	[] Select the various sorting options by using the menu on the top right of the visualisation. Use the Sort by Quarter option and resize the chart
!IMAGE[r487d325.jpg](r487d325.jpg) 
17.	[] Move the Chart to the bottom right of the report page.
18.	[] Create a new line chart visualisation to compare the **Revenue** and **Cost** Measures.  
!IMAGE[i7yoec5b.jpg](i7yoec5b.jpg) 
19.	[] Resize the new chart to the same size as the Units Sold by Quarter chart and place it above this on the bottom right.
20.	[]Your report should look like the following
!IMAGE[ik69em4u.jpg](ik69em4u.jpg) 
21.	[] Rename the report page to Sales Volumes *(double click the page name)*
22.	[] Save the report


####**Task 2: Add a Card visualization**

1. [] Add a new report page.
2. [] Click the Card visualisation.  
!IMAGE[0mj7k0bo.jpg](0mj7k0bo.jpg) 
3. [] With the card selected, check the Profit measure from the Sales table. The card visualisation will change to the following:  
!IMAGE[zesdyfa5.jpg](zesdyfa5.jpg) 
4.	Resize the card and place it in the top left corner of the report page.


####**Task 3: Add a Slicer** 
1.	[] Expand the list of fields in the Order Date table, then Expand the Calendar hierarchy
2.	[] Ensure no visuals are selected on the report page (we wish to create a new one, not add to an existing one).
3.	[] Select the Year field from the Calendar hierarchy
4.	[] Choose the Filter visualisation from the list  
!IMAGE[d8x4qqxo.jpg](d8x4qqxo.jpg) 
5.	[] Resize the slicer to fit underneath the Profit Card.
6.	[] Change to different years and examine the results.
7.	[] No data exists for 2010, so this we will be filtered out.
8.	[] Click the report design surface to ensure no visualisation is selected.
9.	[] In the filters section of the report, drag the **Year** field from the **Order Date** table to the **Page level filters** section.  
!IMAGE[bpu4rab8.jpg](bpu4rab8.jpg) 
10.	[] Place a checkmark in Select All, then clear the checkbox for 2010.
11.	[] Save the report.


####**Task 4: Create a tabular Report** 
1. [] Click to add a table visualisation:  
!IMAGE[vs8j5ung.jpg](vs8j5ung.jpg) 
2. [] Add the following fields: Category, SubCategory, Revenue, Profit, Units Sold and Profit Margin
3. [] Resize the table so the data is displayed across all the columns.
4. [] Move the table to the right of the Card and Slicer  
!IMAGE[5w0gi8pm.jpg](5w0gi8pm.jpg) 
5. [] Create an additional slicer for the **Category** 
6. [] Add a Column chart to compare the **Revenue** and **Profit** by **Subcategory**. Place this chart on the bottom left of the report page:  
!IMAGE[totmgibf.jpg](totmgibf.jpg) 
5. [] Copy and paste the Revenue and Profit by subcategory chart. Move the copy to the bottom right of the report page.
6. [] Remove Revenue and Profit from the value section of the field list and replace with Profit Margin



####**Task 5: Create a line chart** 
1. [] Click in the blank space of the report page.
2. [] Select the Units Sold measure then select the SubCategory field from the Product table.
3. [] Change to a line chart and resize to fit the space in the top right side of the report page.
4. [] Rename the report to **Sales by Category**.  
!IMAGE[ohg9w2g7.jpg](ohg9w2g7.jpg) 
6. [] Experiment with the various slicers and filters. Examine the cross-filtering behaviour of the visualisations


>[!note]*After this exercise, you will have created several reports on multiple pages using the Power BI Desktop*.


===
##Exercise 2
##Creating Interactive Visualisations
Estimated time to complete: 15 min

###Scenario 
In this exercise you will create an animated visualisation in the Power BI Desktop. This can be used to examine data over time.

The main tasks for this exercise are as follows: 

-	Create a scatter chart
-	Explore the Power BI filtering features


####**Task 1: Create a scatter chart** 
1.	[] Add a new report page and rename it to **Sales Over Time**
2.	[] Add a scatter chart visualisation and resize it to fill the report designer.  
!IMAGE[arp78qx4.jpg](arp78qx4.jpg)
3.	[] Add the following fields to the visual  
| Visual Field| Data Field |
|:---------|:---------|
| **Legend**   | Subcategory   |
| **X Axis**   | Profit   |
| **Y Axis**   | Revenue |
| **Size**	   | Units Sold |
| **Play Axis**| Year |  

4. [] Add a visual level filter to display just the data for the **Clothing** category. (Alternatively, you can create a slicer to make the filtering by Category more flexible).
5. [] Press the play button on the left to watch the data points move over time.  
!IMAGE[ovotaohc.jpg](ovotaohc.jpg)   
6. [] Select the data point representing Jerseys to highlight the changes over time.
7. [] Save the report and close the Power BI Desktop.

>[!note]*After this exercise, you will have created a scatter chart to examine the changes in data over time*.