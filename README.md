# -PALMORIA-GROUP-HR-ANALYTICS---Power-BI-Case-Study
‎This repository documents an end-to-end HR data analysis and dashboard project for the Palmoria Group, a Nigerian-based manufacturing company, aimed at uncovering and addressing gender-related issues in the organization using *Power BI*.
‎## Project Objective
‎Palmoria Group faced public scrutiny over gender inequality. The CEO commissioned a data-driven HR analysis to:
‎- Identify gender distribution issues
‎- Analyze salary disparities
‎- Check compliance with labor regulations
‎- Allocate annual performance bonuses
‎
‎## Datasets Used
‎1. Palmoria Group emp-data.csv  
‎   Employee-level dataset containing information on:
‎   - Gender
‎   - Department
‎   - Region
‎   - Performance Rating
‎   - Salary
‎2. Palmoria Group Bonus Rules.xlsx  
‎   A matrix of bonus rates by department and performance rating.
‎
‎## Project Steps
‎
‎### 1. Data Cleaning (Power Query)
‎- Removed:
‎  - Ex-employees with null salaries
‎  - Records with null departments
‎- Assigned "Undisclosed" to missing gender values
‎- Trimmed and formatted department/rating text fields
‎- Created a BonusKey column by merging Department and Rating
‎
‎### 2. Bonus Rules Transformation
‎- Unpivoted department columns to rows
‎- Normalized into:
‎- Created a BonusKey column to match employee data
‎
‎### 3. Data Modeling (Power BI Model View)
‎- Established a *one-to-many* relationship between:
‎### 4. DAX Measures
‎DAX
‎Bonus Amount = RELATED('Bonus Rules'[Bonus Rate]) * 'Employee'[Salary]
‎Total Compensation = 'Employee'[Salary] + 'Employee'[Bonus Amount]
‎
‎## 5. Visuals & Insights
‎### Key Insights Delivered
‎- *Gender Distribution* by Region and Department
‎- *Performance Rating Analysis* by Gender
‎- *Salary Analysis* and Gender Pay Gap Detection
‎- *Regulatory Compliance* with the $90,000 salary threshold
‎- *Bonus Distribution* by Region and Employee Level
‎## How to Use
‎1. Clone or download this repository
‎2. Open the project in *Power BI Desktop*
‎3. Load:
‎   - Palmoria Group emp-data.csv
‎   - Palmoria Group Bonus Rules.xlsx
‎4. Use *Power Query* to clean, merge, and transform the data
‎5. Create relationships using BonusKey
‎6. Apply the DAX measures provided
‎7. Explore the pre-built visuals or create your own based on insights
‎
‎## Result
‎The Power BI dashboard enabled Palmoria Group to:
‎- Visualize disparities in gender and pay
‎- Identify non-compliant regions based on salary thresholds
‎- Automate and validate bonus allocation by department and rating
‎- Deliver a transparent, data-driven HR strategy to stakeholders
‎
‎## Tools & Skills
‎- *Power BI Desktop* for visual analytics
‎- *Power Query* for data cleaning and transformation (ETL)
‎- *DAX* for custom metrics and calculations
‎- *Data Modeling* to structure relationships and KPIs
‎- *HR Analytics* to derive actionable insights from employee data

Author: Daniel Grace Mercy 

‎
