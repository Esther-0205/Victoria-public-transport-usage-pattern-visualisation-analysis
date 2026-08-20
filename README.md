This repository contains a data visualisation project proposal analysing how
public transport patronage in Victoria, Australia changed between January 2018
and June 2026. The project focuses on differences across metropolitan and
regional services, transport modes, and seasonal usage patterns.

The analysis uses monthly patronage data from the Victorian Government's Data
Vic portal and prepares the data for exploratory visualisations in R.

Aim of the project:

The main research question is:

> How have public transport usage patterns changed across Victoria over time,
> and how do these patterns differ by location, transport mode, and season?

The project is designed for transport planners, policymakers, and people
interested in public transport demand across Victoria.

 Proposed Questions

- Which transport modes recovered most strongly after the 2020-2021 decline?
- Which modes remain below the 2018-2019 pre-pandemic level?
- How do metropolitan and regional public transport patterns differ over time?
- Are there seasonal differences in public transport patronage?
- Which visualisation methods best communicate differences between large
  metropolitan services and smaller regional services?

Data Source

Dataset: **Monthly public transport patronage by mode**

Source: Department of Transport and Planning, Victorian Government, Data Vic

Coverage: Victoria, Australia

Time period: January 2018 to June 2026

The dataset contains monthly patronage counts for:

- Metropolitan train
- Metropolitan tram
- Metropolitan bus
- V/Line train
- V/Line coach
- Regional bus

Repository Structure

```text
.
├── README.md
├── proposal_code.R
├── Rplots.pdf
└── data/
    └── monthly_public_transport_patronage_by_mode.csv
```

Files

- `proposal_code.R`: R script for loading, cleaning, reshaping, summarising,
  and visualising the patronage dataset.
- `data/monthly_public_transport_patronage_by_mode.csv`: Main dataset used in
  the project.
- `Rplots.pdf`: Generated plots from the R script.

Data Dictionary

| Column | Description |
| --- | --- |
| `Year` | Calendar year of the observation. |
| `Month` | Month number, from 1 to 12. |
| `Month name` | Month name written as text. |
| `Metropolitan train` | Monthly patronage for metropolitan trains. |
| `Metropolitan tram` | Monthly patronage for metropolitan trams. |
| `Metropolitan bus` | Monthly patronage for metropolitan buses. |
| `V/Line train` | Monthly patronage for regional V/Line trains. |
| `V/Line coach` | Monthly patronage for regional V/Line coaches. |
| `Regional bus` | Monthly patronage for regional buses. |

Method

The R script:

The analysis follows these steps:

1. Load the roadworks dataset.
2. Check the dataset dimensions, including the number of rows and columns.
3. Inspect variable names and variable types.
4. Check for missing values in each column.
5. Summarise key categorical variables such as status, category, type, street name, and direction.
6. Convert date columns into proper date format if needed.
7. Create visualisations to explore roadwork patterns by category, status, location, and time period.

Visualisations

The project currently includes:

- Monthly patronage trends by transport mode.
- Metropolitan versus regional patronage over time.

The proposal also identifies further visualisation directions, including:

- Annual total patronage by year.
- Total patronage by transport mode.
- Seasonal average patronage.
- Indexed recovery charts comparing post-2020 patronage with the 2018-2019
  baseline.

Main Insights From Initial Exploration

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

Requirements

The analysis uses R and the following packages:

- `tidyverse`
- `lubridate`
- `scales`

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

Notes

- The 2026 data only includes January to June, so 2026 should not be compared
  directly with full-year totals.
- One regional bus value is missing for November 2024 and should be considered
  when interpreting regional service patterns.
- Regional bus values are parsed as numeric during cleaning to support summary
  statistics and plotting.
