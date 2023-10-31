---
output:
  pdf_document: default
  html_document: default
---
# Seaflow-Machine-Learning




## Table of Contents
- [About/Abstract](#about)
- [Installation](#installation)
- [Usage](#usage)
- [Authors](#authors)
- [License](#license)

## About
This repository contains all of the data and code for the project titled: "Random Forest Regression Models for Predicting Picophytoplankton 
Biomass Partitioning in the Eastern Pacific."

  ### Abstract
  The partitioning of phytoplankton biomass is crucial for understanding how climate change impacts the carbon cycle as it sheds light on the distribution and dynamics of different phytoplankton groups. However, there is a significant knowledge gap regarding the environmental factors that drive the partitioning of phytoplankton biomass, particularly in warm, nutrient-poor regions that are predicted to expand in future ocean conditions. This study focus on the dominant phytoplankton groups in these regions: Prochlorococcus, Synechococcus, and small eukaryotic phytoplankton (less than 2 µm in diameter). Using random forest regression models, we assessed the predictability of phytoplankton biomass based on salinity, temperature, light intensity, and dissolved inorganic nutrient concentrations (nitrate, phosphorus, and iron). Model performance was evaluated using 2,800 observations per population were obtained through high-frequency flow-cytometry in surface water of the North Subtropical and Subpolar gyres. Mean Absolute Error Percentage varied among picoplankton population’s Random Forest models, Prochlorococcus: 7.71%, Synechococcus: 2.30%, Nanoeukaryotes: 3.34%, and Picoeukaryotes: 6.57%. Results highlight the importance of nitrate, salinity, and to a lesser extent, iron, as predictors of Prochlorococcus biomass. Conversely, phosphate and nitrate emerge as the primary drivers of Synechococcus and picoeukaryote biomass, respectively. The upper and lower limits of the biomass and environmental data in the dataset define the boundaries within which a Random Forest can generate its predictions, making these models specific to the location and timing of this study. Further research is needed to explore additional factors and refine prediction models by considering factors like nutrient uptake rates, grazing pressure, and microbial interactions.




## Installation
Jupyter notebooks, a web-based interactive computing platform, were used as an interface for python within a conda enviorment.

A surest way to run these notebooks is use create a [conda](https://docs.conda.io/en/latest/) environment using the [environment.yml](https://github.com/CristianSwift/Seaflow-Machine-Learning/blob/MoreData/enviorment.yml) file for this repository. On your local machine:

    conda env create -f environment.yml

Once installation is complete:

    conda activate machine-learning-env
    jupyter-notebook

If you get an error 'command not found: jupyter-notebook', first install notebook support in conda:

    conda install nb_conda

## Usage

### Python
Workflow organized numerically from 00 to 05 detailing every step taken on my local machine to conduct this project. Folder 04 ddetails the steps taken to split, train, and test the population specific random forest models. 

A note on directories:  these notebooks use git as a way to locate the nessecary files, but if you have these files 
outside of a repository you will need to substitute your own directory paths.  

- Notebook 00: run every cell as you go
this whole notebook should be able to be ran without modification, but the query will take anywhere between /n
5-30 minutes to run depending on your internet connection and write speed.  

- Notebook 01: run every cell 

- Notebook 02: run every cell

- Notebook 03: run every cell

- Notebook(s) 04: run each notebook in the '04_Populations-model-fitting' folder in order, starting with '01_model-preparation.ipynb'.  You may have to change the file directories on 02-05 to fit your system.  

- Notebook 05: run every cell - this notebook will compare the random forest predictions to known cruise data.  

### RF_models
Contains joblib files of the developed sklearn RandomForestRegressor() models for each plankton population.

### data
contains two folders, original and modified
- original: all data loaded into python notebooks that have not been previously manipulated in this project, including Simon CMAP data queried in notebook 00_cmap-querys. 
- modified: all data that has been previouslt manipulated in this project, usually are saved for intermidiate steps to get from one workflow to another.

### figures
- Where figures are saved throughout the notebook. All figures are displayed in the ipynb notebooks, and some exclusively so.


## Authors
This work was conducted by Cristian Swift (CristianSwift2@gmail.com) under the mentorship of François Ribalet1 and François Ribalet through the School of Oceanography, Univeristy of Washington, Seattle, USA

## License
