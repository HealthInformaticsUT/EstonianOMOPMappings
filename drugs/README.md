# Drug-Related Code Sets Translations to OMOP CDM Standard Concepts

This directory contains translations of various drug-related code sets to OMOP CDM standard concepts.  
Below is a brief description of each code set and the corresponding CSV files located in this directory.

## Code Sets

### 1. ATC Codes
The Anatomical Therapeutic Chemical (ATC) classification system is used to classify drugs according to their therapeutic use and chemical characteristics.

Codes and mappings are sourced from [Athena](https://athena.ohdsi.org/search-terms/start), a repository for Standardized Vocabularies maintained 
by OHDSI (Observational Health Data Sciences and Informatics). 
Additionally, we have supplemented the ATC codes from Athena with some additional ATC codes used in Estonia that are available at [The State Agency of Medicines](https://ravimiregister.ee/).

- **File:** [atc_mappings](atc_mappings.csv)
- **Description:** This file contains a list of ATC codes along with their mappings to OMOP CDM standard concepts.

### 2. Local Drug Package Codes
These codes represent specific drug products available at [The State Agency of Medicines](https://ravimiregister.ee/). 
A package code is a combination of 7 numbers, which identifies a medicine package. 

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

- **File:** [drug_packages_mappings](drug_packages_mappings.csv)
- **Description:** This file includes local drug package codes, along with their mappings to OMOP CDM standard concepts. The list currently includes only mapped codes for drug products.

### 3. Local Drug Administration Route Concepts
These concepts specify the various routes by which drugs can be administered (e.g., oral use, intravenous use, etc.).
The information about drug administration routes is available at [The State Agency of Medicines](https://ravimiregister.ee/).

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

- **File:** [drug_admin_route_mappings](drug_admin_route_mappings.csv)
- **Description:** This file contains local concepts for drug administration routes, along with their mappings to OMOP CDM standard concepts.

### 4. COVID-19 Vaccine Codes (Manufacturer-specific)
This code set includes codes for COVID-19 vaccines categorized by their manufacturers. 
These codes help in tracking and analyzing the administration of different COVID-19 vaccines.

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/).

- **File:** [vaccines_mappings](vaccines_mappings.csv)
- **Description:** This file lists COVID-19 vaccine codes based on manufacturers, along with their mappings to OMOP CDM standard concepts.

## The Structure of Mapping files
Each CSV file contains the following columns:

- **source_code:** The original code or concept from the respective code set. The source code being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. 
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code (e.g., atc, drug_packages, drug_admin_route, vaccines).
- **source_code_description:** A brief description of the source code.
- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Drug, Observation).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Ingredient, Clinical Drug, Route).
- **updated_date:** The date when the mapping was last updated.
- **valid_end_date:** The date until which the mapping is valid.

## How to Use
1. Clone the repository to your local machine.
2. Navigate to the specific directory to access the CSV files.
3. Use the files to map your local data to the OMOP CDM standard concepts.

## Contributions
Contributions are welcome! Please create a pull request or open an issue to discuss any changes or additions.

## License
This repository is licensed under the CC BY-NC-SA 4.0 License. See the [LICENSE](https://creativecommons.org/licenses/by-nc-sa/4.0/) for more details.
