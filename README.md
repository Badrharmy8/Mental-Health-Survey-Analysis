# Mental Health Survey Analysis

## 📌 Project Overview
This project explores mental health among working individuals across different industries and regions.  
The goal is to analyze factors affecting employees’ mental health and identify patterns or issues that could help organizations improve workplace environments and provide better mental health support.  

This analysis is focused on **Exploratory Data Analysis (EDA)**, highlighting initial insights and trends in the dataset. A deeper analysis can be performed in the next stage.

---

## 📌 Dataset Overview
- **Rows:** 3,157  
- **Columns:** 14  

The dataset contains demographic, work-related, and health information for employees. Key columns include:  
- Age, Gender, Region, Industry, Job Role  
- Work Arrangement, Hours per Week, Salary Range  
- Mental Health Status, Burnout Level, Work-Life Balance Score  
- Physical Health Issues, Social Isolation Score

---

## 📌 Data Quality Issues
- **Missing Values:**  
  - `Mental_Health_Status`: 25% → filled with `"Prefer not to say"`  
  - `Physical_Health_Issues`: 9% → interpreted as no physical health issues
- **Duplicates:** None  
- **Data Types:** `Survey_Date` converted from object to `datetime`  

---

## 📌 Data Cleaning & Preprocessing
1. **Survey Date:** Converted to `datetime` format.  
2. **Categorical Encoding:** Converted object columns to category type for memory efficiency.  
3. **Mental Health Status:** Missing values filled with `"Prefer Not To Say"`.  
4. **Physical Health Issues:** Split into separate binary columns:  
   - `Back_Pain`, `Shoulder_Pain`, `Neck_Pain`, `Eye_Strain`, `Wrist_Pain`  
   - Additional column `Physical_Health_Missing` tracks missing values.

---

## 📌 Mental Health Status - Initial Insights (EDA)

### Overview
- Categories: `Stress Disorder`, `ADHD`, `Burnout`, `Anxiety`, `PTSD`, `Depression`  
- Null values: 25% → `"Prefer not to say"`  

### 1. Gender
- Female & Male: 10–15% across categories  
- Non-binary: ADHD & Stress Disorder lowest (~6%), others >10%  
- Prefer not to say: Anxiety & PTSD ~6%, others ≥10%  

### 2. Region
- Percentages vary per region: lowest ~9%, highest <15%  

### 3. Work Arrangement
- Categories: Outside, Hybrid, Remote  
- Slight variation across arrangements  

### 4. Burnout Level
- High, Medium, Low → low variation  
- Low: Stress Disorder ~10%, ADHD highest ~15%  

### 5. Salary Range
- 100-120k: Depression lowest ~9%, Anxiety highest ~15%  
- +120k: Burnout lowest ~8%, Anxiety highest ~15%  
- Other ranges similar  

### 6. Age
- Values increase above 20, decrease approaching 70  

### 7. Hours per Week
- Values increase above 30, decrease approaching 70  

### 8. Social Isolation Score
- Scores 2 & 3 → highest impact on Stress Disorder, ADHD, Burnout, Anxiety  
- Scores 1, 4, 5 → lower impact  

### 9. Work Life Balance Score
- Score 3 → highest impact  

### Summary
- Clear patterns observed for Social Isolation Score, Work Life Balance Score, certain Salary Ranges  
- "Prefer not to say" and Non-binary categories show slightly different distributions  
- Deep analysis will provide more detailed understanding of relationships with Mental Health Status

---

## 📌 Next Steps
- Perform **Deep Analysis** for numeric and categorical variables  
- Explore relationships between **Mental Health Status and Physical Health Issues**  
- Statistical tests and advanced visualizations for more robust insights  


