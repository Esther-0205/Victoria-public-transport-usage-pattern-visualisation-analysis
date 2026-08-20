# Victoria-public-transport-usage-pattern-visualisation-analysis
```

## Files

- `proposal_code.R`: R code for loading, cleaning, summarising, and visualising
  the dataset.
- `data/monthly_public_transport_patronage_by_mode.csv`: Dataset used in the
  proposal.
- `proposal_code.R`: R script for loading, cleaning, reshaping, summarising,
  and visualising the patronage dataset.
- `data/monthly_public_transport_patronage_by_mode.csv`: Main dataset used in
  the project.
- `Rplots.pdf`: Generated plots from the R script.

## Data Dictionary

| `V/Line coach` | Monthly patronage for regional V/Line coaches. |
| `Regional bus` | Monthly patronage for regional buses. |

## How To Run
## Method

Open `proposal_code.R` in RStudio and run the script.
The R script:

The code uses these R packages:
1. Loads the monthly patronage CSV file.
2. Renames columns into a cleaner format.
3. Converts monthly patronage values into numeric format.
4. Creates a date variable from year and month.
5. Reshapes the dataset from wide format to long format.
6. Classifies each mode as either metropolitan or regional.
7. Produces summary statistics by mode and network.
8. Creates visualisations comparing patronage trends over time.

## Visualisations

The project currently includes:

- Monthly patronage trends by transport mode.
- Metropolitan versus regional patronage over time.

The proposal also identifies further visualisation directions, including:

- Annual total patronage by year.
- Total patronage by transport mode.
- Seasonal average patronage.
- Indexed recovery charts comparing post-2020 patronage with the 2018-2019
  baseline.

## Main Insights From Initial Exploration

The initial exploration suggests that public transport patronage was highest in
2018 and 2019, before declining sharply during 2020 and 2021. Patronage began
recovering from 2022 onward, but the 2024 and 2025 totals remained below the
pre-pandemic level.

Metropolitan train recorded the largest total patronage across the period,
followed by metropolitan tram and metropolitan bus. Regional and V/Line services
had smaller totals, so proportional or indexed visualisations may be useful for
comparing changes fairly across service types.

Seasonal averages suggest that patronage is generally higher in autumn and
spring, while summer and winter are lower.

## Requirements

The analysis uses R and the following packages:

- `tidyverse`
- `lubridate`
- `scales`

If needed, install them with:
Install the required packages with:

```r
install.packages(c("tidyverse", "lubridate", "scales"))
```

## How To Run

1. Open the project folder in RStudio.
2. Open `proposal_code.R`.
3. Make sure the dataset is located at:

```text
data/monthly_public_transport_patronage_by_mode.csv
```

4. Run the script.

The script will load the data, prepare it for analysis, print a summary table,
and generate visualisations.

## Notes

The script reshapes the dataset from wide format to long format so that each
transport mode can be compared in the same visualisation. It also parses numeric
patronage values safely in case a value contains accidental text.
- The 2026 data only includes January to June, so 2026 should not be compared
  directly with full-year totals.
- One regional bus value is missing for November 2024 and should be considered
  when interpreting regional service patterns.
- Regional bus values are parsed as numeric during cleaning to support summary
  statistics and plotting.

