Dataset Chosen Prosper Loan Dataset
## by Prachi Pant


## Dataset

Following study explores a dataset containing Loan Data with many attributes like Borrower Rate , Estimated Effective Yield, LenderYield etc 
with over 100000 entries. This document explores this huge dataset and try to analyze its attrbutes and the correlation between them to
find some conclusions.

In this case study, we will analyze Prosper Loan Dataset where we look into various parameters which affect Loan effectiveness,Loan Risk,
Borrower Rate, Lender's yield, profit/Loss and details about people who avail loan like their credit grades, Employment details etc. 

### Main feature(s) of interest in this dataset : 
>1. What is the Maximum Borrower Rate and how is its distribution ?
>2. What is the Maximum Estimated Effective Yield and how is its distribution across ?
>3. How much is the Maximum Estimated loss and Maximum Estimated Returns 
>4. What are the various Loan Status and which kind of Loans are in Highest/Lowest number ?
>5. What is the employment status of Loan Borrowers and how many of the loan borrowers own home ?
>6. Does people with lower Salary or with higher salary tend to avail more loans what is the average monthly loan payment for each of them ?
>7. What is the Correlation between Lender Yield and Borrower Rate ?
>8. Does Borrower Rate , Lenders Yield , Estimated Returns depends on the income range of the people availing Loan?
>9. Who are the people with Higher Credit Grade and Lower Dept to Income Ratio ?
>10. Does Borrower rate influences Estimated Returns and Prosper Score ?
>11. Does Monthly salary of a person determines if its Risky Loan ? 




## Summary of Findings

### Quick Observation while just skimmimg through the Data : 
> 1. Its a Huge Data set with 113937 entries 81 Columns
> 2. avg prosper rating is around 4. 
> 3. Avg Estimated return (0.096068) is higher than avg EstimatedLoss (0.080306)
> 4. Avg Term is around 40 months
> 5. Mean time to close the Loan is 601 Days 


Univariate Exploration Observations :

##### What are the terms available while taking Loan and which one is more popular
there are three terms options available i.e 36, 60, 12 Months but most commonly the Loan is availed for 36 Months Period after that people tend to avail loan for 60 Months Period which seems to be large duration and the least popular term is 12 months very rarely people choose for this option.¶

#####  What are most common ratings given 
most popular rating is 4 while 2 is the least common rating

#####  What are the Top 5 Quaters over the Years where the Loans was availed to the Max
Maximum Loans were from 2012 Q3 to 2014 Q1 
Maximum Loan availed in 2013 Q4 
On a Closer Look following two things were found
Trend of availing the loan in these years (2012,2013, 2014 ) with quater is on consistent increase. 
Surprisingly the Loan data for FY 2014 is showing just for Q1 so either the data is missing or most of the laons are availaed in Q1

##### Which state has higest loan lending data and what are the top 5 states with highest lending records
CA has max loans lending data rest other states are almost equally distributed
Top 5 states with Highest lending records are : CA(Highest), TX, NY, FL, IL

#####  Explore the distribution of Borrower Rate
Thus Maximum Borrower Rate is between 0.1 to 0.2
As the Borrower rate increases from 0.2 we can see a consistent fall on the graph

#####  Distribution of Estimated Effective yield
Estimated Yield is Max from  0.12 - 0.17
Estimated Yield tends to drop ~1.18 onwards  which means that there are much lesser chances to get Estimated Yield of 0.2 to 0.3

##### Distribution of Estimated Loss 
Maximum estimated loss is ~0.03 to 0.08 however after ~0.08 the estimated Loss tends to fall drastically
Its very unlikely to get the Estimated Loss beyond ~0.18

##### Estimated Yield is Max at (0.12 - 0.17) and Maximum estimated loss is ~(0.03 to 0.08) This very clearly states that in Loan business Estimated Yield tends to be much higher than the estimated Loss 

#### Distribution of Estimated Returns
Estimated returns is max at ~(0.05 - 0.1 ) 
There is a steep decline of Estimated Return from 0.14 - 0.15

#####  What are various Loan Status their numbers
The maximum loans are in Current state (56576) followed by Completed Loans (38074) and almost negligible Loans are in Cancelled State (5)
There are 5018 Defaulted Loans and 2067 Past Dues Loans

Appx 50% Loans are in Current state, 
Appx 33 % Loans are completed
Appx 10% Loans are charged off
Appx 4% are Defaulted
Appx 2% are Past Due
Almost negligible loans are cancelled


#####  What is the employment status of Loan Borrowers and how many of the loan borrowers have home
Thus it looks like almost 50% of of people who avail loan already are home owners
Employee status is mostly employed where maximum people are full time employee and retired and not employed usually do not prefer to take loan which is kind of understandable

###############################
Bivariate Exploration Key Points
###############################

### How is the Spread across for Estimated Loss and Estimated Return
#### Estimated Return is usually higher than the Estimated Loss 
#### Peak of Estimated Return is much higher than the peak of Estimated Loss

### How is the spread across for TotalProsperPaymentsBilled and OnTimeProsperPayments
#### Total Prosper Payment Billed and On Time Prosper Payment graph tends to overlap which is kind of expected thats why these loans are called prosper loans as the timely payment is done for almost all of them

### What is the Distribution for the various Financial Category
#### People (Poor Category) with Salary (0-5000)are exponentially higher in no. for availing the loan than the Rich Category with Salary over 25k

### What is the Monthly Loan Payment by various Financial Category
#### Avg. Monthly Loan payment by the Poor category is much lower even when the no. of people availing Loan in this category is much higher

### How is the Monthly Stated Income of these Financial Category
#### Poor Category people availing Loan is much higher than the Rich Category still the avg stated Monthly Income for the Rich category is much higher. This shows a tremendous gap between the Rich and Poor Monthly income.


### What is the Prosper Score for each category in Loan Status
#### Loan Status	Avg Prosper Score
#### Thus the avg Prosper Score for Completed	Loan is   > ~7
####  The avg Prosper Score for Current Loan is  ~6
####  The avg Prosper Score for Past DueLoan is  ~5
#### The avg Prosper Score for Defaulted Loan is  ~6
#### The avg Prosper Score for Charged Off Loan is  ~5
#### The avg Prosper Score for  Final Payment Progress 	Loan is  ~6
#### Thus for obvious reason the Prosper Score for people who have completed the Loan is Higher 

### Whats is the Correlation between Open Revolving Accounts and Open Revolving Monthly Payment
#### As Expected there is a strong positive correlation between Open Revolving Accounts and Open Revolving Monthly Payment which means if the Open Revolving Accounts are more the Open Revolving Monthly Payments will also be higher

### What is the Correlation between Lender Yield and Borrower Rate 
#### Thus there is strong positive relation between the LenderYield and the Borrower rate i.e if the Borrower rate is high Lender's Yield is expected to be High which also makes sense
#### Borrower Rate is mostly lower than 0.35 it becomes rarer after it i.e having much higher Borrower rate is also not so common and mostly it stays between 0.1 to 0.3

### To check the correlation between various parameters : TimeToClose', 'CreditGrade', 'Term' , 'BorrowerRate',  'ProsperScore', 'BorrowerState', 'Occupation', 'EmploymentStatus' etc
#### ProsperScore and BorrowerRate have negative relation which implies people with with Good Prosper Score tend to get lower Borrower Rate
#### Current credit lines and Open credit lines have positive relationship
#### Current credit lines and Total Credit lines past 7 years have positive relationship


### What is the Lender's Yield from Different Income Range People 
#### Analysis shows that as the Salary Range Increases the Lender's Yield decreases may be because the interest rates are higher for people with lower income range as its more risky to lend loan to such people. More interestingly the Lender's Yield is maximum for the unemployed people as for the same reason the risk of lending loan would be higher for unemployed and hence the interest rate would be higher increasing the Lender's Yield

### How is the Lender's Yield from each Finacial Category
#### Analysis shows that the Lender's Yield from the Poor Category is Maximum and that from the Rich Category is Minimum this may be due to two reasons no. of people who availed loan from the poor category is exponentially higher and also the interest rate for people earning less will be higher as the risk to lend money is higher

###################################
## Multivariate Exploration Analysis
###################################

### To check if there is any correlation between Borrower Rate , Estimated Return and Financial Category
#### As the Financial Category improves from poor to Upper Middle the borrower rate reduces i.e for Poor category the Borrower rate is higher than Upper Middle Class
#### Estimated Returns from the Poor Category is High as the Borrower Rate is high for them

### To check if there is any correlation between Borrower Rate , Dept To Income Ratio and Financial Category
#### Dept to Income Ratio is quite high for the Poor class as compared to the Upper Middle Class people as expected and as the Borrower Rate increases this ratio increases exponentially

### To check if there is any correlation between Stated Monthly Salary, Dept To Income Ratio, Credit Grade
#### High Credit Grade People are usually with Higher salary range and with less DeptToIncomeRatio while the lower credit grade people have usually less income and hugher DeptToIncomeRatio This looks relatable

#### To check if there is any correlation between Borrower Rate , Estimated Return and Prosper Score
#### Borrower rate influences Estimated Returns for sure but the Prosper Score demarcation is very significantly represented in this graph which shows that it also has a correlation with other two parameters
#### The lowest Borrower Rate(0.05-0.12) are with lowest risk score (Best Risk Score 10) and also the estimated Returns are reasonably good (upto 0.1)
#### For medium Risk Score (Prosper Score between 4-6) the Estimated Returns is Maximum (upto 0.2) and the Borrower rate is little higher (0.12 - 0.25)
#### For High Risk Score (Prosper Score 2) the Estimated Returns is very low and the Borrower rate is on higher range (0.2 - 0.35)

### To check if there is any correlation between Income Range, Loan Status with Prosper Score
#### Prosper Score is best for the loans where the status is Completed and it actually the prosper score does not depend on the Income Range even the higher income range people will have lower prosper score and ViceVersa


### To check if there is any correlation between Prosper Score, Dept To Income Ratio with Financial Category
#### Dept to Income Ratio keeps getting better (lower) as we move from Poor to Rich Category
#### Finacial Category does not actually define the prosper score so may be Income range is not a key factor to identify risky/non risky Loans 


Sources referred
https://stackoverflow.com/
https://knowledge.udacity.com/
https://matplotlib.org/
https://seaborn.pydata.org/
