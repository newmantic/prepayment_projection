# prepayment_projection

In fixed income, particularly for mortgage-backed securities (MBS) and asset-backed securities (ABS), prepayment models are essential for understanding the risk and return characteristics of these instruments. Prepayments refer to the early repayment of the principal on a loan or mortgage, which can significantly impact the cash flows and value of the security. Accurately modeling prepayments is crucial for pricing, managing, and hedging these securities.


Conditional Prepayment Rate (CPR):
The CPR is an annualized measure of the rate at which borrowers prepay their loans. It represents the percentage of the remaining principal that is expected to be prepaid over a year.

Single Monthly Mortality (SMM):
The SMM is the monthly equivalent of the CPR. It represents the fraction of the remaining principal that is expected to be prepaid in a given month.
The relationship between CPR and SMM is given by:
SMM = 1 - (1 - CPR)^(1/12)

Prepayment Projection:
The prepayment model projects the amount of principal that will be prepaid each period (typically monthly) over the life of the loan or security.



The basic formula for calculating the prepayment amount in a given month is:
Prepayment_t = SMM * Principal_(t-1)
Where:
Prepayment_t is the prepayment in month t.
SMM is the Single Monthly Mortality rate.
Principal_(t-1) is the outstanding principal at the end of the previous month.
Steps in Prepayment Modeling

Calculate the SMM from CPR:
Convert the annual CPR to the monthly SMM using the formula:
SMM = 1 - (1 - CPR)^(1/12)

Project Monthly Prepayments:
Use the SMM to project the prepayment amount each month over the life of the mortgage or loan. The prepayment for month t is:
Prepayment_t = SMM * Principal_(t-1)

Update Principal Balance:
After calculating the prepayment, update the principal balance for the next month:
Principal_t = Principal_(t-1) - Prepayment_t

Repeat for Each Month:
Repeat the process for each month until the loan is fully repaid or matures.

Prepayment Model is to estimate the amount and timing of principal prepayments in mortgage-backed securities and other fixed-income instruments with prepayment options. The Conditional Prepayment Rate (CPR) is the annualized prepayment rate, which is converted to the Single Monthly Mortality (SMM) rate for monthly projections. Prepayments affect the timing and amount of cash flows, making accurate modeling crucial for valuation and risk management.
