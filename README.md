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

## 📖 Table of Contents
- [📖 Table of Contents](#-table-of-contents)
- [📍 Overview](#-overview)
- [📂 Repository Structure](#-repository-structure)
- [📄 License](#-license)
- [👏 Acknowledgments](#-acknowledgments)

---

## 📍 Overview

This repository contains the code used to perform the assessments in the submitted contribution 
"*PULPO: A framework for efficient integration of life cycle inventory models into life cycle product optimization*"

The code for creating the Figures as post-processing of the assessment results can also be found here.

---


## 📂 Repository Structure

```sh
└── pulpo_methanol_case/
    ├── Code/
    │   ├── 00_install_methanol_case_study_db.ipynb
    │   ├── 01_methanol_case_study.ipynb
    │   ├── 02_methanol_demand_loop.ipynb
    │   ├── 03_methanol_other_indicator.ipynb
    │   ├── 04_decrypt_iam_output.ipynb
    │   └── 05_pulpo_install_premise_dbs.ipynb
    └── Figures/
        ├── Figure_5.ipynb
        ├── Figure_6.ipynb
        ├── Figure_7.ipynb
        ├── Figure_S1.ipynb
        ├── Figure_S6.ipynb
        ├── Figure_S7.ipynb
        ├── Figure_S7_pie.ipynb
        ├── Input/
        └── Output/
```
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
