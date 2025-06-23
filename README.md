# Descriptive Project Title i.e. "Cafe Financial Analysis & Insights" 

## Project Overview (1 Paragraph)
Brief summary of scenario and project goal 
[Figma Kaban Board](https://www.figma.com/board/juOigrlEdvkUQz318G1yUE/Mod1_Final-Project-Kaban-Board?node-id=0-1&t=9t959gGv1UOWJsVn-1)

## Business Questions 
- What are the peak sales months?
    - We found that sales peaked in June
- Are weekends busier than weekdays?
    - Yes weekends are buiser than weekends. Thursday experiences the most sales, followed by Friday and Sunday.
    - The least busy day of the week is Wednesday.
- Any other findings stand out and relevant to the stakeholders?
    - We found that salads made up most of their sales on any given day. Cookies' were their least sold item. </p>
- How reliable was the data?  What cleaning was needed?
    - For all columns, we renamed anything that was "UNKNOWN". "ERROR" or Blank to "BLANK"
    - In order to figure out the most sucessful months and days of the week we had to exclude about 460 records. We felt it would negatively skew our data if we used any form of imputation to fill in our "BLANK" with fake dates. </p>

## Data Cleaning Summary 
- Data type corrections made
- Missing data handling strategy
- Duplicate handling
- Any columns dropped or imputed (and why)

## Key Findings
- Summary stats (mean, median, etc.)
- Insights from trends by month/day
- Additional analysis looked at
- Any bonus feature engineering

## Reflections
- Challenges we faced
- Any biases
- What we would do differently next time

## Takeaways & Recommendations 
- What can you tell the cafe owner and why should they care 

## Folder Structure (EXAMPLE ONLY)
```text
.
├── data/
│   ├── raw/
│   └── cleaned/
├── excel/
│   ├── analysis_workbook.xlsx
│   └── cleaning_template.xlsx
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda_insights.ipynb
│   └── README.md
└── slides/
    └── final_presentation.pptx
