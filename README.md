# PBS Utah Major-Gift Prospecting: EDA and Predictive Modeling

This repository contains Tama Wihongi's individual exploratory data analysis (EDA) and predictive-modeling contributions for the PBS Utah major-gift prospecting capstone project.

## Contents

- `PBS_Utah_EDA_Corrected.Rmd` - reproducible R Markdown source with code shown.
- `PBS_Utah_EDA_Corrected.html` - rendered HTML notebook for review or submission.
- `PBS_Utah_Decision_Tree_Modeling.qmd` - Quarto source for the major-donor model comparison.
- `PBS_Utah_Decision_Tree_Modeling.html` - rendered HTML report for review or submission.

## Project question

The analysis investigates how PBS Utah can identify constituents who are most likely to make a major gift. It examines data quality, historical giving, recency and frequency, solicitation response, and potential leakage before model building.

The modeling report evaluates a logistic-regression benchmark against a tuned decision tree for ranking future major-donor prospects. Both models use the same time-safe features and expanding-window chronological validation. Average precision is the primary selection metric, supplemented by PR AUC, ROC AUC, calibration metrics, and top-ranked prospect lift.

In the current report, logistic regression is the preferred model: it produces substantially stronger prospect rankings, while the tuned decision tree collapses to a root-only model with constant scores. The FY2025-to-FY2026 period remains reserved for the final group evaluation.

## Data

The raw synthetic donor data are not stored in this repository. Obtain the authorized project data separately and place the files in a `data/` folder within the cloned repository. Required files are:

```text
data/
|-- constituents_w_memberships.csv
|-- unite_payments.txt
|-- soft_credits.csv
|-- campaign_members.txt
|-- team_approach_legacy_payments.txt
`-- passport_viewing.txt
```

The decision-tree report reads the prebuilt analytic panel at `data/donor_panel_time_safe.csv`. This derived file is excluded from the repository because it is based on the authorized project data.

## Reproducing the analysis

1. Open `PBS_Utah_EDA_Corrected.Rmd` in RStudio or Positron.
2. Install required packages if needed:

   ```r
   install.packages(c("data.table", "ggplot2", "scales", "knitr", "rmarkdown"))
   ```

3. Place the authorized data in `data/`, or set the `data_dir` parameter to its location.
4. Render the notebook to regenerate the HTML output.

To reproduce the decision-tree report, install Quarto plus `tidyverse`, `tidymodels`, `rpart`, `rpart.plot`, `knitr`, and `scales`. Place `donor_panel_time_safe.csv` in `data/`, then run:

```powershell
quarto render PBS_Utah_Decision_Tree_Modeling.qmd
```

## AI use

ChatGPT Codex assisted with repository and schema inspection, reproducible R code, EDA structure, and data-quality and leakage checks. Results and interpretations were verified against the supplied data dictionary, source schemas, and computed notebook output.
