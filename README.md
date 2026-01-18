# Predicting Wine Prices using Machine Learning



This project analyzes and predicts wine prices using machine learning techniques, based on a real-world dataset of wine characteristics. The goal is to identify the key factors influencing wine prices and to compare different predictive models in terms of accuracy and interpretability.



The analysis was developed as an academic project and focuses on the application of statistical learning methods to an economic and market-driven problem.



---



## Project Overview



The global wine market is complex and influenced by multiple factors such as grape variety, alcohol content, vintage year, wine style, and country of origin. Accurately predicting wine prices can support decision-making for producers, distributors, and other stakeholders involved in the wine supply chain.



This project aims to:

- Explore the main drivers of wine pricing

- Model both linear and non-linear relationships between wine characteristics and price

- Compare the predictive performance of different machine learning models



---



## Dataset



The dataset consists of **1,290 wine samples** described by **15 variables**, including both continuous and categorical features.



### Target Variable

- **Price**: Retail price of the wine (in euros), log-transformed to reduce skewness.



### Main Predictors

- Alcohol by Volume (ABV)

- Vintage year

- Wine style (e.g. red, white, rosé)

- Grape variety

- Country of origin

- Bottle closure type



Data preprocessing included:

- Cleaning non-numeric characters

- Handling missing values via imputation

- Simplifying categorical variables

- Splitting the dataset into training (80%) and test (20%) sets



---



## Methods



Three different modeling approaches were implemented and compared:



### 1. Linear Regression (LM)

Used as a baseline model for its simplicity and interpretability.  

The price variable was log-transformed to address skewness.  

While the model identified statistically significant predictors, its performance was limited by the assumption of linear relationships.



### 2. Generalized Additive Models (GAM)

GAMs were used to capture non-linear effects of continuous predictors such as ABV and vintage.  

This approach improved predictive performance compared to linear regression while maintaining interpretability.



### 3. Random Forest

Random Forests were employed to model complex interactions and non-linear relationships without imposing parametric assumptions.  

This model achieved the best predictive performance among all approaches.



---



## Results



Model performance comparison:



| Model              | R²     | RMSE   |

|--------------------|--------|--------|

| Linear Regression  | ~0.46  | Higher |

| GAM                | ~0.55  | Lower  |

| Random Forest      | ~0.76  | ~0.34  |



Key findings:

- **Random Forest** provided the highest accuracy and explained over 75% of the variance in wine prices.

- **ABV, vintage, wine style, and country of origin** were consistently among the most important predictors.

- Higher ABV wines tend to be more expensive.

- Older wines in this dataset were generally priced lower.

- Wines from countries such as France and Italy showed higher average prices.

- Certain wine styles (e.g. “Rich \& Toasty”, “Crisp \& Fruity”) were associated with higher prices.



---



## Discussion



The results highlight the importance of using flexible models when dealing with complex market data. While linear models offer interpretability, they fail to capture non-linear effects and interactions that are crucial in wine pricing.



Random Forests proved to be the most effective model, although some limitations remain, particularly in predicting very high-priced wines. These limitations are likely due to data quality issues, missing values, and the presence of outliers.



---



## Limitations and Future Work



Potential improvements include:

- Expanding the dataset with wine ratings and distribution channels

- Incorporating climate and weather data

- Exploring ensemble methods or deep learning approaches

- Improving predictions for high-end wines through further model tuning



---



## Authors



- Alessandro Conte  

- Stefano Cavallo  



---



## License



This project is released under the MIT License.



