# Exploratory-Data-Analysis-on-Play-Store-App-PowerBI
![google play](https://github.com/bvishnub/Exploratory-Data-Analysis-on-Play-Store-App-Review/assets/169208781/c6c3319c-bff0-4588-b8ad-0f4041c6b44e)



## Table of Contents 
  - [Project Overview](#project-overview)
  - [Background](#background)
  - [Objective](#objective)
  - [Datasets](#datasets)
  - [Setup and Requirements](#setup-and-requirements)
  - [Key Visualizations](#key-visualizations)
  - [Interactivity Features](interactivity-features)
  - [Use of DAX Functions](#use-of-dax-functions)
  - [Key Insights](#key-insights)


## Project Overview

This project extends the Exploratory Data Analysis (EDA) of Play Store data previously conducted using Python. The current extension leverages Microsoft Power BI to provide advanced visualizations and interactive analysis. This shift to Power BI aims to enhance data exploration capabilities and facilitate deeper insights through interactive dashboards.

## Background

In the initial Python-based project, the following steps were completed:

- **Dataset Inspection**: Reviewed the dataset for initial understanding.
- **Removing Duplicates**: Eliminated duplicate entries.
- **Handling Missing Values**: Addressed and filled missing data.
- **Dealing with Outliers**: Identified and managed outliers.
- **Exploratory Data Analysis**: Analyzed basic trends and relationships in the data, generated summary statistics, and visualized findings using various charts and plots for clearer understanding.

The Power BI project builds upon this work by incorporating advanced visualizations and interactive elements to further explore the dataset.

## Objective

- Build upon the initial Python EDA to create interactive dashboards in Power BI.
- Enhance data visualization with Power BI's advanced features.
- Provide deeper insights into app performance, user ratings and review analysis, and revenue analysis.

## Datasets

The project utilizes the cleaned version of the dataset used in the previous EDA. The dataset source is the AlmaBetter Team.

There are two datasets:

1. **Play Store Data**
2. **User Review Data**

### Play Store App Dataset Variables

- **App**: Name of the application.
- **Category**: App category (categorical).
- **Reviews**: Count of reviews for the app (categorical; 55% unique values, needs conversion to numerical).
- **Size**: Size of the application in MB and KB (needs conversion to numerical).
- **Installs**: Total number of downloads (needs conversion to numerical).
- **Type**: Free or Paid.
- **Price**: Installation charges (needs conversion to numerical).
- **Content**: Age group suitable for the app (categorical).
- **Genre**: Genre of the app.
- **Last Updated**: Date when the app was last updated (needs conversion to datetime).
- **Current Ver**: Current version of the app.
- **Android Ver**: Required Android version.


### User Review Dataset Variables

- **App**: Name of the application.
- **Translated_Review**: Translation of the customer review.
- **Sentiment**: Sentiment of the review (positive, negative, or neutral).
- **Sentiment_Polarity**: Polarity of the review (range: [-1, 1]).
- **Sentiment_Subjectivity**: Subjectivity of the review (range: [0, 1]; helps determine if the feedback is personal or factual).


## Setup and Requirements

To work with this project, you need:

- **Microsoft Power BI Desktop**: Ensure you have the latest version installed.
- **Playstore Dataset**: The cleaned dataset in CSV format, as prepared in the Python project.

## Key Visualizations

### Play Store App Dashboard

- Provides a comprehensive overview of download trends across various attributes, including app categories, types, and age groups. This dashboard allows users to quickly assess how different factors influence app downloads.

### Ratings and Reviews Analysis Dashboard

- Offers an in-depth analysis of app ratings and user reviews. This dashboard visualizes rating distributions and review trends to help users evaluate app performance and user satisfaction.

### Revenue Analysis Dashboard

- Analyzes revenue trends by visualizing app pricing and revenue categories. This dashboard provides insights into financial performance and helps understand revenue patterns across different app price ranges.

## Interactivity Features

- **Drill-Down**: Explore data at different levels of detail, from categories to app levels.
- **Drill-Through**: Navigate from summary data to detailed views, e.g., clicking on an app category to view performance metrics.
- **Slicers**: Interactive filtering options for attributes such as app types.
- **Filters**: Refine data views by applying conditions, such as filtering by year.
- **Cross Filters**: Dynamic interaction between visualizations. Selecting a category updates related visualizations.
- **Clear Filter**: Reset all slicers and filters to their default state.

## Use of DAX Functions

- **Measures**: Aggregate measures for key insights:
    - **Total Revenue**: Aggregates total revenue from paid apps.
    - **Total Installs**: Calculates total app installations.
    - **Total Apps**: Counts the total number of apps.
    - **Total Reviews**: Summarizes total user reviews.
    - **Average App Size**: Computes average app size in megabytes.
    - **Average Rating**: Calculates average user rating.
- **Calculated Columns**: Detailed categorization and analysis:
    - **Price Category**: Categorizes apps into price ranges.
    - **Android Versions**: Classifies apps by supported Android versions.
    - **Rating Average in Stars**: Converts ratings to a star format.
    - **Revenue**: Calculates revenue based on installs.
    - **Size Category**: Groups apps into size ranges.
- **Calculated Tables**: Organizes data by time periods:
    - **Calendar Table**: Includes Year, Month, and Quarter columns for time-based analysis.

 ## Key Insights

 ![image](https://github.com/user-attachments/assets/78067fe6-40ac-4f71-a42d-31666aaa29fe)


### Play Store App Dashboard


![image](https://github.com/user-attachments/assets/2c6a2873-1961-4c49-a17b-a7d8c72d286b)



- The Game category is the most popular, with the highest downloads in both paid and free sections.
- Top genres include Communication, Tools, and Productivity.
- Apps with sizes between 10-19 MB are most preferred, with 50 billion downloads.
- Free apps are more popular with maximum Installs.
- The "Everyone" age group is the most popular, accounting for 69.5% of downloads.
- The "Varies with Device" Android version is most popular and can be considered while new apps.
- Data cards provide quick insights into total downloads, average ratings, total reviews, average app size, and total app count.
- We can look at the download trend across the year and months using drill down feature. Also most Installs are done in August and July months and sudden increase in download trend can be observed post 2017.
- Decomposition charts offer detailed understanding of trends by category, year, quarter, and genre.

### Ratings and Review Analysis

![image](https://github.com/user-attachments/assets/60f08209-fd74-4460-b178-fb9cdc53b96f)


- Most ratings are 4 stars (77.4%) with a total of 7.47k in count.
- Total of 2bn reviews are received for apps.
- Paid apps have a higher average rating (4.27) compared to free apps (4.19).
- Overall average rating is 4.19.
- The Events category has the highest average rating (4.40), while Art and Design and Education follow, despite having fewer installs.
- "Varies with Android Versions" is preferred and has the highest ratings i.e. 4.25.
- Positive sentiment accounts for 64% of total reviews.
- We can also observe in sentiment count section that , Games and Health and Fitness Categories are leading with maximum positive sentiment count , also it can observed that maximum negative count sentiment category is also Game category , however same is due to maximum proportion of available apps under games category in play store.

### Revenue Analysis

![image](https://github.com/user-attachments/assets/9e5a902b-d9c9-4572-8a8e-112d189c0a01)


- Family Lifestyle and Game categories are major revenue contributors.
- The most popular price category is <$10.
- Revenue trends are analyzed by year, month, and quarter using drill down feature.
- Data cards provide quick insights into total downloads, revenue, average rating, and total paid apps.
- Around 60% of revenue comes from the "Everyone" age group.
- Android Version 4 and above is most preferred under paid section with highest revenue. contribution.
- Top genres for revenue generation include Arcade, Action, Adventure, and Lifestyle.

## Contact

For any questions or feedback, please contact at vishnub195@gmail.com .
