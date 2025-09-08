# Employee Attrition Analysis – Power BI Dashboard  

## Executive Summary  

### Overview of Findings  
This project provides an in-depth analysis of **employee attrition** at a technology company.  
The goal was to identify the **key drivers of turnover** and create a dashboard that HR leaders can use to monitor, predict, and reduce attrition.  

Attrition is one of the most critical HR metrics because replacing employees is expensive and disruptive.  
This analysis explores how **demographics, job roles, tenure, and compensation** affect attrition.  

The interactive Power BI dashboard enables HR to:  
- Monitor **KPIs** like attrition rate, employee count, average tenure, and average salary.  
- Drill down by demographics, job role, and department.  
- Identify high-risk groups to design targeted retention strategies.  

Below is the overview page from the dashboard. The full interactive version can be downloaded/viewed [here](https://your-link.com).  

---

## Dashboard Screenshot  

<img width="1710" height="1107" alt="Screenshot 2025-09-08 at 10 31 03 AM" src="https://github.com/user-attachments/assets/f7f67c89-ccef-4a5f-b957-d3281228adb3" />



---

## Key Performance Indicators (KPIs)  

The dashboard highlights the following HR-focused KPIs:


- **Employee Count** – Total number of employees in the dataset.  
- **Attrition Count** – Total number of employees who left the company.  
- **Overall Attrition Rate (%)** – Percentage of employees who left, calculated as `(Attrition Count / Employee Count) * 100`.  
- **Average Age** – Mean age of employees.  
- **Average Tenure (Years)** – Average length of service across employees.  
- **Average Monthly Income ($)** – Mean salary across employees.  



<img width="743" height="79" alt="Screenshot 2025-09-08 at 10 33 41 AM" src="https://github.com/user-attachments/assets/eeabc704-1888-4b27-a967-ede64a2baa1a" />






These KPIs serve as benchmarks for HR leaders to measure retention and identify problem areas.  

---

## Key Areas of Analysis  

### 1. Attrition Overview  
- Overall attrition rate across the company.  
- Comparison of attrition vs. retention.  
- Total active employees and leavers.  

### 2. Demographics  
- Younger employees (<35) had nearly **2x the attrition rate** compared to older employees.  
- Employees with only a **Bachelor’s degree** showed higher attrition compared to those with advanced degrees.  
- Gender differences in attrition were minimal, but trends emerged within specific roles.

<img width="344" height="197" alt="Screenshot 2025-09-08 at 10 39 21 AM" src="https://github.com/user-attachments/assets/37db3061-93b8-451d-9858-33a04eb7d1ed" />

 <img width="282" height="162" alt="Screenshot 2025-09-08 at 10 41 39 AM" src="https://github.com/user-attachments/assets/2f4676e4-c60c-4aab-a249-9b0ba20d18ec" />



### 3. Job Roles & Departments  

- **Sales Representatives** experienced the **highest attrition rate**.  
- **Human Resources** also showed above-average turnover.  
- Technical roles (e.g., R&D, IT) had lower attrition, suggesting job specialization may increase retention.  

### 4. Tenure & Experience  
- Employees in their **first 2–3 years** were most likely to leave.  
- **Long-tenured employees (>10 years)** showed extremely low attrition.  
- This highlights the importance of investing in early career development and mentorship.  

### 5. Compensation & Income  
- Employees in **lower salary brackets** were far more likely to leave.  
- Middle salary ranges had the **highest retention**.  
- Very high earners occasionally showed attrition, potentially linked to external opportunities.  

---

## Data Structure & Preparation  

The dataset used was the **IBM HR Analytics Employee Attrition Dataset**, containing over **1,470 employee records**.  

### Key Fields  
- **EmployeeID** – Unique identifier for each employee  
- **Age, Gender, Education** – Demographic attributes  
- **JobRole, Department, Salary** – Professional attributes  
- **YearsAtCompany, YearsInCurrentRole** – Tenure details  
- **Attrition (Yes/No)** – Target variable  

### Data Preparation Steps  
- **Power Query** was used for data cleaning and transformation (removing nulls, formatting columns).  
- **DAX** was used to create calculated measures, including:  
  ```DAX
  Attrition Rate = 
  DIVIDE(
      CALCULATE(COUNTROWS(Employees), Employees[Attrition] = "Yes"),
      COUNTROWS(Employees),
      0
  )

  ---

## Executive Insights  

1. **Early Career Risk**  
   - Employees with less than 3 years of tenure are the most vulnerable to attrition.  
   - Highlights the importance of targeted retention strategies during the early stages of employment.  

2. **Role-Specific Turnover**  
   - Sales Representatives and Human Resources staff experience the highest turnover rates.  
   - These functions require tailored retention initiatives to address unique challenges.  

3. **Demographic Factors**  
   - Younger employees and those with lower education levels are more likely to leave.  
   - Suggests that career development opportunities may reduce attrition within these groups.  

4. **Compensation**  
   - Salary is strongly correlated with retention.  
   - Employees in lower income brackets are significantly more likely to leave compared to mid- and high-level earners.  

---

## Recommendations  

- **Onboarding & Mentorship**  
  Strengthen onboarding programs and provide structured career development support during the first 3 years of employment.  

- **Compensation Review**  
  Reevaluate salary bands and incentive structures, particularly for entry-level and sales employees.  

- **Career Growth Opportunities**  
  Establish clearer advancement paths for employees with Bachelor’s degrees to reduce risk of turnover.  

- **Work-Life Balance Programs**  
  Expand flexible work options and well-being initiatives, especially targeting younger employees who report higher attrition.  

---

## Assumptions & Caveats  

- The dataset is based on IBM’s publicly available **HR Analytics Attrition dataset** and may not fully reflect a real company.  
- Some variables (e.g., work-life balance) are **self-reported**, making them subjective and potentially biased.  
- External factors not included in the dataset (e.g., manager style, geographic job market conditions) may also influence attrition.  

---

