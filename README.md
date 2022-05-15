# Credit-Card-Fraud-Detection-Machine-Learning-Algorithms
R based machine learning algorithms developed using various training and sampling methodologies to detected credit card fraud

# Objective

The median fraud loss in Canada represents about 5% of annual revenues, quite close to the Association of Certified Fraud Examiners (ACFE) estimate of 7% of annual revenues for all U.S. organizations. 

Traditionally, rule-based algorithms have been used to detected credit card fraud in real time. These algorithms, which are based on strict rules are time consuming and costly to maintain. They also have a difficult time identify hidden patterns and responding to new situations that they have not explicitly been trained for. My objective is to develop a more effective and efficient machine learning model making use of various machine learning and sampling technics. 


# About the Data


The data set is meant to mimic real life fraud detection. It is unbalanced and has some incorrect flagging (some outlier fraud cases aren’t flagged). This means that it is difficult to use traditional supervised learning to train our models. These challenges must be address, they are outlined below.

Challenges:
- Unbalanced data
    - Less than 0.5% credit card transactions are fraud
- Operational Efficiency
    - Less than 8 sec to flag a transaction
- Incorrect flagging
    - Excessive incorrect flagging must be avoided




# About the algorithms 

Our data is very imbalanced - the vast majority of the cases are legitimate. If we train our model based off of this it will tend to favour the majority case (= legitimate) causing a large classification error one the fraud cases. The better train our model we must have a more balanced distribution.

We will use the following sampling methods to balance our data and train our model. 

Random over-sampling (ROS) - Increase the number of fraud transactions be creating duplicates of the already present fraud cases.

Random under-sampling (RUS) - Decrease the number of legitimate cases by random removal. 

Bot (RUS & ROS) - Increase the number of fraud transactions and decrease the number of legitimate transactions. 

Synthetic Minority Over-Sampling Technique (SMOTE) - Over-sample minority class (fraud transactions) by created synthetic fraud cases

# Results

ROS:

<img width="397" alt="Screen Shot 2022-05-15 at 5 37 20 PM" src="https://user-images.githubusercontent.com/40481691/168494902-91ebbaae-0741-4815-af50-6cd80eac686e.png">

RUS:
<img width="387" alt="Screen Shot 2022-05-15 at 5 38 51 PM" src="https://user-images.githubusercontent.com/40481691/168494955-2ef97580-5b4b-406a-8a36-8ca880616c97.png">

ROS & RUS
<img width="395" alt="Screen Shot 2022-05-15 at 5 39 48 PM" src="https://user-images.githubusercontent.com/40481691/168494983-44094a25-b1ff-4ce6-a990-6473a6a15269.png">

Model:
<img width="383" alt="Screen Shot 2022-05-15 at 5 41 55 PM" src="https://user-images.githubusercontent.com/40481691/168495059-1161f31e-b8a8-428b-bcbb-d36e8cdca33e.png">

<img width="481" alt="Screen Shot 2022-05-15 at 5 42 46 PM" src="https://user-images.githubusercontent.com/40481691/168495073-2cbff508-0f75-433c-82d8-27fb349cffb4.png">


