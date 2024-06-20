# Lung-Cancer-Dashboard

## Overview
This Power BI dashboard provides a comprehensive visualization of a lung cancer dataset. The dashboard is designed to give insights into the distribution and characteristics of lung cancer cases based on various factors such as gender, age, smoking habits, alcohol consumption, and symptoms.

## Data Source
The dataset used for this dashboard was obtained from Kaggle and includes various attributes related to lung cancer cases. The columns in the dataset are as follows:

GENDER: Gender of the individual (Male, Female)
AGE: Age of the individual
SMOKING: Number of individuals who smoke
YELLOW_FINGERS: Number of individuals with yellow fingers
ANXIETY: Number of individuals with anxiety
PEER_PRESSURE: Number of individuals experiencing peer pressure
CHRONIC_DISEASE: Number of individuals with chronic diseases
FATIGUE: Number of individuals with fatigue
ALLERGY: Number of individuals with allergies
WHEEZING: Number of individuals wheezing
ALCOHOL_CONSUMING: Number of individuals consuming alcohol
COUGHING: Number of individuals coughing
SHORTNESS_OF_BREATH: Number of individuals with shortness of breath
SWALLOWING_DIFFICULTY: Number of individuals with difficulty swallowing
CHEST_PAIN: Number of individuals with chest pain
LUNG_CANCER: Indicator of lung cancer (positive/negative)
### Dashboard Components
 #### Cards
Number of Males: Displays the total number of male individuals in the dataset.
Number of Females: Displays the total number of female individuals in the dataset.
Sum of Smoking: Displays the total number of individuals who smoke.
Total Alcohol Consumers: Displays the total number of individuals who consume alcohol.
#### Bar Charts
Positive Cases by Age Group (≤ 49): A bar chart showing the total number of positive lung cancer cases for individuals aged 49 and below.
Positive Cases by Age Group (> 49): A bar chart showing the total number of positive lung cancer cases for individuals aged above 49.
Negative Cases by Age Group (≤ 49): A bar chart showing the total number of negative lung cancer cases for individuals aged 49 and below.
Negative Cases by Age Group (> 49): A bar chart showing the total number of negative lung cancer cases for individuals aged above 49.
#### Donut Chart
Symptoms of Lung Cancer: A donut chart illustrating the prevalence of various lung cancer symptoms including chest pain, shortness of breath, coughing, and fatigue.
### How to Use the Dashboard
Filtering and Interactivity: The dashboard includes interactive features allowing users to filter and explore the data based on various criteria such as gender, age, smoking habits, and more.
Insights: Users can gain insights into the distribution of lung cancer cases, identify patterns and correlations between different factors, and understand the prevalence of symptoms among the affected individuals.
## Technical Details
Power BI Features Used
Cards: For displaying key metrics and totals.
Bar Charts: For visualizing the distribution of positive and negative lung cancer cases across different age groups.
Donut Chart: For illustrating the prevalence of symptoms among lung cancer cases.
 ## DAX Calculations
Measure for Male and Female Counts:
DAX
Copy code
MaleCount = CALCULATE(COUNT('TableName'[GENDER]), 'TableName'[GENDER] = "Male")
FemaleCount = CALCULATE(COUNT('TableName'[GENDER]), 'TableName'[GENDER] = "Female")
Sum of Smoking:
DAX
Copy code
SumSmoking = SUM('TableName'[SMOKING])
Total Alcohol Consumers:
DAX
Copy code
TotalAlcoholConsumers = SUM('TableName'[ALCOHOL_CONSUMING])
Data Preparation
The dataset was cleaned and preprocessed to ensure accuracy and consistency.
Gender values were standardized to "Male" and "Female".
