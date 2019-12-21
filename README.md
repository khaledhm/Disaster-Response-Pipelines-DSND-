# Disaster-Response-Pipelines-DSND-

## Installation
Beyond the Anaconda distribution of Python, the following packages need to be installed for nltk:
- punkt
- wordnet
- stopwords

## Project Motivation
This project is part of my Data Science Nanodegree program.
I appled data engineering, natural language processing, and machine learning skills to analyze message data that people sent during disasters to build a model for an API that classifies disaster messages.
These messages could potentially be sent to appropriate disaster relief agencies. 

## File Descriptions

* app:
    * run.py: Flask file to run the web application.
    * templates contains html file for the web applicatin.
* data:
    - disaster_categories.csv: dataset including all the categories.
    - disaster_messages.csv: dataset including all the messages.
    - ETL_Pipeline_Preparation.ipynb: Jupyter Notebook containing ETL pipeline scripts to read, clean, and save data into a database.
    - process_data.py: ETL pipeline scripts to read, clean, and save data into a database.
* images: 
    - header.png: screenshot of the web page
    - plots.png: screenshots of the plots
* models:
    - ML_Pipeline_Preparation.ipynb: Jupyter Notebook, tokenize messages from clean data and create new columns through feature engineering. 
        The data with new features are trained with a ML pipeline and pickled.
    - train_classifier.py: Script to tokenize messages from clean data and create new columns through feature engineering. 
        The data with new features are trained with a ML pipeline and pickled.    
        
## Results
1. An ETL pipleline was built to read data from two csv files, clean data, and save data into a SQLite database.
2. A machine learning pipepline was developed to train a classifier to performs multi-output classification on the 36 categories in the dataset.
3. A Flask app was created to show data visualization and classify the message that user enters on the web page.

## Instructions
1.Run the following commands in the project's root directory to set up your database and model.

   - To run ETL pipeline that cleans data and stores in database ` python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/disaster_message_categories.db `
   - To run ML pipeline that trains classifier and saves ` python models/train_classifier.py data/disaster_message_categories.db models/model.p `
2. Run the following command in the app's directory to run your web app. `python run.py`

3. Go to http://0.0.0.0:3001/


## Licensing, Author, Acknowledgements
Credits must be given to Udacity for the starter codes and FigureEight for provding the data used by this project.


