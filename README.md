# Neural_Network_Charity_Analysis

## Overview

Create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup with the information of a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

## Results

### Data Preprocessing

1) Target : Weather "IS_SUCCESSFUL" is 1 or 0

2) Features : Every Columns except "IS_SUCCESSFUL"

3) Variable removed: 'EIN' and 'NAME'

### Compiling, Training, and Evaluating the Model

1) There was two hidden layers with the first having 80 neurons and the second 30 neurons. Both having the activation functions "ReLU" since we are looking at positive numbers. There was an output layer with the activation function "Sigmoid" since we are looking for a probability between 0 and 1.

2) The target model gave us a 72.4% accuracy rate which did not reach the goal of 75% or higher.

![initial accuracy ](https://user-images.githubusercontent.com/111706055/212575195-d0838705-4255-4d81-af46-8bf7852e8ad4.png)

3) Steps taken to try and increase model performance:
  - Attempt 1 : Remove more columns (unwanted variables) : 'EIN','NAME',"AFFILIATION","USE_CASE". This gave us an accuracy of 65.3% (lower than original)
  - Attempt 2 : Returning to the original model, we reduced the number of bins for APPLICATION_TYPE (putting "Other" lower than 1000 instead of 500) and CLASSIFICATION (putting "Other" lower than 4000 instead of 1880). This gave us an accuracy of 72.4% (on par with the original model)
  - Attepmt 3 : Picking off on attempt 2, we increased the number of hidden layers to 4 instead of 2 (with the following number of neurons for each layer repectively from 1 to 4 : 80,50,30,10). This gave us an accuracy of 72.2% (on par with the original model)
  
## Summary

The deep learning model is 72.4% accurate (best attempt). This is not ideal since we wanted a 75% accuracy at a minimum. Hence this model needs to have some additional changes. Some recommendations : Increase the number epochs to the training regiments, increase the number neurons to the layers, or increase the number of bins instead of decreasing.

