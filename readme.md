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

>Initially I focused on studying "Defaulted" loans, however in this dataset most of the loans are in status "Current". So sometimes it has been useful to drop those.
My hypothesis was that on the 2008 economic crisis there would be more loan defaults compared to the other years, that is simply not the case, the general path for listings was increasing until 2008, then it stopped due to the crysis and from 2019 gradually increased until 2014 (which is the last date we have data). It is not that counter-intuitive since the date we are looking at is the date the listing was created, so if a listing becomes Default during the economic crisis it will compute on the year the listing was created and not the year it defaulted. Sadly for the defaulted loans we lack historical infromation of when did the loan became daulted.

> Most of the listings in status "Completed" (and not defualted) are hold by borrowers in a salary range between 25k-50k, however most of the listings in "Current" are in slightly higher borrower salary range: 50k-75k.

>From the scatter plots we see a lot of noise, the strongest correlation that we see was expected between BorrwerAPR and LenderYield, it makes sense that the higher rate a borrower pays, a higher rate the lender recives indeed. 

>Another correlation far less strong is inversely proportional between borrower salary and LenderYield, in conclusion high salary borrowers tend to pay lower interest rates.

>The metrics of Occupation, Employment Stand Emplyment duration are very noisy and with too many non informative classes, further processing should be done in order to take a singificative conclusion.

> Most of the Defaulted loans had the lowest credit grade (HR), which makes sense, also the best credit grades (A, AA) had the lowest defaults, however there was not a significative difference on loan defaults in the mid-range credit rates (B,C,D,E), in fact there were more loan defaults rated in C than in E which is counter intuitive.

> Most of the loans have borrowers with a Debt to income ratio between 0.1 and 0.3. Most of the Completed loans were in the [0.1,0,2] range, most of the Current loans are in the [0.2,0.3] range.

>Low debt to income ratios tend to have better loans (with lower interest rates (borrwer and lender yields)), and lower the loan rating rates are the lower the credit grade is

>The lowest debt to income ratios have the best ratings (AA) as expected, and unexpectedly at the same time many of the lowest debt to income ratios borrowers recive loans with the worse ratings (HR)

## Key Insights for Presentation

> We strat recalling the importance of preventing crisis by seein the impact that the economic crisis had on 2018 (count of listings).
> Following we evaluate the health of our listings comparing our Current listings to the successfully completed listings, we count the number of listings on borrower salary and borrower debt to income ratio.

> The current listings, comparetd to the completed listings have a higher borrower salary and at the same time a higher debt to income ratio.
> FInally we conclude that the increase on borrower debt to income ratio does not compromise the health of the listing since it is a small increase enough not to affect the listing keeping it on the A-D Rating Range keeping reasonable interest rates without having the best or the worse interest reate.



## Implementation
- Entire code is in Python 3.
The main visualization libraries used have been:
- [Altair](https://altair-viz.github.io/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

>The data processing has been done in Pandas and Numpy.
