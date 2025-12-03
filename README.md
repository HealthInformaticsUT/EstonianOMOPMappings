# Main Code Sets Used in the Estonian Healthcare System Translated to OMOP CDM Standard Concepts

This repository contains translations of various health-related code sets used in the Estonian healthcare system to [OMOP CDM](https://ohdsi.github.io/CommonDataModel/index.html) (Common Data Model) standard concepts. 
The translations aim to facilitate the integration and standardization of health data for research and analytics.

All mappings in this repository use **OMOP CDM Vocabulary version v20250827 (released on 27-AUG-25)**. 
For more details, see the [relase notes](https://github.com/OHDSI/Vocabulary-v5.0/releases/tag/v20250827_1756288395.000000).

## Repository Structure

The repository is organized into subdirectories, each containing CSV files with mappings for specific types of code sets. 
Below is a brief description of each subdirectory and its contents.

Each subdirectory contains a README file describing the structure of the CSV files within it and a brief overview of each code set.


### [Diseases](diseases)

This directory contains mappings for disease-related code sets. 
The mappings included are:

- **ICD-10 Codes** 
- **ICD-O-3 Codes** 
- **Cancer Staging Codes, TNM Category Codes, etc.** 
- **Pathology-Related Codes** 
- **Symptoms and Side-Effects-Related Concepts**


### [Drugs](drugs)

This directory contains mappings for drug-related code sets. 
The mappings included are:

- **ATC Codes**
- **Local Drug Package Codes**
- **Local Drug Administration Route Codes** 
- **COVID-19 Vaccine Codes**


### [Healthcare Services](healthcare_services)

This directory contains mappings for healthcare service codes used in Estonian health insurance claims data and 
and Diagnosis Related Groups (DRG) codes. 
The mappings included are:

- **Local Healthcare Service Codes**
- **DRG codes**


### [NCSP](ncsp)

This directory contains mappings for codes from Nomesco Classification of Surgical Procedures (NCSP). 
The mappings included are:

- **NCSP Codes**


### [Lab measurements](lab_measurements)

This directory contains mappings for lab measurements-related code sets. 
The mappings included are:

- **LOINC Codes**
- **LOINC Answers**
- **Other measurements-related concepts**


### [Demographics](demographics)

This directory contains mappings for various demographics-related code sets.
The mappings included are:

- **Highest education acquired** 
- **Main spoken language** 
- **Marital status** 


### [Health behaviour](health_behaviour)

This directory contains mappings for various health behaviour-related code sets.
The mappings included are:

- **Smoking status** 


### [Death Attributes](death_attributes)

This directory contains mappings for various death-related code sets.
The mappings included are:

- **Death Circumstances** 
- **Death Location** 


### [Healthcare Providers](healthcare_providers)

This directory contains mappings for healthcare providers.
The mappings included are:

- **Specialties** 



## Translation Sources

Some of the translations in this repository have been sourced from the OHDSI (Observational Health Data Sciences and Informatics) vocabulary repository, [Athena](https://athena.ohdsi.org/search-terms/start). 
Athena is a comprehensive source of standardized vocabularies used in the OMOP CDM.

Additionally, some mappings were created using the OHDSI tool [Usagi](https://ohdsi.github.io/Usagi/). 
Usagi is a semi-automated mapping tool that uses natural language processing to suggest possible mappings between source codes and standard concepts in OMOP CDM. 
Users can review and validate these suggestions to ensure accurate mappings.

## How to Use

1. Clone the repository to your local machine.
2. Navigate to the appropriate subdirectory to access the CSV files.
3. Use the files to map your local data to the OMOP CDM standard concepts.

## Contributions

Contributions are welcome! Please create a pull request or open an issue to discuss any changes or additions.

## License

Estonian OMOP Mappings © 2024 by Health Informatics Lab, University of Tartu is licensed under CC BY 4.0. See the [LICENSE](LICENSE.txt) for more details.

## Publications
Marek Oja, Sirli Tamm, Kerli Mooses, Maarja Pajusalu, Harry-Anton Talvik, Anne Ott, Marianna Laht, Maria Malk, Marcus Lõo, Johannes Holm, Markus Haug, Hendrik Šuvalov, Dage Särg, Jaak Vilo, Sven Laur, Raivo Kolde, Sulev Reisberg, Transforming Estonian health data to the Observational Medical Outcomes Partnership (OMOP) Common Data Model: lessons learned, JAMIA Open, Volume 6, Issue 4, December 2023, ooad100, https://doi.org/10.1093/jamiaopen/ooad100

## Acknowledgements

Research group of Health-Informatics in University of Tartu https://health-informatics.cs.ut.ee/
