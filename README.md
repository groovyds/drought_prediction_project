# drought_prediction_project
We will utilize both Supervized and Unsupervized ML models to predict degree of drought and evaluate our models!

Kaggle Drought Prediction Project link: 
https://www.kaggle.com/code/emircengel/drought-prediction/notebook

# Drought Prediction Project

## Project Overview
This project aims to predict the degree of drought in various regions based on a dataset containing environmental and weather-related features. The drought levels range from D0 to D4, with D0 representing abnormally dry conditions and D4 indicating exceptional drought.

To tackle this problem, I employed both supervised learning and unsupervised learning techniques to explore and compare model performance.

## Problem Statement
Drought prediction is crucial for water resource management, agriculture, and environmental conservation. The goal of this project is to build machine learning models that predict the drought level (D0, D1, D2, D3, D4) based on historical weather and environmental data.

## Dataset
The dataset used in this project includes the following features:

Weather-related features (e.g., precipitation, temperature, wind speed),
Geographical and environmental data (#fips),
Time-based attributes (day, month, year),
Every seven days, a record is labeled with a drought level ranging from D0 (least severe) to D4 (most severe).
This means score is available every week.

# Data Preprocessing
Missing data handling ( six days of every 7 days is missing the label)
Feature scaling and normalization
Feature engineering (time-based attributes like year, month, day)
Outlier removal using techniques like the 3-sigma rule or IQR

# Machine Learning Models
## Supervised Learning
For the supervised learning models, the target variable was the drought level, and several algorithms were tested and optimized:

Random Forest Classifier: Used for feature selection. 
Decision Trees: Used for multi-class classification of drought levels. 
KNN Classifier. 

Evaluation Metrics: F1-score, Recall, Accuracy, and Confusion Matrix.

# Unsupervised Learning
Also explored unsupervised methods, particularly clustering models, to identify patterns within the data without predefined drought levels:

K-Means Clustering: Applied to the dataset to identify groups of similar regions or conditions based on the environmental data.
Silhouette Score was used to evaluate the clustering quality.


# Results
Supervised Models: KNN Classifier outperformed the Decision Tree model, achieving an accuracy of 77% and an F1-score of 76%.
Unsupervised Models: The K-Means Clustering model identified 2 distinct clusters with silhouette score of 28% as the best score, but we have to keep in mind it only trained on 100,000 samples out of 2,800,000.

# Conclusion
Supervised models such as the Random Forest Classifier would have showed significant improvement in predicting drought levels compared to Decision Tree model but it would have taken considerably longer on every single level. If we were to judge by only the Decision Tree it did not seem promising, not in the least when compared to the KNN Classifier we applied too. We can conclude the Tree based algorithms may not be suitable for this prediction.

The unsupervised K-Means algorithm helped uncover hidden patterns in the data but was less effective in directly predicting drought levels.

## Future Work
Explore other unsupervised learning techniques, such as DBSCAN or Hierarchical Clustering.
Integrate external data sources for better predictive accuracy.
Apply advanced techniques like deep learning to improve performance.




