Intro to Structured Queries

Report on SQL Data Analysis of Alzheimer’s Disease Dataset

1. Dataset Selection

I selected a dataset focused on Alzheimer's disease, containing information on patient demographics, treatment types, cognitive function scores, and lifestyle factors. My interest in this dataset stems from a desire to better understand patterns and potential correlations associated with Alzheimer’s disease, specifically how it varies across demographics and responds to different treatments. Given the increasing global impact of Alzheimer’s, examining these factors could contribute valuable insights for the medical community.

2. Research Questions

To explore the dataset, I formulated three key questions:   
- Distribution Analysis: How is Alzheimer’s distributed across various age groups and regions?
- Treatment Effectiveness: What correlation exists between different types of treatments and improvements in cognitive function scores?
- Lifestyle Impact: Is there a noticeable pattern between patients’ lifestyle habits or genetic predispositions and the frequency of Alzheimer’s diagnoses?

3. SQL Query Development

To address these questions, I wrote specific SQL queries, outlined below, which allowed me to draw insights from the dataset. The dataset includes multiple tables, so I focused on using two tables: `patient_data` for demographic and lifestyle information, and `treatment_outcomes` for treatment effectiveness data.
   
   - Query for Distribution Analysis (Question 1)

      SELECT age_group, region, COUNT() AS case_count 

      FROM patient_data

      WHERE diagnosis = 'Alzheimer’s'

      GROUP BY age_group, region;

This query helped me determine the spread of Alzheimer’s across different age groups and regions. By grouping and counting cases by `age_group` and `region`, I could identify patterns in distribution.
   
   - Query for Treatment Effectiveness (Question 2):

      SELECT treatment_type, AVG(cognitive_score_improvement) AS avg_improvement 

      FROM treatment_outcomes

      WHERE diagnosis = 'Alzheimer’s'

      GROUP BY treatment_type;

This query calculates the average cognitive score improvement for each treatment type. By analyzing the averages, I can compare treatment outcomes and assess if specific treatments show a higher efficacy in managing Alzheimer’s symptoms.
   
   - Query for Lifestyle Impact (Question 3):

      SELECT lifestyle, COUNT() AS cases 

      FROM patient_data

      WHERE diagnosis = 'Alzheimer’s'

      GROUP BY lifestyle;

This query enabled me to examine the relationship between lifestyle factors and Alzheimer’s diagnosis frequency. By grouping data by lifestyle habits, I sought to understand whether certain habits were more prevalent among diagnosed patients.

4. Insights Gained

From my analysis, I observed several trends:
- Age and Region Distribution: The majority of Alzheimer’s cases appeared in older age groups, with some regions showing slightly higher concentrations. This confirmed the expected demographic patterns for Alzheimer’s and highlighted specific areas with higher case density.
- Treatment Effectiveness: Certain treatment types correlated with greater cognitive improvement, suggesting their relative effectiveness. This insight could guide further investigation into best practices for Alzheimer’s care.
- Lifestyle Factors: Patients with certain lifestyle habits exhibited higher diagnosis rates, indicating a potential influence of lifestyle on disease prevalence. This finding supports further exploration into preventive strategies linked to lifestyle changes.


