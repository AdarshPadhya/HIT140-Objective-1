# Student's Description:

## Student ID: S399582

## Student Name: Madan B K

## Group Name: Darwin Group 29

---

# Question:

## "Do winning teams show significantly higher average defensive efficiency (save percentage) than losing team across matches played during the FIFA World Cup 2026?"

---

# Data Wrangling:

## Data Extraction:

### Data was extracted from offical FIFA statistical website. [https://www.fifa.com/en/tournaments/mens/worldcup/canadamexicousa2026/statistics/team-statistics]

## Attributes Extracted from source:

| Attribute             | Description                                                                 |
| --------------------- | --------------------------------------------------------------------------- |
| Winner_Team           | Name of the winning team (from final score)                                 |
| Loser_Team            | Name of the losing team (from final score)                                  |
| Winner_Goals_Conceded | Goals conceded by the winning team                                          |
| Loser_Goals_Conceded  | Goals conceded by the losing team                                           |
| Winner_SOT_Faced      | Losing team's "Attempts on Target" (i.e., shots the winner's defense faced) |
| Loser_SOT_Faced       | Winning team's "Attempts on Target" (i.e., shots the loser's defense faced) |

### Attributes assigned manually

## Key Variables:

### 1. Shots on Target Faced

### 2. Goals Conceded

### 3. Save % = (Shots on Target Faced - Goals Conceded) / Shots on Target Faced x 100

---

# Data preparation and sampling:

## Population:

All 104 matches played during FIFA World Cup 2026 (from group stage to final).
** Eligible population (for this analysis):**
Since above mentioned question requires a clear winner and loser, so, matches ending in a draw (possible only in the group stage, which was 20 draw matches) are excluded. This gives an eligible population of **84 decisive-result matches**:

- 52 decisive group stage matches
- 32 knockout stage matches (Round of 32 through Final — always decisive due to extra time/penalties)

## Sample:

A stratified random sample of **50 matches** was selected from the eligible population:

- 30 matches randomly selected from the 52 decisive group stage matches
- 20 matches randomly selected from the 32 knockout stage matches
  Stratifying by stage ensures both group stage and knockout stage contexts are proportionally represented, rather than a pure random draw potentially over or under sampling one stage.

**Unit of analysis:**
Each sampled match produces **one paired observation**: the winning team's Save % and the losing team's Save % from that same match. A paired-samples design is used because the two observations from a single match are not independent of each other, where they share contextual factors such as referee, weather, and match stakes.

---

# Descriptive statistics:

**Wining Team's defensive efficiency mean: ...**
**Losing Team's defensive efficiency mean: ...**

---

# Inferential statistics (Confidence interval):

## ...

# Inferential statistics (either a One-Sample t-Test OR a Two-sample t-Test):

## ...

# Tools Used:

- **Python** (Numpy,...)
- **FIFA Match Centre** ([fifa.com])
- **Excel** (manual data extraction)
- **Vs code** (programing)
- **Github** (program files store platform)
- **Ms Word** (documentation)
- **Ms Teams** (communication and collab)
- **Ms PowerPoint** (Presentation)

---

# Limitations:

## ...
