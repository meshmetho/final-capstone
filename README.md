INTRODUCTION
Loan defaulting is a serious problem that affects both lenders and borrowers. Lenders lose money and trust when borrowers fail to repay their loans , while borrowers  suffer from damaged credit scores and legal consequences. Therefore, it is important to predict the likelihood of loan default  and take preventive measures to reduce the risk.
In this project we will use machine learning techniques to build a predictive model for loan default based on data from SuperLender, a local digital lending company. SuperLender uses a data-driven  approach to assess the credit risk of its customers and determine  the two fundamental drivers of repayment; `willingness` and `ability’. We will explore how SuperLender uses machine learning models to predict loan outcomes and evaluate their performance

BUSINESS UNDERSTANDING
Defaulting borrowers cause significant financial losses, impacting profit margins and liquidity ultimately affecting long-term business sustainability. Moreover, loan defaults can tarnish a company's reputation, erode investor confidence, and hinder future borrowing opportunities. 

Super Lender a local digital lending company seeks to provide effective credit risk model which determines borrower’s chances of repaying a loan. In this project we seek to develop a credit risk model employing machine learning techniques. The model assesses historical data to predict potential defaults, enabling proactive risk management. Also the model informs credit manager and the institution’s employees on borrower important details to enable data driven decisions not only to deny or advance a loan  but targeted strategies, including personalized loan terms.

PROBLEM STATEMENT
A defaulted loan is an expense to the business. There is a need for financial institutions to enhance their risk assessment strategies and only lend responsibly.  As such predicting customer loan defaults is central to minimizing financial risks and ensuring sustainable lending practices. Chances of customer paying their loan are influenced by demographics and past financial details. The challenge is for financial institutions to distinguish customers who can pay loans and only lend to them.

MAIN OBJECTIVE
To develop a model which predicts customer loan repayment chances

SPECIFIC OBJECTIVE
* Determine which demographic factors affects customer loan repayment chances
*	Determine which past financial details and behavior affects customer loan repayment chances
*	To develop a UI which informs credit manager on customer’s loan repayment details.

DATA UNDERSTANDING
We will make use of the datasets from Zindi, which is the largest professional network for data scientists in Africa. In particular we will be focusing on  3 different datasets for both train and test.

> a) Demographic data
* customerid(primary key) - It combines demographic information with loan history.
* birthdate (date of birth of the customer) - Provide insights into a customer's financial stability, earning potential, and financial maturity, which can affect loan default behavior.
* bank_account_type (type of primary bank account) - indicate a customer's financial engagement and stability, influencing their ability to repay loans.
* latitude_gps / longitude_gps - help identify regional economic disparities, urban vs. rural differences, and access to banking services, all of which can affect a customer's ability to repay loans.
* bank_name_clients (name of the bank) - Different banks may have varying lending policies and customer service quality, which can influence loan repayment behaviors.
* bank_branch_clients(location of the branch) - 
* employment_status_clients -  Employed customers are generally considered less risky than unemployed or irregularly employed individuals. It reflects the customer's income stability.
* level_of_education_clients (highest level of education) - Higher education may suggest better financial management skills and access to higher-paying jobs, lowering the likelihood of loan default.

> b) Perfomance data
* customerid(primary key) - links performance data with demographic and previous loan data to create a comprehensive customer profile.
* systemloanid(id associated with the particular loan) - Tracks individual loans for each customer, enabling the analysis of the performance of each loan separately.
* loannumber(number of loan we are predicting)
* approveddate(date loan was approved)
* creationdate - An indicator of loan processing efficiency or customer need for funds.
* loan amount - Larger loans might carry higher default risk compared to smaller ones.
* totaldue - Evaluates the customer's repayment capacity and risk exposure.
* termdays - Longer terms might have different default patterns compared to shorter terms.
* refferedby - Can be relevant in assessing the risk of referred vs. non-referred customers.
* good_bad_flag(good = settled loan on time; bad = did not settled loan on time) - Its the target variable we want to predict

> c) Previous loans data
* customerid - links previous loan data to other customer information.
* systemloanid - Track each previous loan taken by a customer and understand their historical borrowing behavior.
* loannumber(the number of the loan that we will predict) - Tracks the sequence of loans taken by a customer, which can reveal trends in their borrowing history and how it affects defaults.
* approveddate - 
* creationdate(date the loan was created)
* loanamount
* totaldue
* closeddate - Helps to understand the loan's performance and whether it was settled on time.
* refferedby
* firstduedate - Helps to understand the payment schedule
* firstpaiddate - Provides insights into the customer's initial repayment behavior.
