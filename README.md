# YouTube Video Engagement Prediction Project

## Project Overview

This project aims to predict engagement metrics (likes, comments, dislikes) for YouTube videos. The dataset includes video details such as view count, description, publication date, and sentiment analysis of video descriptions. The goal is to build a regression model to accurately predict engagement ratios and analyze the factors influencing video engagement.

## Data Preprocessing

### Handling Missing Values
- NaN values in numerical columns were imputed using mean imputation.
- Infinite values in the target variable were replaced with NaN and corresponding rows were removed.

### Feature Engineering
- Extracted features like hour, day, month, and day of the week from the 'publishedAt' column.
- Calculated engagement ratio: (likes + comments + dislikes) / views.

## Exploratory Data Analysis (EDA)

### Visualizations
- Correlation heatmap was generated to understand feature correlations.
- Scatter plots, histograms, and box plots were used to explore relationships between variables.
- Distribution of engagement ratio and videos published by day of the week were visualized.

### Analysis Results

- **Correlation Heatmap:** There is a strong positive correlation between 'view_count', 'likeCount', and 'commentCount'. 'Engagement_ratio' has a moderate negative correlation with 'view_count' and 'likeCount'.

- **Engagement Ratio Distribution:** The engagement ratio ranges from 0.008970 to 0.040725 with a mean of 0.019880.

- **Day of Week Distribution:** Videos are most frequently published on Mondays (11 videos) and least on Wednesdays (2 videos).

- **Top 20 Most Common Words in Descriptions:** Most common words include punctuation marks, common stop words, and channel-related terms like 'VICE'. 

- **Sentiment Distribution in Descriptions:** The sentiment in video descriptions is evenly split between positive and negative.

## Model Selection and Evaluation

### Random Forest Regressor
- Utilized Random Forest Regressor for prediction.
- Hyperparameters were tuned using GridSearchCV.
- Evaluated using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared scores.

### Model Performance
- Achieved MSE of 460214439.117984, MAE of 6052.098400000001, and R-squared of 0.8380994530651474.

## Addressing Class Imbalance

### Synthetic Minority Over-sampling Technique (SMOTE)
- Applied SMOTE to balance the class distribution in the target variable.

### Performance Improvement
- After addressing class imbalance, the model achieved improved accuracy and F1 scores.

## Model Comparison and Selection

### Comparison of Models
- Compared Random Forest Regressor, K-Nearest Neighbors, and Naive Bayes models.
- Visualized accuracy scores to identify the best-performing model.

### Best Model
- K-Nearest Neighbors outperformed other models with the highest accuracy and F1 score.

## Future Steps

### Further Tuning
- Continuous improvement by fine-tuning hyperparameters or exploring different algorithms.

### Additional Features
- Exploring additional features or engineered features to enhance model performance.

### Deployment
- Deployment for real-time predictions, possibly integrated into a web application or used via API endpoints.

### Monitoring and Maintenance
- Continuous monitoring of the model's performance and periodic retraining for accuracy and relevance.
