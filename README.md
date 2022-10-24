## Project Title - Crypto Arbitrage
The primary objective of this project is to perform research on arbitrage opportunities with Bitcoin prices between different crytpo exchanges.  


## Project Description
In the search for arbitrage opportunites, we'll be sorting through historical trade data for Bitcoin price dislocations on two exchanges: Bitstamp and Coinbase.  Our task is to apply the three phases of financial analysis to determine if any arbitrage opportunities exist for Bitcoin.  To accomplish these tasks, we'll perform the following phases of financial analysis:
<ol>
<li>Collect CSV data in a Jupyter notebook file.</li>
<li>Prepare the datasets for analysis by cleaning missing and erroneous data.</li>
<li>Analyze the data at a high level through summary statistics and visualizations, and use this information to select areas for deeper analysis. Specifically, we'll select time periods in which to identify arbitrage opportunities.</li>  
</ol>  


## How to Install and Run the Project
Install JupyterLab or Jupyter Notebook using PIP from the Python Package Index and run from the command console: https://jupyter.org/install.


## How to Use the Project

#### 1.) Launch the file, risk_return_analysis.ipynb 

#### 2.) Import the required libraries and dependencies 
<ul>   
           <li>import pandas as pd</li>
           <li>from pathlib import Path</li>
           <li>%matplotlib inline</li>
</ul> 

#### 3.) Use the read_csv function and the Path module to read the files, import the data from bitstamp.csv and coinbase.csv, and create Pandas DataFrames called bitstamp and coinbase. Set the DatetimeIndex as the Timestamp column, and be sure to parse and format the dates.

#### 4.) Prepare and clean the data for analysis, complete the following steps:
<ol>
<li>For the bitstamp DataFrame, replace or drop all NaN, or missing, values in the DataFrame.</li>

<li>Use the str.replace function to remove the dollar signs ($) from the values in the Close column.</li>

<li>Convert the data type of the Close column to a float.</li>

<li>Review the data for duplicated values, and drop them if necessary.</li>

<li>Repeat Steps 1–4 for the coinbase DataFrame.</li>
</ol>

#### 5.) Analyze the Data. Your analysis consists of the following tasks:

<b>a.) Choose the columns of data on which to focus your analysis.</b>  Select the data you want to analyze. Use loc or iloc to select the following columns of data for both the bitstamp and coinbase DataFrames: Timestamp (index) and Close.

<b>b.) Get the summary statistics and plot the data.</b>  Sort through the time series data associated with the bitstamp and coinbase DataFrames to identify potential arbitrage opportunities. To do so, complete the following steps:
<ol>
<li>Generate the summary statistics for each DataFrame by using the describe function.</li>
<li>For each DataFrame, create a line plot for the full period of time in the dataset. Be sure to tailor the figure size, title, and color to each visualization.</li>
<li>In one plot, overlay the visualizations that you created in Step 2 for bitstamp and coinbase. Be sure to adjust the legend and title for this new visualization.</li>
<li>Using the loc and plot functions, plot the price action of the assets on each exchange for different dates and times. Your goal is to evaluate how the spread between the two exchanges changed across the time period that the datasets define. </li>
</ol>

<b>c.) Focus your analysis on specific dates.</b>Focus your analysis on specific dates by completing the following steps:
<ol>
<li>Select three dates to evaluate for arbitrage profitability. Choose one date that’s early in the dataset, one from the middle of the dataset, and one from the last year of the time period.</li>
<li>For each of the three dates, generate the summary statistics and then create a box plot. This big-picture view is meant to help you gain a better understanding of the data before you perform your arbitrage calculations. As you compare the data, what conclusions can you draw?</li>
</ol>

<b>d.) Calculate the arbitrage profits.</b>Calculate the potential profits for each date that you selected in the previous section. Your goal is to determine whether arbitrage opportunities still exist in the Bitcoin market. Complete the following steps:
<ol>
<li>For each of the three dates, measure the arbitrage spread between the two exchanges by subtracting the lower-priced exchange from the higher-priced one. Then use a conditional statement to generate the summary statistics for each arbitrage_spread DataFrame, where the spread is greater than zero.</li>
<li>For each of the three dates, calculate the spread returns. To do so, divide the instances that have a positive arbitrage spread (that is, a spread greater than zero) by the price of Bitcoin from the exchange you’re buying on (that is, the lower-priced exchange). Review the resulting DataFrame.</li>
<li>For each of the three dates, narrow down your trading opportunities even further. To do so, determine the number of times your trades with positive returns exceed the 1% minimum threshold that you need to cover your costs.</li>
<li>Generate the summary statistics of your spread returns that are greater than 1%. How do the average returns compare among the three dates?</li>
<li>For each of the three dates, calculate the potential profit, in dollars, per trade. To do so, multiply the spread returns that were greater than 1% by the cost of what was purchased. Make sure to drop any missing values from the resulting DataFrame.</li>
<li>Generate the summary statistics, and plot the results for each of the three DataFrames.</li>
<li>Calculate the potential arbitrage profits that you can make on each day. To do so, sum the elements in the profit_per_trade DataFrame.</li>
<li>Using the cumsum function, plot the cumulative sum of each of the three DataFrames. </li>


#### 6.) Create Your Analysis Report. This report should summarize your analysis and include the following:

<ol>
  <li>Assumptions or discoveries that you made during the analysis</li>
  <li>Summary tables and calculations</li>
  <li>Visualizations</li>
</ol>

    
# Credits
I would like to give full credit to the products, software and web development teams for their contribution.

# License
No License
        
      
