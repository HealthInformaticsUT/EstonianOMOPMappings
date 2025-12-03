# Death-Related Code Sets Translations to OMOP CDM Standard Concepts

This directory contains translations of various death-related code sets to OMOP CDM standard concepts. 

Below is a brief description of each code set, along with the corresponding CSV files located in this directory.

All mappings in these CSV files were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

## Code Sets

### 1. Death Circumstances Codes
These concepts represent the classification of the death circumstances, i.e. the information about the event that led to the death.
Codes are taken from the [Publishing Centre](https://pub.e-tervis.ee/classifications) managed by Health and Welfare Information Systems Centre (TEHIK), see [here](https://pub.e-tervis.ee/classifications/Surma%20tinginud%20asjaolu/1).


- **File:** [death_circumstances_mappings](death_circumstances_mappings.csv)
- **Description:** This file contains a list of codes representing the death circumstances, along with their mappings to OMOP CDM standard concepts.

### 2. Death Location Codes
These codes represent the classification of the location where the person died. 
Codes are taken from the [Publishing Centre](https://pub.e-tervis.ee/classifications) managed by Health and Welfare Information Systems Centre (TEHIK), see [here](https://pub.e-tervis.ee/classifications/Suremispaik/1).


- **File:** [death_location_mappings](death_location_mappings.csv)
- **Description:** This file contains a list of codes representing the location where the person died, along with their mappings to OMOP CDM standard concepts.


## The Structure of Mapping files
Each CSV file contains the following columns:

- **source_code:** The original code or concept from the respective code set. The source code is being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code (e.g., death_circumstances, death_location).
- **source_code_description:** A brief description of the source code.
- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Observation, Condition).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Clinical Finding, Event).
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
