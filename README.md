# -Rainfall-Binary-Prediction-From-84-to-90-Accuracy-
Overview Welcome to the 2025 Kaggle Playground Series! We plan to continue in the spirit of previous playgrounds, providing interesting and approachable datasets for our community to practice their machine learning skills, and anticipate a competition each month.
🛠️ Step-by-Step Process
1️⃣ Data Cleaning & Preprocessing
Loaded both train.csv and test.csv datasets.
Checked for missing values and handled them using forward fill (ffill) to ensure no NaNs are left.
Verified and corrected data types to ensure smooth processing.
2️⃣ Exploratory Data Analysis (EDA)
Plotted the distribution of rainfall to understand class balance.
Created a correlation heatmap to identify feature relationships.
Used pairplots to visualize trends between important features like humidity, dewpoint, sunshine, and rainfall.
Key EDA Insights:
humidity, cloud, and dewpoint showed a positive correlation with rainfall.
sunshine appeared to have a negative correlation with rainfall (logical right? Less sunshine, more rain! ☁️🌧️).
3️⃣ Feature Engineering
Selected key features:
pressure, maxtemp, temparature, mintemp, dewpoint, humidity, cloud, sunshine, winddirection, windspeed.
Applied StandardScaler to normalize the feature distribution.
4️⃣ Initial Model (Random Forest Classifier)
Split the data into train/validation sets.
Trained a Random Forest Classifier.
Initial Accuracy: 84%
RMSE: ~0.39
5️⃣ Handling Class Imbalance
Observed some imbalance in the rainfall data (0 vs 1 classes).
Applied SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset.
This helped improve generalization on the minority class.
6️⃣ Switched to XGBoost Classifier 🚀
Moved from Random Forest to XGBoost, known for its excellent performance on tabular datasets.
Tuned some basic hyperparameters like n_estimators, learning_rate, and max_depth.
Improved Accuracy to 88%
RMSE reduced to ~0.34
7️⃣ Final Step - Hyperparameter Tuning using GridSearchCV 🧠
Implemented GridSearchCV for automatic hyperparameter tuning.
Tuned parameters:
n_estimators
max_depth
learning_rate
subsample
colsample_bytree
After finding the best combination of hyperparameters, I retrained the model.
🎉 Final Results after Tuning:
Tuned Model Accuracy: 90.76% ✅
Tuned Model RMSE: 0.3040 ✅
📂 Final Steps
Generated predictions on the unseen test.csv data.
Created a proper submission file with columns id and rainfall for the competition.
🚀 Key Learnings:
Importance of handling imbalanced datasets with techniques like SMOTE.
XGBoost + Hyperparameter Tuning is a powerful combo for structured data.
Even small tweaks like tuning subsample and colsample_bytree can give that extra boost in accuracy.
🔵 Next step: I might explore Optuna for even more efficient hyperparameter tuning or try ensemble stacking.

#machinelearning #datascience #EDA #XGBoost #rainfallprediction #classification #gridsearchcv #python #mlops #linkedinlearning

