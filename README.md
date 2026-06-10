📊 IBM HR Analytics: Attrition & Workforce Insights
A data exploration and visualization project using R

This analysis explores employee attrition and performance using the IBM HR Analytics Employee Attrition & Performance dataset (1,470 employees, 35 variables). The workflow includes data import, cleaning, transformation, sampling, and visualization using tidyverse, readxl, and here.


🔧 **1. Data Preparation & Cleaning**
You imported and structured the dataset using:

read_excel() to load the Excel file

glimpse() and str() to inspect structure

Conversion of character variables to factors

Conversion of satisfaction and involvement metrics to ordered factors, e.g.:

“mutate_at(vars(EnvironmentSatisfaction, JobInvolvement, JobSatisfaction…), factor, ordered = TRUE)”

This ensures proper statistical handling of ordinal HR metrics.


🧪 2. **Sampling for Exploration**
You created a reproducible 70% sample for exploratory analysis:

“team_work_samp <- sample_frac(team_div_work_data, size = 0.7)”

This allows efficient plotting and testing without altering the original dataset.


📈 3. **Key Workforce Insights**
Attrition
237 employees marked “Yes” → 16% attrition rate

Attrition varies across job roles, satisfaction levels, and overtime status.

Job Roles
From your count table:

“Sales Executive: 230, Research Scientist: 204, Laboratory Technician: 184…”

The workforce is concentrated in technical and customer‑facing roles.

Gender Distribution by Role
Your cross‑tabulation shows:

“Research Scientist: 83 Female, 121 Male; Sales Executive: 93 Female, 137 Male…”

This highlights gender representation patterns across functions.

Work‑Life Balance & Satisfaction
Most employees rate WorkLifeBalance as 3 or 4

Job satisfaction is widely distributed, with meaningful variation across roles


🎨 **4. Visualizations**
Your document includes several strong ggplot2 visualizations:

a. Job Role Distribution
A horizontal bar chart showing percentage of employees in each role.

b. Gender Representation by Role
A grouped bar chart showing the proportion of men and women in each job role, with percentage labels:

“geom_text(aes(label = paste0(round(pct*100, 1), ‘%’)))”

c. Relative Gender Percentages
A second visualization showing gender percentages within each job role.

These plots demonstrate your ability to communicate HR insights visually.


🧠 **5. What This Project Demonstrates**
This project showcases your ability to:

Clean and structure HR datasets

Convert raw data into meaningful factors

Perform exploratory analysis

Visualize workforce patterns

Communicate insights relevant to HR leaders and people analytics teams
