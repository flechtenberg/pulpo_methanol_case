# README for Figures Notebooks

Get back to main [readme.md](..\README.md)

This document provides a summary of the main functions, inputs, and outputs for each notebook used to create figures in the project. Also, details the necessary input files, stored in the "Input" folder. Results (figures and processed data) are saved in the "Output" folder.

## Figure 4
- **Notebook**: `Figure_4.ipynb`
- **Main Function**: Creates Figure 4 for a selected scenario related to green methanol production systems.
- **Inputs**:
  - Scenario and year specified in the notebook.
  - Data from `results_meoh_case.xlsx` file in the `Input` directory.
- **Outputs**:
  - Plot saved as `Output/Figure 4 [scenario] [year].png`
  - Processed data saved as `Output/Figure 4 [scenario] [year].xlsx`

## Figure 5
- **Notebook**: `Figure_5.ipynb`
- **Main Function**: Creates Figure 5 for a selected scenario related to green methanol production systems.
- **Inputs**:
  - Scenario and year specified in the notebook.
  - Data from `results_meoh_case.xlsx` file in the `Input` directory.
  - Data from `Ecoinvent_to_PREMISE.xlsx` file in the `Input` directory.
  - Data from `countries.geojson` file in the `Input` directory.
- **Outputs**:
  - Plot saved as `Output/Figure 5 [scenario] [year].png`
  - Processed data saved as `Output/Figure 5 [scenario] [year].xlsx`


## Figure 6
- **Notebook**: `Figure_6.ipynb`
- **Main Function**: Creates Figure 6 for a selected scenario related to green methanol production systems.
- **Inputs**:
  - Scenario and year specified in the notebook.
  - Data from `results_meoh_case_demand.xlsx` file in the `Input` directory.
- **Outputs**:
  - Plot saved as `Output/Figure 6.png`
  - Processed data saved as `Output/Figure 6.xlsx`


## Figure S1
- **Notebook**: `Figure_S1.ipynb`
- **Main Function**: Creates Figure S1.
- **Inputs**:
  - None
- **Outputs**:
  - Plot saved as `Output/Figure S1.png`
  - Processed data saved as `Output/Figure S1.xlsx`


## Figure S3
- **Notebook**: `Figure_S3.ipynb`
- **Main Function**: Creates Figure S3 comparing optimized (minimal GWP) and non-optimized results in selected impact categories.
- **Inputs**:
  - None
- **Outputs**:
  - Plot saved as `Output/Figure S3a`, `Output/Figure S3b`, `Output/Figure S3c`


## Figure S7
- **Notebook**: `Figure_S7.ipynb`
- **Main Function**: Creates Figure S7 showing global electricity production evolution according to selected IAM scenarios.
- **Inputs**:
  - Scenario specified in the notebook.
  - Data from `premise_scenario_report.xlsx` file in the `Input` directory.
- **Outputs**:
  - Plot saved as `Output/Figure S7 [scenario].png`
  - Processed data saved as `Output/Figure S7 [scenario].xlsx`


## Figure S8
- **Notebook**: `Figure_S8.ipynb`
- **Main Function**: Creates Figure S8 showing optimum full abatement methanol production systems in the selected year.
- **Inputs**:
  - Year specified in the notebook.
  - Data from `results_meoh_case.xlsx` file in the `Input` directory.
- **Outputs**:
  - Plot saved as `Output/Figure S8 [year].png`
  - Processed data saved as `Output/Figure S8 [year].xlsx`

## Figure S8 Pie
- **Notebook**: `Figure_S8_pie.ipynb`
- **Main Function**: Creates pie charts for Figure S8 showing the technology shares in the optimum full abatement methanol production systems in the selected year and scenario.
- **Inputs**:
  - Scenario and year specified in the notebook.
  - Data from `premise_scenario_report.xlsx` file in the `Input` directory.
  - Data from `meoh_results_full_abatement_xxx.xlsx` file in the `Input` directory, xxx being a placeholder for the scenario (Base, NDC, or PkBudg500).
- **Outputs**:
  - Pie chart saved as `Output/Figure S8 pie - [scenario]_[year].png`
  - Pie chart data saved as `Output/Figure S8 pie - [scenario]_[year].xlsx`

  # Input Subfolder

## countries.geojson
- **Description**: Geographic data for various countries.
- **Origin**: Obtained from the [datasets/geo-countries GitHub repository](https://github.com/datasets/geo-countries/blob/master/data/countries.geojson), which sources data from [Natural Earth Data](https://www.naturalearthdata.com/). Natural Earth is a community effort to create visually pleasing, well-crafted maps with cartography or GIS software at small scale.
- **License**: MIT License
- **Structure**: 
  - **Format**: GeoJSON
  - **Contents**: Contains geographic shapes and properties for different countries.
  - **Fields**:
    - `name`: The common name for the country.
    - `ISO3166-1-Alpha-3`: Three-letter ISO code of the country.


## Ecoinvent_to_PREMISE.xlsx
- **Description**: Mapping of Ecoinvent processes to REMIND regions using information from the REMIND model in PREMISE.
- **Origin**: Extended using information from the paper "REMIND2.1: transformation and innovation dynamics of the energy-economic system within climate and sustainability limits" (doi: 10.5194/gmd-14-6571-2021), specifically Table B.1.
- **Structure**: 
  - **Format**: Excel
  - **Sheets**: 
    - `REMIND`: Contains region abbreviations in REMIND as columns and countries belonging to each region with abbreviations from Ecoinvent as rows.

## meoh_results_full_abatement_Base / NDC / PkBudg500.xlsx
- **Description**: Full abatement results for the Base / NDC / PkBudg500 scenario in 2040.
- **Origin**: Generated via `02_methanol_full_abatement.ipynb`.
- **Structure**:
  - **Format**: Excel
  - **Sheets**:
    - `impacts`: Final optimized impacts (GWP) and epsilon (2 rows, 2 columns: `Key`, `Value`)
    - `scaling_vector`: Complete optimized scaling vector entries (27593 rows, 3 columns: `ID`, `Activity`, `Value`)
    - `slack`: Empty sheet (0 rows, 3 columns: `ID`, `Activity`, `Value`)
    - `choices`: Optimal choice of technologies (396 rows, multiple columns)
    - `project and db`: Brightway2 and database used (1 row, 2 columns)
    - `demand`: Summary of final demand (13 rows, 2 columns: `Unnamed: 0`, `Demand`)
    - `constraints`: List of constrained processes (0 rows, 2 columns: `Unnamed: 0`, `Demand`)


## premise_scenario_report.xlsx
- **Description**: Report on various scenarios modeled in PREMISE, generated via the premise Python package (**v1.6.7**). Contains the electricity generation values for each scenario, year and region.
- **Origin**: Generated when installing a prospective background database using the premise package (https://github.com/polca/premise).
- **Structure**:
  - **Format**: Excel


## results_meoh_case.xlsx
- **Description**: Main results of the assessment, created via `01_methanol_case_study.ipynb`. Contains data for each calculated scenario and year, including the selected optimal technology, the amount of methanol produced, and related metrics.
- **Origin**: Generated via `01_methanol_case_study.ipynb`.
- **Structure**:
  - **Format**: Excel
  - **Sheets**:
    - `Sheet1`: Contains the main results (6350 rows, 9 columns: `scenario`, `year`, `epsilon [%]`, `region`, `tech`, `meoh [Mt]`, `elec [TWh]`, `net-zero GWP [Mt]`, `GWP reduction [Mt]`)


## results_meoh_case_demand.xlsx
- **Description**: Contains the main results of the methanol case study assessment, targeting the full abatement case for varying demand values. Generated via `02_methanol_full_abatement.ipynb`. For each calculated scenario and year, it includes data for each region and electricity constraint. The file provides information on the selected optimal technology and the amount of methanol produced. Additionally, rows where the region is "methanol" detail the amount of BAU methanol still produced, the electricity used, the GWP necessary for producing the entire methanol demand with BAU methanol, and the GWP reduction achieved by producing methanol via captured CO2.
- **Origin**: Generated via the notebook `02_methanol_full_abatement.ipynb`.
- **Structure**:
  - **Format**: Excel
  - **Sheets**:
    - `Sheet1`: Main results (1225 rows, 10 columns: `scenario`, `year`, `epsilon [%]`, `demand [Mt]`, `region`, `tech`, `meoh [Mt]`, `elec [TWh]`, `net-zero GWP [Mt]`, `GWP reduction [Mt]`)


## results_meoh_case_other_ind.xlsx
- **Description**: Contains additional impact category results for the methanol case study assessment. The first sheet has the unmodified optimization results with various impact categories when minimizing GWP. The second sheet extracts part of this information to elaborate the data in Table S6. This data pertains to the PkBudg500 scenario in the year 2040.
- **Origin**: 
  - `Source` sheet generated via the notebook `03_methanol_other_indicator.ipynb`.
  - `Converted` sheet created manually.
- **Structure**:
  - **Format**: Excel
  - **Sheets**:
    - `Source`: Unmodified optimization results (1275 rows, 20+ columns including `scenario`, `year`, `epsilon [%]`, `region`, `tech`, `meoh [Mt]`, `elec [TWh]`, `net-zero GWP [Mt]`, `GWP reduction [Mt]`, and various impact categories)
    - `Converted`: Extracted data for Table S6 (56 rows, 20+ columns including `net-zero GWP [Mt]`, `GWP reduction [Mt]`, and various impact categories)

