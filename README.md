# Epicurious-Recipe-Prediction

An independent data anlysis project focusing on cleaning and analyzing a dataset containing over 20,000 Epicurious recipes. Provides summary statistics and an analysis of machine learning models to predict the Desert category of a given recipe.

## Goal
I wanted to take on this project as a way to learn about Microsoft Azure's data storage and integration capabilities as well as how to use Databricks as a data engineeing, data science, and machine learning tool. Therefore, a large part of the project was self learning the fundumentals of building data storage containers on Azure and connecting the data lake to Databricks. From there, I was able to utilize my existing machine learning skills to conduct analysis on the dataset.

### The Dataset
I found an interesting looking dataset on Kaggle which contains over 20,000 recipes that were scraping direct from the Epicurious website. Each recipe includes nutritional information and binary indicators for 680 categories into which that recipe may fall. I thought that this would be a cool dataset to play around with because it has both numerical and categorical features. I wanted to experiment to see which type of features did the best at making pedictions.

Datset found here: https://www.kaggle.com/datasets/hugodarwood/epirecipes

### Data Engineeing Component
After setting up a Microsoft Azure account, I created an ELT pipeline that ingests data from the Azure cloud storage and loads it into Azure Databricks. This involved creating a Blob Storage Account and loading my dataset into a the container. I then created a notebook in Azure Databricks to mount the Blob Storage Account to the Databricks File System. In the end, this ingests raw data as PySpark data frame and stores it as table on Databricks Delta Lake. Now I can access any data that I upload to the Azure cloud storage container from my Databricks Workspace.

Note: I was only using the 14-day free trial, so I couldn't continue to use Databricks after that. The file in this repo is just the notebook from my Databricks Workspace.

### Data Science Component
Given the finalized pipeline, I was able to analysis on the Epicurious dataset just as I would using a simple Jupyter Notebook. You will find that in the notebook, I outline my process and insights I derived along the way. It walks through how I cleaned and preprocessed the data, goes through model training and testing, hyperparamter tuning, and finally concludes with a summary of how my models peformed.

### Running this code
I've included the dataset I used as well as the code file. You can simply doownload both and run it as you normally would a Jupyter Notebook.
