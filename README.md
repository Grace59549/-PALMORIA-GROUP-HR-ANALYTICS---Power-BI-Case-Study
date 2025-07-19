# PALMORIA GROUP HR ANALYTICS – Power BI Case Study  

> **Uncovering Gender Inequality, Salary Disparities & Bonus Allocation with Data-Driven HR Analytics**  


## 🎯 Project Objective  

Palmoria Group, a Nigerian manufacturing company, faced public scrutiny over **gender inequality**.  
The CEO commissioned a **data-driven HR analysis** to:  

✅ Identify gender distribution issues  
✅ Analyze salary disparities and detect gender pay gaps  
✅ Check compliance with labor regulations  
✅ Automate and validate annual performance bonus allocation  



## 📂 Datasets Used  

1. **Palmoria Group emp-data.csv**  
   Contains employee-level data, including:  
   - Gender  
   - Department  
   - Region  
   - Performance Rating  
   - Salary  

2. **Palmoria Group Bonus Rules.xlsx**  
   A matrix of bonus rates defined by **Department** and **Performance Rating**.  



## 🛠️ Project Steps  

### 1️⃣ Data Cleaning (Power Query)  
- Removed:  
  - Ex-employees with null salaries  
  - Records with null department values  
- Assigned **"Undisclosed"** to missing gender values  
- Trimmed & standardized text fields for Department and Rating  
- Created a **BonusKey** column by merging *Department* and *Performance Rating*  

### 2️⃣ Bonus Rules Transformation  
- **Unpivoted** department columns into rows  
- Normalized the bonus rules into a clean lookup table  
- Created a **BonusKey** column to match employee data  

### 3️⃣ Data Modeling (Power BI Model View)  
- Established a **one-to-many relationship** between:  
  - Employee Data ↔ Bonus Rules  

### 4️⃣ DAX Measures  
```DAX
Bonus Amount = RELATED('Bonus Rules'[Bonus Rate]) * 'Employee'[Salary]  
Total Compensation = 'Employee'[Salary] + 'Employee'[Bonus Amount]
