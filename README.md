# Sentiment-Analysis-on-AWS-SageMaker

This project performs sentiment analysis on movie review data using AWS SageMaker.

## Overview

The SageMaker Project Jupyter notebook trains a recurrent neural network (RNN) model to perform binary sentiment classification on IMDB movie review data. The model is trained and deployed using Amazon's SageMaker service.

The notebook performs the following steps:

1. Downloads and explores the IMDB dataset
2. Uploads the data to S3
3. Trains an RNN model on SageMaker using the training data
4. Deploys the trained model to a SageMaker endpoint
5. Evaluates the deployed model on test data

## Setup Instructions

The notebooks provided in this repository are intended to be executed using Amazon's SageMaker platform. The following is a brief set of instructions on setting up a managed notebook instance using SageMaker, from which the notebooks can be completed and run.

### Log in to the AWS console and create a notebook instance

Log in to the AWS console and go to the SageMaker dashboard. Click on 'Create notebook instance'. The notebook name can be anything and using ml.t2.medium is a good idea as it is covered under the free tier. For the role, creating a new role works fine. Using the default options is also okay. Important to note that you need the notebook instance to have access to S3 resources, which it does by default. In particular, any S3 bucket or objectt with sagemaker in the name is available to the notebook.

### Use git to clone the repository into the notebook instance

Once the instance has been started and is accessible, click on 'open' to get the Jupyter notebook main page. We will begin by cloning the SageMaker Deployment github repository into the notebook instance. Note that we want to make sure to clone this into the appropriate directory so that the data will be preserved between sessions.

Click on the 'new' dropdown menu and select 'terminal'. By default, the working directory of the terminal instance is the home directory, however, the Jupyter notebook hub's root directory is under 'SageMaker'. Enter the appropriate directory and clone the repository as follows.

```bash
cd SageMaker
git clone https://github.com/udacity/sagemaker-deployment.git
exit
```

After you have finished, close the terminal window.

## Results

The trained RNN model achieves an accuracy of over 85% on the IMDB test set.