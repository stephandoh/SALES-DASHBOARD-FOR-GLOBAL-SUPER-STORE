# SALES-DASHBOARD-FOR-GLOBAL-SUPER-STORE
Global Super Store is an online giant store that has worldwide operations. This store takes orders and delivers products across the globe and deals with all major product categories like furniture, office supplies, technology, and so on.

As a Power BI developer, I analyzed the sales based on the provided historical data to plan for inventory and business processes accordingly. I also performed the analysis to understand the product's and customer’s behavior.

## DATA MODELING

This project uses the Orders table as the fact table, containing key details such as Category, City, Country, Customer Name, Market, and Region. The table below are the dim tables, and these include:

Returns Table - Tracks returned orders with columns like Order ID, Region, and Returned.
People Table - Lists regional managers (Person) and their assigned Region.
Date Table - Provides time-related details like Month Name, Week Number, and Year.

<img width="618" alt="image" src="https://github.com/user-attachments/assets/ea980402-17e2-466d-8500-5a0d9b79e069">

<img width="538" alt="image" src="https://github.com/user-attachments/assets/07694317-b942-4b90-95b2-125290c67e94">

## DAX MEASURES

1. As of Date = “Report as of date: “ & Max(Orders[Order Date])

2. Profit Ratio = DIVIDE([Total Profit],[Total Sales],0)

3. Total Profit = SUM(Orders[Profit])

4. Total Sales = SUMX(Orders, Orders[Unit Price] * Orders[Quantity])

5. UserPrincipalName = USERPRINCIPALNAME()

## DASHBOARD AND INSIGHTS

