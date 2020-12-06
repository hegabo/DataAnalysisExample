# Loan Data Exploration
This is an example project done as part of a Nano Degree program at Udacity. 

## Dataset
The data used is prosper loand data from https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv. The data consists of information regarding 113937 loans in 81 columns, some of which contain null values. It was noted in the dictionary that there are certain fields that only have values for loans after July 2009, so only those loans were included n the study.


## Summary of Findings
For the purpose of the study, a copy of the dataset was made, including only the most interesting columns. Columns that are missing too many values were not included. Columns that are of interest but have smaller number of missing values were kept, and those records were dropped.
Histograms and scatterplot matrix were plotted for the numerical columns to have a look at the data and have a first look at the expected correlations. Research questions were then formed for those columns and also some Boolean columns. The questions were
* What's the mean loan amounts for each listing category? And what's the total?
* How does APR compare to rate (i.e. overhead on borrower)?
* How does yield compare to estimated return (i.e. deductions from lender)?
* How do rates compare to scores?
* How do the term, loan amount and rate relate?
* Does employment status affect the APR? How about occupation?

While calculating the average credit score, it was noted that that range width is always 19, but that's probably dependant on how the agency calculates it. It was also noted that some proper score records have values of 11, while the dictionary suggest that the values should be from 1 to 10.
While the individual loan amounts were found reasonably varying among the loan category, the total loans amount for each category were found hugely different. Debt Consolidation was found to make the most of the total amount of loans.
Next, I compare rates versus fees and deductions (for both borrowers and lenders). It appears that the difference between Borrower Rate and APR does not change much (with the exception of loans for lower rates, while we see steady increase in the difference between Lender Yield and Estimated Return as the yield increases.
Both plots have fluctuation in the differences, though it is more apparent for the investor.

## Key Insights for Presentation
Does the credit score of a borrower affect the APR rate they pay? Or does the proposer rate correlate with Estimated return for an investor? Scatter plots are plotted for each pair, and it appears there is negative correlation between the rate and the score, although it's less definite for the lender.
As for the loan amount versus the APR, it appears there is some correlation, albeit probably not the strongest. The term, however, does not seem to affect either variables, especially when we look at the 36 and 60-months term. The 12-months had a much smaller number of records, and therefore was not so conclusive.
Then comes the question of how employment status affect APR, and how does ownership of a flat factor in. The relationship between the employment status and the APR do not seem to perfectly correlate. There can be a room for further investigation there, as it is possible that other criteria factor in, causing what is known as Simpson's paradox. It could very well be that Occupation plays a role here. However, due to the big number of occupations, for the sake of this project we will just study occupation versus APR, regardless of the employment status.
It appears that flat ownership affects the APR positively except for those who are not employed. It is possible that banks offer lower rates for unemployed if they do not own a flat, or it could be support from the local authorities. That can be a point for further investigation. 
Even though it didn’t seem very feasible for the size of this project to compare APR to both occupation and employment status at the same time, I thought a starting point would be to see how APR average for occupation, to have some idea about how occupation plays a role and how could it have affected APR by employment status. From the bar plot, we do not expect drastic effect, although it's interesting that most students get the highest rate except College Sophomore gets the lowest rate of all occupations.



