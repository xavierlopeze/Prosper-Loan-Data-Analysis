# Prosper Loan Data Exploration
## by Xavier López


## Dataset

[Prosper](https://www.prosper.com/) is a **peer-to-peer lending marketplace** in the United States. It has facilitated more than \$18 bilion loans in more than 1.060.000 people.

Through Prosper, people can invest in each other in a way that is financially and socially rewarding.  
Borrowers apply online for a fixed-rate, fixed-term loan between 2.000 and  40.000 USD dollars \$.  
Individuals and institutions can invest in the loans and earn attractive returns.  
Prosper handles all loan servicing on behalf of the matched borrowers and investors.

The dataset analyzed ([data/prosperLoanData.csv](https://github.com/xavierlopeze/Prosper-Loan-Data-Analysis/blob/master/data/prosperLoanData.csv)) contains data from Prosper's listings, the definition of the fields can be found at [data/prosperLoanData_variable_definition.csv](https://github.com/xavierlopeze/Prosper-Loan-Data-Analysis/blob/master/data/prosperLoanData_variable_definition.csv).

## Summary of Findings

Initially I focused on studying "Defaulted" loans, however in this dataset most of the loans are in status "Current". So sometimes it has been useful to drop those.
My hypothesis was that on the 2018 economic crysis there would be more loan defaults, that is simply not the case, the general path for listings was increasing until 2018, then it stopped due to the crysis and from 2019 gradually increased until 2014 (which is the last date we have data). It is not that counter-intuitive since the date we are looking at is the date the listing was created, so if a listing becomes Default during the economic crisis it will compute on the year the listing was created and not the year it defaulted. Sadly for the defaulted loans we lack historical infromation of when did the loan became daulted.

## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.


## Implementation
- Entire code is in Python 3.
The main visualization libraries used have been:
- [Altair](https://altair-viz.github.io/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

>The data processing has been done in Pandas and Numpy.
