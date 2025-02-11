# Aviation Accidents - Risk Analysis
**Author**: Endalkachew Dessalegne

## Overview
The company is planning to expand to the aviation industry by purchasing and operating airplanes for commercial and private enterprises. This project uses descriptive statistical analysis on aviation accident data from Kaggle to gain insight into which aircraft is with the lowest risk. It analyzes aviation accidents data to find out the potential risks of purchasing different aircrafts and recommend which aircraft to purchase. This require insight into which types of aircrafts are with the lowest risk. That is by analyzing how make and model of aircrafts, number and type of engines relate to accidents and injuries and This project can be improved by taking a dataset of accidents by highly and equally operational aircrafts in the world and finding out the ones with the lowest accident.damages caused by aircraft accidents which occurred within the United States, its territories and possessions, and in international waters. The data analysis generally shows that as the number of engines the aircraft has increases the number of accidents and injuries and damages decreases. It also shows that aircrafts with certain types of engine type are more involved in accidents than the others. This engine types includes Reciprocating engine. Moreover, some aircraft Make such as Cessna and its Models 152 and 172 are shown to be involved in accidents than others. My recommendation for which type of aircraft to purchase would be to focus on the number and type of engines of the aircrafts. To avoid aircraft-Make such as Cessna and choosing any other Make and Model should mainly focus on the type and number of engines.


## Business Problem
The company wants to expand into the aviation industry and wants to purchase aircrafts with the lowest risk in order to maximize profit. To determine this, aviation accident dataset was analyzed to find out which factors decrease the risk of aviation accidents so as to gain an insight to which type of aircraft to purchase for the company to minimize risk and maximize profit.


***

## Data

The data analyzed came from The NTSB aviation accident database from on Kaggle website. It contains information from 1962 and later about civil aviation accidents and selected incidents within the United States, its territories and possessions, and in international waters. I used one file to get an insight on how aircraft Make and Model, and number and type of engine correlates with number of accidents, fatal and serious injuries and damage to aircraft.

I read the data from the data/AviationData.csv file and store it as DataFrame aviation_df.

After checking the information on the table to see column names, number of column and rows, and checked the descriptive summary of the data non-null and null counts and data type values, I then cleaned up the data by dropping columns which are not necessary for this project and those with a large proportion of null values. Then I dealt with numerical value columns by replacing null values with the median of each column. Then I have gone through the value counts of the remaining columns to decide to replace or fill null values with the most common value of with 'Unknown' or drop the columns with the null values. For 'Make' and 'Model' column I strip and replace unnecessary characters. From the "event_date" column I extracted the year and created new column - "event_year".

## Methods

The data analyzed came from The NTSB aviation accident database from on Kaggle website. It contains information from 1962 and later about civil aviation accidents and selected incidents within the United States, its territories and possessions, and in international waters. I used one file to get an insight on how aircraft Make and Model, and number and type of engine correlates with number of accidents, fatal and serious injuries and damage to aircraft.

***
After checking the information on the table to see column names, number of column and rows, and checked the descriptive summary of the data non-null and null counts and data types values, I then cleaned up the data by dropping columns which are not necessary for this project and those with a large proportion of null values. Then I dealt with numerical value columns by replacing null values with the median of each column. Then I have gone through the value counts of the remaining columns to decide to replace or fill null values with the most common value of with 'Unknown' or drop the columns with the null values. For 'Make' and 'Model' column I strip and replace unnecessary characters. I have added a new colun of 'total_enjuries' adding up two otheer columns. From the "event_date" column I extracted the year and created new column - "event_year".
***

## Results

The first graphs shows that the number of aircraft accidents and incidents decreased significantly over the years. 
  ![img](./images/image-yearly.png)
The second graph and summary table show that aircrafts with certain types of engine type are more involved in accidents and caused more injuries and damage than the others. This engine types includes Reciprocating, Turbo shaft, Turbo Prop engines.
 ![img](./images/image-engines_type_data.png)
The third graph shows that as the number of engines the aircraft has increases the number of accidents and injuries and damages decreases. Aircrafts with one engine are involved in vast majority of the accidents registered. 
 ![img](./images/image-engines_num_data.png)
The fourth graph and summary table show that some aircraft Make such as Cessna and its Models 152 and 172 are shown to be involved in more accidents and caused more injuries and damages than the others. 
 ![img](./images/image-top_20_make_accidents.png)
Groupby analysis of Make/Engine_Type and Make/Number_of_engines also shows that some combination of factors such as Cessna Make, Reciprocating type one engine resulted in the highest number of accidents and injuries.


I also did an interactive visualizasion using Tableau. Here is the link:

[Aviation Accidents Analysis](https://public.tableau.com/app/profile/endalkachew.dessalegne/viz/AviationAccidents-Analysis/Dashboard1)

To improve confidence in the results next time I would: -

Focus only on accidents which occurred as recently as the past 20-30 years and on filter out only the major Aircraft Make and Models which are operating around the world instead of all in this dataset.


***

***

## Conclusions

This analysis leads to three recommendations for the decision to purchase of aircraft with the lowest risk

Consider buying aircrafts with a greater number of engines and engines types which are with the lowest accidents recorded. Aircrafts with engine types such as Reciprocating must be avoided.
Aircrafts Make and Models must be highly regarded during aircraft purchase. Make and Models such as Cessna and its Models 152 and 172 which are shown to be more involved in accidents than others must be avoided.
Most importantly avoid purchasing aircrafts with a combination of all the above factors.
Aircrafts with the least number of accident records in this dataset are not considered to be with lowest risk in this analysis because this can probably be due to their low level of operation which in turn reduce the chance of accidents.

Limitations- what is the number of flights each type of aircraft operating monthly or annually? 
This is because least number of accidents and incidents may be resulted from low level of operation by some Make and Models of aircrafts.

Future analysis must compare operation and accidents level side by side to reach at a conclusion as to which aircraft Make and Model has the lowest risk. 
***





## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                                <- The top-level README for reviewers of this project
├── aviation-accidents-risk-analysis.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── Presentation.pdf                         <- PDF version of project presentation
├── data                                     <- Both sourced externally and generated from code
└── images                                   <- Both sourced externally and generated from code
```
