# Module 3 project: MAchine learning for Diamonds price prediction

## **Objectives:**
The goal is the prediction of the price of diamonds based on their characteristics (weight, color, quality of cut, etc.). This is an academic competition created for the students of Iron Hack Data Analytics Bootcamp, edition dapt202011mad, using the Kaggle platform (see more info [here](https://www.kaggle.com/c/dapt202011mad/overview)) .


## **Steps:**

- Do an exploratory data analysis (see [project module 2](https://github.com/Alvaru89/ih_datamadpt1120_project_m2)) and data pre-processing. The data pre-processing included feature engineering, category creation, one hot encoding, imputing values and data scaling in two stages (one for numeric features only and a final scaling to all features).  

- Create a machine learning model. Different models were tested to achieve the minimum [rmse] (https://en.wikipedia.org/wiki/Root-mean-square_deviation). The best model proved to be LightGBM.

- Once the best model is selected, look for the best hyperparameters using grid/random search. The best hyperparameters were:

      boosting='dart',
      n_estimators=1000,
      max_depth=150-200,
      num_leaves=40-50
      
## **Unsucessful tries:**
- Dropping unnecessary columns (from exploratory data analysis)
- Projection to reduce dataset dimensions and remove non-relevant columns.
- Projection for clustering
- Clustering to find subsets in the full dataset
- RobustScaler. It did not give better model results, alone or in combination with StandardScaler.
- LabelEncoding and drop first option in One Hot Encoding.
- Neural network (without hypterparameter tuning): the results were on the same range but slightly above light GBM (worse rmse).


DISCLAIMER: Originally this repository was not planned to be uploaded to Github so apologies in advance for the spaghetti code.