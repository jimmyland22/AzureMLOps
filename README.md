# CMPE 258 Final Project
### Team United
#### Samer Baslan
#### Rohan Kumar
#### Jimmy Liang

## Project Overview
The goal of this project is to create a NLP based drug recommendation system and establish an end-to-end machine learning pipeline using an established Cloud service provider. We decided to focus on the Azure MLOps ecosystem for this project.
![MLOps](https://github.com/jimmyland22/AzureMLOps/blob/master/images/ml-lifecycle.png)

Utilizing the [UCI Drug Review dataset](https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Drugs.com%29)

### Goals:
* Utilize Deep Learning to create a Drug Recommendation System
* Explore MLOps for end-to-end Machine Learning. 

## Deliverables
### Project Presentation
* Link to video here

### Colab
* Link to colab1
* Link to Colab 2

### Project Paper
* Link to report

## Trial & Errors
The team experimented with a lot of differnt things throughout this project to varying degrees of success.

### Model Building
#### Colab Notebooks
NLP is a hard topic to pick up. The team references many NLP examples on Kaggle and other places but ran into multiple issues along the way. As we are not experienced in Tensorflow, errors relating to version differences were very time consuming and hard to troubleshoot. Some of the reference notebooks we used include:
* link...

#### AutoML
We tried using Azure AutoML to create various models and select the one with the best accuracy. We ran AutoML for over 24 hours and had to stop due to the cost it is incurring. It did create ~30 models, but the accuracy peaks at 20%.
![AutoML Trial](https://github.com/jimmyland22/AzureMLOps/blob/master/images/automl-trial.png)

### ML Designer
We tried using the Azure ML Designer to visually create training pipelines
![Designer Trial](https://github.com/jimmyland22/AzureMLOps/blob/master/images/ml-designer.png)

