This repository contains all the code used for my senior thesis, “A Sustainable Extension of the Fama-French Factor Models: The Role of Carbon Emissions-Based Factors in Describing U.S. Stock Returns” (submitted April 2025).

The code files in this repository can be broken down into the following categories:

**Data Cleaning:** I broke my data cleaning code into three more digestible steps/files. STEP 2 starts with importing the resulting .csv file from STEP 1; Similarly, STEP 3 starts with importing the resulting .csv file from STEP 2. Therefore, I would strongly recommend following the three steps in order. Some steps in the code will require you to manually obtain data from other sites and then load it into the code before proceeding; All of these instructions are documented in comments throughout the code. The dataset obtained after completing STEP 3 is ‘relevantdata.csv’, which will be THE file used to create `factordata.csv’: the main data file containing ALL relevant data for this research project.
* (STEP 1) Cleaning CUSIPs and Sectors.ipynb
* (STEP 2) Pivoting and Merging with Total Assets Data.ipynb
* (STEP 3) Creating Comprehensive Dataset (All Necessary Data).ipynb

**Key Code Files:** The Factor Construction and Key Analysis.ipynb file is the main code file from our project. As stated above, it will transform ‘relevantdata.csv’ into ‘factordata.csv.’ The file also conducts analysis on sector representation, CO2 estimation method breakdowns, and portfolio composition and recalibration (volatility). The Main Regressions.ipynb file contains the code used to run the regressions found in the main “Results and Discussion” chapter of the thesis.
* Factor Construction and Key Analysis.ipynb
* Main Regressions.ipynb

**Other Analysis:** The Summary Statistics and Chart Creation.ipynb file contains the code I used to generate the majority of my summary statistics tables and charts. (The figures created for GMB portfolio dissimilarities and composition were created in the Factor Construction and Key Analysis.ipynb file.) The Carbon Emissions as Raw Regressors.ipynb file contains an additional regression included in the Appendix and referenced in the main thesis when defending/explaining our choice to build factors instead of just using carbon emissions as raw regressors.
* Summary Statistics and Chart Creation.ipynb
* Carbon Emissions as Raw Regressors.ipynb

**Robustness Analysis:** These files contain the code used for the regressions explored in the “Robustness Analysis” section of the thesis. Note, the percentile sensitivity analysis contains an additional file: Creating Factors with Different Percentiles.ipynb, which is used to generate the datasets with the updated factors constructed using different percentile levels. The datasets for all other robustness checks were created either in the regression code files themselves or at the bottom of the Factor Construction and Key Analysis.ipynb file.  
* (Robustness Analysis) Creating Factors with Different Percentiles.ipynb
* (Robustness Analysis) Regressions with Factors from 90-10 Percentiles.ipynb
* (Robustness Analysis) Regressions with Factors from 97.5-2.5 Percentiles.ipynb
* (Robustness Analysis) Regressions on Dataset Excluding Salient Sectors.ipynb
* (Robustness Analysis) Regressions on Dataset Excluding GMB Portfolio Stocks.ipynb

Lastly, unfortunately, I was unable to upload ‘factordata.csv’ to this repository as the file size exceeds the limit for GitHub. However, a similar file can be obtained by using the data cleaning code and key code files. My ‘factordata.csv’ file can also be provided upon request.
