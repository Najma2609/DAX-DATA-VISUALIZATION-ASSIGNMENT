# DAX-DATA-VISUALIZATION-ASSIGNMENT
Calcualted columns and measures using DAX function and formulas and data visualization
loaded and transformed e-commerce sales data - in power query
in list of order table promoted header,changed data type of date ,removed duplicates, trim and clean text columns
in order detail table just trim and clean text column
sales target table replaced 18 and 19 to 2018 and 2019,changed data type ,trim and clean text columns
created calculated column "category type" using CONCATENATE (VALUE1,VALUE 2) IN ORDER_DETAIL TABLE
created calculated column "revenue" ='Order Details '[Amount]*'Order Details '[Quantity]
calculated column "Sales Category"=IF('Order Details '[Amount]>287.67,"Above Average","Below Average"), average amount= AVERAGE('Order Details '[Amount])
calculated measures:Total Orders = count('Order Details '[Order ID]) , Average Profit in Delhi = CALCULATE(AVERAGE('Order Details '[Profit]),'List of Orders '[State]="Delhi"), YTD Sales = TOTALYTD([TOTAL SALES],'List of Orders '[Order Date])
manage relationship list of order-order detail and sales target-order detail
Data visualizations was done for sales target by category using clustered column chart
MAX profit margin by sub category using donut chart where Profit Margin = DIVIDE(sum('Order Details '[Profit]),sum('Order Details '[Revenue]))
monthly sale trend using line chart
comparison of profit and quantity by sub category using scatter chart.
comparison of total sales and target using cards
sales performance matrix -matrix table
geographic sale analysis -map
sales distribution by sub category -tree map 
ordr count analysis by state using funnel chart
format each chart to enhance visual appeal
