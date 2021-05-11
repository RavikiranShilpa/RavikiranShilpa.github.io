# Portfolio

## Natural Language Processing


### Detect Non-negative Airline Tweets: BERT for Sentiment Analysis

[![Run in Google Colab](https://img.shields.io/badge/Colab-Run_in_Google_Colab-blue?logo=Google&logoColor=FDBA18)](https://colab.research.google.com/drive/1lwa-qlK-ZnYpJgErZQXv4mjxTsa_ed1U)

<div style="text-align: justify">The release of Google's BERT is described as the beginning of a new era in NLP. In this notebook I'll use the HuggingFace's transformers library to fine-tune pretrained BERT model for a classification task. Then I will compare BERT's performance with a baseline model, in which I use a TF-IDF vectorizer and a Naive Bayes classifier. The transformers library helps us quickly and efficiently fine-tune the state-of-the-art BERT model and yield an accuracy rate 10% higher than the baseline model.</div>

<center><img src="images/BERT-classification.png"/></center>

---
### Detect Food Trends from Facebook Posts: Co-occurence Matrix, Lift and PPMI

[![Open Notebook](https://img.shields.io/badge/Jupyter-Open_Notebook-blue?logo=Jupyter)](projects/detect-food-trends-facebook.html)
[![View on GitHub](https://img.shields.io/badge/GitHub-View_on_GitHub-blue?logo=GitHub)](https://github.com/chriskhanhtran/facebook-detect-food-trends)

<div style="text-align: justify">First I build co-occurence matrices of ingredients from Facebook posts from 2011 to 2015. Then, to identify interesting and rare ingredient combinations that occur more than by chance, I calculate Lift and PPMI metrics. Lastly, I plot time-series data of identified trends to validate my findings. Interesting food trends have emerged from this analysis.</div>
<br>
<center><img src="images/fb-food-trends.png"></center>
<br>

---


## Data Science

### Kaggle Competition: Predict Ames House Price using Lasso, Ridge, XGBoost and LightGBM

[![Open Notebook](https://img.shields.io/badge/Jupyter-Open_Notebook-blue?logo=Jupyter)](projects/ames_house_price.html)
[![View on GitHub](https://img.shields.io/badge/GitHub-View_on_GitHub-blue?logo=GitHub)](https://github.com/RavikiranShilpa/ML-case-study/blob/master/ames_house_price.ipynb)

<div style="text-align: justify">I performed comprehensive EDA to understand important variables, handled missing values, outliers, performed feature engineering, and ensembled machine learning models to predict house prices. My best model had Mean Absolute Error (MAE) of 12293.919, ranking <b>95/15502</b>, approximately <b>top 0.6%</b> in the Kaggle leaderboard.</div>
<br>
<center><img src="images/ames-house-price.jpg"/></center>
<br>

---



<center>© 2020 Shilpa angadi. Powered by Jekyll and the Minimal Theme.</center>
