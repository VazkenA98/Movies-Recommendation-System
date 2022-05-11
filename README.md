# Movies-Recommendation-System
Movie Recommendation System built with Python, Collaborative Filtering and Surprise library

# Dataset

# SET1: DATA Wrangling

## Step1_Loading Raw data, Preprocessing and Train Test split.ipynb
This notebook takes the full raw dataset, creates a data frame and also divides into train & test. (This train dataset has later been used in Step3 EDA notebook)

## Step2_Dataset Dimensionality Reduction (Size Reduction).ipynb: 
This notebook takes the above step's full data frame, slices the data using various filters (i.e., makes a smaller dataset) and creates train_slice.csv and test_slice.csv

## Step3_Exploratory Data Analysis on Train Data_FINAL.ipynb:  
This notebook takes the full dataframe of step 1 and does various EDA. No other notebook depends on this notebook, hence even if this notebook is not present, there will not be any impact on any other notebook.

# SET2: Cosine similarity

## Step4_Computing Similarity Matrices and Prediction using Cosine Similarity.ipynb: 
This notebook does not depend on Step3 notebook.  
This takes train_sliced.csv as input and calculates Cosine Similarity matrices (User-User Cosine Similarity Matrix and Movie-Movie Similarity Matrix)
This notebook also recommends movies for a user id
Steps Followed:
1. Find the last n (say last 2) liked movies for a user (which he rated high 4 or 5)
2. Find movies similar to above n movies, and recommend to the user 

# SET3: Models from Surprise Library

## Step5_Building_Recommender_System_with_Surprise.ipynb
This takes data_sliced.csv as input (as train-test division is done by surprise library only internally)
After some exploratory data analysis, various modes from the surprise library are trained on the dataset. These models are: KNN, NMF, SVD etc.
Best performing model is used for prediction.
Here, we are not finding similar movies (which was the approach taken for Cosine Similarity methods). Instead, the approach taken here is: rating is predicted for all the movies for a given user id and then, top n ratings are recommended to the user.


