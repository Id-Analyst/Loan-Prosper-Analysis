# Introduction

Exploratory and Explanatory Analysis of a Sample Dataset from **Loan Prosper** which was meant to potentially look at the impact of selected variables on Loan and the possibility of requestors getting loans or not.

## Dataset

The main data set contain 113937 row and 81 columns. All the columns ain't essential for this analysis, for that reason I worked with 113937 row and 15 column. The details of the columns are below:

* ListingNumber: The number that uniquely identifies the listing to the public as displayed on the website.
* Term: The length of the loan expressed in months.
* LoanStatus: The current status of the loan: <b> Cancelled, Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
* BorrowerAPR: The Borrower's Annual Percentage Rate (APR) for the loan.
* BorrowerRate: The Borrower's interest rate for this loan.
* ProsperRating: The Prosper Rating assigned at the time the listing was created between AA - HR. Applicable for loans originated after July 2009.
* ProsperScore: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score. Applicable for loans originated after July 2009.
* BorrowerState: The two letter abbreviation of the state of the address of the borrower at the time the Listing was created.
* Occupation: The Occupation selected by the Borrower at the time they created the listing.
* EmploymentStatus:The employment status of the borrower at the time they posted the listing.
* IsBorrowerHomeOwner: A Borrower will be classified as a home-owner if they have a mortgage on their credit profile or provide documentation confirming they are a home-owner.
* IncomeRange: The income range of the borrower at the time the listing was created.
* LoanOriginalAmount: The origination amount of the loan.
* LoanOriginationDate: The date the loan was originated.
* Listing_Category: The category of the listing that the borrower selected when posting their listing


## Summary of Findings

### **Univariate Analysis**

From my investigation, I discovered that there was a significant correlation between the borrower's APR and rate. They shared the same plot line. It is typical given that the borrower’s APR is calculated by adding the borrower rate to other fees. The loan amount was unevenly dispersed, ranging from $1,000 to well over $30,000. The prosper Score distribution revealed that it is multimodal, with the population being dominated by scores of 4, 6, and 8. The most prevalent rating among borrowers, according to the Prosper Rating distribution, was C, and the highest rating, AA, was held by the fewest number of borrowers. The majority of people who requested for loans were employed, with retirees making up the least number in the job status distribution. In the population, the distribution of homeowners was uniform. Many of the debtors fall into the high-income bracket. The highest borrowers on the log scale are those who are actively enrolled in the loan plan, followed by those who have paid off their loan. The majority of the loan was obtained for debt relief.

### **Bivariate Analysis**

The distribution of the average borrower APR by year, obtained using a bar plot, showed that 2011 had the highest APR.  The distribution of APR by month, however, revealed that more people took loans during the months with lower APRs.

Using a bar plot to show the relationship between the prosper rating and score, it can be seen that the ratings and scores are negatively correlated with borrower APR. 

A correlation heatmap that displays the relationship between borrower APR, loan amount, and Prosper Score confirms the box plot above by demonstrating a stronger correlation between borrower APR and rating and a weaker association between Prosper Score and APR.

When a heatmap was used to illustrate the relationship between income range and homeownership, the distribution reveals that the majority of borrowers are in the range of $10,000 and lower. Additionally, in the range of higher loans collected by borrowers with incomes of $15k and above, homeowners dominated the distribution.

Using a clustered bar chart to display how the loan amount has been distributed by term, the plot reveals that the 36 term, or 3 years, had the highest distribution of the total amount collected, with the exception of the amounts up to $30k, which had a slightly higher distribution than the 60 term, or 5 years. Only a few customers received loans for an entire year, and for the larger loans starting at $25,000, nobody received them for the entire year.

### **Multivariate Analysis**

With an additional look at the bivariate plot using a heatmap to highlight how the borrower APR affects the loan range and homeowner relationship, the distribution reveals that the borrower APR had no impact on the homeowner correlation. However, the relationship between the loan amount and the borrower APR was inverse.


The figure indicates that the longer term (5 years) had a higher borrower APR when looking deeper into the clustered bar chart in the bivariate while adding Term to the distribution. It implies that the longer the borrower repays the loan, the higher their APR becomes.


## Key Insights for Presentation

The first multivariate analysis revealed that owning a home had no impact on the range of loan amounts and that the higher the APR, the smaller the loan collected. However, utilizing the period demonstrates that the APR increases regardless of the loan's amount, the longer the duration over which it was paid off.
