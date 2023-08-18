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

## Usage

### Python
Workflow organized numerically from 00 to 05 detailing every step taken on my local machine to conduct this project. Folder 04 ddetails the steps taken to split, train, and test the population specific random forest models. 

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
