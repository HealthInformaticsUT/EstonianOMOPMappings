# Healthcare Providers-Related Code Sets Translations to OMOP CDM Standard Concepts

This directory contains translations of healthcare providers-related code sets to OMOP CDM standard concepts.  
Below is a brief description of each code set and the corresponding CSV files located in this directory.

## Code Sets

### 1. Specialties Codes
These codes represent the classification of the healthcare professionals' specialties.
Codes are taken from the [Publishing Centre](https://pub.e-tervis.ee/classifications) managed by Health and Welfare Information Systems Centre (TEHIK), see [here](http://pub.e-tervis.ee/classifications/Erialad).

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

- **File:** [specialties_mappings](specialties_mappings.csv)
- **Description:** This file contains a list of codes representing the healthcare professionals' specialties, along with their mappings to OMOP CDM standard concepts.


## The Structure of Mapping files
Each CSV file contains the following columns:

- **source_code:** The original code or concept from the respective code set. The source code being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code (e.g., specialties).
- **source_code_description:** A brief description of the source code.
- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Provider).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Physician Specialty, Provider).
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
