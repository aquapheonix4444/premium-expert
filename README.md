# Annual Premium Prediction — A Data Science Approach

This repository presents a complete data science workflow aimed at predicting annual insurance premiums based on client-specific features. The project includes data cleaning, feature engineering, model development, and evaluation. In addition to the main predictive analysis, we also conducted a focused segmentation study based on the age of clients, which is detailed below.

##  Project Structure

###  Main Files
- `ml_premium_prediction.ipynb`: The core notebook containing data preprocessing, exploratory data analysis (EDA), feature selection, model training, hyperparameter tuning, and evaluation.
  
###  Data Segmentation
As part of our extended analysis, we explored the possibility that clients of different age groups might follow different premium patterns. To address this hypothesis, we divided the data based on age:

- `data_segmentation.ipynb`: Script used to split the dataset into two groups based on age:
  - `premium_rest.xlsx`: Clients with age > 25
  - `premium_young.xlsx`: Clients with age ≤ 25

This segmentation was motivated by significant variations in premium values for younger clients during EDA and error analysis.

###  Segmented Model Files
- `ml_premium_prediction_rest.ipynb`: Analysis and model training exclusively for the `age > 25` segment.
- `ml_premium_prediction_young.ipynb`: Separate analysis for clients aged 25 or younger.

##  Conclusion from Segmentation

Our findings indicated that:
- **Clients aged above 25** had a more stable and consistent pattern with respect to their premium amounts, and the model performed well on this subset.
- **Clients aged 25 and below** showed erratic premium behaviors, leading to higher residual errors and reduced model reliability.

This suggested the need for additional or more relevant features for younger clients to capture the premium distribution effectively. Future iterations may involve deeper feature engineering or data collection efforts targeted at this demographic.

---

##  Getting Started
To explore the project:
1. Clone the repository.
2. Open any of the notebooks in Jupyter or VS Code.
3. Run through the segmentation process in `data_segmentation.ipynb` if needed.
4. Review models in `ml_premium_prediction_rest.ipynb` and `ml_premium_prediction_young.ipynb`.

---

##  Requirements
Standard Python data science libraries are used:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

---
