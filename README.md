# PBS Utah Donor Prediction: Individual EDA

This repository contains Tama Wihongi's individual exploratory data analysis (EDA) contribution for a PBS Utah donor-prediction capstone project.

## Contents

- `Tama Wihongi EDA.Rmd` — reproducible R Markdown source, with code shown.
- `Tama Wihongi EDA.html` — rendered HTML notebook for review or submission.

## Project question

The analysis frames the problem as predicting whether a constituent will make credited giving in FY2026, using only information available at the end of FY2025. It examines data quality, giving patterns, recent donor behavior, solicitation response, and potential leakage before model building.

## Data

The raw synthetic donor data are not stored in this repository. Obtain the authorized project data separately and place the files in the same folder layout expected by the notebook. The current local setup uses:

```text
Capstone 1/
├── Tama Wihongi EDA.Rmd
├── constituents_w_memberships.csv
├── unite_payments.txt
├── soft_credits.csv
├── campaign_members.txt
├── team_approach_legacy_payments.txt
└── passport_viewing.txt
```

If your data are in another location, change the `table_dir` value in the notebook's setup chunk before rendering.

## Reproducing the analysis

1. Open `Tama Wihongi EDA.Rmd` in RStudio or Positron.
2. Install required packages if needed:

   ```r
   install.packages(c("data.table", "ggplot2", "scales", "knitr", "rmarkdown"))
   ```

3. Confirm `table_dir` points to the folder containing the raw files.
4. Render the notebook to regenerate the HTML output.

## AI use

ChatGPT Codex assisted with repository/documentation inspection, reproducible R code, EDA structure, and data-quality and leakage checks. Results and interpretations were verified against the supplied data dictionary, CSV schemas, and computed notebook output.
