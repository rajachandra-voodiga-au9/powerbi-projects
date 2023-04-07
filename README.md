# powerbi-projects
## project1
### Festman stores financial analysis
In this project, you are required to model the data and perform analysis using DAX. This is the outline of the requirements:
•	Create a Date Table using CALENDARAUTO. This will support the time intelligence analysis.
•	Create a relationship between the financial table and the data table using the Date columns in both Tables.
•	Create measures to answer the business questions using DAX. These are some of the measures you can create: Total orders, Total Sales Amount, Total Discount offered, Total Profit, Profit Margin etc.
•	Perform time intelligence analysis by creating measures that calculate the same measures in the requirement above for the previous year(2013).

In the final task of this project, you are required to visualize your insights by leveraging the advanced visualization features in Power BI. Visualizing your insights will help to bring your insights to life and make it easier for your audience to consume your findings.

 ### Here are the steps performed:

Customize the report theme for your dashboard
Visualize the Key Performance indicators such as Total orders, Total Profit. Choose an appropriate visual that will help compare the Key performance indicators for the two years. This will provide context for the CFO to assess their performance.

Create a visual that breaks down the Total orders by Country, Profit Margin by Country, and % discount by discount bands.

Create a visual for profit margin by segment(Apply conditional formatting to highlight loss-making segment(s), Sales performance by year and month as well as a visual that highlight the top 3 products by Sales Amount(apply conditional formatting to highlight the top 3 products based on the sales amount).

Finally, create a visual that analyzes the profit margin by Segment, and products.

## project2
### Super store analysis
   ### problem statement:
Super Store manager needs help to better understand his/her Data. Store Manager wants data team to design the dashboard to analyse and interpret the data to help provide valuable insights.
### Dataset:
A Superstore dataset typically includes information about the products, customers, and sales associated with a retail store. 
### Step1:DataExtraction, Cleaning, Loading and Transformation
•	Data source is a excel file which is loaded by clicking on get data tab and since data is in raw format transform data tab is used to clean and prepare the data.
•	The dataset is provided with a table called “orders” which includes different columns.
•	Orders table is checked for appropriate data types specified for each column.
•	Empty rows and columns had been removed from order table.
•	We split the address column to different columns such as City, State, Country and Pincode.
•	Replace value tab is used to replace FC with first class.
•	Removed duplicates using remove duplicates tab.
### step2: Data Modeling:
•	Inorder to design a star schema from orders table (fact table) three dimension tables are created such as ,’Order details’, ‘Customer’ and ‘Product’.
•	One to many relationships is been created between fact table and dimensions table.
### Step3: Data Analysis:
•	A new calculated column called sales is created using the formula (Sales = Qty*price per qty*(1- % Discount)) and displayed total sales using card visualisation. (Total sales: 63.58k).
•	Sales from discounted products is calculated and displayed using card visualisation (Total sales from discounted products:63.54k).
•	A new column called cart value is created using the Dax formula Cart Value = IF(Orders[Sales]<1000,"Low",IF(Orders[Sales]<3500,"Medium",IF(Orders[Sales]<10000,"High",IF(Orders[Sales]>10000,"Very High")))).
•	Separately visualized the total sales just from the low cart value category using column chart.
•	sales from low cart category and discount greater than 50 percent = 
CALCULATE([Total Sales],Orders[Cart Value]="Low",Orders[Discount]>=0.5) is calculated and used card visualizer to display.
•	A column chart is created to show average no of days for each shipment type Dax formula used Number of days to deliver = DATEDIFF(Orders[Order Date],Orders[Ship Date],DAY).
•	Created a matrix visualization that displays order date as hierarchy , sales and sales year to date. 
•	YOY is calculated using Dax formula 
•	previous year sales = CALCULATE([Total Sales],SAMEPERIODLASTYEAR(Orders[Order Date].[Date]))

### Over All Analysis:
1.	Sales had been decreased in the year 2015 compared to 2014-year sales.
2.	63 percent sales are from the cart value (Low) highest compared to other cart categories.



         

