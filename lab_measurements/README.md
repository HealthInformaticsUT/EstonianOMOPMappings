# Lab Measurements-Related Code Sets Translations to OMOP CDM Standard Concepts

This directory contains translations of various lab measurements-related code sets to OMOP CDM standard concepts.  
Below is a brief description of each code set, along with the corresponding CSV files located in this directory.

## Code Sets

### 1. LOINC codes
These codes represent the laboratory test codes from the LOINC (Logical Observation Identifiers Names and Codes) standard.

Codes are sourced from a [web application]((https://elhr.digilugu.ee/data/algandmedList.html)) that is managed by Health and Welfare Information Systems Centre (TEHIK), and which describes all laboratory tests performed in Estonia and their corresponding LOINC codes.
Mappings are sourced from [Athena](https://athena.ohdsi.org/search-terms/start), a repository for Standardized Vocabularies maintained 
by OHDSI (Observational Health Data Sciences and Informatics). 

Additionally, we have supplemented the LOINC codes from Athena with additional LOINC codes:
- *local codes*, starting with 'L-' and, 
- *temporary codes*, starting with 'A-'.

Temporary codes are used for analyses that do not have an official LOINC code in the international LOINC classification. 
These temporary codes may become official LOINC codes if requested from the Regenstrief Institute and added to the international LOINC classification. 
Local codes are intended solely for use within Estonia and are mostly used to label test panels. 
Official LOINC codes are not requested for local codes, and such codes do not become official LOINC codes.


- **File:** [loinc_mappings](loinc_mappings.csv)
- **Description:** This file contains a list of LOINC codes, along with their mappings to OMOP CDM standard concepts. The list currently includes only LOINC codes used in Estonia.


### 2. LOINC Answer Codes
These codes represent the possible answers or results associated with LOINC tests. 

Codes and mappings are sourced from [Athena](https://athena.ohdsi.org/search-terms/start), a repository for Standardized Vocabularies maintained 
by OHDSI (Observational Health Data Sciences and Informatics). 

- **File:** [loinc_answer_mappings](loinc_answer_mappings.csv)
- **Description:** This file contains a list of LOINC codes, their possible answers, the standardised answers found in Estonian health data, and their mappings to OMOP CDM standard concepts.


### 3. Other measurements-related concepts
These concepts relate to measurements (e.g., Body mass index, Systolic blood pressure, etc.) that are extracted and classified from Estonian medical texts.

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

- **File:** [custom_concepts_mappings](custom_concepts_mappings.csv)
- **Description:** This file contains a list of concepts related to measurements, along with their mappings to OMOP CDM standard concepts.


## The Structure of Mapping files
### LOINC Codes CSV File Structure
CSV files for LOINC codes and other measurement-related mappings contain the following columns:

- **source_code:** The original code or concept from the respective code set. The source code is being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code (e.g., loinc, custom).
- **source_code_description:** A brief description of the source code.


- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Measurement).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Lab Test, Clinical Observation, Observable Entity).


- **updated_date:** The date when the mapping was last updated.
- **valid_end_date:** The date until which the mapping is valid.

### LOINC Answers CSV File Structure

The CSV file for LOINC Answers contains the following columns:

- **loinc_code:** The LOINC code corresponding to the laboratory test.
- **loinc_name_est:** The name in Estonian that corresponds to the LOINC code.
- **loinc_concept_name:** The name that corresponds to the LOINC code in OMOP CDM.
- **loinc_concept_id:** The unique identifier of the Concept related to the LOINC code.
- **loinc_answer_standardised_est:** The standardised answer for the LOINC code found in Estonian health data.
- **answer_concept_id_name:** Lists all available and allowed answers related to the LOINC code. If both attributes exist (`loinc_answer_standardised_est` and `answer_concept_id_name`), this column shows the mapping between `loinc_answer_standardised_est` and `answer_concept_id_name`.
- **answer_concept_id:** The unique identifier of the target Concept to which the answer is being mapped.
- **answer_concept_code:** The target Concept code to which the answer is being mapped.


## How to Use
1. Clone the repository to your local machine.
2. Navigate to the specific directory to access the CSV files.
3. Use the files to map your local data to the OMOP CDM standard concepts.

## Contributions
Contributions are welcome! Please create a pull request or open an issue to discuss any changes or additions.

## License
Estonian OMOP Mappings © 2024 by Health Informatics Lab, University of Tartu is licensed under CC BY 4.0. See the [LICENSE](../LICENSE.txt) for more details.
