# Data Professional Survey Breakdown — Power BI Dashboard

An interactive Power BI dashboard that analyzes survey responses from data professionals to uncover trends in salaries, job roles, tooling, and job satisfaction.

## Project Overview

This project takes raw survey data collected from people working in data careers (Data Analysts, Data Scientists, Data Engineers, Database Developers, students/aspirants, and others) and turns it into a single-page, fully interactive report. The goal is to answer practical career questions such as which roles pay the most, which programming languages the community prefers, how difficult it is to break into data, and how satisfied professionals are with their pay and work-life balance.

## Tech Stack

- **Power BI Desktop** — report building and visualization
- **Power Query** — data extraction, cleaning, and transformation
- **DAX** — calculated measures and KPIs

## Dataset

The dataset consists of survey responses covering fields such as:

- Current job title / role
- Salary (converted into a usable numeric midpoint)
- Country of residence
- Favorite programming language
- Difficulty of breaking into data
- Happiness with salary and with work-life balance
- Demographics (age, gender, education, industry)

## Data Preparation

Cleaning and transformation steps performed in Power Query:

- Removed duplicate and incomplete responses
- Standardized inconsistent job title and country entries
- Converted salary text ranges into numeric values for aggregation
- Corrected data types for numeric, categorical, and date columns
- Renamed columns for readability in visuals

## Dashboard Features

**KPI cards**

- Total survey respondents
- Average salary
- Average age of respondents
- Average difficulty of breaking into data

**Visuals**

- Average salary by job title (bar chart)
- Count of respondents by country (map / bar chart)
- Favorite programming language (bar chart)
- Difficulty of breaking into data (donut chart)
- Happiness with salary vs. work-life balance (gauge visuals)
- Respondent breakdown by gender and education level

**Interactivity**

- Slicers for country, job title, and gender
- Cross-filtering across all visuals
- Tooltips with supporting detail

## Key Insights

- Salary varies significantly by role, with engineering and science roles generally above analyst roles.
- Python is the dominant language of choice among respondents.
- A large share of respondents rate breaking into the data field as difficult or very difficult.
- Work-life balance satisfaction tends to score higher than salary satisfaction.

_Insight figures depend on the survey snapshot loaded in the .pbix file._

## Repository Structure

```
├── Power bi.pbix    # Power BI report file (data model, measures, and dashboard)
└── README.md        # Project documentation
```

## How to Use

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
2. Clone or download this repository:

   ```bash
   git clone https://github.com/AnuSHAR-214/Data-Professional-Survey---Project-2.git
   ```

3. Open `Power bi.pbix` in Power BI Desktop.
4. Click **Refresh** if you want to reload the source data, then explore the report using the slicers.

## What I Learned

- End-to-end BI workflow: raw data to cleaning, modeling, visualization, and insight
- Writing DAX measures for KPIs and averages
- Designing a readable single-page dashboard layout with consistent formatting
- Translating survey data into career-relevant conclusions

## Author

**Anusha R** — [@AnuSHAR-214](https://github.com/AnuSHAR-214)
