# Healthcare Service Codes Translations to OMOP CDM Standard Concepts

This directory contains translations of Estonian Health Insurance Fund (Tervisekassa) **healthcare service codes** and 
**Diagnosis Related Groups (DRG) codes** to OMOP CDM standard concepts.  
Below is a brief description of these code sets and the corresponding CSV files located in this directory.

## Service codes
This code list includes all medical services, procedures, necessary hospital medications, and other items covered 
under the health insurance package. 

[The Health Insurance Fund (Tervisekassa)](https://www.tervisekassa.ee/) pays for the services listed in 
the [Health Service List](https://www.tervisekassa.ee/partnerile/raviasutusele/tervishoiuteenuste-loetelu) 
if they are provided to an insured person based on medical indications.


There are two sources for Service Codes:
1. [The Health Service List](https://www.tervisekassa.ee/partnerile/raviasutusele/tervishoiuteenuste-loetelu) on the Health Insurance Fund webpage.
2. [The Health Service List](http://pub.e-tervis.ee/classifications/Haigekassa%20hinnakiri) in the [Publishing Centre](https://pub.e-tervis.ee/classifications) managed by Health and Welfare Information Systems Centre (TEHIK).

Both sources have the same data file.

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/). 


- **File:** [service_mappings](service_mappings.csv)
- **Description:** This file contains a list of healthcare service codes, along with their mappings to OMOP CDM standard concepts. 

## DRG codes
In Estonia, the **NordDRG system** is used. NordDRG is a diagnosis-related group (DRG) system that classifies patient cases 
based on clinical characteristics and resource consumption. It categorises cases using ICD-10 diagnosis codes, surgical procedure codes (NCSP), 
and other patient-related factors. It is integrated into Estonia’s electronic medical billing system.

For more information, see the Health Insurance Fund [webpage](https://www.tervisekassa.ee/partnerile/raviasutusele/tervishoiuteenuste-loetelu/drg).

In the OMOP CDM, standard concepts are derived from the **Medicare Severity Diagnosis Related Group (MS-DRG) system**, which is implemented in the United States. 
Like NordDRG, MS-DRG categorises inpatient hospital stays based on patients' principal diagnoses, secondary conditions, procedures performed, age, sex, and discharge status. 
Although MS-DRG is specifically tailored for the Medicare population (primarily individuals aged 65 and older) 
and may follow different principles due to regional healthcare practices and standards, 
we still attempted to map as many NordDRG codes to MS-DRG as possible.

The mappings in this CSV file were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/). 


- **File:** [drg_mappings](drg_mappings.csv)
- **Description:** This file contains a list of DRG codes, along with their mappings to OMOP CDM standard concepts. 


## The Structure of Mapping files

The CSV file for service codes mappings contains the following columns:

- **source_code:** The original code from the respective code set. The source code is being translated into a Standard Concept. 
- **source_concept_id:** A foreign key to the Source Concept (refers to OMOP CDM CONCEPT table) that is being translated into a Standard Concept. For all source codes, we created custom concepts with concept IDs greater than 2 billion.
- **source_vocabulary_id:** A foreign key to the OMOP CDM VOCABULARY table defining the vocabulary of the source code that is being translated to a Standard Concept. 
- **source_code_type:** The type of the source code ('ehif_service').
- **source_code_description:** A brief description of the source code.
- **source_code_category_name:** The type name of healthcare service.
- **source_code_category_code:** The type code of healthcare service.


- **target_concept_name:** The name of the target Concept to which the source code is being mapped. 
- **target_concept_code:** The target Concept code to which the source code is being mapped. 
- **target_concept_id:** The unique identifier of the target Concept to which the source code is being mapped. 
- **target_vocabulary_id:** The identifier of the vocabulary from which the target Concept originates.
- **target_domain:** The domain in OMOP CDM to which the target Concept belongs (e.g., Observation, Procedure, Measurement, Drug, Condition).
- **target_concept_class_id:** The class ID of the target Concept (e.g., Procedure, Lab Test, Ingredient).


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




