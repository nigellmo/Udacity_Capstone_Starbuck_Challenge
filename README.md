# Customer Behaviors Prediction Project

# Libraries used in the project
The project is run under Python 3.0 with utilization of below libraries:
1. Pandas
2. Numpy
3. Matplotlib
4. Seaborn
5. Datatime
6. Sklearn

# Motivation for the project
Analysis of customer behaviors is getting tactical. When a Buy-one-get-one free offer was scarce to consumers in many cases in the past, the incentive was good enough to gather demographic information from consumers, which favored companies to develop the next marketing strategies to keep engaging their targeted customers.
Nowadays, with radical strategies to expand market share from robust competitors, discount offers are ubiquitous — collection of demographic information from consumers becomes secondary but pushing user experience to gather response is more direct to understand customers.
This study utilizes both simulated demographic data of customers and transaction record mimicking customer behavior on the Starbucks rewards mobile app. The goal of this analysis is to predict if customers will complete the offer when they receive the offer(discount or Buy-one-get-one) next time.
This project is also Capstone project for Data Scientist Nanodegree of Udacity Inc.

# File Descriptions
The notebook for analysis can be found in the mother directory.
Stored under ```/data```, there are three set of data, which is a simplified version of data that mimics customer behaviors on the Starbucks rewards mobile app, initialized for the analysis:

- ```portfolio.json```: Offer details on the three types of offers(buy-one-get-one, discount and informational) including channels, difficulty, etc.
- ```profile.json```: demographic data of members using the Starbucks rewards mobile app
- ```transcript.json```: transaction record with member's id, transaction time, actional type(offers received, offers viewed, and offers completed)

Under ```/data/processed data```, there are processed data based on original data derived from data preparation in section one of the notebook.

# Summary of the results of the analysis
Findings from the analysis can be found in the notebook or [here](https://medium.com/@nigel.mo/how-do-consumers-react-to-discount-offer-in-user-app-603cbc91ba09)

There are two parts in the analysis which was challenging:
Two parts in the analysis was challenging:
1. Limited features of demographic informations of customers that there is no obvious indicator for customer behaviors, which I could only segment targeting groups for analysis through comparison.
2. Understand the hidden logics in the transcript in order to work out flow matrix to facilitate anlysis and prediction

Here is a brief of results from the analysis for reference:
1) On Demographic data,
i) most of the members become members in 2017 and 2018
ii) Age of member peak at 50
iii) There are more male than female members, yet low spending groups are also dominant by male
2) Spending in average: In overall it is 104 dollar; in high spending group it is 283 dollars; while in low spending group it is 9 dollars
3) In average high spending members spend in Starbucks once every 3 days. Consider together with point 2, it seems consumption in Starbucks is a consumption habit that offers with low difficulty(e.g. buy-5-get-5) seems not necessary.
4) Most of high spending members complete offers after receiving and viewing the details in most time. But there are also members complete offer without viewing since it is consumption habit as mentioned in point 4.
5) There is a cluster of members who spend exceptionally high(range around 400 to 1300 dollars) which there are one-shot high spending amount proportional to their income.
6) Consider similarity in consumption behavior and completion history to offers of a member, predicive model can achieve accuracy of 82% using Logistic Regression or KNN.

# Acknowledgement
Credit to Starbucks and Udacity Inc. for such interesting dataset!
