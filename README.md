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

6.Data Extraction
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
Medium PA → medium active states                           
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

How to Run the Notebook:

-Ensure the following files are in the same folder:           
YRBSS_analysis.ipynb,YRBSS_cleaned_dataset.csv         
-Open the notebook in Jupyter Notebook or VS Code.         
-Run all cells from top to bottom.

All visualizations will be displayed inside the notebook and saved as .png files in the project folder.

7.Visualization
-

Several charts were created to visually compare obesity across the different behavior categories:

-Bar chart: Obesity vs Physical Activity    
Shows how obesity changes across Low, Medium, and High activity levels.

-Bar charts: Obesity vs Sugary Drink Intake                   
Shows the relationship between soda consumption and obesity.

-Bar charts: Obesity vs Insufficient Fruit/Vegetable Intake             
Highlights how poor nutrition relates to obesity.


8.Interpretation
-

Patterns from the visualizations were used to determine:

-Which behavior showed the strongest relationship with obesity               
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



10.Relative Strength of Behavioral Associations
-
Based on the observed differences in obesity prevalence and correlation strength, the behaviors rank as follows in their contribution to obesity:

Sugary drink intake – strongest positive contributor

Physical activity – strongest protective factor (inverse relationship)

Insufficient vegetable intake – moderate contributor

Insufficient fruit intake – weakest contributor        


11.Conclusion
-

This analysis of YRBSS data from 2001–2023 demonstrates that behavioral factors contribute to obesity in unequal ways among U.S. high school students.

Sugary drink intake is the strongest behavioral predictor of obesity, with obesity prevalence increasing substantially as consumption rises.

Physical activity has a consistent protective effect, with higher activity levels associated with lower obesity prevalence.

Insufficient vegetable intake contributes meaningfully to obesity, while insufficient fruit intake shows a weaker but still positive association.

Overall,

Reducing sugary drink consumption and increasing physical activity would likely have the greatest impact on lowering adolescent obesity rates, while improving fruit and vegetable intake provides additional but smaller benefits.

These findings support public health strategies that prioritize limiting sugar-sweetened beverages and promoting physical activity, alongside broader efforts to improve dietary quality among adolescents.