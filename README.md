# Credit-Card-Fraud-Detection-Machine-Learning-Model
R-based Classification And Regression Tree machine learning model developed using various training and sampling methodologies to detect credit card fraud

# Objective

The median fraud loss in Canada represents about 5% of annual revenues, quite close to the Association of Certified Fraud Examiners (ACFE) estimate of 7% of annual revenues for all U.S. organizations. 

Traditionally, rule-based algorithms have been used to detect credit card fraud in real time. These algorithms, which are based on strict rules, are time-consuming and costly to maintain. They also have a difficult time identifying hidden patterns and responding to new situations that they have not explicitly been trained for. My objective is to develop a more effective and efficient machine learning model making use of various machine learning and sampling techniques. 


# About the Data


The data set is meant to mimic real life fraud detection. It is unbalanced and has some incorrect flagging (some outlier fraud cases aren’t flagged). This means that it is difficult to use traditional supervised learning to train our models. These challenges must be addressed, they are outlined below.

Challenges:
- Unbalanced data
    - Less than 0.5% credit card transactions are fraud
- Operational Efficiency
    - Less than 8 sec to flag a transaction
- Incorrect flagging
    - Excessive incorrect flagging must be avoided




# About the algorithms 

The data is very imbalanced - the vast majority of the cases are legitimate. If the model is trained based off of the imbalanced data it will tend to favour the majority case (= legitimate) causing a large classification error for the fraud cases. To better train the model a more balanced distribution must be used.

The following sampling methods will be used to balance our data and train the machine learning model. 

Random over-sampling (ROS) - Increase the number of fraud transactions by creating duplicates of the already present fraud cases.

Random under-sampling (RUS) - Decrease the number of legitimate cases by random removal. 

Bot (RUS & ROS) - Increase the number of fraud transactions and decrease the number of legitimate transactions. 

Synthetic Minority Over-Sampling Technique (SMOTE) - Over-sample minority class (fraud transactions) by creating synthetic fraud cases

Once the data is balanced we will use it to train a Classification And Regression Tree (CART) as our predictive model

# Results
- Breakdown of fraud vs legitamate cases in our original dataset
<img width="502" alt="image" src="https://user-images.githubusercontent.com/40481691/168497501-0377812f-013f-4269-891d-28330ac0f384.png">

- Confusion Matrix of with no model - 0/64 fraud cases were successfuly identified
<img width="334" alt="image" src="https://user-images.githubusercontent.com/40481691/168497583-14913f4f-1458-45c5-bd91-67e38a995deb.png">

- ROS dataset:
<img width="501" alt="image" src="https://user-images.githubusercontent.com/40481691/168498189-f2cae321-1bb5-40e4-b741-cb59055bb26d.png">

- RUS dataset:
<img width="503" alt="image" src="https://user-images.githubusercontent.com/40481691/168498835-c2c938e5-ad10-41a5-92e8-6881eee71101.png">

- SMOTE dataset:
<img width="502" alt="image" src="https://user-images.githubusercontent.com/40481691/168498288-51679fe2-fc3d-4ed6-85cd-8db384e8dfdb.png">


- Classification And Regression Tree Predictive Model:
<img width="383" alt="Screen Shot 2022-05-15 at 5 41 55 PM" src="https://user-images.githubusercontent.com/40481691/168495059-1161f31e-b8a8-428b-bcbb-d36e8cdca33e.png">


- Confusion Matrix after training. The model succesfully identified one fraud cause in the testing dataset.  
<img width="481" alt="Screen Shot 2022-05-15 at 5 42 46 PM" src="https://user-images.githubusercontent.com/40481691/168495073-2cbff508-0f75-433c-82d8-27fb349cffb4.png">


