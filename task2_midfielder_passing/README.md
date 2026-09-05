# FIFA World Cup 2026: Midfielder Playing Time Analysis



*Student ID:* S400545  
*Student Name:* Md Osman Syed  
*Group Name:* Darwin Group 29  

## Question

*Is there a significant difference in playing time between starting midfielders and substitute midfielders at the 2026 FIFA World Cup?*

## Data Wrangling

### Data Extraction
The dataset was taken from *FBref* and used to analyse midfielder playing time at the 2026 FIFA World Cup.

*Source:* https://fbref.com/en/

### Variables Used

| Variable | Description |
|---|---|
| Player | Player name |
| Pos | Player position |
| Squad | National team |
| Age | Player age |
| Club | Player's club |
| MP | Matches played |
| Starts | Number of starts |
| Min | Total minutes played |
| Group | Starter or Substitute |

### Midfielder Selection
Players with position labels containing *MF* were selected, including combined positions such as *FWMF, DFMF, MFFW and MFDF*.

- *Starter:* started at least one match.
- *Substitute:* had zero starts.

### Data Quality Checks
- 2 missing values were found in the Club column.
- 0 duplicate player records were found.
- 345 Starters
- 164 Substitutes

## Data Preparation and Sampling

### Population
All midfielders in the dataset.

### Sample
A stratified random sample of 200 midfielders was selected:

- 100 Starters
- 100 Substitutes

Equal group sizes were used to make the comparison more balanced.

## Descriptive Statistics

| Statistic | Starter | Substitute |
|---|---:|---:|
| n | 100 | 100 |
| Mean | 250.09 | 34.81 |
| Median | 244.50 | 26.50 |
| Standard deviation | 134.688 | 30.597 |
| Minimum | 45 | 1 |
| Maximum | 659 | 140 |
| Q1 | 146.00 | 14.00 |
| Q3 | 316.00 | 46.00 |

### Summary
- Mean difference: *215.28 minutes*
- Overall sample mean: *142.45 minutes*
- Overall sample standard deviation: *145.38 minutes*

## Graphical Representation

The boxplot and histogram show that starting midfielders generally played more minutes than substitute midfielders. Starter playing times were also more widely spread.

## Confidence Interval

- *Starter 95% CI:* 223.36 to 276.82 minutes
- *Substitute 95% CI:* 28.74 to 40.88 minutes

## Welch Two-Sample t-Test

### Assumption Check

- Starter Shapiro-Wilk: *W = 0.931, p = 0.0001*
- Substitute Shapiro-Wilk: *W = 0.859, p < 0.0001*
- Levene's test: *71.473, p < 0.0001*

### Hypotheses

- *H₀:* The mean playing time of starting midfielders equals that of substitute midfielders.
- *H₁:* The mean playing time of starting midfielders differs from that of substitute midfielders.

*Significance level:* α = 0.05

### Results

- *t-statistic:* 15.586
- *p-value:* < 0.0001
- *Cohen's d:* 2.204
- *Decision:* Reject H₀

## Conclusion

There is a statistically significant difference in mean playing time between starting and substitute midfielders. Starters played substantially more minutes on average.

## Limitations

- Starter means a player started at least one match.
- Combined MF positions were included.
- Playing time may also depend on team progression, injuries, tactics and substitutions.
- The balanced 100/100 sample does not reflect the original population proportions.

## Tools Used

- Python
- Pandas
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook
- Microsoft Excel
- GitHub
