## Melbourne Housing Price Prediction

### Project overview

The goal of this project was to predict housing prices in Melbourne using machine learning. The dataset contains information about property characteristics, location, property type, sale method and other factors that may influence the final selling price.

### Data cleaning and preprocessing

The following preprocessing steps were performed:

* removed unnecessary columns;
* handled missing values using imputation;
* created new features (property age, sale year, sale month, indicators for missing values);
* applied frequency encoding for the **Suburb** feature;
* encoded categorical variables using One-Hot Encoding;
* built a preprocessing pipeline using **ColumnTransformer** and **Pipeline**.

### Analysis results

Exploratory data analysis showed that property price is strongly related to its characteristics and location. Larger properties with more rooms and bathrooms generally have higher prices. Distance from the city centre also influences property value, while additional engineered features helped improve the predictive performance of the models.

### Model performance

Three models were evaluated:

| Model             |         MAE |        RMSE |        R² |
| ----------------- | ----------: | ----------: | --------: |
| Baseline (Mean)   |     490,911 |     721,693 |     0.000 |
| Linear Regression |     251,840 |     464,514 |     0.586 |
| **Random Forest** | **183,784** | **392,073** | **0.705** |

The **Random Forest** model achieved the best performance with the **lowest prediction error (MAE = 183,784 AUD)** and the **highest coefficient of determination (R² = 0.705)**. This means the model explains approximately **70.5%** of the variation in housing prices and significantly outperforms both the baseline model and Linear Regression.

### Possible improvements

* Include additional location-based features such as proximity to schools, public transport and parks.


