# ATM-data-transactions---analysis
In this project I am focusing on analysis transactions coming from five different ATMs. I am checking relationship among variables and doing basic visualizations.

Description of the data set: 

Data comes from Kaggle website: https://www.kaggle.com/datasets/saadfareed/data-set-of-atm-transaction-of-xyz-bank It has 10 columns and 11589 rows.
It contains ATMs transactions of XYZ cards and no XYZ cards from 2011 till 2016, value of this trancations and information which day of the week the withdrawal has been done. Transactions cames from five ATMs. The location was not changed from 2011 till 2016.

Dataset has three categorical variables:atm_name,weekday,working_day and six numerical variables:  No_Of_Withdrawals which is the sum of two numerical variables no_of_XYZ_card_withdrawals and no_of_other_card_withdrawals. We have total_amount_withdrawn which is the sum of two numerical variables amount_withdrawn_XYZ_card and amount_withdrawn_other_card. There are also dates which we can work as date objects thanks to import a module named datetime.

Cleaning the data-checking if it is necessarly:
There is no missing values in the dataset and no duplicates.

TimeSeries analysis of transactions numbers and their amount:

From two TimeSeries charts we can see that the total number of withdrawals had increasing tendancy between 2012 and 2014.  What is more, transactions of not XYZ cards at this period are slightly higher however the increasing tendency we can observe in the number XYZ cards transactions. The question for buissnes units can be, what happened between 2012-2014 that more and more of XYZ withdrawals has been done? The location of this ATMs hasn't change. 
Was it for example some special promo for XYZ card to do cash withdrawal? We see also decrasing tendency in total starting from 2015. What happen the end of November 2016? Is it an effect of buissnes decision? We can see total decline in transactions. After this, increasing tendency of not XYZ withdrawals, which for the first time since 2011 almost covers the numbers of XYZ card withdrawals. About the amount of transactions: We can observe the same trend as in case of transactions numbers. Increasing tendancy between 2012-2014 after decresing trend till the end 2016. After total decline in November 2016 and can noticed immediately incerasing tendancy, particulary for not XYZ cards. The amount of XYZ cash withdrawal is above amount for XYZ card till the 2016 after tendancy has changed.  Obviously there is linear correlation between number of transaction and amount of cash withdrawal.

Checking categorical data:

We have got categocical data: atm_name (five diffrent ATMs), working_day(H,W), weekday(monday-sunday). All transactions are coming from five diffrent ATMs. We can noticed that almost half of the transactions is taking place on the weekend. Workdays ( Mon-Fri) consists of 57.13 % of all other days. Sunday is the best day of cash withdrawals for all five locations. This information might be useful in order to schedule service intervention for putting cash in the machine. It means also that in the weekend machines are working as hard as in the week. Having this in mind, we can check  the data about when this ATMs are out of order to prevent it to be unavaiable especially in the weekend.  What are the status of cash inside the machine before weekend? Having more data we can try to analysis if lack of cash during the weekend doesn't accure, if all these ATMs are usually on-service. 

Checking numerical variables:

From the regression plot, the transaction number seems to have direct relationship with the transaction amount. From a hexbin plot, I can see that many samples (the peaks) have a number of transactions about 90-150, and correspondingly, the total amount is in the range of around 500000-800000.
From KDE plot, I can see that the more transactions starting from around 100 level, the more diferences in the amounts.

I can say that, transactions number for XYZ card are slightly better related with XYZ cards amount than for no XYZ cards (more stick to the regression line).

We can see that ATM 'BIG Street' and Airport ATM has direct relationship and no so much outstanding values, hovever the situation is slightly diffrent for KK Nagar ATM. Bigger transaction numbers varies more for the transaction amount. The Mount Road ATM has more outstanding values in the weekends. KK Nagar and Christ College ATM both weekend and week.

Headmap shows strong linear relationship between number of trx and amount of transactions. Pearson correlation coefficient (=0.916) shows strong positive relationship.

Boxplot is showing presens of outliers both for numbers and amount of transactions. Total number of outliers are 3.67 % of all numeric values.
