# Stock-prediction-based-on-sentimental-analysis
This project use Sentimental Analysis on $AAPL, $AMZN,$MSFT,$NFLX

# General Flowchart
![image](https://user-images.githubusercontent.com/100210059/163676388-bd4919e7-a5f2-4437-a145-a5d300646a74.png)

# VarS
VarS includes four stocks mentioned above in 2021 whole year, downloaded from Yahoo Finance

# VarT
All corresponding tweets data is harvested by using $ + stockname(e.g. $AAPL), the scraper is twint from https://github.com/twintproject/twint

Here to explore the relationship between different time divison and stock trend, we have 3 different time division here

Big Day: To make use of data of weekend tweets, Weekend / Festival Sentimental Score is assembled using fucntion:

Compound-Senti-Score(Day t) = 
[Compound-Senti-Score(Day t-1) * n1^2 + Compound-Senti-Score(Day t-2) * n2^2 + Compound-Senti-Score(Day t-3) * n3^2...] / (n1^2 + n2^2 + n3^2...)
(how many n depends on the number of non-transaction days, n1 = 1, n2 = 2, n3 = 3.......)

No Big Day: Just Compound-Senti-Score for each 

Senti: Apply Vader on each tweet

TEXT: Including original data

# VarT
Combined data used for final train and machine learning 

#
If you have any question, feel free to contact me.
