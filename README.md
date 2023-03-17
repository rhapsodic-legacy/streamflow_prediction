# streamflow_prediction
#### This project is hosted by NRCan and Aggregate Intellect aimed at predicting streamflow across Canada's watersheds. (https://community.ai.science/streamflow-prediction-in-the-canadian-prairies)

This project was the winner of the compatition to make the most accurate 24 hour flood prediction model. 

+ The 'watershed isolate' Jupyter Notebook file includes how to isolate the relevant columns in the dataset, as well as a given watershed (in this case, watershed 205). 
  + Note: Null value imputation necessary for all watersheds. The interpolate method done herein will not be effective on many other watersheds, due to the enormity of missing target (discharge) values. 
