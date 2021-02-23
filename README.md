# Project 2: Ames Housing Market Analysis

### Problem Statement

We are provided with a dataset including 80 features and 2,051 residential sales provided by the Ames City Assessor’s Office. Our goal is to build a model that can accurately predict housing prices in Ames, Iowa.

### Executive Summary

I will begin by importing and cleaning the data, which will include imputation and feature engineering. Next, I will use exploratory data analysis and data visualization to investigate our dataset and identify key features prior to model building. Next, in a new notebook, I will use the cleaned and feature engineered data to build three versions of a Ridge Regression model using various preprocessors. Finally, in conclusions, I will identify uses for each type of model, as well as overall findings.


### Contents:
##### Part 1: Data Cleaning and EDA
- Obtain and Inspect the Data
- Data Cleaning
- Checking for Incorrect Values
- Feature Engineering
- Exploratory Data Analysis
- Additional Data Cleaning and Feature Engineering

##### Part 2: Modeling
- Read in Clean Data
- Set up X and y
- Categorical Column Transforming
- Ridge Regression with Standard Scaler
- Ridge Regression with Quantile Transformer
- Black Box Kaggle Model
- Conclusion

### Data Dictionary

The data dictionary for this project can be found here: http://jse.amstat.org/v19n3/decock/DataDocumentation.txt

### Data

[Training Data](./datasets/train.csv)  
[Testing Data](./datasets/test.csv)  
[Cleaned Training Data](./datasets/train_clean.csv)  
[Cleaned Testing Data](./datasets/test_clean.csv)  

### Conclusion

Model selection: The three models demonstrated are all useful for different purposes. The Black Box model makes the most accurate prediction. This would be most useful for scenarios that have all of the feature information and ultimately care about getting closest to the target. Zillow and Redfin price estimators come to mind. This might also be useful for a potential buyer, who could use this model for inference: is the home they are looking to buy priced correctly? Should they negotiate a lower offer, or put in a higher bid?
The Ridge Regression using a Quantile transformer might be most useful to a real estate firm, where neighborhood and location are of utmost important. The normalization of this model places a higher emphasis on traditional real estate metrics - location, square footage, and age.
The Ridge Regression using Standard Scaler might be best for the homeowner and focuses on the features that can increase or decrease value of a home, and may help them make better investments. For example, the focus on overall quality and square footage may lead them to re-paint their house, upgrade appliances, or pursue a remodel or addition with greater peace of mind.

What features matter? The Ridge Regression models confirms what was discovered during exploratory data analysis. The three most important factors to determine Sale Price are Location (neighborhood), Size (above ground square footage, lot area, and other square footage features), and Quality (overall quality, new house dummy, overall condition, and age).

Areas for Further Study: Time constraints prevented me from further investigating certain features such as home type, kitchen quality, and unique individual features such as fireplaces, pools, etc. I would also like to experiment with segmenting the model by other factors such as new vs old home, sale type, and neighborhood.

### Sources

http://jse.amstat.org/v19n3/decock.pdf
https://medium.com/@jobethmuncy/different-ways-to-view-a-pandas-dataframe-528d193b7320
https://datavizpyr.com/sort-boxplot-by-mean-with-seaborn-in-python/
https://www.drawingfromdata.com/how-to-rotate-axis-labels-in-seaborn-and-matplotlib
https://stackoverflow.com/questions/52005576/seaborn-boxplot-horizontal-line-annotation
https://stackoverflow.com/questions/27967914/efficient-way-to-compute-intersectinn-two-numpy-arrays
https://stackoverflow.com/questions/14861891/runtimewarning-invalid-value-encountered-in-divide



