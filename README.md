### Project Title

Housing Price Prediction using Ames Dataset

**Author**
Arun Sai Pendyala

#### Executive summary

This project analyzes the Ames Housing dataset (2,930 home sales, 80 features) to explore what factors drive house prices and to build a baseline predictive model. Through exploratory data analysis (EDA) and a simple linear regression model, we identify the most influential features and establish a foundation for more advanced modeling in future assignments.

#### Rationale

Housing affordability and valuation are critical issues for buyers, sellers, real estate agents, and policymakers. Accurately predicting home prices can help buyers avoid overpaying, assist sellers in setting competitive prices, and allow city planners to better understand housing market trends.

#### Research Question

What are the key factors that influence housing prices, and how accurately can we predict home sale prices using a baseline linear regression model?

#### Data Sources

- **Ames Housing dataset**: Residential property sales in Ames, Iowa, with 80 explanatory variables.
- Source: [AmesHousing dataset on Kaggle](https://www.kaggle.com/datasets/prevek18/ames-housing-dataset)

#### Methodology

1. **Data Cleaning**

   - Dropped ID columns (`Order`, `PID`)
   - Filled missing numeric values with median
   - Filled missing categorical values with mode
   - Result: 2,930 rows × 80 features, no missing values

2. **Exploratory Data Analysis**

   - Examined distribution of `SalePrice` (right-skewed, median ~$160K)
   - Correlation analysis identified top drivers: `Overall Qual`, `Gr Liv Area`, `Garage Cars`, `Year Built`
   - Boxplots showed significant price variation across neighborhoods

3. **Baseline Model**
   - Linear Regression with four features: `Overall Qual`, `Gr Liv Area`, `Garage Cars`, `Year Built`
   - Evaluation metrics: RMSE, MAE, R²
   - Model interpretation using coefficients

#### Results

- **Model Performance**

  - RMSE: ~43,339
  - MAE: ~28,315
  - R²: 0.766 (explains ~77% of price variation)

- **Key Insights**
  - Home quality is the strongest driver: each one-point increase in quality rating adds ~$23K.
  - Garage capacity adds ~$14.7K per additional car.
  - Living area and newer construction years also positively influence price.
  - Model underestimates very high-priced homes, indicating limitations of linear regression.

#### Next steps

- Apply transformations to address skewness (e.g., log of `SalePrice`)
- Encode categorical variables (e.g., neighborhood, style)
- Experiment with regularized models (Lasso, Ridge)
- Test tree-based and ensemble methods (Random Forest, Gradient Boosting)

#### Outline of project

- [Exploratory Data Analysis Notebook](notebooks/exploratory_analysis.ipynb)

##### Contact and Further Information

For questions, please contact: arunpendyala01@gmail.com
