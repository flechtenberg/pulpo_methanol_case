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
</div>

---

## 📖 Table of Contents
- [📖 Table of Contents](#-table-of-contents)
- [📍 Overview](#-overview)
- [📂 Repository Structure](#-repository-structure)
- [⚙️ Modules](#modules)
- [📄 License](#-license)
- [👏 Acknowledgments](#-acknowledgments)

---


## 📍 Overview

This repository contains the code used to perform the assessments in the submitted contribution 
"*Python-based User-defined Lifecycle Product Optimization (PULPO) framework: Application to carbon capture and utilization*"

The code for creating the Figures as post-processing of the assessment results can also be found here.

---


## 📂 Repository Structure

```sh
└── pulpo_methanol_case/
    ├── Code/
    │   ├── .ipynb_checkpoints/
    │   ├── 00_install_methanol_case_study_db.ipynb
    │   ├── 01_methanol_case_study.ipynb
    │   ├── 02_methanol_demand_loop.ipynb
    │   ├── 03_methanol_other_indicator.ipynb
    │   ├── 04_decrypt_iam_output.ipynb
    │   └── 05_pulpo_install_premise_dbs.ipynb
    └── Figures/
        ├── .ipynb_checkpoints/
        ├── Figure_3.ipynb
        ├── Figure_4.ipynb
        ├── Figure_4_pie.ipynb
        ├── Figure_5.ipynb
        ├── Figure_6.ipynb
        ├── Figure_S1.ipynb
        ├── Figure_S2.ipynb
        ├── Input/
        └── Output/
```


---

## ⚙️ Modules

<details closed><summary>Root</summary>

| File                                                                                                                                                                                           | Summary                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ---  | ---  | 
| [00_install_methanol_case_study_db.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Code/00_install_methanol_case_study_db.ipynb)                                          | This code installs the new carbon capture and methanol synthesis inventories on top of the premise databases.                                                                                                                                                                                                                                                                                   |
| [01_methanol_case_study.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Code/01_methanol_case_study.ipynb)                                                                | This code performs a base GWP minimization for a given epsilon, including all necessary reference calculations.                                                                                                                                                                                                                                                                                  |
| [02_methanol_demand_loop.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Code/02_methanol_demand_loop.ipynb)                                                              | This code calculates the full abatement scenario.                                                                                                                                                                                                                                                                                  |
| [03_methanol_other_indicator.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Code/03_methanol_other_indicator.ipynb)                                                      | This code performs a base GWP minimization while calculating a range of alternative environmental indicators simultaneously.                                                                                                                                                                                                                                                                                  |
| [04_decrypt_iam_output.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Code/04_decrypt_iam_output.ipynb)                                                                  | This code imports encrypted IAM results, decrypts them using a provided key, and then saves the decrypted data as separate CSV files for further analysis.                                                                                                                                                                                                                                                                                  |
| [05_pulpo_install_premise_dbs.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Code/05_pulpo_install_premise_dbs.ipynb)                                                    | The code installs selected premise databases in a specified project, extracts IAM scenarios, updates ecoinvent activities, and saves the changes to Brightway. Additionally, it installs a modified IPCC2013 method with added characterization factors.                                                                                                                                                                                    |
| [Figure_3.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Figures/Figure_3.ipynb)                                                                                         | The code in the provided Jupyter notebook generates Figure 3 for a selected scenario. It imports necessary libraries, prepares data, and plots the figure. The figure displays the distribution of different technologies (BAU, DAC, PSC) for methanol production and their electricity requirements. The figure also shows the reduction in greenhouse gas emissions. The resulting figure is saved as both a PNG image and an Excel file. |
| [Figure_4.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Figures/Figure_4.ipynb)                                                                                         | This code generates Figure 4 for three selected scenarios. It imports data, interpolates values, prepares data for plotting, and creates a bar chart with stacked bars representing methanol production and a line chart indicating additional electricity. It saves the figure as an image and outputs the interpolated data.                                                                                                              |
| [Figure_5.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Figures/Figure_5.ipynb)                                                                                         | This code generates Figure 5 for a specified scenario and year (Regionalized)                                                                      |
| [Figure_6.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Figures/Figure_6.ipynb)                                                                                         | This code generates Figure 6 for a specified scenario and year (Demand). It imports necessary libraries, prepares data from an Excel file, calculates production ratios, and plots the results. The figure includes stacked area plots of methanol production and a line plot of DAC/PSC ratio. The final figure is saved as an image, and the data is saved in an Excel file.                                                                       |
| [Figure_S1.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Figures/Figure_S1.ipynb)                                                                                       | The code generates Figure S1, which shows visualizes a minimal working example of PULPO.                                                                                                                                                                                                                                                                                              |
| [Figure_S2.ipynb](https://github.com/flechtenberg/pulpo_methanol_case/blob/main/Figures/Figure_S2.ipynb)                                                                                       | The code generates Figure S2, whcih visualizes the evolution of the electricity mixes in the three selected scenarios.                                                                                                                                                                                                                                                                                                |

</details>

---

### 🤖 Running pulpo_methanol_case
To run the assessments you may create a new conda environment e.g. "*pulpo_methanol_case*" and install the requirements:

```sh
pip install -r requirements.txt
```

Furthermore, you will need to have the [PULPO](https://github.com/flechtenberg/pulpo) package in the same directory as this folder. In future versions, once PULPO is in the pypi index, a new requirement for pip installing pulpo will be added.


---

## 📄 License

This project is licensed under the `ℹ️  BSD 3-Clause` License. See the [LICENSE](LICENSE) file for additional info.
Copyright (c) 2023, Fabian Lechtenberg. All rights reserved.

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
