**ANALYSIS OF DATA IS DONE IN THE NOTEBOOK UNDER EACH OUTPUT**

**HOW TO RUN THE CODE:**

1. GO TO THE GOOGLE COLLAB NOTEBOOK AND PRESS OPEN IN COLLAB

2. DOWNLOAD THE all_cities.zip FOLDER AND UPLOAD IT INTO THE GOOGLE COLLAB, IT MIGHT TAKE A MINTUE OR TWO

3. TO UNZIP THE FILE BY RUNNING THE FIRST CELL (IF YOUR PATH IS DIFFERENT PLEASE REPLACE IT)

4. ONCE THE FILE IS UNZIPPED LOCATE THE UNZIPPED FOLDER, ENSURE THE PATH IS CORRECT IN THE 3rd CELL WHERE WE ARE LOADING THE DATA. IF IT IS DIFFERENT PLEASE CHANGE IT.

5. RUN THE FULL NOTEBOOK, ENSURE THE DATA WAS LOADED CORRECTLY FROM THE OUTPUT OF PREPROCESSING

6. LOOK AT THE OUTPUTS UNDER EACH CELL. I HAVE WRITTEN ANALYSIS FOR EACH PART OF THE NOTEBOOK.

7. EACH TASK HAS EXPLAINATIONS IN THE NOTEBOOK, PLEASE LOOK AT THE NOTEBOOK FOR EASIER UNDERSTANDING(NOTEBOOK HAS ALL THE CHARTS/VISUAL DATA). I WILL INCLUDE THE REPORT HERE AS WELL




**INDIVIDUAL ANALYSIS**

After creating, and training our models for each individual city it looks like the XGBoost model outperformed the Neural Networks for most of the citites. For 9/12 cities the RMSE was lower and the R^2 value was higher for XGBoost over the neural networks. This is a clear sign that for this specific problem XGBoost is the prefered model.
XGBoost looks to have been better for almost all the cities except for the smaller cities, both Salem and Columbus had better performance with the neural network 1 over XGBoost. But for salem we can see that the R^2 values are extremely low (negative) for all models which can maybe be explained by the fact that Salem has only 351 listing compared to the thousands of listings for the other cities. This can be an issue for multiple reasons one of them being that outliers can heavily affect the predictions since it can heavily skew the averages due to the little ammount of data. For future training we can improve on the model by fidning more data, or tweaking the model to learn better on a smaller dataset by trying to remove obvious outliers for smaller datasets.




**CITY GROUPS ANALYSIS**

When training the models on groups of big cities, medium cities, and small cities we can we an obvious winner of XGBoost. For all 3 groups XGBoost had a RSME significantly higher than either Neural Network. Additionally the R^2 was also higher for all 3 further supporting XGBoost being the better model for this scenerio. 





**CROSS TRAINING/TESTING ANALYSIS**

As we can see from the chart above the RMSE for some combination is extremely high with an extremely low R^2. The combinations that performed the worst are are medium model prediciting on big city data, and the small city model prediciting on the big city data. The pattern seems to be that if the model is trained on a smaller city data set and used on a bigger city dataset the model will be completly inaccurate.

We can see that when you use a model trained on a bigger city data set and tested on a smaller city dataset(Big city model predicting small city prices) the predictions arent as bad. We can see a pattern where the Big city model predicted prices fairly well for all city sizes, the medium model predicted small and medium sized prices well but completely flopped on predicting prices of the big cities, the small model predicited well for only the small city data set and it flopped on predicting on the medium and big dataset which shows a pretty clear pattern.



***CHART/VISUALIZATION ANALYSIS IN COLAB NOTEBOOK***



AIRBNB LISTING DATES

New york - october 1 2025
Los Angeles - september 1 2025
San Fran - september 1 2025
Chicago - June 17 2025

Austin - June 13 2025
Seattle - September 25 2025
Denver - September 29 2025
Portland - September 06 2025

Asheville - June 17 2025
Santa cruz - June 28 2025
Salem  - September 25 2025
Columbus - September 26 2025
