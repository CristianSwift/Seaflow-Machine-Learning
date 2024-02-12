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
All of this has been installed on MacOS systems. Ubuntu/linux and Windows users may have a slightly different experience.  

Jupyter notebooks, a web-based interactive computing platform, were used as an interface for python within a conda enviorment.

A surest way to run these notebooks is use create a [conda](https://docs.conda.io/en/latest/) environment using the [environment.yml](https://github.com/CristianSwift/Seaflow-Machine-Learning/blob/MoreData/enviorment.yml) file for this repository. On your local machine:

    conda env create -f environment.yml

Once installation is complete:

    conda activate machine-learning-env
    jupyter notebook

If you get an error 'command not found: jupyter-notebook', first install notebook support in conda:

    conda install nb_conda

## Usage

### data_ingest

- Notebook data_examples: 
  This notebook contains examples of the two main datasets used in the model, and explanations for each of them

#### CMAP_queries

- Notebook 00:  
  This notebook samples the nutrient, temperature, salinity, and current speed data from CMAP for all of the cruises in our dataset.  This notebook will take ~3 hours to run, but the repository already has this information included, so unless you change the variables or parameters you will not need to run this.

- Notebook 01:  
  This notebook samples the same variables from CMAP, but for our global prediction dataset.  Similar to the previous notebook, you should not run this unless you change the variables or parameters.

- Notebook 02: 
  This notebook is a WIP 

- Notebook 03: run every cell
  This notebook is a WIP

#### data_cleaning

- Notebook 00:
  This notebook combines the sampled CMAP variables for our cruise data into one useable training set.  This will run quickly, but shouldn't need to be run unless you change anything in this or other data notebooks.  

- Notebook 01:
  This notebook adds the 'hours since sunrise' variable to the cruises dataset and cleans up the variable names so they are more readable.  This will run quickly, but shouldn't need to be run unless you change anything in this or other data notebooks.  

- Notebook 02: 
  This notebook does the same as the previous, but for the global dataset.

#### data
contains two folders, original and modified
- original: all data loaded into python notebooks that have not been previously manipulated in this project, including Simon CMAP data queried in notebook 00_cmap-querys. 
- modified: all data that has been previouslt manipulated in this project, usually saved for intermidiate steps to get from one workflow to another.  

### cross_validation

- Notebook functions:  
  This notebook contains functions for all of our cross validation notebooks.  It does not need to be ran by itself, but each following      notebook will run it inline.

- Notebook cross_val:  
  This notebook contains examples of the cross validation we used for our models.  It is very useful to understand cross validation for statistical learning, so you should run this notebook and read each of the explanations contained within.

- Notebook auto_cor:
  This notebook explains the pitfalls of one common form of cross validation.

- Notebook hyperparam_tuning:
  This notebook explains how different hyperparameters change the predictions from our random forest regression model.

- Notebook feature_tuning:  
  This notebook demonstrates how removing certain features (training variables) changes the output of the model.

### Predictions

- Notebook prediction_prep:
  This notebook trains the models for our predictions, and contains functions for use in predictions.ipynb.  This does not need to be ran, as predictions.ipynb runs it inline.

### RF_models
Contains joblib files of the developed sklearn RandomForestRegressor() models for each plankton population.  These can be pulled from this folder into your own notebook.  

### figures
- Where figures are saved throughout the notebook. All figures are displayed in the ipynb notebooks, and some exclusively so.


## Authors
This work was conducted by Cristian Swift (CristianSwift2@gmail.com) under the mentorship of François Ribalet1 and François Ribalet through the School of Oceanography, Univeristy of Washington, Seattle, USA

## License
