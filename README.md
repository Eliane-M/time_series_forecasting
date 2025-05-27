# Air Quality Forecasting with RNN/LSTM

## Project Overview
As PM2.5 concentrations increase in the atmosphere, they increase the chances of it entering people's lungs and potentially destroying their lives. The model below uses historical data from Beijing to forecast the concentration of PM2.5 and overall improve the air quality

## Dataset
The dataset used is from [kaggle]('https://www.kaggle.com/competitions/assignment-1-time-series-forecasting-may-2025/data'), and these were the rows in the train.csv used to train the model:
'No', 'DEWP', 'TEMP', 'PRES', 'Iws', 'Is', 'Ir', 'datetime', 'cbwd_NW','cbwd_SE', 'cbwd_cv', 'pm2.5'

## Project Structure
In this repository, the files are arranged like this:

```
Time series forecasting/
│
├── README.md
│
├── src/
│    └── air_quality_forecasting.ipynb
│
├── data/
│    ├── predictions/
│    ├── raw/
|        |__test.csv
|        |__train.csv
│
├── data/
│    ├── train/
│    └── test/
│
├── models/
│    ├── nn_model_5.h5
│    ├── static/
│    └── uploads/
│
├── requirements.txt

```

## Setup Instructions and Reproducing results
1. Clone the repository
2. Create your environment
```
python -m venv venv
```
and activate it  
```
source venv/Scripts/activate
```
3. Install dependencies: `pip install -r requirements.txt`
4. Download datasets from Kaggle and place in `data/raw/`
5. Use the notebook from the src directory and run the cells for results.

## Model Architecture and experiments
I trained a LSTM model and tuned hyperparameters during various experiments to find the best working model. The best Final Training Loss I got was 4608.207483328819. More information can be found in [this detailed report]('https://docs.google.com/document/d/1HcIfFqssuAx5ypMrYpTI_AAwH1K1FJelqovvVCTHOEU/edit?tab=t.0')

## Summary
This project successfully developed an LSTM-based air quality forecasting system, achieving MSE of 4608.207483328819 for PM2.5 prediction in Beijing. Through systematic experimentation with different architectures and hyperparameter combinations, we identified bidirectional LSTMs with 24-hour input sequences as the optimal configuration.
