# Streamflow Prediction
### This project is hosted by NRCan and Aggregate Intellect aimed at predicting streamflow across Canada's watersheds. 

#### Why It Exists 
##### This repository houses the winning submission from the 2022 NRCan-sponsored co-opatition (a collaborative competition) hosted by Aggregate Intellect, focused on flood prediction using the HYSETS dataset. The winning model, a highly specialized LSTM-GRU ensemble, achieved remarkable accuracy for 24-hour flood predictions by leveraging overfitting, tailored to the competition's constraints. Additionally, the repository includes a more conventional machine learning example: a deep learning-based flood prediction model trained on the “65 Years of Weather Data Bangladesh (1948–2013)” Kaggle dataset. This model serves as an educational demonstration of applying standard deep learning techniques to flood prediction, offering a contrast to the NRCan model's unconventional approach.

     
#### What's in It     
   
            
##### Files           
         
  
##### streamflow_final_lstm_gru.ipynb: The Jupyter notebook containing the winning co-opatition model, an LSTM-GRU ensemble for 24-hour flood prediction on Watershed 205 from the HYSETS dataset. It achieves sMAPE scores of 6.26% (LSTM), 5.65% (GRU), and 4.97% (combined), optimized for Google Colab.
   
##### NRCan_flood_prediction_hackathon.txt: A detailed explanation of the NRCan co-opatition, outlining the challenges faced (e.g., sparse data, hardware limitations, regional variability), why the winning model embraced overfitting, and its strengths and limitations.

##### streamflow_prediction Folder  


##### 65 Years of Weather Data Bangladesh (1948 - 2013).csv: The Kaggle dataset used for the Bangladesh flood prediction model, containing monthly weather data (e.g., rainfall, temperature, humidity) from 1948 to 2013.

##### bangladesh_dataset_analysis.txt: An analysis of the Kaggle dataset, detailing its structure, feature distributions, and suitability for flood prediction.

##### bangladesh_streamflow.ipynb: A Jupyter notebook implementing a deep learning-based binary classification model for flood prediction in Bangladesh. The model uses a feedforward neural network built with TensorFlow and Keras, processing features like rainfall, temperature, humidity, wind speed, cloud coverage, sunshine, month, and a regional indicator (coastal vs. deltaic). It classifies months as flood (1) or non-flood (0) based on rainfall thresholds (550 mm/month for deltaic, 1100 mm/month for coastal during June–October). The architecture includes an input layer (64 neurons, ReLU), two hidden layers (32 and 16 neurons, ReLU, 20% dropout), and a sigmoid output layer, trained with Adam optimizer, binary cross-entropy loss, and class weights to handle a 9:1 class imbalance. It achieves 99% accuracy, 100% flood recall, and 91% flood precision at a 0.7 threshold, with diagnostics via RandomForest feature importance (66% rainfall dominance), cross-validation (F1-score 0.977 ± 0.01), and visualizations (e.g., confusion matrix). The model is designed for educational clarity, running efficiently in Google Colab.

##### walkthrough.txt: A comprehensive description of the Bangladesh model, explaining its architecture, preprocessing, tools (e.g., Pandas, sklearn, seaborn), and design choices, emphasizing its balance of simplicity and performance, and limitations (e.g., reliance on rainfall).

### License


##### This project is licensed under the MIT License - see below for details.
##### MIT License

Copyright (c) 2025 Rhapsodic Legacy 

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

