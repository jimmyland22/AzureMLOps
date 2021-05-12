# CMPE 258 Final Project
### Team United
#### Samer Baslan
#### Rohan Kumar
#### Jimmy Liang

## Project Overview
The goal of this project is to create a NLP based drug recommendation system and establish an end-to-end machine learning pipeline using an established Cloud service provider. We decided to focus on the Azure MLOps ecosystem for this project, including the following steps.
![MLOps](https://github.com/jimmyland22/AzureMLOps/blob/master/images/ml-lifecycle.png)

The dataset we used comes from UCI's Machine Learning Repository.

* [Drug Review (Druglib.com) Data Set](https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Druglib.com%29)
* [Drug Review (Drugs.com) Data Set](https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Drugs.com%29)

### Goals:
* Utilize Deep Learning to create a Drug Recommendation System.
* Explore MLOps for end-to-end Machine Learning. 
* Flask webapp frontend to invoke the inference API.

The machine learning model for this project will be 2-fold. 
1. Be able to take as input the text description of the symptoms that someone is experiencing, create an embedding, and using simple cosine similarity, compute the most likely drugs that is used to treat the symptoms.
2. Given that we have the reviews for each drug, we will use sentiment analysis and the drug's accompanying rating to predict whether a particular drug is good or not.
Using the above 2 criteria, we will offer a recommendation of which drug a user should take, given the symptoms.

We utilized Azure's MLOps tutorial as the mase of our MLOps setup. This includes creating an Azure DevOps project, connecting it to this GitHub repository, and creating multiple pipelines into an Azure ML Workspace. Changes to this repository will automatically trigger the Continuous Integration pipeline in Azure DevOps to train and register a model (if necessary).



## Deliverables
### Project Presentation
* Link to video here

### Colab
* Link to Colab
* Link to Colab 2

### Project Paper
* Link to report

## Trial & Errors
The team experimented with a lot of differnt things throughout this project to varying degrees of success.

### Model Building
#### Colab Notebooks
NLP is a hard topic to pick up. The team references many NLP examples on Kaggle and other places but ran into multiple issues along the way. As we are not experienced in Tensorflow, errors relating to version differences were very time consuming and hard to troubleshoot. Some of the reference notebooks we used include:
* [Recommendation Medicines by using a review](https://www.kaggle.com/chocozzz/recommendation-medicines-by-using-a-review)
* [Medicine Recommendation](https://www.kaggle.com/annabellachen/medicine-recommendation)
* [Sentiment Analysis and Product Recommendation](https://github.com/umaraju18/Capstone_project_2/blob/master/code/amazon_electronics_recommendation.ipynb)

#### AutoML
We tried using Azure AutoML to create various models and select the one with the best accuracy. We ran AutoML for over 24 hours and had to stop due to the cost it is incurring. It did create ~30 models, but the accuracy peaks at 20%.
![AutoML Trial](https://github.com/jimmyland22/AzureMLOps/blob/master/images/automl-trial.png)

### ML Designer
We used the Azure ML Designer to visually create training pipelines. It has a bit of a learning curve, as each 'block' is very specific on the data type it takes as an input.
![Designer Trial](https://github.com/jimmyland22/AzureMLOps/blob/master/images/ml-designer.png)

We also created an inference pipeline and an inference endpoing. We did run into errors that was not very descriptive. This might be a big issue with these 'black box' type designers.
![Inference Error](https://github.com/jimmyland22/AzureMLOps/blob/master/images/inference-error.png)

### MLOps
We followed the Azure **Getting Started with MLOpsPython** [Guide](https://github.com/microsoft/MLOpsPython/blob/master/docs/getting_started.md) tutorial to create the end-to-end machine learning pipeline. It was overall successful but we did ran into issues along the way due to the fast changing nature of this landscape and type of Azure account subscription we were using.

#### Issue 1
The first thing we ran into is that Azure changed how its parallel grants work for private projects [Azure Blog](https://devblogs.microsoft.com/devops/change-in-azure-pipelines-grant-for-private-projects/). We got past this first hurdle by going through the requesting process outlined in the blog.

#### Issue 2
We were using an Azure for Student subscription. While most things work flawlessly, there were some quirks that resulted in time consuling troubleshooting. Most of the issues relates to the level of permission that a student account has. 

