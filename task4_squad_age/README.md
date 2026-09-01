# FIFA World Cup 2026 — Squad Age Analysis

## Student's Description

- **Student ID:** 401743
- **Student Name:** Adarsh Padhya
- **Group Name:** Darwin Group 29

---

## Question

> **Is the mean average squad age of national teams at the 2026 FIFA World Cup significantly different from 27 years?**

---

## Data Wrangling

### Data source

The data was extracted from FBref's *2026 World Cup Squad Standard Stats* table:

https://fbref.com/en/comps/1/2026/2026-FIFA-World-Cup-Stats

### Attributes extracted from the source

| Attribute | Description |
|---|---|
| `Squad` | National team name |
| `# Pl` | Number of players listed in the squad |
| `Age` | Average age of the national squad in years |

### Cleaning performed in Python

- Imported the original Excel file using the second row as the header because the first row contains grouped table headings.
- Retained only `Squad`, `# Pl`, and `Age`.
- Removed FBref country-code prefixes from squad names.
- Converted player-count and age columns to numeric values.
- Removed missing values and duplicate squad records.

The final cleaned dataset contained **48 national squads** and no missing values in the selected variables.

---

## Data Preparation and Sampling

### Population

The population is all **48 national squads** that competed in the 2026 FIFA World Cup.

### Sample

A **simple random sample without replacement** of **36 squads** was selected from the 48 squads. A fixed random seed (`42`) was used so the sample can be reproduced exactly.

### Unit of analysis

Each observation is one national team's **average squad age**.

---

## Descriptive Statistics

| Statistic | Result |
|---|---:|
| Sample size | 36 squads |
| Mean squad age | 27.88 years |
| Median squad age | 28.05 years |
| Standard deviation | 1.20 years |
| Minimum squad age | 25.30 years |
| Maximum squad age | 30.00 years |

---

## Inferential Statistics — Confidence Interval

A 95% confidence interval was calculated for the mean average squad age.

> **95% confidence interval: 27.48 to 28.29 years**

This indicates that the population mean average squad age is estimated to lie between 27.48 and 28.29 years.

---

## Inferential Statistics — One-Sample t-Test

The analysis uses a two-tailed one-sample t-test with a benchmark age of 27 years.

- **Null hypothesis (H₀):** The mean average squad age is 27 years.
- **Alternative hypothesis (H₁):** The mean average squad age is different from 27 years.
- **Significance level:** α = 0.05

| Result | Value |
|---|---:|
| t-statistic | 4.406 |
| p-value | 0.0001 |
| Decision | Reject H₀ |

Because the p-value is below 0.05, there is statistically significant evidence that the mean average squad age differs from 27 years. The sample mean is higher than 27 years.

---

## Files

| File | Purpose |
|---|---|
| `squad_age_analysis.ipynb` | Python notebook containing data wrangling, sampling, descriptive statistics, confidence interval, t-test, and visualisation |
| `../datasets/Squad Standard Stats(1).xlsx` | Original FBref dataset used in the analysis |

---

## Tools Used

- **Python:** pandas, SciPy, Matplotlib
- **FBref:** source of World Cup squad statistics
- **Microsoft Excel:** raw dataset preparation
- **VS Code / Jupyter Notebook:** Python coding and execution
- **GitHub:** code and dataset repository
- **Microsoft Teams:** group communication and evidence of collaboration
- **Microsoft PowerPoint:** presentation slides

---

## Limitations

- The analysis uses average squad age only; it does not examine individual player ages or player positions.
- A sample of 36 squads was used rather than all 48 squads, so results may vary slightly with a different random sample.
- The analysis identifies a statistical difference from the benchmark of 27 years, but it does not explain why squad ages differ.
- Results are specific to the 2026 FIFA World Cup and should not automatically be generalised to other tournaments.
