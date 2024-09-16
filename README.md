
# Amazon Delivery Data Analysis

![Amazon Logo](https://github.com/ngambip/Amazon_Delivery./blob/main/Images/Amazon_logo.png)

## Introduction

This project involves analyzing a dataset of Amazon deliveries to uncover key patterns and insights related to delivery efficiency, vehicle usage, weather conditions, and delivery times. The analysis focuses on understanding various factors affecting delivery performance and identifying trends that can help improve the process. The dataset consists of 43,739 rows and 16 columns, including attributes such as order time, pickup time, agent details, delivery time, and weather conditions.

## Project Overview

The analysis follows a structured approach:

   -[Data Exploration and Understanding](#Data-Exploration-and-Understanding)
   
   -[Data cleaning](#Data-Cleaning)
   
   -[Exploratory Data Analysis (EDA)](Exploratory-Data-Analysis-(EDA))
   
   -[Stastical Calculations and Insights](#Statistical-Calculations-and-Insights)
   
   -[Analysis and Visualization](#Analysis-and-Visualization)
   
   -[Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Technologies Used

    Python: Primary language for data analysis.
    Pandas: Data manipulation and cleaning.
    NumPy: Numerical calculations.
    Matplotlib/Seaborn: Data visualization.
    GitHub: Version control and collaboration.

# Data Exploration and Understanding

The first step was exploring the dataset using:

    df.head(),to understand its structure.
    df.columns(), column names.
    df.describe(), basic statistical summary.
    

#### Key features:
Order Time and Pickup Time: For calculating the time difference between order and pickup.

Delivery Time: To evaluate delivery efficiency.

Agent Rating and Agent Age: Influencing factors on delivery performance.

Weather and Traffic: External factors affecting delivery delays.

# Data Cleaning

To ensure accurate analysis, the data was cleaned through these steps:

- Handling missing values: Missing values in columns like Agent_Rating, Order_Time, and Weather were filled with the 
  median to maintain data integrity without distorting results.
- Time conversion: Order_Time and Pickup_Time were converted to datetime objects and formatted to only contain time for 
  easier time difference calculations.
- Data Type Corrections: Ensured correct data types for Order_Time, Pickup_Time, and Delivery_Time for further processing.
  Duplicate Removal: Removed duplicate records, ensuring each delivery was unique.

# Exploratory Data Analysis (EDA)

During EDA, several insights were drawn:

-   Vehicle Usage: Majority of deliveries were performed using scooters and bikes, with fewer van deliveries.
-   Delivery Times: Most deliveries were completed within 90 to 160 minutes, though some outliers took much longer.
-   Agent Rating vs. Delivery Efficiency: Higher-rated agents consistently performed better.
-   Weather Impact: Poor weather (cloudy, windy, and stormy) correlated with longer delivery times.

We visualized these patterns through bar charts, scatter plots, and histograms to show distributions and relationships.

# Statistical Calculations and Insights

## Central Tendencies (Mean, Median, and Mode)

-   Mean: The average delivery time was calculated to provide a sense of typical delivery duration.
    For example, the mean delivery time was found to be around 124.9 minutes, indicating that most deliveries hover around 
    this time.

-    Median: The median provides the middle value in the data and is useful when the data contains outliers.
     In this case, the median delivery time was 125 minutes, very close to the mean, suggesting a fairly symmetrical distribution of delivery times.

-    Mode: The most frequently occurring delivery time helps identify the most common duration for deliveries.
        The mode for delivery time was 90 minutes, indicating that a significant portion of deliveries tended to be faster.

-    Standard Deviation and Variability

     Standard Deviation: I calculated the standard deviation of delivery times to understand the spread and consistency.
     A standard deviation of 51.9 minutes shows moderate variability, meaning while many deliveries are around the 125-minute mark, there are some that deviate                  significantly.

  -   Interquartile Range (IQR): The IQR was used to assess the range between the 25th and 75th percentiles, which were 90 minutes and 160 minutes, respectively. This implies that the middle 50% of delivery times are fairly consistent.

-   Time Differences

   To measure efficiency, the time difference between Order_Time and Pickup_Time was calculated, accounting for midnight crossover. This calculation provided a more 
   accurate representation of agent efficiency.

   Average, median, and mode values for time differences were computed to assess the pickup speed.
   
# Analysis and Visualization

This section addresses key questions using Python, with results visualized for better interpretation:

-   Delivery Time Analysis: The distribution of delivery times was plotted using a histogram, showing that most deliveries    took between 90 to 160 minutes.
   
-  Agent Performance: Agent ratings were compared with delivery times to show that higher-rated agents consistently delivered faster.
-  Vehicle Usage: A Donut Chart was created to display the count of deliveries made using different vehicle types,highlighting the popularity of scooters and bikes.
-  A Pie chart was used to show that almost 75% of the orders where from Metropolitan
-  Scartter graph was used to determine the correlation between Agent Age and delivery time and there was a weak relationship of 0.26, meaning no effeect on    the 
   delivery time.
-  Another scartter graph was used to determine the Correlation between Agents rating and agent age and it gave a negative relation meaning it have compeletely no effect
    
# Conclusions and Recommendations

Based on the analysis, the following Analysis were drawn:
-   Vehicle Selection: Scooter and bike deliveries were faster and more efficient in metropolitan areas, even in challenging weather.
-   Agent Rating Matters: Higher-rated agents delivered faster, suggesting the importance of experience and performance in improving delivery efficiency.
-   Weather Impact: Adverse weather conditions significantly impacted delivery times, particularly for scooter and bike deliveries.
  
 ### Strengths

Agent Ratings and Performance: The data shows a positive correlation between agent ratings and faster delivery times, suggesting that Amazon’s system of rating agents is effectively rewarding good performance. Agents with ratings above 4.7 generally deliver faster, which reflects good management and service quality.

 Vehicle Efficiency: Scooter and motorcycle deliveries are generally faster, especially in metropolitan areas, which indicates that Amazon has optimized vehicle types for different areas. This operational decision helps reduce delivery times, particularly in congested urban areas.

### Areas for Improvement

-   Weather-Related Delays: The analysis shows that adverse weather conditions (such as storms and wind) significantly         slow down delivery times, by as much as 20%. This is expected, but it also shows that Amazon may need to improve           logistics or communication during poor weather. It could mean equipping drivers with better tools or planning for          weather contingencies.

-   Midnight Transactions: Orders placed around midnight are facing longer pickup delays, likely due to reduced workforce      or resources during late hours. This could be a point for improvement—either by optimizing the schedule of delivery       agents for late-night orders or better managing customer expectations for deliveries during non-peak hours.

### Possible Misleading Data

Outliers and Data Quality: There may be outliers in the data that skew the overall perception of delivery times. For example, extreme values for Delivery_Time or Order_Time may indicate data recording issues or special cases that aren't reflective of general performance. These need to be carefully analyzed and possibly excluded to avoid misleading conclusions.

 Geographical Extremes: Certain locations with unusual latitudes and longitudes might be affecting average delivery times. If these represent rural or difficult-to-access areas, they might not be reflective of the majority of Amazon's deliveries, especially if most orders are metropolitan.

# Conclusion: Amazon Is Doing Well, But There’s Room for Improvement

In general, Amazon seems to have a solid delivery system in place, but the data reveals a few areas where delivery times could be improved, particularly in challenging weather conditions and during late-night operations. The presence of outliers and extreme cases suggests that the data should be cleaned further to remove misleading points before drawing any final conclusions. It’s important for Amazon to focus on these edge cases to maintain high efficiency across the board.

