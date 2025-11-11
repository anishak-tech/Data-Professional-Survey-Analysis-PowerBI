# **Data Professional Survey Analysis**

This project details the process and outcomes of a guided Power BI project focused on transforming and visualizing real-world survey data collected from data professionals. It covers the complete Power BI workflow—from data cleaning to creating interactive dashboards.

---

## **Project Objectives and Data Source**

The main objective of this project was to practice the full Power BI workflow: transforming raw data using Power Query, creating visualizations, building interactive dashboards, and applying a custom theme and color scheme.

**Data Source:**
The dataset is based on real survey data collected from data professionals through platforms such as LinkedIn and Twitter. Around **600–700 responses** were recorded. The dataset was available as a raw CSV file and included both professional and demographic information.

**Raw Data Overview:**
The dataset included:

* **Job Title:** Contained pre-defined options and open-text entries, resulting in many variations.
* **Current Yearly Salary:** Entered as ranges (e.g., 106–125K) that required transformation.
* **Industry**
* **Favorite Programming Language:** Included multiple selections and free-text entries.
* **Happiness Scores (0–10 scale):** Ratings for salary, work-life balance, management, coworkers, and learning opportunities.
* **Difficulty to Break into Data:** Ranked from very difficult to very easy.
* **Demographics:** Gender, age range, and country of residence.

---

## **Data Transformation and Cleaning (Power Query)**

The raw data contained inconsistencies and formatting issues, especially in text and salary fields. The transformations performed in Power Query focused on standardizing the data for analysis.

### **Column Management and Standardization**

| Column                            | Transformation                                                      | Purpose                                                                                                          |
| :-------------------------------- | :------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------- |
| **Initial Cleanup**               | Removed unnecessary columns such as email, browser, and time spent. | Simplified dataset for visualization.                                                                            |
| **Job Title**                     | Split the column using “(” as a delimiter and normalized entries.   | Condensed hundreds of variations into standard roles such as Data Analyst, Data Scientist, Engineer, and others. |
| **Favorite Programming Language** | Split using “:” as a delimiter and standardized values.             | Simplified the list of languages and grouped similar ones.                                                       |
| **Industry & Country**            | Split using custom delimiters.                                      | Standardized entries for clearer reporting.                                                                      |

### **Salary Transformation**

The **Current Yearly Salary** column required conversion from text ranges to numeric values.

**Steps taken:**

1. Duplicated the salary column.
2. Split the duplicated column using digit-to-non-digit delimiters.
3. Removed special characters like “K,” “–,” and “+.”
4. Converted both split columns to Whole Number type.
5. Created a new column, **Average Salary**, using the formula:
   `(Salary_Column_1 + Salary_Column_2) / 2`
6. Converted the **Average Salary** column to **Decimal Number** for accurate aggregation.

---

## **Dashboard Design and Visualizations**

The dashboard, titled **Data Professional Survey Breakdown**, provides a high-level overview of survey insights, salary analysis, and satisfaction metrics.

### **High-Level Summary Cards**

* **Count of Survey Takers:** 630
* **Average Age of Respondents:** ~30 years

### **Key Visualizations and Insights**

| Visualization              | Description                      | Insights                                                                                                                                                     |
| :------------------------- | :------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stacked Bar Chart**      | Average Salary by Job Title      | Data Scientists reported the highest average salary (~$93,000), followed by Data Engineers and Data Architects. Data Analysts earned an average of ~$55,000. |
| **Clustered Column Chart** | Favorite Programming Languages   | Python was the most popular programming language among all roles.                                                                                            |
| **Treemap**                | Country of Survey Takers         | Salaries varied by region; Data Scientists in the U.S. earned significantly more than those in other countries.                                              |
| **Gauge 1**                | Happiness with Work-Life Balance | Average score: **5.74**, indicating moderate satisfaction.                                                                                                   |
| **Gauge 2**                | Happiness with Salary            | Average score was lower than work-life balance, showing relative dissatisfaction with compensation.                                                          |
| **Donut Chart**            | Difficulty to Break into Data    | Displayed responses ranging from “Very Difficult” to “Very Easy” using a custom color palette.                                                               |

### **Dashboard Theme**

A custom Power BI theme was applied to improve aesthetics and consistency. The color scheme was adjusted for better contrast and visual appeal.

---

## **Summary and Future Scope**

This guided Power BI project successfully demonstrated:

* The use of Power Query for transforming and cleaning survey data.
* Building effective, interactive dashboards for analyzing real-world insights.
* Visual storytelling through metrics, charts, and color themes.

**Future Improvements:**

* Apply more advanced cleaning using Excel or SQL for better standardization.
* Add DAX measures for deeper insights and trend analysis.
* Enhance interactivity by integrating filters and custom visuals.

---
