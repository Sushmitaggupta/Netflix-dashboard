# Netflix Dashboard
Power BI Netflix Dashboard: Visualizes streaming trends, user engagement, and content performance, providing insights for strategic decision-making within the Netflix platform.
Abstract- The vast content of Netflix is segregated into different sections and every section is graphically analyzed to produce insights useful for the business to make data-driven decisions, keeping in mind the region, genre, type and age group of every customer. The customer data was mapped into CRM and various insights were drawn through visualizations.
Data Preparation:

Data Cleaning:
In this Power BI project, the initial phase involves meticulous data cleaning and preparation. Leveraging a random data generator like Mockaroo, we curated customer data with the assistance of Microsoft Excel and SQL Server Management Studio. PowerQuery and Microsoft Excel played pivotal roles in the data pre-processing steps:

A. Microsoft Excel:

Parsed genre data enclosed in parentheses, transforming each genre into a separate row using a delimiter.
Generated country and continent based on the country code (Figure 1: Country data cleaning).
Grouped ages in the user_details sheet into four categories (18-28, 29-39, 40-50, 51 & above) (Figure 2: Age-group data).
B. PowerQuery:

Corrected data types across all tables, converting IDs to numeric and setting movie titles to alphanumeric formats.
Converted decimal-format numbers to the nearest whole number.
Converted the "YEAR" data type into date format.
Created a "Popularity Group" column based on IMDB scores, categorizing items into "High Popularity" and "Low Popularity."
Transformed the role column into two new columns, 'Actor' and 'Director.'
Created calculative measures based on visualizations.
Addressed 16 missing values.
Netflix Data Structure:
The Netflix data comprises five main tabs (movie_detail, country, title, person_actor, user_datanetflix). The 'id' column serves as a common link between movie_detail, title, and person_actor, while person_actor acts as a central table with person_id and id.

System Design Process:

The system design phase involves defining entities and modules to meet specific requirements, considering factors such as scalability, performance, and usability.

Functional Requirements - NETFLIX- DECODING TRENDS & STRATEGIES:

Content Management: A vast library categorized by genres, popularity, and relevant criteria.
Regionalization: Handling regional data and ensuring equitable content distribution.
User Segmentation: Implementing features for user segmentation based on region, subscription plan, and age group.
Engagement Metrics: Tracking and analyzing user engagement metrics with different content pieces.
Visual Analytics: Implementing visualizations to aid in understanding content balance, user engagement, and genre popularity.
Field Checks:

Content Library Balance Rule: Ensuring a balanced distribution of content across genres.
Global Content Distribution Rule: Distributing content proportionally across different countries.
Genre Popularity and Characteristics Rule: Implementing field checks for accuracy and integrity during data processing.
Data Processing Phase - Field Checks:

Character Length Limitation: Ensuring descriptions adhere to specified character limits.
Email Field Verification: Regular expression checks for correct email format.
Subscription Validation: Ensuring non-null subscription values.
Release Year Restriction: Imposing a restriction that the "release year" attribute for movies cannot be beyond 2023.
Data Completeness Checks: Identifying and addressing missing records (16 in total).
Data Range Checks: Verifying age-group falls within specified ranges.
Unique Identifier Checks: Verifying uniqueness of fields like id and person_id.
Business Rules:

Genre Popularity Analysis Rule: Understanding genre popularity based on factors like runtime, content type, and user engagement.
Preferred Content Duration Rule: Providing insights into user preferences regarding content duration and its correlation with popularity.
User Segregation Analysis Rule: Understanding user demographics for targeted content recommendations.
Popular Director Analysis Rule: Analyzing data to identify the most watched and popular directors.
User Engagement Level Rule: Evaluating user engagement with different content pieces to enhance recommendations.
