# Classification Project Write-up
## Will The Booking For Hotel Reservation Be Canceled?

### Abstract
Every hotel in the world faces a same isuue in its daily operation, that is, there is a possible people will cancel their booking. Too many cancellations will obviously have negative impact on the hotel's profit and revenue. But how possible is a booking will be cancled? What features can help find potential cancellations? And what hotel can do to decrease cancelation rate or to avoid cancelation? In this project, classification models are used to make prediction of hotel booking cancelation, and suggestions to help decrease cancelation rate will also be provided.

### Design
The project is designed to help hotels to predict if a booking will be canceled, find potential related features with booking cancelation, thus may adopt appropriate measures to decrease cancelation rate, and to increase profit.

### Data
 The dataset is obtained from [Kaggle](https://www.kaggle.com/jessemostipak/hotel-booking-demand), which is comporised of over 119k observations and 32 features.  The data is a mixture of quantitative and categorical features and the target is a binary value of 0 and 1, with 0 means no cancelation and 1 represents the booking is canceled. Some features highlights include ```lead_time```(Number of days that elapsed between the entering date of the booking into the PMS and the arrival date), ```total_of_special_requests```(Number of special requests made by the customer),```assigned_room_type```,```adults```,```children```,```babies``` and etc. Some categorical features are transfered to dummy varibles and combined into classification models.

### Algorithms
- **Feature Engineering**
  - Transfering categorical features to binary dummy variables.
  - Dropping features with little importance to simplify models.

- **Models**  

k-nearest neighbors,Logistic regression, decision trees,naive bayes and various ensembling techiniques are used before choosing the strongest model for cross validation performance. After performing aformentioned basic models, we adopted the random forest model as our final model. We tuned the model by adjusting hyper paramters to optimizing and avoid overfitting.

- **Model Evaluation and Metric Selection**  


For this analysis, we would like to decrease both false positive and false negative rate. False positive happens when hotel incorrectly classifies on-cancelation booking as cancelation case, thus might leads to overbooking; on the other hand, false negative is the model incorrectly classifies cancled booking as non-cancelation case, which might lead to underbooking. Therefore, the project seeks to both good ```precison``` and ```recall measurement```, in this case, ```f1```score which combines both becomes the main metrics of our model.

- **Result**
  - Final random forest 5 fold cross validation:
    - f1 score:0.88136
  - Hold out:
    - accuracy: 0.86515:
    - precision: 0.88939:
    - recall: 0.73088:
    - f1: 0.80238:
    - confusion matrix of test data is:

      [[14121   813]   
      [ 2407  6537]]

### tools
- Numpy and Pandas for data manipulation.
- Scikit-learn for modeling.
- Matplotlib and Seaborn for plotting.
- plotly for geographic plots.

### Communications
A PPT presentation will be presented.
