# An Analysis of Green Stocks

## Overview of Project

### Purpose

The purpose of this project is to provide Steve with an effective and efficient tool for the analysis of stocks. The results of two years of green stock performance will be analized to determine a recommendation for investment. Furthermore, refactored code will be compared to the orignally developed code to determine the best method for conducting the analysis Steve requires going forward.

## Results

### Stock performance

Comparing the results of the stock performance analysis shown below, it is recommended that Steve invest in the stock with ticker ENPH as this stock had strong performance in both years with an overall average return of 105.72%. If diversification is needed then the only other stock that demonstrated positive returns in both years is the one with the ticker RUN which had an overall average return of 44.75%.

![Original script 2017 analysis](./Original_script_2017_analysis.PNG)

![Original script 2018 analysis](./Original_script_2018_analysis.PNG)

### Code performance

The performance of the refactored code is clearly more efficent then the original script. This can be seen by comparing the run times of the respective analyses. The screenshots provided in the prior section on stock performance also display the runtime using the original script. The screenshots below provide the runtime for the same analysis performed with the refactored code. 

![Refactored 2017 analysis](./VBA_Challenge_2017.PNG)
![Refactored 2018 analysis](./VBA_Challenge_2018.PNG)

A comparison of the runtime results for both blocks of code is summarized in the chart below.

|Code| 2017 | 2018 |
|---|---|---|
|Original|1.015625 seconds|0.9960938 seconds|
|Refactored|0.1054688 seconds|0.1054688 seconds|

As can be seen the refactored code runs nearly 10 times faster then the original script and so is clearly the most efficent for Steve to use going forward. This efficency comes from the fact that the refactored code does away with nested loops. In the original script the code used nested loops to run through the full rowCount (j) while calculating the values for each ticker (i) and then writing that ticker's results in the output cells before restarting the loop again for the next ticker.

![Original script code snip](./Original_script_code_snip.png)

The refactored code does away with the nested loop by making use of an tickerIndex variable so that a single loop is used to determine the outputs for all the tickers before  a separate loop is then used to write all ticker results to the output cells. This significantly speeds up the code runtime.

![Refactored_code_snip](./Refactored_code_snip.png)


## Summary

The practice of refactoring code has both positives and negatives. The postives are that the refactored code is often cleaner, easier to understand, and simplier to maintain. The negatives are that refactoring takes time, both in the intial rewriting of the code, and in the subsequent retesting to ensure the refactored code is functioning in the same was as the original was. For programmers time is money so there is a very real cost to refactoring. 

In the specific case of this VBA Challenge analysis the pros of faster run time out weigh the cons of time spent doing the refactoring. This is because this tool has the flexibility and power to be used for multiple analyses over many years. Over a long time the effort it took to refactor the code will be dwarfed by the time saved by the faster runtimes and easier maintenance of the code. 
