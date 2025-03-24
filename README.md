# Diabetes-Prediction
Diabetes Prediction Using Random Forest

Data Preprocessing

Handling Missing or Incorrect Values

Observed that some columns contain incorrect values. For example:

SkinThickness has many instances with a value of 0, which is unrealistic.

Insulin also has several instances with 0, which is unlikely.

Replaced these incorrect values with the median of the respective columns.

Identifying Patterns in Data

Count plot analysis shows:

Individuals with 0 to 7 pregnancies have a lower chance of diabetes.

Individuals with more than 7 pregnancies have a higher chance of diabetes.

Glucose Levels:

125-140 mg/dL: Lower chances of diabetes.

Above 140 mg/dL: Higher chances of diabetes.

Handling Outliers

Detected outliers in multiple columns.

Used the Interquartile Range (IQR) method to handle outliers.

After removing outliers, merged the cleaned data back into the main dataset.

Model Training

Random Forest Classifier

Initial accuracy on the imbalanced dataset: 72.63%

Imbalanced dataset issue: The dataset had a skewed class distribution (95% class 0, 5% class 1), leading to the model ignoring the minority class.

Applying SMOTE for Balancing Data

Used SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset.

Applied balanced data to the Random Forest Classifier.

Final accuracy after balancing the data: 73.1%

Conclusion

Handling missing values and outliers improved data quality.

Balancing the dataset using SMOTE helped improve model performance.

Future improvements can include hyperparameter tuning and trying different models for better accuracy.
