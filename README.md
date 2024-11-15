# Sales Performance Analysis Project

In this project, I conducted a comprehensive analysis of sales performance by examining various KPIs that impact overall business success. 
The KPIs included:
- Total Sales and Cost Analysis: Analyzed the total sales and associated costs to determine the overall profitability of the business.
- Profit and Profit Margin Calculation: Calculated profits and profit margins across different product categories and departments, providing insights into the most profitable areas.
- Sales by Product Category, Store Type, Store City, and Location: Conducted a detailed breakdown of sales performance based on product categories, store types, geographical locations, and store cities to identify trends and growth opportunities.
- Sales by Promotion Analysis: Evaluated the effectiveness of promotional campaigns by comparing sales data before, during, and after promotional periods.
- Profit Margin by Product Category: Assessed the profit margin for each product category, helping to prioritize products with higher profitability.
- Unit Sales Analysis by Department: Analyzed unit sales by department to understand demand fluctuations and optimize inventory management.
- This analysis provided valuable insights to enhance decision-making, optimize sales strategies, and improve overall performance.
## Steps for Analysis: 
- Data Preparation: Load the data, check for missing values, and clean the dataset.
-  Gender Analysis: Investigate sales by gender.
-  Education Analysis: Explore how education level relates to sales.
-  Sales by Country: Compare sales across different countries.
-  Visualization: Visualize results using bar charts.
-   Statistical Testing (Optional): Perform hypothesis testing to check if the demographic variables significantly affect sales.
### Findings 
- Total Sales (in millions): 395261
- Total Cost (in millions): 158288
- Total Profit (in millions): 236972
- Profit Margin (%): 59.9
- Sales by food category (Vegetables was the highest 50067.64 while Canned Sardines was the least 868.28)
  
![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-6)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-7)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-8)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-9)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-10)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-11)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-12)

I futher focused on exploring customer demographics and how they relate to sales.I used gender, education, and sales_country columns to examine potential patterns in purchasing behavior. 

### Findings 
- Sales by gender
  
![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-13)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-14)

- Sales by education level

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-15)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-16)

- Sales by country

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-17)

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-18)

# Statistical Test 
- To test whether demographic variables significantly impact sales, I performed a t-test for Gender vs Sales
- One-Way ANOVA for eductational level vs sales

# Finindgs 
t-test gender vs sales 
- T-statistic: 0.03268977520314505, P-value: 0.9739220857097762
- Since the p-value is higher than 0.05, I accept the null hypothesis (H₀), meaning that there is no statistical evidence to support that sales are significantly different between genders in this case.
- We can conclude based on this dataset, that gender does not have a significant impact on sales. In other words, male and female customers are purchasing similarly in terms of total sales.
One-Way ANOVA eductation level vs sales
- F-statistic: 4.063287525685017, P-value: 0.002699925083035422
-  Since the p-value (0.0027) is less than the typical significance level of 0.05, this result is statistically significant. It means there is strong evidence to reject the null hypothesis, which states that there is no difference in sales across different education levels.
-   In practical terms, a statistically significant result here suggests that education level has a meaningful effect on sales. The sales amounts vary significantly depending on the education levels of the customers in the dataset.

# Further Finding 
Now that we know education level significantly affects sales, I examined the mean sales for each education level to identify which specific groups spend more or less. 
I also used the post-hoc tests (Tukey's HSD test) to determine which specific education groups differ significantly from each other in terms of sales. This can provide more granular insights into which levels of education are driving the differences.

![alt text](https://github.com/uchy4life/Sale-Performance-Analysis-/blob/main/Unknown-19)

Based on the mean sales values for each education group, we can interpret the following:
- High School Degree holders have the highest mean sales at approximately 6.61 million.
- Bachelors Degree and Partial High School holders have close mean sales, around 6.51–6.54 million.
- Graduate Degree holders have slightly lower mean sales compared to other groups, at about 6.39 million.
  
Given that the average sales are close across groups, the Tukey’s HSD test results will be especially helpful in confirming if any of these observed differences are statistically significant. If any education level pairs show a significant difference in sales, this could indicate that specific education levels have unique purchasing behaviors or tendencies.

- The only pair with a statistically significant difference in mean sales is between Graduate Degree and High School Degree holders. This is indicated by: meandiff (mean difference) of 0.2224, with p-adj = 0.0084, which is below 0.05, suggesting a significant difference. Reject = True for this pair, meaning the null hypothesis (no difference in means) is rejected, so Graduate Degree holders and High School Degree holders have a statistically different average sales. No Significant Differences Among Other Groups: All other comparisons have p-values above 0.05, and reject = False, meaning we do not have evidence to conclude there are significant differences in sales between these groups. Interpretation Graduate Degree vs. High School Degree: This result suggests that customers with High School Degrees tend to have higher sales than those with Graduate Degrees, based on the positive mean difference. Practical Insight: The difference, while statistically significant, is relatively small (0.22 million). However, it may still indicate some behavioral difference where customers with a High School education level are, on average, spending more than those with Graduate Degrees.
## Next Steps & Recommendations 

Targeting High School Graduates: This finding could inform targeted marketing efforts or promotions aimed at High School graduates, as this group shows a tendency to spend more on average.
