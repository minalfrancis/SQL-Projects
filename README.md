
/*Purpose: Analyze sales data to identify trends, top-selling products, and revenue metrics for business decision-making.

Description: In this project, you will dive into a large sales dataset to extract valuable insights. 
You will explore sales trends over time, identify the best-selling products, calculate revenue metrics such as
total sales and profit margins. */


/* Problem 1: Daily trend for product sales */

select * from sales_data

select datename(dw, order_date) as order_day, count(distinct(order_id)) as total_orders
from sales_data
group by datename(dw, order_date)
order by total_orders desc;
