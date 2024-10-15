# Emergency Services Data analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Exploritory Data Analysis](#exploritory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project overview

This project analyzes Emergency Call data from the London Borough of Barnet, London, focusing on road traffic accidents. It explores trends, severity, and location patterns to improve traffic safety and urban planning insights.

### Data Sources

The primary dataset used for this analysis is the "cleaned_barnet_data.csv" file, The data represents road traffic accidents and includes various details, such as the severity of accidents, date and time, location coordinates, and accident conditions like weather or road surface.  

### Tools

- Excel - Data Cleaning
- SQL Server - Data analysis
- Tableau - Creating reports


### Data Cleaning/Preparation

In the initial data preparation phase I performed the following tasks.
1. Data loading and inspection.
2. Handling missing values.
3. data cleaning and formatting


### Exploritory Data Analysis

EDA involved exploring the Emergency calls data to anser key questions, such as:

- Which weather conditions are associated with the highest accident severity?
- Which times of day have the highest frequency of accidents?
- Is there a particular day of the week when accidents are more frequent?

### Data Analysis

Includes some interesting code/features

```sql
SELECT 
    Road_Type, 
    COUNT(*) AS Total_Accidents
FROM 
    accidents_table
GROUP BY 
    Road_Type
ORDER BY 
    Total_Accidents DESC;
```

### Results and Findings

The analysis shows that certain road types are more associated with severe accidents (Fatal + Serious). In particular, main roads and dual carriageways tend to have higher counts of severe accidents compared to residential or minor roads. This could be due to higher traffic volumes and speeds on these road types, which increases the risk of more serious incidents.

### Recommendations

Based on the data analysis, here are some recommendations to improve road safety:

1. **Increase safety measures on high-risk roads**: Since major roads, motorways, and dual carriageways are associated with more severe accidents, it’s critical to install more safety features like speed cameras, better lighting, and barriers on these roads.

2. **Speed limit enforcement**: Higher speeds increase the risk of severe accidents. Stricter speed enforcement on roads with high accident severity could reduce fatal and serious accidents.

3. **Improve road design**: For roads with frequent severe accidents, consider redesigning sections to minimize sharp curves, blind spots, or dangerous intersections.

4. **Targeted driver education**: Initiatives aimed at educating drivers about the dangers of speeding, especially on high-risk roads, could help in reducing severe accidents.

5. **Traffic calming measures on residential roads**: While severe accidents are less common on residential roads, ensuring low speeds through speed bumps, signage, and better pedestrian safety features can still help prevent incidents.

These measures focus on reducing both the frequency and severity of accidents, with particular attention to high-risk road types.

### Limitations

1. Convert the Date and Time columns to datetime objects.
2. Drop irrelevant columns.
3. Map categorical columns to meaningful names.
4. Checked for and handled outliers and anomalies.
5. All zero values were removed.

### References

1. Microsoft SQL Server 2019: A Beginner's Guide, Seventh Edition
2. Stack Overflow

  
