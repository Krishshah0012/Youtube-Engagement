# Youtube-Engagement
ML pipeline predicting YouTube video engagement using sentiment, readability, upload behavior &amp; metadata (87% accuracy)

This project builds a machine learning pipeline to predict YouTube video engagement, measured by likes-to-views ratio, based on various metadata and content-derived features.

##  Project Overview

We aim to help creators and analysts forecast how engaging a video will be before uploading. By analyzing historical data, we predict whether a video will likely perform well using features like sentiment, readability, upload behavior, and metadata.

##  Dataset

- Cleaned dataset of YouTube videos from various creators
- Columns include:
  - `title`, `description`, `upload_time`, `keywords`, `likes`, `views`, `comments_enabled`, etc.

##  Features Engineered

| Feature                     | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `sentiment_score`          | Compound score from VADER (based on title text)                            |
| `readability_score`        | Flesch-Kincaid score using TextStat (on description)                       |
| `avg_gap_last_50_uploads`  | Mean time (in hours) between previous 50 uploads (consistency metric)       |
| `num_keywords`             | Count of YouTube tags                                                       |
| `length_title`, `length_desc` | Character length of title and description                                |
| `comments_enabled`         | Binary indicator for whether comments are turned off                        |
| `hour_of_day`, `day_of_week`| Time-related categorical variables for upload timing                       |

##  Tools & Technologies

- Python (Pandas, NumPy, scikit-learn)
- XGBoost, Random Forest, SVM
- VADER (NLTK), TextStat
- Matplotlib / Seaborn for visualization

##  Model Performance

| Model         | Accuracy | RMSE   | R² Score |
|---------------|----------|--------|----------|
| XGBoost       | 87%      | 0.041  | 0.72     |
| Random Forest | 84%      | 0.046  | 0.68     |
| SVM           | 79%      | 0.052  | 0.61     |

XGBoost performed the best after hyperparameter tuning using GridSearchCV.

##  Visualizations

- Correlation heatmaps
- Feature importance plots
- Engagement distribution by upload hour/day
- Sentiment vs. engagement scatter

##  Example Use Case

Upload metadata can be pre-scored for potential engagement, helping creators optimize:
- Video title
- Description clarity
- Upload timing
- Keyword/tag usage

##  Future Improvements

- Integrate deep learning with YouTube thumbnails
- Include video/audio sentiment via audio transcript analysis
- Automate real-time scoring from new video uploads

##  Contact

Built by **Krish Shah**  
Feel free to connect with me on [LinkedIn](linkedin.com/in/krish-shah-40a1b1244) or check out my other projects!
