## Analysis of what consumers a looking for in cars and how it affects price

I have analyzed a dataset with approximately 450 thousand entries of car sales across the United States in order to establish what are the car features that matter the most to users in order to understand the pricing.   This analysis will be useful for car sales dealers when transacting with cars in order to price them properly, maximize profits, be fair with the consurmer given the market trends and also help them for example tune their inventory for a particular need or market segment where the car dealer business operates or targets.

In this analysis, i will describe the methodology used, provide links and overview of the code used and provide a final report for the end user (in this case a car dealer) on how to approach this problem without the need for the customer to have any knowledge in data science, and be able to take it in practical use. 

 **Methodology**
 
Using the CRISP-DM (cross industry standard process for data mining) framework to start with the business problem and establish a process to analyze the data and develop the proper steps to structure the problem.   More information on CRISP-DM can be found **here** and **here**.  Sources that i have utilized to perform this analysis.  We want to use this methodology and avoid rushing into analytics and spend unnecessary time and resources.

**Business understanding**

The business goals are the following:

 - Provide a list of recommendation to the customer of what consumers value in a used car
 - What factors make a car more or less expensive
 - Provide proper limitations and disclaimers on the information with its associated risks and failure points, how was obtained and its accuracy and cost of improvement.    
 
 The analysis provided is based on a statistical model that include limitations dictated by the data provided and it is impacted by data quality, quantity and also compute resources available in order to provide this analysis timely and cost efficient given the conditions of this task.

 **Data understanding**
 
We have a car sales data set with about 450 thousand entries.   There are several columns or categories describing different  characteristics of a car and its associated transactional features as well such as price, model year, odometer and title status, that complete the needed information to transact a car between two parties.   We will assess the following:

 - Data completeness:  How many fields are missing (blanks or unknown values)
 - Quality: The non-numeric fields may include typos, abbreviations or variations from entry to entry that describe the same item for example
 - Data granularity: How many features or categories exist per entry.   Is all the data relevant to the business objective? what is the impact of getting to the solution given the amount of data provided
 
 **Data preparation**

Based on the understanding above we need to clean and scrub the data to get it ready for modeling and analysis.  This is a critical step in order to avoid time-consuming and compute intensive situations that will make the initial analysis impractical given the resources.    To be specific the focus is to clean and simplify the dataset as possible, remove incomplete entries and outliers that can impact the analysis.     We will apply some basic domain knowledge in order to aid this process, for example cars that are zero cost, exotic cars which are very small sample and things like that.   The code and walkthrough below will describe the process and the rationale utilized. 
 
  **Modeling**

Given the business goals above, we will create a model that will assist calculations and predictions with the intent of identifying what drives the car price and what is important to the end user when paying for a car this will be identified anicand commuted as a list of car features that are important, that will help to draw the business strategy around it.  This model will also help to quanitfy the expectation of error and risk when say a new car arrives at the lot and a pricing needs to be set.   The model can always be improved resulting in better accuracy, a set of recommendations that may require further investing will be described as well. 

The initial phase will be an exploratory analysis to understand the data and the potential models that can be applied, for example a linear regression, a ridge model and other parameters to evaluate the options given the constraints we have in terms of data volume and compute limitations.  I will select a model and "tune it" based on observations on the data provided and the transformations in the data.

  **Evaluation and implementation**

Given the model selected, it is critical to find a way to measure the success and understand how accurate the model and conclusions are as we want to provide expectations on how much to rely on the model in order to be applied to the problem statement. I will provide the average error and what features to pay attention to, given their influence on the vehicle price.   The model will be tested with "new" data meaning data not utilized during the training phase of the model emulating a new batch of data influx and evaluate the model behavior as this data is previously known, so we can compare results.

