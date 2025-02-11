# Demographics-Related Code Sets Translations to OMOP CDM Standard Concepts

This directory contains translations of various demographics-related code sets to OMOP CDM standard concepts.  
Below is a brief description of each code set and the corresponding CSV files located in this directory.

All mappings in these CSV files were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

## Code Sets

### 1. Education Codes
These codes represent the highest education acquired.
Codes are taken from the [classifications portal](https://klassifikaatorid.stat.ee/) managed by Statistics Estonia, see [here](https://klassifikaatorid.stat.ee/item/stat.ee/1e38c151-38ae-4be3-ab46-a591c0096b99/5).
The classification of acquired highest education is based on the International Standard Classification of Education ISCED-A 2011 and it contains only the possible levels of education acquired in Estonia. 
The code contains the letter "A" plus a one- to two-digit number. 

- **File:** [education_mappings](education_mappings.csv)
- **Description:** This file contains a list of codes representing the highest education acquired, along with their mappings to OMOP CDM standard concepts.

### 2. Language Codes
These codes represent the classification of languages. 
Codes are taken from the [classifications portal](https://klassifikaatorid.stat.ee/) managed by Statistics Estonia, see [here](https://klassifikaatorid.stat.ee/item/stat.ee/e42103c7-6fc6-4c66-921f-c46fbcfef205/11).
Codes have been developed on the basis of the international standard Codes for the Representation of Names of Languages ISO 639-2. 
Each language has been assigned a three-digit letter code.

- **File:** [language_mappings](language_mappings.csv)
- **Description:** This file contains a list of codes representing the main spoken language, along with their mappings to OMOP CDM standard concepts.

### 3. Marital Status Codes
These codes represent the classification of the actual marital status.
Codes are taken from the [Publishing Centre](https://pub.e-tervis.ee/classifications) managed by Health and Welfare Information Systems Centre (TEHIK), see [here](https://pub.e-tervis.ee/classifications/Tegelik%20perekonnaseis).
The description of the codes is slightly modified.

- **File:** [marital_status_mappings](marital_status_mappings.csv)
- **Description:** This file contains local codes for actual marital status, along with their mappings to OMOP CDM standard concepts.


## The Structure of Mapping files
Each CSV file contains the following columns:

- **source_code:** The original code or concept from the respective code set. The source code being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code (e.g., education, language, marital_status).
- **source_code_description:** A brief description of the source code.
- **source_name_eng:** A brief description of the source code in English, only for Education and Language codes.

- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Observation).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Clinical Finding).

- **updated_date:** The date when the mapping was last updated.
- **valid_end_date:** The date until which the mapping is valid.

## How to Use
1. Clone the repository to your local machine.
2. Navigate to the specific directory to access the CSV files.
3. Use the files to map your local data to the OMOP CDM standard concepts.

## Contributions
Contributions are welcome! Please create a pull request or open an issue to discuss any changes or additions.

## License
Estonian OMOP Mappings © 2024 by Health Informatics Lab, University of Tartu is licensed under CC BY 4.0. See the [LICENSE](../LICENSE.txt) for more details.
