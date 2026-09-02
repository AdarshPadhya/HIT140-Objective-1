## AAKRITI BC 

# Goalkeeper Saves and Clean Sheets — FIFA World Cup 2026

A statistical analysis investigating whether goalkeeper saves per match differ
significantly between teams that recorded zero clean sheets and teams that
recorded one or more clean sheets during the FIFA World Cup 2026.

## Research Question

> Is there a significant difference in the average number of goalkeeper saves
> per match between teams that recorded zero clean sheets and teams that
> recorded one or more clean sheets during the FIFA World Cup 2026?



## Key Findings

| Metric | Zero clean sheets | One or more clean sheets |
|---|---|---|
| n | 21 | 27 |
| Mean saves/match | 3.153 | 3.346 |
| Std. dev | 0.998 | 1.365 |

- **95% CI for the difference in means:** (-0.879, 0.494)
- **Welch's t-test:** t(45.86) = -0.564, p = 0.575
- **Effect size (Cohen's d):** -0.158 (negligible)
- **Conclusion:** Fail to reject H₀ — no statistically significant difference
  detected. Teams with one or more clean sheets averaged slightly *more*
  saves per match, not fewer, suggesting clean sheets are not primarily
  driven by save volume.


## Skills Demonstrated

1. **Analytic question formulation** — hypotheses, variables, and
   significance level defined up front
2. **Data wrangling** — column standardization, missing value / duplicate /
   logical consistency checks, label normalization
3. **Data preparation and sampling** — simple random sampling and stratified
   sampling (by clean-sheet group), compared for group-balance preservation
4. **Descriptive statistics** — group-wise mean, median, std, quartiles;
   boxplot and histogram visualizations
5. **Inferential statistics — Confidence interval** — 95% CI for the
   difference in group means (Welch method)
6. **Inferential statistics — Two-sample t-test** — Welch's t-test with
   Shapiro-Wilk normality checks and Levene's test for equal variances as
   assumption checks, plus Cohen's d effect size

## How to Run

**Requirements:**
```bash
pip install pandas numpy scipy matplotlib openpyxl
```

**Run the notebook:**
1. Clone this repository
2. Ensure `GOALKEEPERSAVESPERMATCH.xlsx` is in your folder
3. Open `GOALKEEPERSAVES.ipynb` in Jupyter Notebook / JupyterLab / VS Code
4. Run all cells top to bottom

```bash
jupyter notebook GOALKEEPERSAVES.ipynb
```

## Data Source

Team-level FIFA World Cup 2026 statistics (48 teams), including matches
played, total goalkeeper saves, and clean sheets per team.

## Limitations

- The 48 teams represent the full tournament population, not a sample drawn
  from a larger population of "all possible World Cups" — inference should
  be read as describing this specific tournament rather than generalized
  broadly.
- Group sizes are unequal (21 vs 27); Welch's t-test accounts for this, but
  it is still worth noting.
- Saves-per-match is an association measure, not a causal one, and does not
  distinguish routine saves from decisive, game-saving stops.

## License

This project is for educational purposes.
