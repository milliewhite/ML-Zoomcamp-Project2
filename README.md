# ML-Zoomcamp-Project2
# The project
Predicting the development of diabetes in a patient given certain features using random forest classification.

# The Files Explained

*Notebook (suggested name - notebook.ipynb) with
Data preparation and data clearning
EDA, feature importance analysis

* Model selection process and parameter tuning
Script train.py
-Training the final model
-Saving it to a file (e.g. pickle called model.bin)

*Script predict.py 
-Loading the model
-Serving it via a web serice (e.g. with Flask)

*Pipenv and Pipenv.lock

*Dockerfile for running the service

#Model deployment as a web service on local machine

Open 2 command terminals and navigate to the folder with the files
From one terminal session run the following command to host the prediction model as a web service.
```pipenv run gunicorn --bind 0.0.0.0:9696 predict:app```

From other terminal session from the cloned project directory, execute the following command to make a request to this web service
```python request.py```

#Deploy model as a web service to Docker container
Navigate to the folder with the files
docker build -t project2 .
docker run -it --rm project2
