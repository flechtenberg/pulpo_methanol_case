# README for Code and Data Folders

Get back to main [readme.md](..\README.md)

## Code Folder

This folder contains various Jupyter notebooks used for different stages of the methanol case study assessment and data processing.

**00_install_methanol_case_study_db.ipynb**
- **Description**: Installs the methanol case study databases.
- **Purpose**: Prepares the databases needed for the methanol case study.
- **Inputs**: 
  - Prospective Ecoinvent databases generated via premise in brightway2, specified via the "project", "database", and "iam" strings.
- **Outputs**: 
  - Modified databases with added carbon capture, CO2 synthesis, etc. processes. These modified databases are stored in Brightway2; no external output is generated.
- **Note**:
  - For the results presented in the manuscript, the following databases were used:
    - `Base 2040`
    - `NDC 2040`
    - `PkBudg500 2040`
    - `PkBudg500 2050`
    - `PkBudg500 2030`

**01_methanol_case_study.ipynb**
- **Description**: Main methanol case study assessment.
- **Purpose**: Contains the main results for each scenario and year, detailing the selected optimal technology, the amount of methanol produced, and related metrics.
- **Inputs**: 
  - Project, scenario, year, and database. These are the databases produced with the `00_install_methanol_case_study_db.ipynb` notebook.
  - Performs all necessary assessment steps (calculation of reference, with and without electricity, and optimization with electricity bound, including optional loop over electricity bound).
- **Outputs**: 
  - `meoh_only_meoh.xlsx`, `meoh_with_elec.xlsx`, and `meoh_results.xlsx` containing the detailed results for reference, reference with electricity, and optimized results.

**02_methanol_full_abatement.ipynb**
- **Description**: Full abatement case study for methanol.
- **Purpose**: Generates results for the full abatement case with varying demand values.
- **Inputs**: 
  - Project, scenario, year, and database. These are the databases produced with the `00_install_methanol_case_study_db.ipynb` notebook.
  - Performs all necessary assessment steps (calculation of reference, with and without electricity, and optimization with electricity bound, including optional loop over electricity bound).
- **Method**: Instead of using a specified electricity bound as a constraint, an algorithm is implemented to find the electricity bound value that just reaches full abatement (given a final demand).
- **Outputs**: 
  - Results are stored in `results_meoh_case_demand.xlsx`.

**03_methanol_other_indicator.ipynb**
- **Description**: Generates additional impact category results.
- **Purpose**: Produces unmodified optimization results for various impact categories when minimizing GWP.
- **Inputs**: 
  - Project, scenario, year, and database. These are the databases produced with the "00_install_methanol_case_study_db.ipynb" notebook.
  - Performs all necessary assessment steps (calculation of reference, with and without electricity, and optimization with electricity bound, including optional loop over electricity bound).
- **Method**: Calculates alongside the GWP the following indicators:
  - `('IPCC 2013', 'climate change', 'GWP 100a, incl. H and bio CO2')`
  - `('ReCiPe Endpoint (H,A)', 'total', 'total')`
  - `('ReCiPe Endpoint (H,A)', 'ecosystem quality', 'total')`
  - `('ReCiPe Endpoint (H,A)', 'resources', 'total')`
  - `('ReCiPe Endpoint (H,A)', 'human health', 'total')`
  - `('EF v3.0', 'acidification', 'accumulated exceedance (ae)')`
  - `('EF v3.0', 'ecotoxicity: freshwater', 'comparative toxic unit for ecosystems (CTUe) ')`
  - `('EF v3.0', 'energy resources: non-renewable', 'abiotic depletion potential (ADP): fossil fuels')`
  - `('EF v3.0', 'eutrophication: freshwater', 'fraction of nutrients reaching freshwater end compartment (P)')`
  - `('EF v3.0', 'eutrophication: marine', 'fraction of nutrients reaching marine end compartment (N)')`
  - `('EF v3.0', 'eutrophication: terrestrial', 'accumulated exceedance (AE) ')`
  - `('EF v3.0', 'human toxicity: carcinogenic', 'comparative toxic unit for human (CTUh) ')`
  - `('EF v3.0', 'human toxicity: non-carcinogenic', 'comparative toxic unit for human (CTUh) ')`
  - `('EF v3.0', 'ionising radiation: human health', 'human exposure efficiency relative to u235')`
  - `('EF v3.0', 'land use', 'soil quality index')`
  - `('EF v3.0', 'material resources: metals/minerals', 'abiotic depletion potential (ADP): elements (ultimate reserves)')`
  - `('EF v3.0', 'ozone depletion', 'ozone depletion potential (ODP) ')`
  - `('EF v3.0', 'particulate matter formation', 'impact on human health')`
  - `('EF v3.0', 'photochemical ozone formation: human health', 'tropospheric ozone concentration increase')`
  - `('EF v3.0', 'water use', 'user deprivation potential (deprivation-weighted water consumption)')`
  - Also, loops over final demand.
- **Outputs**: 
  - Unmodified optimization results for the specified indicators.

**04_decrypt_iam_output.ipynb**
   - **Description**: Decrypts IAM output files.
   - **Purpose**: Decrypts files using the `Fernet` package and a premise key to access raw data.

**05_pulpo_install_premise_dbs.ipynb**
   - **Description**: Installs premise databases.
   - **Purpose**: Sets up the databases required for the study using the `premise` package.

## Data Sub-Folder

This folder contains the necessary files and subdirectories for data processing and analysis.

**premise-key.txt**
   - **Description**: Text file to store the user's premise key.
   - **Purpose**: Needed for decrypting IAM output files using the notebook `04_decrypt_iam_output.ipynb`.

**results** (folder)
   - **Description**: Empty folder intended for storing results.
   - **Purpose**: To be populated with results generated from the various notebooks.

**raw** (folder)
   - **Description**: Contains subfolders for raw data.
   - **Structure**:
     - **decrypted**: Empty folder where decrypted files will be stored.
     - **encrypted**: Folder containing encrypted IAM output files.

**remind_SSP2-Base.csv**
   - **Description**: Encrypted IAM output for the Base scenario.
   - **Purpose**: Needs to be decrypted using `04_decrypt_iam_output.ipynb`.

**remind_SSP2-NDC.csv**
   - **Description**: Encrypted IAM output for the NDC scenario.
   - **Purpose**: Needs to be decrypted using `04_decrypt_iam_output.ipynb`.

**remind_SSP2-PkBudg500.csv**
   - **Description**: Encrypted IAM output for the PkBudg500 scenario.
   - **Purpose**: Needs to be decrypted using `04_decrypt_iam_output.ipynb`.

## How to Use

1. **Decrypt IAM Output Files**
   - Ensure you have a valid premise key and insert it into `premise-key.txt`.
   - Run `04_decrypt_iam_output.ipynb` to decrypt the encrypted IAM output files in the `raw/encrypted` folder. The decrypted files will be stored in `raw/decrypted`.

2. **Install Premise Databases**
   - Use `05_pulpo_install_premise_dbs.ipynb` to install the required premise databases.

3. **Prepare the Database**
   - Run `00_install_methanol_case_study_db.ipynb` to install the methanol case study database.

4. **Main Case Study Assessment**
   - Use `01_methanol_case_study.ipynb` for the main methanol case study assessment.

5. **Full Abatement Case Study**
   - Run `02_methanol_full_abatement.ipynb` to generate results for the full abatement case.

6. **Additional Impact Categories**
   - Use `03_methanol_other_indicator.ipynb` to generate results for additional impact categories.
