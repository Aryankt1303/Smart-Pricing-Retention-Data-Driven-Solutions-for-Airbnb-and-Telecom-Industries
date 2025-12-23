# Smart-Pricing-Retention-Data-Driven-Solutions-for-Airbnb-and-Telecom-Industries

1. Airbnb Price Prediction
Project Overview
The goal of this project was to predict Airbnb listing prices using regression models. By analyzing over 74,000 listings, the project aimed to identify the most important features that influence rental prices and provide actionable insights for hosts and platforms.
Dataset
- Size: 74,000+ listings
- Features: Property type, room type, number of bathrooms/bedrooms, amenities, location (latitude/longitude), host details, reviews, etc.
- Target Variable: log_price (transformed to stabilize variance)
Methodology
- Data Cleaning & Preprocessing
- Handled missing values (bathrooms, bedrooms, beds).
- Encoded categorical variables (room type, property type, cancellation policy).
- Engineered new features: amenities count, host experience years.
- Standardized numerical features (accommodates, reviews, latitude/longitude).
- Modeling
- Compared multiple regression models:
- Linear Regression (baseline, R² ≈ 0.54)
- Decision Trees
- Random Forest Regressor (best performer, R² ≈ 0.71 on test data)
- Hyperparameter tuning with RandomizedSearchCV.
- Feature Importance
- Top drivers of price:
- Room type (37%)
- Location (longitude/latitude ~24%)
- Bathrooms (12%)
- Reviews and amenities count (≈ 8%)
Results
- Best Model: Random Forest Regressor
- Performance: R² = 0.71 (test set)
- Key Insight: Room type and location are the strongest predictors of price.

2. Customer Churn Prediction
Project Overview
This project focused on predicting customer churn in a telecom dataset. The aim was to help the company identify customers at risk of leaving and design retention strategies.
Dataset
- Size: 7,000+ customer records
- Features: Demographics (gender, senior citizen, dependents), services (phone, internet, streaming), contract type, billing/payment methods, tenure, monthly charges, total charges.
- Target Variable: Churn (Yes/No)
Methodology
- Data Cleaning & Preprocessing
- Removed duplicates and handled missing values in TotalCharges.
- Encoded categorical variables (Contract, PaymentMethod, InternetService).
- Converted binary features (gender, partner, dependents, phone service).
- Modeling
- Tested multiple classifiers:
- Decision Tree (accuracy ≈ 73%)
- KNN (accuracy ≈ 77%)
- SVM (accuracy ≈ 79%)
- Random Forest Classifier (best performer, accuracy ≈ 95%)
- Hyperparameter tuning with RandomizedSearchCV (n_estimators = 300, random_state = 10).
- Evaluation
- Confusion Matrix & Classification Report:
- Accuracy: 94.7%
- Precision (Churn): 0.92
- Recall (Churn): 0.87
- F1-score: 0.89
- Feature Importance
- Top churn drivers:
- Tenure (26%)
- Monthly Charges (17%)
- Tech Support & Online Security (~10%)
- Contract type and payment method also significant.
Results
- Best Model: Random Forest Classifier
- Performance: 94.7% test accuracy
- Key Insight: Customers with short tenure, high monthly charges, and lack of support services are most likely to churn.

