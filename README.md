# Disaster Response Pipeline Project


### Project Motivation:
In this project data engineering concepts are mainly used to analyze disaster data from [Figure Eight](https://appen.com/ "Figure Eight") to build a model for an API that classifies disaster messages.

The datasets used contain real messages that were sent during disaster events.Machine learning pipline is build to categorize these event to reach out for a relevant relief agency.

### File Structure:


    - app
    | - template
    |  |- master.html  # main page of web app
    |  |- go.html  # classification result page of web app
    |- run.py  # Flask file that runs app
    
    - data
    |- disaster_categories.csv  # data to process 
    |- disaster_messages.csv  # data to process
    |- process_data.py
    |- InsertDatabaseName.db   # database to save clean data to
    
    - models
    |- train_classifier.py
    |- classifier.pkl  # saved model 
    
    - README.md

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

### Sample Image

![](https://video.udacity-data.com/topher/2018/September/5b967bef_disaster-response-project1/disaster-response-project1.png)
![](https://video.udacity-data.com/topher/2018/September/5b967cda_disaster-response-project2/disaster-response-project2.png)

### Acknowledgements

Many thanks to Figure-8 for making this available to Udacity for training purposes. Special thanks to udacity for the training. Feel free to utilize this repo.