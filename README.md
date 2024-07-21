<div align="center">
<h1 align="center">
<br>pulpo_methanol_case</h1>
<h3>◦ Developed with the software and tools below.</h3>

<p align="center">
<img src="https://img.shields.io/badge/Jupyter-F37626.svg?style&logo=Jupyter&logoColor=white" alt="Jupyter" />
</p>
<img src="https://img.shields.io/github/license/flechtenberg/pulpo_methanol_case?style=flat&color=5D6D7E" alt="GitHub license" />
<img src="https://img.shields.io/github/last-commit/flechtenberg/pulpo_methanol_case?style=flat&color=5D6D7E" alt="git-last-commit" />
<img src="https://img.shields.io/github/commit-activity/m/flechtenberg/pulpo_methanol_case?style=flat&color=5D6D7E" alt="GitHub commit activity" />
<img src="https://img.shields.io/github/languages/top/flechtenberg/pulpo_methanol_case?style=flat&color=5D6D7E" alt="GitHub top language" />
</p>
<a href="https://zenodo.org/badge/latestdoi/700827165"><img src="https://zenodo.org/badge/700827165.svg" alt="DOI"></a>
</div>

---

## Repository Structure

This repository supports the CCU case study presented in the manuscript "**PULPO: A framework for efficient integration of life cycle inventory models into life cycle product optimization**" published in the *Journal of Industrial Ecology*. It is structured as follows:

### Code Folder
This folder contains all the necessary notebooks and input data to reproduce the case study. This involves:
- Generating the necessary inputs from premise.
- Installing premise databases.
- Adapting them to the production system of the case study (including CO2 capture, etc.).
- Running the optimization in the base and full abatement cases.
- Assessing burden shifting using other indicators.

Refer to the readme of the folder ("[readme_code.md](Code/readme_code.md)
") for details on each and every file contained in this folder.

### Figures Folder
This folder contains all the notebooks used to create the figures of the manuscript, using the outputs generated from the **Code Folder** in combination with a few additional inputs. Refer to the readme of the folder ("[readme_figures.md](Figures/readme_figures.md)") for details on each and every file contained in this folder.

### Main Folder
The main folder contains the numeric data that underlies every figure in the manuscript. Below is a brief explanation of each file:

#### Figures 4
- **Figure_4_Base.csv**
- **Figure_4_NDC.csv**
- **Figure_4_PkBudg500.csv**
  - **Description**: For a given epsilon, these files contain the quantities of methanol produced with PSC, DAC, BAU, and the necessary additional electricity.
  - **Columns**: `Epsilon [-]`, `PSC [Mt]`, `DAC [Mt]`, `BAU [Mt]`, `Electricity [TWh]`

#### Figures 5
- **Figure_5_2030.csv**
- **Figure_5_2040.csv**
- **Figure_5_2050.csv**
  - **Description**: For the different years (noted by the year in the file title), these files contain the optimal production quantities by technology in each region.
  - **Rows**: Regions
  - **Columns**: `PSC`, `DAC`, `Total CCU meoh production`

#### Figure 6
- **Figure_6.csv**
  - **Description**: Contains data for each demand, for each region indicating the employed tech and production values with PSC, DAC, or BAU.
  - **Columns**: `scenario`, `year`, `epsilon [%]`, `demand [Mt]`, `region`, `tech`, `meoh [Mt]`, `elec [TWh]`, `net-zero GWP [Mt]`, `GWP reduction [Mt]`

#### Figures S1
- **Figure_S1.csv**
- **Figure_S1_constraints.csv**
- **Figure_S1_optima.csv**
  - **Description**: Hypothetical data for the indication of the objective function values, the constraints, and the two optima (constrained and unconstrained).

#### Figures S3
- **Figure_S3_biosphere.csv**
- **Figure_S3_outcomes.csv**
- **Figure_S3_technosphere.csv**
  - **Description**: Data for the bar charts, comparing optimized and non-optimized impacts, technosphere, and biosphere flows.

#### Figures S7
- **Figure_S7_Base.csv**
- **Figure_S7_NDC.csv**
- **Figure_S7_PkBudg500.csv**
  - **Description**: Contains the electricity production technologies for each scenario as indicated by the filename.
  - **Rows**: Years
  - **Columns**: Electricity production technologies

#### Figures S8
- **Figure_S8_additional_electricity.csv**
  - **Description**: Contains the total electricity values and the corresponding epsilon values for each scenario.
  - **Columns**: Scenarios
  - **Rows**: Total electricity values and the corresponding epsilon values

- **Figure_S8_electricity_mix.csv**
  - **Description**: Contains the electricity production technologies as a result of the optimization (in TWh) for the full abatement case.
  - **Columns**: Scenarios
  - **Rows**: Electricity production technologies

- **Figure_S8_meoh_production.csv**
  - **Description**: Contains the methanol production technologies (BAU, PSC, and DAC) for the full abatement case.
  - **Columns**: Scenarios (Base, NDC, PkBudg500)
  - **Rows**: Meoh production technologies
  
Additionally, there is an **[abbreviations.md](abbreviations.md)** file (TBD) which contains all the metadata and abbreviations used within the data and notebooks.

---

### 🤖 Running pulpo_methanol_case
To run the assessments you may create a new conda environment e.g. "*pulpo_methanol_case*" and install the requirements:

```sh
pip install -r requirements.txt
```

One of the requirements is to have the [PULPO](https://github.com/flechtenberg/pulpo) package installed (for this version, use v0.0.4 of PULPO).


---

## 📄 License

This project is licensed under the `ℹ️  BSD 3-Clause` License. See the [LICENSE](LICENSE) file for additional info.
Copyright (c) 2024, Fabian Lechtenberg. All rights reserved.

---

## 👏 Acknowledgments

This publication was created as part of NCCR Catalysis (grant number 180544), a National Centre of Competence in Research funded by the Swiss National Science Foundation. Grant PID2020-116051RB-I00 (CEPI) funded by MCIN/AEI/10.13039/501100011033 and by “ERDF A way of making Europe” is fully acknowledged. Fabian Lechtenberg gratefully acknowledges the “Departament de Recerca i Universitats de la Generalitat de Catalunya” for the financial support of his predoctoral grant FI-2022.

---
## Authors
- [@flechtenberg](https://www.github.com/flechtenberg)
- [@robyistrate](https://www.github.com/robyistrate)
- [@vtulus](https://www.github.com/vtulus)
---
[↑ Return](#Top)
