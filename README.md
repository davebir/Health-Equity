# Health Equity

⚠️ Currently working on this project ⚠️

"Health equity is the state in which everyone has a fair and just opportunity to attain their highest level of health"
Centers for Disease Control and Prevention

Everyone deserves a fair and just opportunity in their health journey. 

This project aims to uncover ways hospitals are exceeding in their health equity and ways they can become better.

All data contributing to this project is the intellectual property of Synthea:
https://synthetichealth.github.io/synthea/

# Questions for this project

1. How many patients in the dataset belong to each racial or ethnic group?
2. What are the most common conditions for patients in specific age groups?
3. What percentage of patients have health insurance? How does it vary by demographics?
4. What are the differences in healthcare between urban and rural areas?
5. Which conditions are most prevalent among patients from different racial or ethnic groups?


# How many patients in the dataset belong to each racial or ethnic group?

SELECT
	race,
	ethnicity,
	COUNT(*) AS patient_count
FROM patients
GROUP BY
	race,
	ethnicity
ORDER BY patient_count DESC;

Commentary: Since race and ethnicity are in separate columns, I selected both and the count function and gave it the alias "patient_coount". This is in the "patients" table and grouped race and ethnicity. I then ordered the "patient_count" in descending order.

# What are the most common conditions for patients in specific age groups?

