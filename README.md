# Green Stocks Refactored

## Overview of Project

### This project has the intention to analyze 12 green stocks and identify those which had a better performance between 2017 and 2018. For this scope, the performance will be measured by a relative high trading volume during the year as well as high return during 1 year period. I developed 2 different VBA codes for the analysis and it is important to present the one that runs faster and more efficient. In the end, time is money.

---

## Results

2018 was a tough year for Green Stocks. From a basket of 12 green stocks, only 2 had a positive return (ENPH & RUN) In general the whole sector was heavily affected by low trading volume and a lost of confidence from investors due to regulatory risks.
![Captura de Pantalla 2022-10-03 a la(s) 20 54 07](https://user-images.githubusercontent.com/113866707/193721760-d6216db3-4d44-4078-b16c-559b5d4a98eb.png)

  
For this project, it all start from the user of this file perspective, this project is customized in order to provide returns and volume for 12 stocks during years 2017 & 2018. User can enter the year and the whole data will populate.
    
![Captura de Pantalla 2022-10-03 a la(s) 20 53 38](https://user-images.githubusercontent.com/113866707/193721815-05c52504-ac3f-4159-9ed9-0220f461ce95.png)

This analysis was performed with VBA code. To automatically loop through the data and calculate total volume and return (starting price / ending price - 1).
    
On my first attempt of code, I created an array for the 12 stocks, but only created one output variable "tickers". Then with nested loops, I was able to make the code to identify each separate ticker, read through the data raws and accumulate for each ticker the volume and capture the first trading price and ending price. With a little bit of magic, added some formatting to identify visually the best performing stocks.
    
This code was good until I ran a timer code to review how long does it take for my code to run. It turns out that after a few changes to the code (aka refactoring) I was able to save 0.27 seconds which in the end benefits the ending user of the file.
    
In order to refactor the original code, I had to rely on the array of tickers and create an Index to reference for each ticker that could interact with new variables for volume, starting price and ending price. This new code uses loops as well as conditionals in order to read through the data and compute the applicable operations.
    
---
### Comparison of my codes:

#### Original:

![Captura de Pantalla 2022-10-03 a la(s) 21 12 58](https://user-images.githubusercontent.com/113866707/193721985-38dce354-a928-4cb3-8602-7ee90830e330.png)

#### Refactored:
![Captura de Pantalla 2022-10-03 a la(s) 21 15 34](https://user-images.githubusercontent.com/113866707/193722001-3a5ecb99-bbed-4f86-9388-29ccabf65f4d.png)
![Captura de Pantalla 2022-10-03 a la(s) 21 16 11](https://user-images.githubusercontent.com/113866707/193722013-d634680b-e8c4-4275-b732-689714bbee8e.png)

---

## Summary

- By refactoring the original code, the performance increased as the code was able to be more effective at following the script and run the calculations. For this to happen I had to interiorize and understand my original code and identify possible new ways of being less redundant with my script and leverage on the VBA capabilities. Before refactoring, always save the original code, you don't want to end with a half-refactored code and no original.

- The original code allowed me to follow simple steps in the coding process, however, the refactored one allowed me to push my knowledge further and understand other methods that perform better for this macro. In the end there was a saving of 0.27 seconds between original and refactored code.
![VBA_Challenge_2018](https://user-images.githubusercontent.com/113866707/193722510-8b0bf10e-2cd7-464e-85e0-fec5a205df6f.png)
![VBA_Challenge_2018_Refactored](https://user-images.githubusercontent.com/113866707/193722522-320c022c-0571-44a2-8ea4-1180542e7638.png)

