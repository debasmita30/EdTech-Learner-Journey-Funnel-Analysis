# EdTech-Learner-Journey-Funnel-Analysis
Project Overview
This project presents an end-to-end Business Intelligence analysis of the online learner journey, from initial course discovery to final enrollment. The goal is to model and understand prospective student behavior, identify critical drop-off points in the enrollment funnel, and provide data-driven recommendations to improve conversion rates for RiseUpp.com.

The core of this project is an interactive dashboard built in Microsoft Power BI that visualizes the learner drop-off rate at each stage and calculates key enrollment metrics.

Live Dashboard: [Link to your published Power BI Dashboard] <- Make sure to update this link!

Business Objectives
Aligned with RiseUpp's mission, this dashboard was designed to help marketing and admissions teams answer critical questions:

Funnel Performance: What is the overall conversion rate from a learner viewing a course to successfully enrolling?

Drop-off Points: At which stage (Course View -> Added to Cart/Interest -> Enrollment) do we lose the most prospective students?

Learner Engagement: How many unique learners are engaging at each step of the journey?

Actionable Insights: How can we refine our marketing strategies and platform experience to increase course enrollments?

Data Source & Analogy
This analysis uses the RetailRocket Recommender System Dataset as a powerful proxy to model the online learner journey. The behavioral events in the dataset are directly analogous to the steps a student takes on an EdTech platform:

Dataset: E-commerce Dataset by RetailRocket

Methodology: E-commerce events were mapped to the EdTech journey:

view -> Course Page View

addtocart -> Expressed Interest / Saved Course

transaction -> Successful Enrollment

This approach demonstrates the ability to apply analytical frameworks to different business domains.

Tools & Technologies
Business Intelligence Tool: Microsoft Power BI

Data Transformation (ETL): Power Query

Data Modeling & Calculations: DAX (Data Analysis Expressions)

Methodology
1. Data Transformation (ETL)
The raw events.csv file was loaded into Power Query for cleaning and preparation. Key steps included:

Timestamp Conversion: Converted the Unix timestamp into a standard DateTime format for time-series analysis.

Data Type Correction: Ensured all columns, especially visitorid (mapped to learner ID), were set to the correct data types.

2. Data Modeling & DAX
A logical data model was created to support the analysis.

Funnel Order Table: A calculated table was created to enforce the correct sorting of the funnel stages (Course View -> Expressed Interest -> Enrollment).

DAX Measures: Key performance indicators were calculated using DAX to measure learner behavior accurately.

Code snippet

// Calculates the number of unique prospective learners
Distinct Learners = DISTINCTCOUNT(events[visitorid])

// Calculates the conversion rate from viewing a course to showing interest
View to Interest % = DIVIDE([Interested Learners], [Viewing Learners])

// Calculates the overall enrollment rate from initial view
Overall Enrollment Rate = DIVIDE([Enrolled Learners], [Viewing Learners])
3. Visualization
An interactive dashboard was built in Power BI to present findings in an intuitive format.

Funnel Chart: The central visual, clearly showing the number of unique learners and the drop-off percentage between stages.

KPI Cards: High-level metrics such as Total Prospective Learners, Overall Enrollment Rate, and Total Enrollments are displayed for an at-a-glance performance overview.

Dashboard Preview
A snapshot of the main dashboard, showcasing the learner enrollment funnel and key conversion metrics.

Key Insights & Recommendations
This analysis yielded several actionable insights relevant to the EdTech space:

Insight 1: Major Drop-off After Course Discovery: The analysis reveals that the most significant drop-off occurs between learners viewing a course and showing active interest (e.g., saving it or adding to a cart).

Recommendation: Enhance course landing pages with more engaging content like student testimonials, career outcome statistics, and detailed syllabus previews. Implement a "Compare Courses" feature to help learners make more informed decisions.

Insight 2: High Intent from Interested Learners: Learners who save a course or add it to their cart have a much higher probability of enrolling. This is a high-intent audience segment.

Recommendation: Develop targeted email nurturing campaigns for learners who show interest but don't enroll immediately. Offer them webinars with faculty, application deadline reminders, or information on similar courses to keep them engaged and guide them toward enrollment.

How to View the Project
Live Dashboard: The interactive Power BI report can be accessed here: [Your Public Power BI Link]

Source File: The Power BI .pbix file containing all data transformations, DAX measures, and visualizations is included in this repository.

Data: The original dataset can be downloaded from the Kaggle link provided above.
