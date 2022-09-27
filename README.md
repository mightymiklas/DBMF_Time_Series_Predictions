# DBMF_Time_Series_Predictions
A LSTM model for iMGP DBi Managed Futures Strategy ETF

## Data Source: 
[Yahoo](https://finance.yahoo.com/quote/DBMF/history?period1=1557273600&period2=1664150400&interval=1d&filter=history&frequency=1d&includeAdjustedClose=true)


## Technologies
--Requirements
python 3.7

- [plotly](https://pypi.org/project/plotly/) - for plotting data
- [pandas](https://pypi.org/project/pandas/) - for analyzing data 
- [numpy](https://pypi.org/project/numpy/) - for analyzing data 
- [sklearn](https://pypi.org/project/sklearn/) - for calculating Mean Squared Error
- [matplotlib](https://pypi.org/project/matplotlib/) - for visualizing data
- [jupyter](https://pypi.org/project/jupyterlab/) - an IDE
- [tensorflow](https://pypi.org/project/tensorflow/) - for calculating LSTM model, Dense, and Sequential Layers
  
---

## Preview
![Training Validation Loss](https://user-images.githubusercontent.com/94579605/192651730-7b8cc4b1-5598-4a1a-a9f0-0d783ef4edde.png)

As you can see, over 200 epochs, the model decreases its validation loss, which infers that the model is learning from the data and improving performance.

![Model predictions](https://user-images.githubusercontent.com/94579605/192651795-e112fc86-a36d-4718-bebb-70851a6ecbd4.png)

The model has near perfect prediction which implies a number of things that were done incorrectly. Using prices as inputs/targets does not provide reliable results in real world setting in beating the random walk hypotehesis which dictates that stock prices are unpredictable. LSTM models are meant for sequences, however stock prices are non-sequential. The use of min,max scaler on stock prices is not a reliable modal as stock prices have no fixed max range, but are infinite. Standardization is the preferred method for computing models, on daily % returns than stock prices. 

Next steps... 

				
## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pandas
  pip install plotly
  pip install numpy
  pip install sci-kit learn
  pip install matplotlib
  pip install jupyter

```
---
## Usage
To execute the application, first clone the repository using 'git clone' and then run 'BitcoinTradingStrategy.ipynb' from within your chosen jupyter environment that fulfills the application requirements, in order to run the program properly. 


## Contributors
