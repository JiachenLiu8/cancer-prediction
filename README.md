# Cancer prediction


I experiemented with the following **Machine Learning** techniques on the wisconsin cancer dataset:
+ **Kth Nearest Neighbor**
+ **Random Forest**
+ **Neural Networks**:  


The multiple python scripts are organized into the following sections:
+ **Exploratory Analysis**
+ **K-Nearest Neighbors**
+ **Random Forest**
+ **Multilayer Perceptron**


## Running .py Script
You could download all the necessary packages from the `requirements.txt` using:

	pip3 install -r requirements.txt

Once this is done you can then run the scripts using the usual terminal command:

	$ python3 exploratory_analysis.py

### Model performance and evaluation


| Model/Algorithm      | Test Error Rate | False Negative for Test Set | Area under the Curve for ROC | Cross Validation Score        | Hyperparameter Optimization |
|----------------------|-----------------|-----------------------------|------------------------------|-------------------------------|-----------------------|
| K-Nearest Neighbors  | 0.07  | 5 | 0.980 | Accuracy:  0.93 (+/-  0.03) | Optimal *K* is 3 |
| Random Forest        | 0.035 | 3 | 0.996 | Accuracy:  0.96 (+/-  0.01) | {'max_features': 'log2', 'max_depth': 3, 'bootstrap': True, 'criterion': 'gini'}	|
| Multilayer Perceptron| 0.035 | 1 | 0.982 | Accuracy:  0.97 (+/-  0.01) | {'hidden_layer_sizes': 12, 'activation': 'tanh', 'learning_rate_init': 0.05} |


The ROC Curves suggests **Random Forest** have a higher performance for this specific cases, though more extensive hyperparameter tuning could make a difference.
