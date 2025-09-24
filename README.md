# Machine-learning
STUDENTS SOCIAL MEDIA ADICTION
Problem statement
Student addiction towards social media is become a growing concern now a days, as excessive use of social media it is leading to reduced academic performance, poor concentration, disrupted sleep patterns, and isolation from the natural life. Here my project projects about the study of the students who have been addicted to social media and how it is affecting their day to day activities.
STAGE-1 Dateset selection with Initial EDA
Source-Kaggle
Timeline-2025
Location-Universal
Type of problem--Regression
Target feature
Addicted_score
Input feature Age Gender Academic_Level Country Avg_Daily_Usage_Hours Most_Used_Platform Affects_Academic_Performance Sleep_Hours_Per_Night Mental_Health_Score Relationship_Status Conflicts_Over_Social_MediaRows: 705, Columns: 13. All columns are almost filled in this file. sleep hours is strongly associated with addiction, mental-health score, and conflict indicators in this dataset.
Number of duplicate rows: 0

Duplicate rows:
Empty DataFrame
Columns: [Student_ID, Age, Gender, Academic_Level, Country, Avg_Daily_Usage_Hours, Most_Used_Platform, Affects_Academic_Performance, Sleep_Hours_Per_Night, Mental_Health_Score, Relationship_Status, Conflicts_Over_Social_Media, Addicted_Score]
 Avg_Daily_Usage_Hours is the only feature with outliers. All other numeric features (Age, Sleep Hours, Mental Health Score) have no outliers.
The skewness values before and after transformation are almost the same.That’s because none of the numerical columns are highly skewed (all are close to 0, within -0.5 to +0.5).
So I could see that in this dataset skewness is not a big problem and did not need any transformations. 
Most students spend 4–6 hours/day on social media, this corresponds with slightly reduced sleep in some cases (<6 hours).
Addiction scores are mostly on the higher side supporting the concern While most data is normally distributed, outliers exist in high usage and low sleep patterns, indicating risk groups.
Higher daily usage, reduced sleep, lower mental health, and more conflicts are all strongly linked with higher addiction scores.
 Dropped ID column (not useful for modeling).

Encoded categorical features:

Label Encoding for binary categories (Gender, Academic Performance, Relationship Status).

One-Hot Encoding for multi-class categories (Academic Level, Country, Most Used Platform).

Scaled numerical features:

StandardScaler (mean=0, std=1).

MinMaxScaler (range [0,1]).
Dropped ID column (not useful for modeling).

Encoded categorical features:

Label Encoding for binary categories (Gender, Academic Performance, Relationship Status).

One-Hot Encoding for multi-class categories (Academic Level, Country, Most Used Platform).

Scaled numerical features:

StandardScaler (mean=0, std=1).

MinMaxScaler (range [0,1]).
Model training
Used Linear Regression--baseline model for regression tasks

Data was splitted into 80% for training and 20% for testing.

Model learns the relationship between independent variables (features like usage patterns, demographics, etc.) and the target (Addicted_Score).
Project: Predicting Students Social Media Addiction
The project's aim is to build a machine learning system that predicts whether a student is addicted to social media based on survey data.

It included the process of Data preparation Model training Hyperparameter tuning and performance evaluation.

Process Overview
Dataset Inspection: Checked the dataset for structure, missing values, and identified the target column as addicted score.

Exploratory Data Analysis: Explored class balance Feature distributions and correlations to understand underlying patterns.

Data Preprocessing: Cleaned missing values, standardized numeric features, and converted categorical data into machine-readable form.

Train/Test Split: Divided the dataset into training (80%) and testing (20%) sets to fairly evaluate performance.

Models Used:

Random Forest

Gaussian Naive Bayes

Support Vector Machine

Hyperparameter Tuning: Applied RandomizedSearchCV to optimize each model’s parameters for best performance.

Key Findings

Random Forest generally performed best, offering a balance of accuracy and robustness.

Naive Bayes was simple and fast but less accurate.

SVM provided good results but was slower on larger datasets.

Evaluation showed the importance of checking both accuracy and other metrics like precision/recall, especially in imbalanced datasets.

Challenges & Solutions

Missing values: Handled with imputation strategies.

Deploy the best model as a web application for real-time predictions.

Conclusion

The project successfully demonstrates a complete workflow from raw data to evaluated and saved predictive models. Random Forest emerged as the most reliable model.

project documentation
Target creation — Addicted_Score Binarized it using the median

Did Feature engineering and future enhancements

Handled NaNs / infinities produced by ratios.

Preprocessing pipeline:

Numeric imputation (median) + StandardScaler.

Categorical imputation (most_frequent) + OneHotEncoder.

Modeling:

GridSearchCV for LogisticRegression and RandomForest using compact grids

Feature importance:

Top features were displayed.

Converted Addicted_Score → binary target.

LogisticRegression Test ROC AUC ≈ 0.9998

RandomForest Test ROC AUC ≈ 1.0000

The AUC values are extremely high
