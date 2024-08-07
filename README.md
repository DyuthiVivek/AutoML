## Predict Bike Sharing Demand with AutoGluon

The AutoGluon AutoML framework automates machine learning tasks, making it easier for us to focus on EDA and the features.

The dataset is taken from the bike sharing demand Kaggle contest.

## EDA and Feature Engineering:

The datetime feature was divided into year, month, day and hour. Splitting the datetime features helped in enhancing the performance by helping in identifying any seasonal patterns. The season and weather features were transformed into the category data type.


## Hyperparameter tuning:
|model|hpo1|hpo2|hpo3|kaggle score|
|--|--|--|--|--|
|initial|default_vals|default_vals|default_vals|1.80501|
|add_features|default_vals|default_vals|default_vals|0.68289|
|hpo|GBM: num_leaves: lower=26, upper=66|NN_TORCH: dropout_prob: 0.0, 0.5|GBM: num_boost_round: 100|0.46402|


The `WeightedEnsemble_L3` model performed the best with a score of -30.252839 in AutoGluon.

Kaggle score: 0.46402.

