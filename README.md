# Jet Airline Safety Analysis

**Analyst:** Atilio Barreda

## Business question

This project analyzes aviation accident records for an airline/aircraft insurer. The goal is to identify professionally built airplane manufacturers and make/model combinations associated with comparatively low fatal-or-serious injury fractions and low aircraft-destruction rates when an accident occurs.

The analysis follows the client brief by:

- retaining airplanes only;
- excluding amateur-built aircraft;
- using accidents from 1983 onward;
- separating small and large aircraft at 20 people aboard;
- requiring adequate sample sizes before comparing manufacturers or models; and
- examining weather condition and phase of flight as additional safety factors.

## Repository files

- `Aviation_Accidents_Cleaning.ipynb` — loads, inspects, filters, cleans, and transforms the source data; creates the injury and destruction measures; and saves the cleaned CSV.
- `Aviation_Accidents_Data_Analysis.ipynb` — performs grouped descriptive analysis, creates the required visualizations, recommends small and large aircraft makes/models, and examines two additional factors.
- `data/AviationData.csv` — the source CSV already included in the Flatiron starter repository.
- `data/AviationData_cleaned.csv` — generated after running the cleaning notebook.

## Core measures

The main injury metric is:

```text
(fatal injuries + serious injuries) / estimated people aboard
```

Aircraft destruction is represented as a binary variable, allowing the group mean to be interpreted as the destruction rate.

## Analysis and recommendations

The analysis notebook produces separate safety tables and plots for:

- small-aircraft manufacturers;
- large-aircraft manufacturers;
- small-aircraft make/model combinations;
- large-aircraft make/model combinations;
- weather conditions; and
- broad phases of flight.

Recommendations combine mean injury fraction and aircraft-destruction rate and enforce minimum sample sizes. The final recommendation tables are displayed in the analysis notebook.

## Important limitation

The dataset contains accident records rather than all flights or flight hours. The results therefore compare accident severity conditional on a recorded accident; they do not estimate exposure-adjusted accident probability.

## Run order

1. Run `Aviation_Accidents_Cleaning.ipynb`.
2. Run `Aviation_Accidents_Data_Analysis.ipynb`.
