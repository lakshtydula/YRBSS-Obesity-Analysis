1.Overview
-

This project analyzes the relationship between key health behaviors and obesity among U.S. high school students using data from the Youth Risk Behavior Surveillance System (YRBSS) from 2001–2023.
The primary objective is to identify which behaviors sugary drink intake, physical activity, and nutrition habits are most strongly associated with obesity.

2.Research Question
-

What behavioral factors, such as physical activity levels, nutrition habits, and sugary drink intake, are most strongly associated with obesity among U.S. high school students according to the YRBSS?

3.Data Source
-

Dataset: YRBSS – Nutrition, Physical Activity, and Obesity Indicators        
Years included: 2001–2023        
Source: Centers for Disease Control and Prevention (CDC)          
File Used: YRBSS_cleaned_dataset.csv

The YRBSS collects state-level estimates of youth health behaviors, including:       
Obesity prevalence        
Physical activity          
Sugary drink (soda) consumption            
Fruit and vegetable intake

Note: Some behaviors (e.g., physical activity, sugary drink intake) were not included in early years. Obesity and fruit/vegetable indicators appear in all years.

4.Data Cleaning & Preparation
-

The cleaned dataset includes:

-Removal of rows without numeric data_value       
-Extraction of specific behavioral indicators using keyword matching in the question field        
-Aggregation of values to the state-year level


5.Analysis 
-

The analysis followed a step-by-step approach to determine how different health behaviors relate to obesity among high school students. The full dataset covered the years 2001–2023, and the analysis focused on the following behaviors:

-Physical Activity (e.g., being active for at least 60 minutes per day)             
-Sugary Drink Intake (soda and other sugar-sweetened beverages)

Nutrition Habits

-Insufficient fruit intake: eating fruit less than once daily            
-Insufficient vegetable intake: eating vegetables less than once daily

5.Data Extraction
-

Each behavior and the obesity measure were pulled from the dataset by matching keywords in the survey question text.
For example:            
Questions mentioning “obese” or “obesity” → obesity measure              
Questions mentioning “drank soda” or “sugar-sweetened beverage” → sugary drink intake              
Questions stating “fruit less than 1 time daily” → insufficient fruit intake     
Questions stating “vegetable less than 1 time daily” → insufficient vegetable intake           
These values were then averaged at the state-year level, giving one value per state per year for each behavior.

-> Merging the Indicators

All extracted behavior indicators were combined into a single table called analysis_df, containing:

State           
Year           
Obesity percentage               
Soda intake percentage                
Physical activity percentage                 
Insufficient fruit intake percentage                 
Insufficient vegetable intake percentage

This created a unified dataset where each row represented one state in one survey year, with all relevant behaviors.

-> Creating Behavior Categories:

To make comparisons easier, each behavior was divided into Low, Medium, or High groups.

Examples:

Physical Activity        
Low PA → lowest activity levels                         
High PA → most active states

Sugary Drink Intake     
Low Soda → lowest soda consumption    
Medium Soda → medium soda consumption          
High Soda → highest soda consumption

Nutrition Habits
These measure insufficient intake, not healthy intake              
Low Poor Intake → better eating habits   
Medium Poor Intake → medium eating habits       
High Poor Intake → worst habits (rarely eating fruit/vegetables)             
These categories allow us to easily compare groups with different behavior patterns.

6.Visualization
-

Several charts were created to visually compare obesity across the different behavior categories:

-Bar chart: Obesity vs Physical Activity    
Shows how obesity changes across Low, Medium, and High activity levels.

-Bar & line charts: Obesity vs Sugary Drink Intake                   
Shows the relationship between soda consumption and obesity.

-Bar charts: Obesity vs Insufficient Fruit/Vegetable Intake             
Highlights how poor nutrition relates to obesity.


7.Interpretation
-

Patterns from the visualizations were used to determine:

-Which behavior showed the strongest relationship with obesity               
-Whether the relationship was positive (increasing obesity) or negative (decreasing obesity)            
-How strong the effect was compared to other behaviors

This allowed us to answer the research question clearly and based on evidence from the visualizations.

8.Key Findings
-

-Sugary drink intake is the strongest behavioral predictor of obesity.
Obesity prevalence rises sharply among states with higher sugary drink consumption.

-Physical activity shows a moderate inverse relationship.
States with higher physical activity levels exhibit lower obesity rates.

-Insufficient fruit and vegetable intake show weaker associations.
States with more students consuming fruit/vegetables less than once daily have moderately higher obesity levels.


9.Conclusion
-

Across the 2001–2023 YRBSS dataset, sugary drink consumption is most strongly linked to obesity, followed by physical activity.
Poor nutrition habits also contribute to obesity but to a lesser extent.

These findings highlight the importance of public health interventions that:
Reduce sugary drink consumption
Encourage regular physical activity
Promote increased fruit and vegetable intake