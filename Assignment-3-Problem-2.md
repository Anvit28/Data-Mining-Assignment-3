## Tree modeling: dengue cases

Dataset: dengue.csv

The features of the dataset that I have used in the models are: city,
season,
precipitation\_amt,air\_temp,avg\_temp\_k,dew\_point\_temp\_k,specific\_humidity
and tdtr\_k.

I have used one-hot encoding to deal with dummy variables of the data
set.

Since there are also many observations in the data set with zero dengue
cases so using log dengue cases does not make sense. So we are
predicting dengue cases.

Next, we split the data into training and test data. The training data
comprises of 80% of overall data, and test data comprises of remaining
20% of the data.

I have performed k-fold (k=5) cross-validation on training set for
tuning hyper parameters of the models.

We obtain the following RMSE values for CART, Random Forest and
Gradient-Boosted Trees:-

    ## [1] "The RMSE of CART model on test data is: 23.3834563869149"

    ## [1] "The RMSE of Random Forest model on test data is: 22.946287689396"

    ##  [1] 27.72445 27.72445 27.72445 27.72445 27.72445 27.72445 27.72445 27.72445
    ##  [9] 27.72445 27.72445 27.72445 27.72445 27.72445 27.72445 27.72445 27.72445

    ## [1] "The RMSE of Gradient Boosted Tree model on test data is: 24.5966587253318"

We can see that Random Forest performs the best. We will now use this
model to make partial dependence plots.

We obtain the following partial dependence plot for
specific\_humidity:-  
![](Assignment-3-Problem-1_files/figure-markdown_strict/2.partial%20dependence%20plot%20for%20specific_humidity-1.png)
We obtain the following partial dependence plot for
precipitation\_amt:-  
![](Assignment-3-Problem-1_files/figure-markdown_strict/2.partial%20dependence%20plot%20for%20precipitation_amt-1.png)
We obtain the following partial dependence plot for avg\_temp\_k:-  
![](Assignment-3-Problem-1_files/figure-markdown_strict/2.partial%20dependence%20plot%20for%20avg_temp_k-1.png)
