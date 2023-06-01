# **Digital-pharmacology-hackathon**

## Digital pharmacology hackathon at the ITMO Infochemistry Centre with Sintelli and Medtech.Moscow

This repository is the result of the collaboration between ITMO Center for Infochemistry, Sintelli, and Medtech.Moscow for the "Digital Pharmacology: Predictive Modeling" hackathon. The event took place from April 28th to April 30th, and the technological partner for this event is Selectel.

Participants had the opportunity to make breakthroughs in predictive modeling of the side effects of pharmaceutical and bioactive compounds and contribute to the development of digital methods in medicine.

## Goal
The goal of the hackathon was to build machine learning models to accurately predict parameters characterizing the toxicity of chemical compounds. Teams collected their datasets from open sources using natural language processing technologies. The winning teams demonstrated high model accuracy and its applicability to a wide range of compound classes (relevant benchmarks were provided).

## Impact
Developers and researchers in the field of medicinal chemistry need new digital methods for navigating and filtering the chemical space to design innovative and safe drugs. These methods can significantly reduce the time and resources required for the development and implementation of new bioactive compounds. Moreover, they can reduce the use of laboratory animals in experiments and minimize the risks of adverse drug effects on humans.

## Participants
The hackathon invited students in natural sciences, technical specialties, IT developers, data scientists, chemists, pharmacologists, medical professionals, toxicologists, biologists, young scientists, researchers, and R&D businesses.

## Preparation
Participants were encouraged to prepare for the hackathon in advance by familiarizing themselves with data collection and processing technologies, studying literature and open data sources, gathering necessary datasets (the more diverse and extensive the datasets, the better the chances of building a strong model and winning), and understanding the parameters characterizing toxicity. Sets of parameters characterizing toxicity and relevant benchmarks were provided on the website.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Task:
#### Based on open (available in the literature and on the Internet) data, assemble your own original dataset and build a machine learning model to predict the toxicity performance of chemical compounds. 

### Solution:
1.	Presentation describing his solution
2. Jupyter notebooks that:
(a) The input for each model is a test .csv file with a list of molecules in SMILES format, and the output is a .csv file with the same list of SMILES and the corresponding value of the predicted indicator for each SMILES (two columns in total). The test SMILES are presented in canonical form from the RDKit library. 
3. training datasets used to build the model for each predictive parameter in .csv format with several columns: list of SMILES, experimental value of predictive indicator corresponding to SMILES (for each source a different column).

## List of toxicity indicators used:

- Developmental toxicity
- Skin Sensitization
- Blood Brain Barrier Penetration
- Hepatotoxicity
- Cardiotoxicity/HERG inhibition
 -Carcinogenicity
- Endocrine system disruption
- Eye Irritation
- Eye Corrosion
- "Mouse / Rat / Rabbit / Guinea Pig Intraperitoneal LD50"
- "Mouse / Rat / Rabbit / Guinea Pig Intraperitoneal LDLo"
- "Mouse / Rat / Rabbit / Guinea Pig Intravenous LD50"
- "Mouse / Rat / Rabbit / Guinea Pig Intravenous LDLo"
- "Mouse / Rat / Rabbit / Guinea Pig Oral LD50"
- "Mouse / Rat / Rabbit / Guinea Pig Oral LDLo"
- "Mouse / Rat / Rabbit / Guinea Pig Subcutaneous LD50"
- "Mouse / Rat / Rabbit / Guinea Pig Subcutaneous LDLo"
- "Mouse / Rat / Rabbit / Guinea Pig Skin LD50"
- "Mouse / Rat / Rabbit / Guinea Pig Skin LDLo"
- Bioconcentration factor
- 40 hour Tetrahymena pyriformis IGC50
- Mouse Carcinogenic potency TD50
- Ames test / Mutagenicity

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


To collect the dataset, we in the team used different data sources and quantified each source according to requirements.

First, we tried to get the data through the API. For this, we used three different sources, but in some cases it was not possible to get the data through the API. In such cases, we used parsing the data from a single source, and we also conducted manual searches on five different sources.

To account for the diversity of experimental data sources, we collected data from 13 different sources, including databases and scientific publications. We also checked whether these sources contained more than 1000 structures with experimental data.

We predicted several indicators of toxicity and made sure that only one model could be provided for each indicator.


In addition, we tried to assemble a diverse dataset containing data from different areas of chemistry. We also considered the uniqueness of the toxicity indicator space and tried to predict indicators that are not available in other datasets.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Setting up the required environment:

`conda create -n pharma python=3.10 conda activate pharma conda install -c anaconda ipykernel python -m ipykernel install --user --name=pharma pip install -r requirements.txt`

Don't forget to enable visualisation:

`jupyter nbextension enable --py widgetsnbextension`




