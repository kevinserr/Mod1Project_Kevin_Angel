# Cafe Financial Analysis & Insights

## Project Overview

Angel and I have been hired by the owner of a popular café chain to clean and analyze their messy transaction dataset. The original dataset includes the following columns: `Transaction ID`, `Item`, `Quantity`, `Price Per Unit`, `Total Spent`, `Payment Method`, `Location`, and `Transaction Date`.

Our goal is to uncover meaningful trends within the café's sales data. Specifically, we aim to determine:

- Which item sells the best  
- Which month generates the most profit  
- Which day of the week is the most successful over the course of a year  

Our plan is to first clean the dataset, addressing any missing values as accurately as possible without introducing false information that could distort our findings. Ultimately, we hope to provide data-driven recommendations to help the café improve overall sales and performance.

🔗 [Figma Kanban Board](https://www.figma.com/board/juOigrlEdvkUQz318G1yUE/Mod1_Final-Project-Kaban-Board?node-id=0-1&t=9t959gGv1UOWJsVn-1)

---

## Business Questions

- **What are the peak sales months?**  
  Sales peaked in **June**, likely due to warmer weather. **October** came in second, which may reflect increased coffee demand as temperatures drop.

- **Are weekends busier than weekdays?**  
  Yes, weekends are generally busier. **Thursday** had the highest number of sales, followed by **Friday** and **Sunday**.  
  We were surprised that **Saturday** wasn't among the top days. One theory is that customers tend to sleep in and skip their usual coffee run.  
  **Wednesday** was the slowest day of the week. We recommend offering discounts or promotions on Wednesdays to boost sales.

- **Any other findings relevant to stakeholders?**  
  - **Salads** made up most of the café's daily sales.  
  - **Sandwiches** were also a strong performer.  
  - **Coffee**, surprisingly, only accounted for about **9%** of total sales.  
  - **Cookies** were the least sold item.  
  The café’s diversified menu appears to be a smart business decision, allowing it to cater to a broader audience.

- **How reliable was the data? What cleaning was needed?**  
  While we did not collect the data ourselves, around **5.7%** of item entries were labeled as `'UNKNOWN'`, `'ERROR'`, or were blank.  
  This relatively small portion likely did not skew the findings. However, more consistent data collection would help improve future analyses.

---

## Data Cleaning Summary

- Replaced all `'UNKNOWN'`, `'ERROR'`, or empty cells with `'BLANK'` across relevant columns.
- Since only 5.7% of the `Item` column was blank, we chose not to delete those records. Instead, we kept them and preserved their `Total Spent`.
- Removed about **460 records** with missing or blank transaction dates to avoid skewing day/month-based trends. We chose not to impute dates to maintain data integrity.

---

## Key Findings

- **Summary Statistics:**  
  ![Summary Image](https://github.com/user-attachments/assets/6a99ed30-4a67-4ab4-ab60-3e5f255d3fdf)

- **Peak Sales Month**: June  
- **Top 3 Sales Months**: June, October, January  
- **Busiest Days**: Thursday, Friday, Sunday  
- **Slowest Day**: Wednesday  
- **Top Item**: Salads  
- **Least Sold Item**: Cookies  
- **Coffee Sales**: Only ~9% of total sales

---

## Reflections

- One of the biggest challenges was deciding whether incomplete records should be dropped or if we should invest more time in recovering missing values.
- Initial data cleaning took multiple passes. At first, we wanted to delete rows with blanks, but realized we could infer some values:
  - If `Total Spent` and `Quantity` were present, we calculated `Price Per Unit`.
  - If `Quantity` and `Price Per Unit` were available, we calculated `Total Spent`.
  - For some rows, we inferred the `Item` type based on unique pricing. For example, if an item was priced at `$1.50`, we could assume it was **Tea**.
  - For non-unique prices, we left the `Item` as `'BLANK'` to avoid incorrect assumptions.

- **Next Steps**:  
  We'd like to explore trends in **Payment Methods** to see if certain methods correlate with higher sales. This could help optimize the checkout process and improve customer experience.

---

## Takeaways & Recommendations 
Weekday Promotions to Drive Sales

- **10% Off Coffee or Tea (Monday–Thursday)**
  - Incentivize visits on slower weekdays
  - Boost sales during morning and afternoon hours

- **Salad Combo Bundles**
  - **Salad + Juice**: Save $1.50 when purchased together
  - **Salad + Sandwich**: Get 10% off the sandwich with any salad
  - Use strong salad sales to lift sales in other product categories

- **Cookie Promotions**
  - **Coffee + Cookie**: Buy any coffee, get a cookie for 15% off
  - **Buy 2, Get 1 Free**: Encourage higher volume purchases and increase average order value

### Suggested Weekly Structure

| Day       | Promotion                             |
|-----------|----------------------------------------|
| Monday    | 10% off Coffee or Tea                  |
| Tuesday   | Salad + Juice Combo                    |
| Wednesday | Buy 2 Cookies, Get 1 Free              |
| Thursday  | Salad + Sandwich Combo                 |
| Friday    | Coffee + Cookie for 15% off            |



## Folder Structure
```text
.
├── data/
│   ├── raw/
│         └── cafe_sales.csv
│   └── cleaned/
│        └── cleanedCafeSalesPython.csv
│        └── cleanedCafeSalesPython.xlsx
├── excel/
│   ├── analysis_workbook.xlsx
├── notebooks/
│   ├── main.ipynb
└── slides/
│   └── final_presentation.pptx
└── README.md
