# Online News Popularity Prediction

## Project Overview
This project aims to predict the popularity rating of online news articles based on various features such as content length, keyword statistics, sentiment polarity, and other metadata. The prediction is formulated as a classification problem where the model assigns a discrete rating (1 to 5) to each article.

## Dataset
The dataset used is **Online News Popularity**, which contains various attributes extracted from online news articles. The dataset includes features related to textual content, social engagement, and metadata.

### Key Features
- `n_tokens_title`: Number of words in the title
- `n_tokens_content`: Number of words in the content
- `num_hrefs`: Number of hyperlinks
- `num_imgs`: Number of images
- `kw_avg_avg`: Average keyword frequency
- `title_sentiment_polarity`: Sentiment score of the title
- `rating`: The target variable (discrete values 1 to 5)

## Data Preprocessing
1. **Handling Missing Values**: Checked and imputed missing values if any.
2. **Outlier Detection and Removal**: Used the IQR method to remove extreme outliers.
3. **Feature Scaling**: Applied MinMaxScaler to normalize numerical features.
4. **Handling Skewness**: Used transformations such as Log, Box-Cox, and Yeo-Johnson.
5. **Class Imbalance Handling**: Used SMOTE (Synthetic Minority Over-sampling Technique) to balance class distribution.

## Exploratory Data Analysis (EDA)
- **Pairplot Analysis**: Checked relationships between numerical variables.
- **Violin and Box Plots**: Visualized distributions of key features.
- **Heatmap**: Analyzed feature correlations.
- **Countplot**: Checked class distribution of the target variable.

## Model Selection
Several machine learning models were tested for classification:
- Logistic Regression
- Random Forest
- Gradient Boosting
- Support Vector Machine (SVM)

## Model Evaluation
The models were evaluated using:
- **Accuracy**: Percentage of correctly classified articles.
- **Precision, Recall, F1-score**: Evaluated using a classification report.
- **Confusion Matrix**: Visualized misclassification.
- **ROC Curve**: Measured model performance using AUC-ROC.

## Results
- The best-performing model was **XGBoost**, achieving the highest accuracy and F1-score.
- Feature importance analysis showed that `title_sentiment_polarity`, `kw_avg_avg`, and `n_tokens_content` were the most influential features.

## Conclusion
- The model successfully predicts article popularity with high accuracy.
- Preprocessing techniques like handling skewness, scaling, and SMOTE improved performance.
- Future improvements can include deep learning models like LSTMs for better text representation.

## How to Run the Project

1. Load the dataset and run `Online_News_Popularity_Project.ipynb`.
2. Train the model and evaluate results.

## Contributors
- Bibin C Mathew

## License
This project is open-source and available under the MIT License.

