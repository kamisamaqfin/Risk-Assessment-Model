# Risk-Assessment-Model

This is an example of a Risk Assessment Data Analysis work that I had to do for FINRA. 

--Dataset: 200 rows of institutional/retail brokers with their characteristics, the exam scores of their representatives, districts they belong to and their violations and risk scores ( a simpler version of proprietary FINRA data )

--Objective: Assess which characteristics can help determine which firms are going to violate or not

--Implementation: Tried a thorough analysis of the brokers to glean insights into how many fall in which risk groups, test score distribution statistics ( these are FINRA Exam scores that reps must have to obtain broker licenses) and any other pertinent trends and statistics. Exam scores more positively correlated with industry awards, districts and violations other than being highly correlated with each other. Risk Group negatively correlated with all other variables other than client base. 

--Model: Logistic Regression used to model the characteristics against whether a firm violates or not (binary dependent variable). Created dummy variables for appropriate independent variables which were not numerical in nature. Also, the test scores were continuous variables so decided to try quantile cuts of them (binning their ranges) and making them into categorical variables with weighted order and run Logit again. 

--Result: Risk Group, Client Base and Industry Awards turned out to be significant at 5% confidence interval with odd ratios of small broker type, T3 categ test score and industry awards being higher than other endogenous variables. 88.75% accuracy achieved on test dataset with ROC-AUC score being 89%. 
