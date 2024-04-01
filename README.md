# Project 2: Ames Housing Data and Kaggle Challenge

As a prominent real estate consultant in the country, the city of Ames Iowa asked me to help them predict the housing prices of a local builders’ new development. They were interested in my expertise because I am an Adobe DSI student, and locals are anxiously worried their mortgages would experience sympathetic effects of the new builds. The objective of this my new study is to develop a model that best predicts the price of Red Oak Construction as close as possible. I aim to predict these prices so the city of Ames can decide if they should increase property taxes throughout the city, or if they should lower property taxes to help their citizens.

# Data Dictionary

|Selected Features|Type|Dataset|Description|
|---|---|---|---|
|Total Bath|int|train|Feature egineered total bathroom count of the house| 
|Overall Qual|int|train|Rates the overall material and finish of the house| 
|Overall Cond|int|train|Rates the overall condition of the house| 
|Year Remod/Add|int|train|Remodel date (same as construction date if no remodeling or additions)| 
|Bedroom AbvGr|int|train|Bedrooms located on floors above ground level (does NOT include basement bedrooms)|
|Kitchen AbvGr|int|train| Kitchens located on floors above ground level|
|TotRms AbvGrd| int| train | Rooms located on floors above ground level (does NOT include bathrooms)|
|Fireplaces| int | train | Number of fireplaces|
|Garage Cars| int| train | Size of garage in car capacity|
|Mo Sold| int | train | Month Sold (MM)

For a more detailed dictionary, review the Ames Housing Data dictionary by [clicking here](https://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

# Executive Summary

##### Background: 
The Ames Housing Dataset is an exceptionally detailed and robust dataset with over 70 columns of different features relating to houses. It is my job to predict the sales price for each house. For each Id in the test set, I must predict the value of the SalePrice variable ([Kaggle](https://www.kaggle.com/competitions/adobe-dsb-34/overview)).

##### Methodology: 

Using machine modeling and predictive analysis, a regression model was created to predict the housing price of 513 houses located in Ames, Iowa.

Before conducting analysis, data cleaning was applied where appropriate. This involved removing house features with more than 50% of it's data missing, filling any remaining null values with none, zeros, and median aggregators as some nulls signify the house lacks that feature. I selected 10 features to conduct my predictive modelling and thus retained only those relevant columns pertinent to my analysis. Additionally, I engineered featuers in my datasets to facilitate increased interpretability in my analysis.

Subsequently, questions pertaining to my problem statement were explored. An example of the type of questions is outlined below: 
- Does the target follow LINE assumptions?
  
- How do the selected features correlate with the target?

- What is the distribution of the selected features in relation to the target?


##### Key Findings:
The best model I found to perform best at predicting house prices was a Linear Regression model with zero penalty. The selected performed better than the baseline which had an RMSE of 78286.72. Of the selected features used in my model, overall quality of the house had the most correlation to the sale price of a house. The higher the quality of the house, the more the sale price is predicted to be. Also in relation to house quality, if the house's condition is Average, it is slated to be priced more expensively than other houses. Overall, the linear regression model had the highest R^2 score of 0.8314 on unseen data. This means that for the features I selected, the model was able to explain 83.14% of variation in sale prices. My model had an RMSE of 32141.41, meaning the magnitude of error present made the predictions off by $32141.41.


##### Next Steps?
Due to the impact of house features on sale prices, I recommend that officials in Ames, Iowa, refrain from implementing tax increases. According to the Ames Tribune, house sale prices can exceed the assessed value by 25% to 30%. Additionally, new construction can lead to an increase of $1,000 in tax bills the following year, as reported by The Motley Fool. The city should allow more development to enhance the local environment and encourage more investments to stimulate economic growth. This could create a favorable business climate, providing incentives for entrepreneurs, attracting outside investments and newhomeowners, and fostering innovation. By doing this, the city can generate increased economic activity, create jobs, and improve overall prosperity for its residents.
