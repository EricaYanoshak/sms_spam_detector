# Transformers and Language Models: SMS Spam Detector Challenge
This week's challenge involved refactoring code for a binary text classification model. Specifically, transforming code from a previous activity into a function that constructs a linear SVC model, and provides feedback to users.

## Installation
The following libraries and dependencies were used to successfully run this project:
* Install Gradio if not already installed: `!pip install gradio`
* import pandas as pd
* from sklearn.model_selection import train_test_split
* from sklearn.pipeline import Pipeline
* from sklearn.feature_extraction.text import TfidfVectorizer
* from sklearn.svm import LinearSVC
* import gradio as gr 

## Description
This assignment consisted of refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created, Gradio is used to host and test the application. The application provides feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

## Methodology
### Part 1: Create the SMS Classification Function
Set the variables and split the data into training and testing sets. Followed by building a pipeline to transform the test set to compare to the training set, fit the model to the transformed training data and return model. Finally load the csv file into a DataFrame and call the sms_classification function, settng the result to the "text_clf" variable.

### Part 2: Create the SMS Prediction Function
Use the sms_prediction function to predict the classification of a new text.

### Part 3: Create the Gradio Interface Application
Create a Gradio Interface application that takes a textbox for the inputs and has a textbox for the output, with labels. 

### Part 4: Launch and Test the Gradio Application
- Launch the Gradio application: Running on public URL: https://a6eab2328ed8c72514.gradio.live

[**SMS Prediction Gradio Application Interface**](https://a6eab2328ed8c72514.gradio.live/)
 
- Testing the Gradio application and Results
  1. You are a lucky winner of $5000! = **NOT SPAM**
  2. You won 2 free tickets to the Super Bowl. = **SPAM**
  3. You won 2 free tickets to the Super Bowl. Text us to claim your prize. = **SPAM**
  4. Thanks for registering. Text 4343 to receive free updates on medicare. = **SPAM**

## Conclusion and Results
It was surprising to see the only test text message that resulted in NOT SPAM was *#1. You are a lucky winner of $5000!* I would have thought that *#4. Thanks for registering. Text 4343 to receive free updates on medicare*, would be the most likely to be real and not spam. This is because the user is thanked for registering, which would immediately alert the user if they did not register, as well as seems to require an additional action on the receivers' end to further the communication.

## References Used
- Tiago, A., Hidalgo, J. 2012. SMS Spam Collection. UCI Machine Learning Repository. Available https://archive.ics.uci.edu/dataset/228/sms+spam+collectionLinks to an external site. [2023, October 25]. (CC-BY 4.0Links to an external site.).
- Class notes and activities from AI Bootcamp, Model 21. (2023). edX Boot Camps LLC
- This project utilizes Google Colaboratory for code execution and development.
- Libraries such as pandas, scikit-learn, and Gradio were instrumental in data manipulation, model building, and user interface development, respectively.
- Scikit-learn's LinearSVC and TF-IDF vectorization were used to build the spam classification model.