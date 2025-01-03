Download a dataset with issues from platforms like Kaggle or Google Dataset. Search, clean the data, and document the steps you took to resolve the anomalies.
1. Duplicate Entries (Email and Name Fields):
   - Issue Identified: The dataset contains multiple fields representing the email addresses and names of the participants. For example, the `Email Address` and `Email Address.1` columns appear to represent similar data. 
   - Resolution: I verified the content in both fields to check for discrepancies, removed redundant columns, and retained the accurate email information.
2. Inconsistent Casing in Text Fields (Institution/University, Department/Field):
   - Issue Identified: Some text fields such as `Institution/University` and `Department/Field` had inconsistent capitalization (e.g., "FUTA" and "futa").
   - Resolution: I applied text standardization to ensure uniform casing, converting all the entries to sentence case (first letter uppercase, rest lowercase).
3. Missing Data in Open-Ended Responses:
   - Issue Identified: The `Why would you like to participate in this workshop?` and `How do you plan to use the lessons from the workshop?` columns contained vague, incomplete, or irrelevant entries (e.g., "ggh", "j"). There were also missing values in some cases.
   - Resolution: I flagged rows with non-informative responses (like random letters) and considered them as missing data. If necessary, these entries were either filled based on available information or marked as missing.
4. Missing Values in Questions Column:
   - Issue Identified: Some participants did not provide specific questions for facilitators in the `Do you have any specific questions or topics you would like the facilitators to address?` column.
   - Resolution: I ensured that missing values in this column were filled with "None" where applicable or left blank if no data was provided.
5. Inconsistent Spelling (Position and Department):
   - Issue Identified: The `Position` field had misspellings or inconsistent entries, such as "Undergraguate" instead of "Undergraduate."
   - Resolution: I corrected spelling errors and ensured uniformity in the `Position` and `Department/Field` columns.
6. Removing Unnecessary Spaces:
   - Issue Identified: Some entries had extra spaces at the beginning or end of the text (e.g., extra spaces in `Institution/University` or `Department/Field`).
   - Resolution: I used Excel’s `TRIM` function to remove unnecessary spaces, ensuring a cleaner presentation of the data.
7. Categorical Data Cleaning:
   - Issue Identified: The responses in some columns (e.g., `Are you a member of the SCIENCOON Club?`) were limited to two or three categories (Yes/No). There were no major inconsistencies, but they were reviewed for accuracy.
   - Resolution: I ensured consistency in these fields by verifying that the responses were limited to the valid options.
