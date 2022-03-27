# Credit-Risk-Analysis
Designed Logistic Regression model for computing Probability of Default and calculated Credit Scores for borrowers. Also designed Linear and Logistic Regression Models for computing for computing Loss at Default and Expected Loss at exposure.

A bank needs to keep sufficient amount of capital in its treasury to recover from losses that it encounters from non repayment/delayed payment  of loans by borrowers.
In order to accomodate this the banks perform credit score analysis based on which it is going to determine whether its going to offer a loan to a particular customer.
These credit scores are calculated on the basis of some established well known statistical methodologies -Probability of Default.The customers are put into default if the customer is not able to repay/or the payment is delayed due to some unforeseen circumstances.We use Machine Learning Algorithms to desin the Probabilty at default and set a threshold which helps the algorithm to decide whether the customer should be put into default or not.However while designing this ML algorithms we should keep in mind the main purpose of Bank is business, it should be able to offer loans to its customers when desired.So this threshold set for ML models calculate Probabilty at default comes with a tradeoff between quality customers and the business that banks want to do.If this threhold is too high then the losses would very low however at the same time the banks won't be able to much loans and hence its buisness would fall.So the machine learning models should be designed in such a way so that they balance this tradeoff.


So below are the steps that I followed to create Credit Scores for a customer(individual/firms).

1)A PD model needs all of it variables to be categorigal in nature because its a Logistic Regression model where we cannot use continious variables because we would be calculating the log of odds.
2)We can achieve the same by creating dummies for the continious variables and using fine classing use can categorize them.
3)Further computed the weight of evidence to check which all independepent variables are relevant 
4)Used this weight of evidence to perform course classing on the dummies created for each independent variable.
5)Followed the same technique for Discrete Variables
5)Designed the Logistic Regression Model using all the relevant fetaures on the basis of weight of evidence
6)Modified the Logistic Regression model to get the p values for each of the independent features that were used earlier to design the model.
7)Using those P values identified the key features that would be statistically significant in deteremining the Probalility at Default.
8)Evaluated the performnace of this Model using metrics such as Gini and Kolmogorov Smirnov scores
9)Used the above PD model to calculate Credit Scores.The credit score calculation steps are given in the code.

Steps for conmputing the total final loss that that is expected for a bank on the basis of it should determine its capital.

1)Calualted the Probability at default from the above PD model
2)Designed Beta Regression Models =Logistic+Linear for determining the Loss at Default.
3)Also designed Linear Regression Model to compute the EAD that is the loss that cannot be recovered .
All the setps are given in the code

Final loss =PD*LGD *EAD

