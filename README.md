# Song-BPM-Prediction-LGBM
Kaggle Competition: Predicting the BPM of songs with a LGBM model

<img width="560" height="280" alt="image" src="https://github.com/user-attachments/assets/af1e69a6-18d5-4af2-80c9-e11671aeb99d" />

---

### About the Project

This notebook has been completed as part of Kaggle's Playground Prediction Competition [Predicting the Beats-per-Minute of Songs](https://www.kaggle.com/competitions/playground-series-s5e9/overview).

I have created this notebook to provide a simple, understandable solution. As with most of my work on Kaggle, I try to explain each line of code so that anyone, from budding data scientist to machine learning pro, can understand my process and hopefully learn something new.

The overarching goal of this project is to predict a song's beats per minute (BPM). In music, tempo is the speed or pace of a given composition and is measured in BPM. For example, a song with 60 BPM has one beat per second, while a song with 120 BPM has two beats per second.

As BPM is represented by a numeric value, this project is thus a regression task, i.e. the goal is to predict a continuous numeric value based upon the given independent features. Regression problems can be solved by utilizing supervised learning techniques such as linear regression, support vector machines, decision trees, random forests, and ensemble learning.

The model I have selected for this project is [Light Gradient Boosting Machine](https://lightgbm.readthedocs.io/en/latest/index.html) (LGBM). LGBM is an ensemble learning framework that leverages multiple decision trees and gradient boosting. LGBM works by growing leaves with the highest loss reduction and thus sequentially minimizes loss using gradient descent. LGBM is an excellent tool for tabular data problems and I have enjoyed using it for various regression and classification tasks.

The evaluation metric used for this project and competition is the [Root Mean Squared Error](https://en.wikipedia.org/wiki/Root_mean_square_deviation) (RMSE). This is a typical metric used for evaluating the predictive performance of regression models. The goal here is to MINIMIZE this value.

<img width="479" height="201" alt="image" src="https://github.com/user-attachments/assets/11668c6b-d0ed-4ae7-afaa-277e2956a724" />

The general structure/pipeline of this project is as follows:
- Set up & data loading
- Exploratory data analysis (viewing distributions and interactions)
- Data preprocessing (cleaning, removing outliers, feature engineering)
- Modeling (cross validation with KFold)

I hope you enjoy this project! If you have any comments, questions, criticism, or recommendations, please let me know. I'm always eager to continue to refine my data skills and learn from this community.

---

### About the Data

The data used in this project is synthetically generated tabular data provided by Kaggle. This data was generated from the original [BPM Prediction Challenge](https://www.kaggle.com/datasets/gauravduttakiit/bpm-prediction-challenge) dataset.

Typically, as mentioned by Kaggle, the feature distributions of both the original and synthetic data are roughly similar, but not exactly the same. In past competitions, I have used [adversarial validation](https://blog.zakjost.com/post/adversarial_validation/) to test the degree of difference between the original and Kaggle datasets.

For this particular project, I wanted to streamline my notebook and thus have not included adversarial validation. However, I did complete this behind the scenes and found that the datasets had significantly different feature distributions (AUC-ROC ~0.86). Because of this, I have opted to not include the original data in this project. However, training a model with more robust data (different distributions) may help generalize performance on novel/test data.

Target Variable:
- BeatsPerMinute

Features:
- id
- RhythmScore
- AudioLoudness
- VocalContent
- AcousticQuality
- InstrumentalScore
- LivePerformanceLikelihood
- MoodScore
- TrackDurationMs
- Energy

---

### Methods
Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- catboost
- sklearn
- lightgbm
- shap
- optuna

---

### Results

<img width="720" height="479" alt="image" src="https://github.com/user-attachments/assets/b927d2fb-0196-46fa-ba72-dae483f3078f" />

<img width="1014" height="556" alt="image" src="https://github.com/user-attachments/assets/329a5bf5-c1ed-49dd-8ee1-e8b4acce8c08" />
