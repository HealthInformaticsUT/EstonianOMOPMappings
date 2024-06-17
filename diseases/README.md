# Diseases-Related Code Sets Translations to OMOP CDM Standard Concepts

This directory contains translations of various diseases-related code sets to OMOP CDM standard concepts.  
Below is a brief description of each code set and the corresponding CSV files located in this directory.

## Code Sets

### 1. Cancer Staging Codes, TNM Category Codes, etc.
These codes describe cancer staging according to AJCC/UICC (The American Joint Committee on Cancer/The Union for International Cancer Control), 
including clinical stage codes and TNM category codes. Additionally, Gleason Scores and Gradings are provided.

- **File:** [cancer_stages_categories_mappings](cancer_stages_categories_mappings.csv)
- **Description:** This file contains a list of cancer staging codes, along with their mappings to OMOP CDM standard concepts.


### 2. ICD10 Codes
These codes represent the classification of diseases and related health problems. 
Codes and mappings are sourced from [Athena](https://athena.ohdsi.org/search-terms/start), a repository for Standardized Vocabularies maintained 
by OHDSI (Observational Health Data Sciences and Informatics). 
Additionally, we have supplemented the ICD10 codes from Athena with more specific ICD10 codes used in Estonia (e.g., more detailed codes from chapter F00–F99, etc.).

- **File:** [icd10_mappings](icd10_mappings.csv)
- **Description:** This file contains a list of ICD10 codes representing the diseases and health problems, along with their mappings to OMOP CDM standard concepts.


### 3. ICD-O-3 Codes
These codes represent the classification of the International Classification of Diseases for Oncology, 3rd Edition (ICD-O-3)
Codes and mappings are sourced from [Athena](https://athena.ohdsi.org/search-terms/start), a repository for Standardized Vocabularies maintained 
by OHDSI (Observational Health Data Sciences and Informatics). 

- **File:** [icdo3_mappings](icdo3_mappings.csv)
- **Description:** This file contains a list of ICD-O-3 codes, along with their mappings to OMOP CDM standard concepts.


### 4. Pathology-Related Codes
These codes relate to pathology findings from Estonian health data.
Some of them are SNOMED codes, some local pathology codes, etc.

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/). 

- **File:** [pathology_mappings](pathology_mappings.csv)
- **Description:** This file contains a list of pathology-related codes, along with their mappings to OMOP CDM standard concepts.


### 5. Conditions, Symptoms, and Side-Effects from Unstructured Data
These concepts relate to conditions, symptoms, and side-effects that are extracted and classified from Estonian health data.

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

- **File:** [side_effects_mappings](side_effects_mappings.csv)
- **Description:** This file contains a list of concepts related to symptoms and side-effects, along with their mappings to OMOP CDM standard concepts.


## The Structure of Mapping files
Each CSV file contains the following columns:

- **source_code:** The original code or concept from the respective code set. The source code being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code (e.g., cancer, icd10, icdo3, pathology, side_effects).
- **source_code_description:** A brief description of the source code.


- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Condition, Observation, Measurement).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Clinical Finding, Staging/Grading, Morph Abnormality).


- **target_value_concept_name:** The name of the target *value* Concept to which the source code is being mapped (only for ICD10 mappings).
- **target_value_concept_code:** The target *value* Concept code to which the source code is being mapped (only for ICD10 mappings).
- **target_value_concept_id:** The unique identifier of the target *value* Concept to which the source code is being mapped (only for ICD10 mappings).
- **target_value_vocabulary_id:** The identifier of the vocabulary from which the target *value* Concept originates (only for ICD10 mappings).
- **target_value_domain:** The domain in OMOP CDM to which the target *value* Concept belongs (e.g., Condition, Observation, Procedure, Spec Disease Status, Meas Value) (only for ICD10 mappings).
- **target_value_concept_class_id:** The class ID of the target *value* Concept (e.g., Clinical Finding, Event, Qualifier Value) (only for ICD10 mappings).


- **updated_date:** The date when the mapping was last updated.
- **valid_end_date:** The date until which the mapping is valid.

## How to Use
1. Clone the repository to your local machine.
2. Navigate to the specific directory to access the CSV files.
3. Use the files to map your local data to the OMOP CDM standard concepts.

## Contributions
Contributions are welcome! Please create a pull request or open an issue to discuss any changes or additions.

## License
Estonian OMOP Mappings © 2024 by Health Informatics Lab, University of Tartu is licensed under CC BY-NC-SA 4.0. See the [LICENSE](../LICENSE.txt) for more details.
