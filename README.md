# Air_Quality_Analysis

Project requirements : python , google collab, dataset
Libraries requirements : numpy, pandas,matplotlib,seaborn,scikit learn

Dataset details:
Location wise daily ambient air-quality tamilnadu-year 2014
It has the columns named as Stn Code, Sampling Date, State, City/Town/Village/Area, Location
of Monitoring Station, Agency, Type of Location, SO2, NO2, RSPM/PM10, PM 2.5

# Step 1:Load the dataset and  Understanding the Dataset 

Imported dataset using pandas library , by using inbuild fucntion .head() ,.tail() , .info() , .describe() we understand the datset.
for example, the .head() method is used to display the first five rows of a DataFrame.By default, it shows the first 5 rows, but you can specify the number of rows to display by passing an argument, like df.head(10) to display the first 10 rows.
It is helpful for quickly inspecting the structure and content of a DataFrame.

# step 2:Data Pre-Processing 
I drop the column PM 2.5 having full of NaN values.
Replace missing values in all rows by mean value of that row. 
And checking for duplicates , but no duplicates were found so , dataset remains the same.

# step 3: Visualization and Analysis

# Time Series Plots:
Time series plots are essential for visualizing how air quality parameters change over 
time. 

# Line charts:
Can show trends, seasonal patterns, and long-term changes in pollutant 
concentrations.

# count plots:
The countplot is used to represent the occurrence(counts) of the observation present in the categorical variable. It uses the concept of a bar chart for the visual depiction.
![image](https://github.com/TSakthikeerthika/Air_Quality_Analysis/assets/146413153/03334775-f1b5-4318-be61-1ee3981f02cc)

# Bar Charts:
Bar charts can be used to compare pollutant levels across different categories or time 
intervals. For instance, you can use bar charts to compare air quality in different cities or during 
different months.
![image](https://github.com/TSakthikeerthika/Air_Quality_Analysis/assets/146413153/6187ce2d-1b87-4f2e-ad0d-aa27090d77b4)

# Correlation matrix:
A correlation matrix is used to analyze the relationships or associations between variables in a dataset. It provides a structured way to understand how different variables are related to each other. 

# Pie-charts:
Distribution of Pollutants: Used pie-charts to show the proportion of different pollutants (e.g., SO2, NO2, RSPM/PM10) in the overall air quality data.
![image](https://github.com/TSakthikeerthika/Air_Quality_Analysis/assets/146413153/096ae108-ebda-4218-8bb8-3274febf0998)

Location-Based Analysis: Used Pie charts to show the distribution of air quality levels across different monitoring stations or locations.
![image](https://github.com/TSakthikeerthika/Air_Quality_Analysis/assets/146413153/bbaa3caa-9a17-446b-89d6-a7317df86472)

![image](https://github.com/TSakthikeerthika/Air_Quality_Analysis/assets/146413153/4ca64caf-617c-4b75-9c97-9c488adce9a9)


Comparing Locations: Pie charts to compare the air quality categories for different cities or areas within a region.

# Matplotlib and Seaborn:
For data visualization, Matplotlib and Seaborn has been employed. These 
libraries offer a wide range of plotting options, allowing us to create informative visualizations that 
depict air quality trends, pollution hotspots, and model predictions.


# step 4: Predictive model 
Scikit-Learn has been used for building the predictive model. It provides various 
machine learning algorithms, model evaluation metrics, and tools for model training and testing.
 For this I added a new column named AirQualityCategory which contains a categorical values named as 
low or Moderate or High based on the mean levels of 3 pollution’s distribution in that respective row .
 This code performs classification using a Random Forest classifier to predict air quality categories 
based on the levels of two pollutant variables, SO2 and NO2.
