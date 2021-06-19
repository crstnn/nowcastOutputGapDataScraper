----------------------------------------------------------------TO RUN-------------------------------------------------------------
Simply, download and click on 'scraper.exe' for Windows 
(and for MAC OS, click scrape.app in MAC_OS folder - please download the whole folder in the root of this directory)
and wait until 3 csvs show up in the root directory 
(if any major errors occur all csvs will be populated with an error statement), 
this may take around 10 seconds. Close all related CSVs before running the program.

Please note that this program may alert your PC's virus software, this is because the executable hasn't been published with a developer certificate. If this occurs, you can "allow" the executable within the software.

All data is scraped from the FRED API unless otherwised specified below.

All daily data uses average aggregation, except from SP500 which is 'end of period'.

Structure follows similarly the previous version bar a few minor changes.

////////////////////////////////////////////////////Contents of monthly_data.csv/////////////////////////////////////////////
Column order structure: FEDFUNDS, UMCSENT, UNRATE, CPIAUCSL, INDPRO, HOUST, SP500

Each row represents the month end value

first row STARTS with date: 1967-01-xx

SP500 data is purely from Yahoo Finance (using the yfinance package), each observation is of the month's end not the month's average.


UMCSENT uses QUANDL's API (https://www.quandl.com/data/UMICH/SOC1-University-of-Michigan-Consumer-Survey-Index-of-Consumer-Sentiment) 
except for the most recent two months which are scraped off the Y Charts website (as QUANDL does not have the latest values). 

////////////////////////////////////////////////////Contents of monthly_spread_data.csv/////////////////////////////////////
Column order structure: BAA, AAA, DGS10, DGS1

Each row represents the month end value

first row STARTS with date: 1967-01-xx

//////////////////////////////////////////////////////Contents of quarterly_data.csv//////////////////////////////////////////
Column order structure: GDPC1

Each row represents the quarter end value

first row STARTS with date: 1967-01-xx

--------------------------------------------------------------LEGEND-----------------------------------------------------------
FEDFUNDS: Effective Federal Funds Rate
UMCSENT: University of Michigan: Consumer Sentiment
UNRATE: Unemployment Rate
CPIAUCSL: Consumer Price Index for All Urban Consumers: All Items in U.S. City Average
INDPRO: Industrial Production Index
HOUST: Housing Starts: Total: New Privately Owned Housing Units Started
SP500: S&P 500 Real Index Value

BAA: Moody's Seasoned Baa Corporate Bond Rate
AAA: Moody's Seasoned Aaa Corporate Bond Rate
DGS10: 10-Year Treasury Constant Maturity Rate
DGS1: 1-Year Treasury Constant Maturity Rate

GDPC1: Real Gross Domestic Product