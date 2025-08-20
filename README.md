# Sales & Customers Dashboard

## Overview

A dashboard was created using Tableau to showcase the performance of top products. Tableau was chosen to make data sharing easy and simple. The author of the dataset was Leanne Vermeulen, who generated the fictitious data used throughout this project.

>[Link to the Tableau Public page](https://public.tableau.com/app/profile/david.golacis/viz/SalesCustomersDashboard_17556899946560/SalesDashboard).

### First Dashboard

The first page features general sales information, including KPIs, target metrics, visualisations, and high-level and detailed product breakdowns. KPIs for the number of sales, orders, customers, customers who've made a sale, and average days to shipment were added to clarify the performance of the product line for decision-makers. Dynamic bar charts were implemented to visualise what proportion of customers had made a purchase, and the proportion of sub-categories by sales was included to support this further. Additionally, there are controls to change which data is being viewed: sales, quantity, or orders. At the bottom of the dashboard lies a high-level product overview, complemented by a detailed breakdown of individual products. Lastly, static sales targets for sub-categories have been established to state the business's objectives, which, when paired with the high-level overview, will guide decision-makers in investigating under-performing stock at the low-level details.

### Second Dashboard

The second page features aggregations of customers' data: their experience ratings, registration age, address, and a detailed view of their orders. The order ratings and registration age were displayed as bar charts for easy comparison. A line chart was used to display the number of new members daily over the last 12 months, and addresses were shown on a map with additional city information. Finally, a granular table was used to show details of orders, sorted by customer IDs. This table also featured a total at the top row, allowing for quick scanning of high-level information.

## Preparation of the Dashboard

Four CSV files were imported and joined using primary and foreign keys from the following tables: Sales, Customers, Products, and Monthly Sales Targets.

Two of these files required additional steps before they could be joined to the master sales table: these were products and monthly sales targets. The products file had the Product ID key split into two headers, 'Item Code Abbr' and 'Item Code Index', which required concatenation to allow for the join with the sales table. The monthly sales targets file was unpivoted inside Tableau and exported as a CSV file before a relationship with the sales table could be established. Full outer joins were used to identify if and how many missing products, customers, or orders were present in this dataset. However, for this dashboard, the null values were omitted as they did not impact the quality of the data by even 1% of the total number of records.

Please note that, since this data was no longer actively supported and maintained, the date of 1st August 2024 was used as the current date to identify when new customers joined the service, as the alternative would be that all customers had joined over a year ago, with no new acquisitions.
