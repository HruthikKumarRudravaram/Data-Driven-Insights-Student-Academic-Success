# Data-Driven-Insights-Student-Academic-Success
Led EDA on 30+ student performance features with Python. Identified strong correlation (≈0.75−0.85) between study hours &amp; exam scores. Produced 10+ visualizations for actionable insights, driving student success.

# Student Performance Analytics: Exploratory Data Analysis (EDA)

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on a dataset related to student habits and academic performance. The primary goal is to understand the underlying patterns, relationships, and insights within the data that may influence student exam scores. This analysis leverages various Python libraries for data manipulation, statistical summarization, and comprehensive data visualization.

## Dataset

The analysis uses the `student_habits_performance.csv` dataset, which includes the following features:
* `student_id`
* `age`
* `gender`
* `study_hours_per_day`
* `social_media_hours`
* `netflix_hours`
* `part_time_job`
* `attendance_percentage`
* `sleep_hours`
* `diet_quality`
* `exercise_frequency`
* `parental_education_level`
* `internet_quality`
* `mental_health_rating`
* `extracurricular_participation`
* `exam_score`

## Exploratory Data Analysis (EDA) Steps & Key Findings

The EDA process involved several critical steps to understand the dataset's characteristics and uncover meaningful insights:

1.  **Environment Setup & Data Loading**:
    * Imported `pandas`, `numpy`, `matplotlib.pyplot`, and `seaborn` for data handling and visualization.
    * Loaded the `student_habits_performance.csv` file into a pandas DataFrame.

2.  **Initial Data Inspection**:
    * Inspected the first and last 5 rows of the DataFrame (`df.head()`, `df.tail()`) to get a quick overview of the data structure and content.
    * Checked the dataset's dimensions (`df.shape`) to confirm 1000 rows and 16 columns.
    * Examined data types for each column (`df.dtypes`) to ensure appropriate data representation (e.g., numerical vs. categorical).
    * Converted the 'mental_health_rating' column from numerical to categorical type, as it represents a rating scale.

3.  **Missing Values & Summary Statistics**:
    * Verified the presence of missing values across all columns using `df.isnull().sum()`, identifying 91 missing entries in 'parental_education_level' and no others.
    * Generated descriptive statistics (`df.describe()`) for numerical features to understand central tendencies, spread, and potential outliers.

4.  **Feature Separation**:
    * Programmatically separated features into `categorical_features` and `numerical_features` lists based on their data types for targeted analysis.
    * Performed value counts for all categorical features to analyze their distribution (e.g., gender, part-time job, diet quality).

5.  **Data Visualization & Relationship Discovery**:

    * **Histograms of Numerical Features**:
        * Visualized the distribution of all numerical features using histograms (`df[numerical_features].hist()`).
        * *Finding*: Helps in understanding the skewness and spread of data like 'age', 'study_hours_per_day', 'exam_score', etc.

    * **Correlation Heatmap**:
        * Generated a heatmap to visualize the correlation coefficients between numerical features.
        * *Finding*: Provided an immediate view of strong and weak linear relationships between variables (e.g., 'study_hours_per_day' and 'exam_score' showed a strong positive correlation).

    * **Study Hours vs. Exam Score Scatterplot**:
        * Created a scatterplot to analyze the relationship between 'study_hours_per_day' and 'exam_score', differentiated by 'part_time_job' status.
        * *Finding*: Observed a **strong positive linear relationship** (clear upward trend) between study hours and exam scores. Students studying less than 2 hours/day tended to have lower, more varied scores. The presence of a part-time job did not significantly alter this trend.

    * **Social Media Hours vs. Exam Score Scatterplot**:
        * Visualized 'social_media_hours' against 'exam_score', also split by 'part_time_job'.
        * *Finding*: Showed a **very weak or no clear correlation**. Scores were randomly scattered, with high social media usage only slightly associated with lower scores. Part-time job status had no visible impact.

    * **Netflix Hours vs. Exam Score Scatterplot**:
        * Plotted 'netflix_hours' against 'exam_score', distinguishing by 'part_time_job'.
        * *Finding*: Similar to social media, a **very weak or no clear correlation** was observed. High Netflix hours (>3) were slightly linked to lower scores, but the overall relationship was minimal. Part-time job status had no visible impact here.

    * **Exercise Frequency vs. Exam Score Scatterplot**:
        * Examined 'exercise_frequency' against 'exam_score', with 'part_time_job' as hue.
        * *Finding*: No clear pattern or strong correlation was visible; exam scores were widely spread across all exercise frequencies. Exercise frequency and part-time work did not show an obvious correlation to exam scores.

    * **Mental Health Rating vs. Exam Score Boxplot**:
        * Used box plots to compare the distribution of 'exam_score' across different 'mental_health_rating' categories.
        * *Finding*: Revealed a **slight upward trend**, where higher mental health ratings (7-10) were associated with slightly higher median exam scores. However, significant variability remained across all ratings.

    * **Mean Exam Scores by Mental Health Rating**:
        * Calculated the mean 'exam_score' for each 'mental_health_rating' category to numerically support the boxplot observations.
        * *Finding*: Confirmed the upward trend, with mean scores generally increasing from 62.37 (rating 1) to 77.95 (rating 10), reinforcing that better mental health is associated with improved academic performance.

## Conclusion

This EDA project successfully identified key factors influencing student academic performance, most notably the strong positive correlation between study hours and exam scores. While some lifestyle factors like social media, Netflix usage, and exercise frequency showed very weak or no clear correlation, mental health rating demonstrated a subtle positive association with performance. These insights can inform further analysis, predictive modeling, or intervention strategies aimed at improving student outcomes.

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook** (or similar environment like Google Colab, VS Code)

## How to Run

1.  **Clone the repository** (if applicable) or download the `Student Performance Analytics.ipynb` file.
2.  Ensure you have Python installed, along with the required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`). You can install them via pip:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
3.  Place the `student_habits_performance.csv` dataset in the same directory as the Jupyter Notebook file.
4.  Open the notebook using Jupyter Notebook, JupyterLab, Google Colab, or VS Code with the Python extension.
5.  Run the cells sequentially to reproduce the analysis.
