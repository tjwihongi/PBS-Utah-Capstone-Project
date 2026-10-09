# PBS Utah Major-Gift Prospecting: Individual EDA

This repository contains Tama Wihongi's individual exploratory data analysis (EDA) contribution for the PBS Utah major-gift prospecting capstone project.

## Contents

- `PBS_Utah_EDA_Corrected.Rmd` — reproducible R Markdown source with code shown.
- `PBS_Utah_EDA_Corrected.html` — rendered HTML notebook for review or submission.

## Project question

The analysis investigates how PBS Utah can identify constituents who are most likely to make a major gift. It examines data quality, historical giving, recency and frequency, solicitation response, and potential leakage before model building.

## Data

The raw synthetic donor data are not stored in this repository. Obtain the authorized project data separately and place the files in a `data/` folder within the cloned repository, or supply a different folder with the notebook's `data_dir` render parameter. Required files are:

```text
data/
├── constituents_w_memberships.csv
├── unite_payments.txt
├── soft_credits.csv
├── campaign_members.txt
├── team_approach_legacy_payments.txt
└── passport_viewing.txt
```

## Reproducing the analysis

1. Open `PBS_Utah_EDA_Corrected.Rmd` in RStudio or Positron.
2. Install required packages if needed:

   ```r
   install.packages(c("data.table", "ggplot2", "scales", "knitr", "rmarkdown"))
   ```

3. Place the authorized data in `data/`, or set the `data_dir` parameter to its location.
4. Render the notebook to regenerate the HTML output.

## AI use

ChatGPT Codex assisted with repository and schema inspection, reproducible R code, EDA structure, and data-quality and leakage checks. Results and interpretations were verified against the supplied data dictionary, source schemas, and computed notebook output.
