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

<img width="533" alt="image" src="https://github.com/user-attachments/assets/6f989cbd-a5e5-44e7-ba70-2ecf17557c51">

<img width="530" alt="image" src="https://github.com/user-attachments/assets/4ea58da3-6864-450d-9791-3da0fe4772e1">

1. Total Sales trended up, resulting in a 444.86% increase between January 2012 and December 2015.
2. Total Sales started trending up on July 2015, rising by 101.85% ($1,255,800.5) in 5 months.
3. Total Sales jumped from $1,233,009.1 to $2,488,809.7 during its steepest incline between July 2015 and December 2015.
4. Across all 165 Country, Total Sales ranged from $20.0 to $11,931,578.1.
5. At $11,931,578.1, the United States had the highest Total Sales and was 59,717,508.17% higher than The Gambia, which had the lowest Total Sales at $20.0
6. Across Category, Office Supplies had the most interesting recent trend and started trending up on 2012, rising by 88.15% ($3,005,595.9) in 3 years.
7. Technology had the highest Total Sales at $23,493,698.9, followed by Furniture at $20,086,582.5 and Office Supplies at $18,687,583.7.
8. At $387,583.4, Gilbert Wolff had the highest Total Sales and was 85.24% higher than Nicodemo Bautista, which had the lowest Total Sales at $209,229.7.
9. Across all 5 Person, Total Sales ranged from $209,229.7 to $387,583.4

## BOOKMARKS USED

For the sales dashboard, I created two bookmarks. One for Total Profit, and the other for Total Sales. This way I can easily navigate between both graphs.

## ROW LEVEL SECURITY

I created 5 key roles based on the markets Global Super Store operates in. These include Africa, Asia Pacific, Europe, LATAM, and USCA.



