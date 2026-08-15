# Data Professional Survey Breakdown — Power BI Dashboard

A single-page Power BI report that summarizes responses from a survey of data
professionals. It profiles who took the survey, what they earn, what tools they
prefer, how hard they found it to enter the field, and how satisfied they are
with pay and work/life balance.

- **Report / page title:** Data Professional Survey Breakdown
- **Platform:** Power BI Service (app.powerbi.com)
- **Data last refreshed:** 15/08/26
- **Respondents in scope:** 630
- **Report-level filters:** none

## Dashboard Layout

The canvas is arranged in three columns: respondent demographics on the left,
salary and career-entry analysis in the centre, and KPI cards plus satisfaction
gauges on the right.

| Visual | Type | Dimension | Measure |
|---|---|---|---|
| Country Of Survey Takers | Treemap | Q11 – Which Country do you live in? | Count of respondents |
| Favorite Programming Language | Stacked column chart | Favorite Programming Language, legend = Q1 – Which Title Best Fits your Current Role? | Count of Voters |
| Average Salary By Job Title | Bar chart | Q1 – Which Title Best Fits your Current Role? | Average of Average Salary |
| Difficulty to break into Data | Donut chart | Q7 – How difficult was it for you to break into Data? | Count of respondents (with %) |
| Count of Survey counters | Card | — | Row count |
| Average Age of Survey Takers | Card | — | Average age |
| Happy with Work Life | Gauge (0–10) | — | Average of Q6 – How Happy are you in your Current Position with the following? (Work/Life Balance) |
| Happy With Salary | Gauge (0–10) | — | Average of Q6 – How Happy are you in your Current Position with the following? (Salary) |

## Key Figures

**Headline KPIs**

- Survey respondents: **630**
- Average age: **29.87**
- Work/life balance satisfaction: **5.74 / 10**
- Salary satisfaction: **4.27 / 10**

**Average salary by job title**

Displayed on a 0–100 axis as unitless decimals; the bar labels are rounded.

| Job title | Average of Average Salary |
|---|---|
| Data Scientist | 93.78 |
| Data Engineer | 65.09 |
| Data Architect | 63.67 |
| Other | 60.49 |
| Data Analyst | 55.30 |
| Database Developer | 33.20 |
| Student/Looking/None | 26.58 |

**Country of respondents**

| Country | Respondents |
|---|---|
| United States | 261 |
| Other | 224 |
| India | 73 |
| United Kingdom | 40 |
| Canada | 32 |
| **Total** | **630** |

**Difficulty breaking into data**

| Response | Respondents | Share |
|---|---|---|
| Neither easy nor difficult | 269 | 42.70% |
| Difficult | 156 | 24.76% |
| Easy | 134 | 21.27% |
| Very Difficult | 44 | 6.98% |
| Very Easy | 27 | 4.29% |

**Favorite programming language, by job title**

| Language | Data Analyst | Data Architect | Data Engineer | Data Scientist | Database Developer | Other | Student/Looking/None | Total |
|---|---|---|---|---|---|---|---|---|
| Python | 255 | 3 | 29 | 20 | 3 | 54 | 56 | 420 |
| R | 61 | — | 2 | 4 | — | 15 | 19 | 101 |
| Other | 60 | — | 5 | 1 | 2 | 14 | 13 | 95 |
| C/C++ | 5 | — | — | — | — | 2 | — | 7 |
| JavaScript | — | — | 2 | — | — | 2 | 2 | 6 |
| Java | — | — | — | — | — | 1 | — | 1 |
| **Total** | **381** | **3** | **38** | **25** | **5** | **88** | **90** | **630** |

Python accounts for roughly two thirds of all responses (420 of 630), with R a
distant second.

## Field Reference

The model is built directly on the survey export, so column names mirror the
questionnaire wording:

- `Q1 - Which Title Best Fits your Current Role?` — job title dimension used by
  the salary chart and as the legend of the language chart. Seven values:
  Data Analyst, Data Architect, Data Engineer, Data Scientist,
  Database Developer, Other, Student/Looking/None.
- `Q6 - How Happy are you in your Current Position with the following? (Salary)`
  — 0–10 satisfaction score.
- `Q6 - How Happy are you in your Current Position with the following?
  (Work/Life Balance)` — 0–10 satisfaction score.
- `Q7 - How difficult was it for you to break into Data?` — five-point ordinal
  scale.
- `Q11 - Which Country do you live in?` — country dimension, five values with
  smaller countries grouped as "Other".
- `Favorite Programming Language` — language dimension, six values.
- `Average Salary` — numeric salary estimate, aggregated as an average.
- `Voters` / row count — used for the count measures.

## How to Use the Report

Every visual is cross-filtering, so selecting a country tile, a job-title bar,
a language column or a donut segment filters the rest of the page. For example,
clicking "India" in the treemap re-scopes the salary chart, the satisfaction
gauges and both KPI cards to Indian respondents only. Use Ctrl+click to select
multiple values, and click an empty area of a visual to clear the selection.
The Filters pane on the right is empty by default and can be used to add ad-hoc
slicing. Hovering any data point shows a tooltip with the exact underlying
value and the source question name, and right-click → "Show as a table" exposes
the precise numbers behind any visual.

## Notes and Caveats

The `Average Salary` measure is rendered without a currency symbol or scale
suffix, so the unit is not documented in the report itself. Values fall in the
26–94 range on a 0–100 axis, which is consistent with salaries expressed in
thousands of a single currency, but this should be confirmed against the source
dataset before the numbers are quoted externally. Figures are self-reported and
are not adjusted for cost of living or exchange rates, so cross-country
comparison is indicative only.

Job titles and countries with few responses are bucketed into "Other", which is
why "Other" is a sizeable category in several visuals — 224 of 630 respondents
for country, and 88 for job title. Satisfaction scores are subjective 0–10
self-ratings. The sample is heavily skewed toward US-based data analysts using
Python, so results are not representative of the global data profession.
