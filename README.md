# Descriptive Project Title i.e. "Cafe Financial Analysis & Insights" 

## Project Overview (1 Paragraph)
Angel and I have been hired by the owner of a popular café chain to clean and analyze their messy transaction dataset. The original dataset includes the following columns: Transaction ID, Item, Quantity, Price Per Unit, Total Spent, Payment Method, Location, and Transaction Date.

Our goal is to uncover meaningful trends within the café's sales data. Specifically, we aim to determine:

- Which item sells the best
- Which month generates the most profit
- Which day of the week is the most successful over the course of a year.
  
Our plan is to first clean the dataset, addressing any missing values as accurately as possible without introducing false information that could distort our findings. Ultimately, we hope to provide data-driven recommendations to help the café improve overall sales and performance.

[Figma Kanban Board](https://www.figma.com/board/juOigrlEdvkUQz318G1yUE/Mod1_Final-Project-Kaban-Board?node-id=0-1&t=9t959gGv1UOWJsVn-1)

## Business Questions 
- What are the peak sales months?
    - We found that sales peaked in June. As the weather gets warmer more people tend to be outside. October came in second, which also makes sense as coffee would probably sell best in colder temperatures.
- Are weekends busier than weekdays?
    - Yes weekends are buiser than weekends. Thursday experiences the most sales, followed by Friday and Sunday. We were intially surprised with the fact that Saturdays was not one of the more busier days. Upon further thought we concluded that most people typically sleep in on Saturdays after a long week of work. We were also surprised at how busy Thursdays were. We have yet to come up with a theory on this. 
    - The least busy day of the week is Wednesday. We also haven't came up with a reason as to why Wednesday are the slowest. We recommend adding discounts on the day in order to boost sales. 
- Any other findings stand out and relevant to the stakeholders?
    - We found that salads made up most of their sales on any given day. Sandwiches also made up a big portion of sales. Surprisly coffee only made up about 9% of their total sales. It is a smart buiness move on their side to diversify their menu.  Cookies' were their least sold item. 
- How reliable was the data?  What cleaning was needed?
    - We cannot speak on the reliability of the data set as we did not collect the data ourselves. We can say that about 5.7% of items were either 'UNKNOWN', 'ERROR' or Blank. Since it is not a huge portion of sales we don't think it skew our findings in any particular direction. We would love to collect more consistent data from this cafe to get an even better picture of their trends. However, this does not mean that our findinds are insignificant.

## Data Cleaning Summary 
- For all columns, we renamed anything that was "UNKNOWN". "ERROR" or empty to "BLANK". For item type only 5.7% was "BLANK" we felt it wasn't signicant enough to outright delete the entries. Instead we kept their entries and total spent. Regardless of what a customer purchased their sale was still recorded and completed. 
- In order to figure out the most sucessful months and days of the week we had to exclude about 460 records. We felt it would negatively skew our data if we used any form of imputation to fill in our "BLANK" with fake dates.

## Key Findings
- Summary stats:
    -![image](https://github.com/user-attachments/assets/6a99ed30-4a67-4ab4-ab60-3e5f255d3fdf)
 
- Peak sales month is June, followed by October and January
- The weekends are busier than the weekdays. Thursdays experience the most sales.
- Salads made up the majority of their sales monthly while cookies were the opposite.

## Reflections
- A challenge we faced was the decision making needed to choose whether or not a chunk of data was needed to be dropped or a lot more work needed for a few.
- Initial Data Cleaning proved to be a challenge. We had to go over the data set a few times in order for it to work for us. Initially we wanted to delete any record with blanks. Upon further inspection we realized we could fill in the blanks with the rest of the information. For example if we knew the 'Total Spent' and 'Quantity' then we could infer the 'Price Per Unit' by dividing the two. Similarly if we had the 'Quanity' and 'Price Per Unit' then we could find the 'Total Spent' by multiplying. We could also infer the item type by the 'Price Per Unit' for items with unique prices. For example from the data we knew that a cup of tea costs $1.50. Therefore any blank item type with a price of $1.50 could be filled in for. For items with the same price we left as 'BLANK'.
- Moving forward we would like to further explore trends in 'Payment Methods' and see if we can find a way to use that information to improve sales and make it more convinent for customers to buy from the cafe. 


## Takeaways & Recommendations 
Weekday Promotions to Drive Sales
  - 10% Off Coffee or Tea (Monday–Thursday)
  - Encourage more weekday visits
  - Boost morning and afternoon sales
  - Salad Combo Bundles
  - Salad + Juice Bundle: Save $1.50 when purchased together
  - Salad + Sandwich Bundle: Get 10% off the sandwich with any salad
  - Leverage strong salad sales to lift other categories

Cookie Promotions

  - Coffee + Cookie Deal: Buy any coffee, get a cookie for 15% off
  - Buy 2 Get 1 Free on Cookies: Increases order value and moves more product
    
Suggested Weekly Structure

  - Monday: 10% off Coffee or Tea
  - Tuesday: Salad + Juice Combo
  - Wednesday: Buy 2 Cookies, Get 1 Free
  - Thursday: Salad + Sandwich Combo
  - Friday: Coffee + Cookie for 15% off


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
