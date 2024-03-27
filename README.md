Introduction

This project comes from a talent sourcing company that finds talentend individuals to suit technology roles.  An understanding of the roles in technology are required to identify the right talent for the job.  In this project, data was sourced in a tabulated format as outlined in the data description to develop a pipeline of code to rank candidates based on how well they fit the role given search criteria in compared to the data of candidates present.  Everytime a candidate is starred, the candidate is removed from the table and the ranks are re-calculated.  Finally, a robust machine learning LLM model was created to rank candidates from the given table of data based on the input of their job title.

Data Description:

The data is tabulated with mixed data types containing 104 rows with 4 columns and 1 target variable column:

id : unique identifier for candidate (numeric)
job_title : job title for candidate (text)
location : geographical location for candidate (text)
connections: number of connections candidate has, 500+ means over 500 (text)

Output (desired target):
fit - how fit the candidate is for the role? (numeric, probability between 0-1)

Structure:
1. The data was read and a small example of cosine simmiliarity was carried out to understand the nature of cosine simmilarity in application to the project.
2. I introduced a simmilar formula; fraction of words which derives from cosine simmilarity.
3. The connections column was cleaned and considered in calculating the fitness column with a result of a pipeline of code taking into account job title and number of connections.
4. An LLM model was created using the job title only in calculating the fitness score.
5. The error of the model was measured by using the mean squared error test.

Conclusion:

The LLM model created used the job title only and works pretty effectively for this dataset.  One possible improvement to the project is to create an LLM model that takes into account both text and numerical data as in the job title and the number of connections.
