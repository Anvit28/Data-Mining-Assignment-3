## ECO 395M: Exercises 3

## Group Members - Alina Khindanova, Anvit Sachdev, Shreya Kamble

## Problem 4: Predictive model building: California housing

Dataset: CAhousing.csv

Instead of using total rooms and total bedrooms, I am using average
rooms per household and average Bedrooms per household (by diving
totalRooms and totalBedrooms by households).

Next, we split the data into training and test data. The training data
comprises of 80% of overall data, and test data comprises of remaining
20% of the data.

I have performed k-fold (k=5) cross-validation on training set for
tuning hyper parameters of the models.

I tried CART, Random Forest and Gradient-Boosted Trees to predict the
medianHouseValue.  
We obtain the following RMSE values for CART, Random Forest and
Gradient-Boosted Trees:-

    ## [1] "The RMSE of CART model on test data is: 95933.2664739326"

    ## [1] "The RMSE of Random Forest model on test data is: 74301.9348693619"

    ## [1] "The RMSE of Gradient Boosted Tree model on test data is: 59082.9443250177"

We can see that the Gradient Boosted Tree gives the least RMSE.  
We will now use this to make the respective plots. We obtain the
following geometric polygons:-

1.  log medianHouseValue V/S longitude (x) and latitude (y)  
    ![](Assignment-3-Problem-4_files/figure-markdown_strict/log%20medianHouseValue%20V/S%20longitude%20(x)%20and%20latitude%20(y)-1.png)
2.  log predicted\_medianHouseValue V/S longitude (x) and latitude (y)  
    ![](Assignment-3-Problem-4_files/figure-markdown_strict/log%20predicted_medianHouseValue%20V/S%20longitude%20(x)%20and%20latitude%20(y)-1.png)
3.  log AbsoluteResidual\_medianHouseValue V/S longitude (x) and
    latitude (y)  
    ![](Assignment-3-Problem-4_files/figure-markdown_strict/log%20AbsoluteResidual_medianHouseValue%20V/S%20longitude%20(x)%20and%20latitude%20(y)-1.png)
