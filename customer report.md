**Strategic Insights for Optimizing Your Used Car Inventory**

**Executive Summary:**

Our comprehensive analysis focused on understanding the key factors influencing used car prices, employing machine learning using statistical models and transformations.

**Introduction:**

In today's competitive used car market, staying ahead requires a deep understanding of what influences prices. Our analysis aims to provide actionable insights for fine-tuning your inventory to meet customer preferences effectively.

**Methodology**

We explored 11 different model-transformer combinations, to validate and deliver the most accurate predictions with a measurement of the expected error in dollars on average.

We analyzed about 400000 sale transactions across the United States to come to the conclusions. The data set analyzed contained the following data per transaction entry:

_Price, Region, Year, Manufacturer, Model, Condition, Cylinders, Fuel, Odometer, Title status, Transmission, Drive type, Size, Type of car, Paint color, State_

Key Findings:

1. **Most important features:**
    - Regardless of manufacturer the top 4 features were:
        - mileage (odometer)
        - year of manufacture
        - title status
        - car drive is 4WD
    - Next set of characteristics will be:
        - front wheel drive
        - type of car being the most important: sedan, SUV and wagon
        - Condition of the car (fair, good, excellent, etc)
        - Title status (salvage, clean, lien, rebuilt)
    - It is recommended to look at the combination of the features above to acquire cars that will have the features that drive prices to help adjust inventory and meet specific demands within your region.
2. **Price Sensitivity:**
    - **Year**
        
<img src="/images/pricevsyear.png" alt="Year" width="500"/>

In the above figure it can be seen that cars older than 1995 or so have very little change in price, for this case looking at the other features maybe more important

- - **Mileage**

<img src="/images/pricevsmiles.png" alt="Mileage" width="500"/>

After 200k miles, it becomes less important to determine the price

1. **Other factors Influencing Car Prices:**
    - **Title status:**

<img src="/images/titlestatus.png" alt="Title" width="500"/>

Clean and Lien titles are the most desirable. Special attention should be paid to the title information that is unknown, and an additional effort should be made to clarify the title status of a vehicle that is reported as such, as this is not a known factor to impact the price, as it could be on any category. Missing and parts-only titles are the lowest priced as that indicates the vehicle is not drivable or transactable.

- - **Condition**

<img src="/images/condition.png" alt="Prediction error" width="500"/>

- - The condition of the vehicle has some details to pay attention to. Similar to the title status, if the condition is unknown, the casr should be inspected and assessed one ot the other 6 options. An ‘unknown’ condition should not be used to understand the price of a car or to help set a price as it is not deterministic and does not provide guidance to price as it basically can be any of the other 6 options. Any car that is in good, excellent and like new state will command the highest prices.

Recommendations and future investments

1. **Modeling Enhancement:**
    - Consider accessing more powerful computer resources, especially increased memory, this will increase the cost but will provide a more accurate prediction model and will also allow a larger dataset to be processed
2. **Localizing Analysis:**
    - Develop sub-models specific to states and car manufacturers to tailor recommendations based on localized conditions.
3. **Guided Decision-Making:**
    - Utilize the analysis as guidance, considering the margin of error. Focus on informing inventory selection rather than precise price prediction.
4. **Interpreting error**
    - With the resources utilized for this analysis we were able to provide guidance on what features drive car prices. If the customer needs to develop a model to help set and predict car prices, it is recommended to invest in more compute resources and time in order to develop a more complex model. As of this model we average error is about $4500 on average for the whole data set. The chart below illustrates an example of the meaning of this difference comparing real prices called (training) that we used to create the model and predicted prices. The gap between the two is the error in dollars. The chart below represents 50 random samples of the dataset and its price prediction
<img src="/images/error vs prediction.png" alt="Prediction error" width="1000"/>
