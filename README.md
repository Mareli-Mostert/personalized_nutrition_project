# Personalized nutrition project

## Introduction
Personalized nutrition (‘DNA diets’) has been proposed as an alternative to generalised (‘one-size-fits-all’) recommendations. Commercial genetic testing companies aim to provide personalized dietary recommendations based on the genetic variation (‘DNA profile’) of their consumers. The usefulness of these dietary recommendations, however, are uncertain for individuals from populations with great genetic diversity, like the South African population. The aim of this study was to investigate whether the genetic variants identified from the literature, were useful for making recommendations in a South African population, specifically a Black South African population.

## Methods

### Black South African study population
Individuals from the African Longitudinal Facial Appearance and Health Study (ALFAH) study were used to evaluate the usefulness of the single nucleotide polymorphisms (SNPs) associated with diet-related health outcomes, identified from the literature, in a Black South African population. The ALFAH study was approved by the following ethics committees at the University of Pretoria, South Africa: Natural and Agricultural Sciences (EC160429-024), Health Sciences (259/2016), and Humanities (25309995/HUM030/0819). Written informed consent was obtained from all 271 Black South African individuals included in the ALFAH study (53.3% male). The ALFAH study paticipants were recruited from the University of Pretoria and the Sefako Makgatho University, Pretoria, South Africa. The measures of associations analysed during this study were body composition measures, namely body fat (%) and muscle mass (kg).

### Data extraction & combining datasets
The genotyping data provided in a large text file from sequencing facilities was extracted using the R 4.2.2 programme. Refer to: data_extraction_from_text_files_in_R.txt

The ALFAH dataset was joined with the corresponding genotype data of each individual using MySQL 8.0. Refer to: join_tables_in_mysql.txt

### Data processing & clean-up
The combined ALFAH genotype dataset was processed, cleaned, and samples with missing data were addressed using Jupyter Notebooks (v. 6.5.4) in Python 3.11. Refer to: combined_data_cleanup.ipynb

### Data analysis
The forward linear regressions between the identified SNPs and the body composition measures were performed using Jupyter Notebooks (v. 6.5.4) in Python 3.11. Note: Body composition is sex influenced, therefore the coefficient of determination (R2) was calculated for sex only and for sex with body fat and muscle mass, respectively. Refer to: snp_sex_linear_regressions.ipynb
