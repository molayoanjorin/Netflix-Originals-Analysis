# Netflix Originals Content Analysis

## Project Overview
This project analyzes a dataset of Netflix Original productions using Microsoft Power BI.

The goal of the project is to understand Netflix’s Original content library from different perspectives, including content volume, genre distribution, language diversity, IMDb performance, production trends, and runtime.

Rather than simply presenting descriptive statistics, the dashboard was designed to answer specific analytical questions and communicate meaningful insights through interactive visualizations.

The final output is a single-page interactive Power BI dashboard that provides an overview of Netflix Original content and allows users to explore the data using slicers.

## Business Problem

Streaming platforms produce a large amount of content across different genres, languages, release periods, and formats. Analyzing this content can help identify patterns in production and audience ratings.

For this project, the analysis focuses on understanding:

* How extensive Netflix’s Original content library is.
* Which genres dominate the content library.
* Which genres receive higher IMDb ratings.
* How diverse Netflix’s Original content is across languages.
* How Netflix’s Original production changed over time.
* Whether runtime categories show noticeable differences in IMDb ratings.

### Key Business Questions

1. How extensive is Netflix’s Original content library?
2. Which genres dominate Netflix’s Original content?
3. Which genres achieve the highest IMDb ratings?
4. How diverse is Netflix’s Original content across languages?
5. How has Netflix’s Original production changed over time?
6. Do different runtime categories show differences in IMDb performance?

## Dataset Description

The dataset contains information about Netflix Original productions.

### Dataset Size

* 584 titles
* 6 original columns
* 115 unique genres
* 38 unique languages
* Release period: 2014–2021

## Main Data Components 

* Title
* Genre
* Premiere
* Runtime
* IMBD Score
* Language

## Dataset Characteristics

The dataset contains a mixture of films and other Netflix Original productions with different runtimes, genres, languages, and IMDb scores.

The Genre field contains a large number of distinct and sometimes highly specific genre combinations. For example, some records contain multiple genre descriptions within a single category.

## Tools & Technologies

### Microsoft Power BI

Used for:

* Data transformation
* Data modeling
* DAX calculations
* Dashboard development
* Interactive filtering
* Data visualization

### Power Query

Used for:

* Data cleaning
* Data type correction
* Text transformation
* Date transformation
* Data quality checks

### DAX

Used for:

* KPI calculations
* Distinct counts
* Average calculations
* Conditional calculations
* Time-based analysis
* Runtime categorization

### Dax Measures Calculated 

* Total Titles
* Total Genres
* Total Languages
* Total Runtime
* Titles by Genre
* Titles by Language
* Average IMBD Score
* Average Runtime
* Highly Rated Titles
* Calculated Columns — Premiere Year & Runtime Category

## Data Cleaning & Preparation

Before creating the dashboard, the dataset was reviewed for data quality issues and prepared for analysis.

### 1. Data Type Validation

The following fields were reviewed and assigned appropriate data types:

* Title → Text
* Genre → Text
* Premiere → Date
* Runtime → Whole Number
* IMDB Score → Decimal Number
* Language → Text

Correct data types were important for accurate aggregation and visualization.

### 2. Premiere Date Cleaning

The Premiere column contained inconsistent date formatting.

One example included a period instead of the expected comma in the date string.

The date values were standardized and converted into a proper Date field.

### 3. Duplicate Check

Duplicate records were checked across the dataset.

No complete duplicate rows were identified.

The Title field was also reviewed for duplicate title names.

### 4. Missing Value Check

The dataset was checked for missing values across all six original columns.

No missing values were identified in the final dataset.

### 5. Runtime Categorization

To make runtime analysis easier to interpret, runtime values were grouped into four categories:

* Under 60 minutes
* 60 - 89 minutes
* 90 - 119 minutes
* 120+ minutes

This allowed runtime to be analyzed as meaningful groups rather than only individual minute values.

## Data Model

This project uses a single-table data model because the dataset is relatively small and already contains the attributes required for the analysis.

No separate dimension tables were required for this version of the project because the analysis is focused on a single dataset and a single-page dashboard.

## Dashboard Visuals

### KPI Cards

The dashboard includes KPI cards for:

* Total Titles
* Total Genres
* Total Languages
* Average IMDb Score
* Average Runtime

These provide an immediate summary of the Netflix Original content library.

### Visuals 

#### Netflix Originals by Genre

A horizontal bar chart shows the genres with the highest number of Netflix Original titles.

This visual addresses:

Which genres dominate Netflix’s Original content?

#### Average IMDb Score by Genre

A genre-based comparison shows differences in average IMDb performance across genres.

This addresses:

Which genres achieve higher IMDb ratings?

#### Top Languages by Content

A horizontal bar chart displays the languages with the highest number of Netflix Original titles.

This addresses:

How diverse is Netflix’s Original content across languages?

#### Original Releases Over Time

A line chart tracks the number of Netflix Original titles released each year.

This addresses:

How has Netflix’s Original production changed over time?

#### IMDb Score by Runtime Category

The runtime was grouped into categories and compared using average IMDb scores.

The categories are:

* Under 1 hour
* 1-1.5 hours 
* 1.5-2 hours 
* Over 2 hours 

This addresses:

Do different runtime categories show differences in IMDb performance?

### Interactive Slicers 

The dashboard includes slicers that allow users to dynamically explore the data.

Premiere Year

Allows users to filter the dashboard by release year.

Genre

Allows users to explore specific genres.

Language

Allows users to focus on specific languages.

## Key Insights

### 1. Netflix’s Original Library

The dataset contains 584 Netflix Original titles across 115 genres and 38 languages.

The average IMDb score is approximately 6.27, while the average runtime is approximately 93.58 minutes.

### 2. Genre Concentration

Documentary is the most represented genre in the dataset, with 159 titles, followed by:

* Drama — 77
* Comedy — 49
* Romantic comedy — 39
* Thriller — 33

This indicates that Netflix Original content is not evenly distributed across genres, with a relatively small number of genres accounting for a large share of the dataset.

### 3. Language Distribution

English dominates the dataset with 401 titles, considerably more than the next most represented languages:

* Hindi — 33
* Spanish — 31
* French — 20
* Italian — 14
* Portuguese — 12

Although 38 languages are represented, the content distribution is heavily concentrated in English.

### 4. Production Growth

Netflix Original production increased substantially throughout the period covered by the dataset.

The dataset reaches its highest recorded annual production volume in 2020, with 183 titles.

The lower figure in 2021 should not automatically be interpreted as a decline in Netflix’s overall production because the dataset may not represent a complete calendar year or the full Netflix catalogue.

### 5. IMDb Performance

There are 152 titles with an IMDb score of 7.0 or higher, representing a significant portion of the dataset.

However, average IMDb performance varies across genres, and highly specific genres with only one or two titles can produce unusually high or low averages.

Therefore, genre performance should be interpreted alongside the number of titles represented in each genre.

### 6. Runtime Patterns

The majority of titles fall within the Over 2 hours runtime category.

The results show that IMDb performance varies across runtime groups, but runtime alone should not be treated as proof of a causal relationship with IMDb ratings.

## Recommendations

Based on the analysis, the following recommendations can be considered:

### 1. Monitor Genre Concentration

The large concentration of titles in a small number of genres suggests an opportunity to monitor genre diversity and identify underrepresented content categories.

### 2. Continue Tracking International Content

Although 38 languages are represented, English accounts for the majority of titles. Tracking language distribution over time could provide a clearer picture of international content expansion.

### 3. Monitor Runtime Distribution

Since most titles fall within the Over 2 hours range, runtime trends could be monitored alongside genre and IMDb performance to understand how content formats evolve.

## Conclusion

The analysis shows that the Netflix Original library in this dataset is characterized by:

* A large concentration of content in selected genres.
* Strong representation of English-language content.
* Significant growth in Original production between 2014 and 2020.
* Variation in IMDb performance across genres and runtime categories.
* A broad range of content spanning 115 genres and 38 languages.

The project also highlights an important principle in data analysis: volume alone does not tell the complete story. Content quantity, audience ratings, genre representation, language diversity, runtime, and time trends should be considered together when evaluating a content library.

## Skills Demonstrated

This project demonstrates practical experience with:

* Data cleaning
* Power Query
* Data transformation
* Data modeling
* DAX
* Calculated columns
* KPI development
* Data visualization
* Dashboard design
* Interactive filtering
* Trend analysis
* Categorical analysis
* Data quality assessment
* Business storytelling
* Insight generation
