# StockPicking
# The stockpicking project is trying to get the stock information day by day and pick top stocks for investing. 
# Python and R would be used in the project.
## useful links: https://ntguardian.wordpress.com/2016/09/19/introduction-stock-market-data-python-1/


### install yahoo-finance (in command line)
cd C:\Python\Python36-32\Scripts\
python -m pip install yahoo-finance
pip install pandas-datareader

### in python:
from yahoo_finance import Share
yahoo.refresh()

### get the list of stocks in the US exchange market:
# NYSE
url_nyse = "http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=nyse&render=download"
# Nasdaq
url_nasdaq = "http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=nasdaq&render=download"
# AMEX
url_amex = "http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=amex&render=download"

import pandas as pd

df = pd.DataFrame.from_csv(url_nyse)
stocks = df.index.tolist()
