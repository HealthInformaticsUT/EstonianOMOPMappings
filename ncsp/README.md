# Nomesco Classification of Surgical Procedures (NCSP) Translations to OMOP CDM Standard Concepts

This directory contains translations of Nomesco Classification of Surgical Procedures (NCSP) used in Estonia to OMOP CDM standard concepts.  
Below is a brief description of this code set and the corresponding CSV file located in this directory.

## NSCP codes
These codes represent surgical procedure-related concepts from the NCSP standard.

Codes are taken from the [Publishing Centre](https://pub.e-tervis.ee/classifications) managed by Health and Welfare Information Systems Centre (TEHIK), see [here](https://pub.e-tervis.ee/classifications/NCSP).

We use the [NOMESCO Classification of Surgical Procedures Version 1.6](http://pub.e-tervis.ee/classifications/NCSP/7/NCSP.pdf), which remains valid as of 2024. 
Although TEHIK has restored the full hierarchy of the NOMESCO classification system from 2022 to 2024, 
we haven't updated the NCSP code set since 2022. Despite this, the majority of the codes have remained unchanged.


The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/). 

We also considered mappings that other researchers have published:
* https://github.com/thehyve/ohdsi-etl-sweden/blob/master/mapping_tables/kva-nomesco_source_to_concept_map.csv
* https://github.com/FinOMOP/FinOMOP_OMOP_vocabulary_test/tree/main/VOCABULARIES/NCSPfi 

- **File:** [ncsp_mappings](ncsp_mappings.csv)
- **Description:** This file contains a list of NCSP codes, along with their mappings to OMOP CDM standard concepts. 


## The Structure of Mapping files
CSV file for NCSP codes mappings contain the following columns:

- **source_code:** The original code from the respective code set. The source code being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code ('ncsp').
- **source_code_description:** A brief description of the source code.
- **source_name_eng:** A brief description of the source code in English.


- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Procedure, Spec Anatomic Site, Device, Measurement).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Procedure, Physical Object, Body Structure).


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




