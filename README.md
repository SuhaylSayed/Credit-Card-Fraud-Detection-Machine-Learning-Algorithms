# Credit-Card-Fraud-Detection-Machine-Learning-Model
R-based Classification And Regression Tree machine learning model developed using various training and sampling methodologies to detect credit card fraud

# Objective

The median fraud loss in Canada represents about 5% of annual revenues, quite close to the Association of Certified Fraud Examiners (ACFE) estimate of 7% of annual revenues for all U.S. organizations. 

Traditionally, rule-based algorithms have been used to detect credit card fraud in real time. These algorithms, which are based on strict rules, are time-consuming and costly to maintain. They also have a difficult time identifying hidden patterns and responding to new situations that they have not explicitly been trained for. My objective is to develop a more effective and efficient machine learning model making use of various machine learning and sampling techniques. 


# Exploring Challenges with Training Data

The dataset is designed to simulate real-life fraud detection. As a result, it is quite imbalanced, with a minimal number of fraudulent transactions. Less than 0.5% of credit card transactions are fraudulent in total. This imbalance makes it challenging to use traditional supervised learning to train the model without overfitting, as it must account for the small number of fraud outliers.


# Balancing Training Data

The data is imbalanced - the vast majority of the cases are legitimate. If the model is trained based off of the imbalanced data it will tend to favour the majority case (= legitimate) causing a large classification error for the fraud cases. To better train the model a more balanced distribution must be used.

The following sampling methods were used to balance the training data. 

Random over-sampling (ROS) - Increase the number of fraud transactions by creating duplicates of the already present fraud cases.

Random under-sampling (RUS) - Decrease the number of legitimate cases by random removal. 

Bot (RUS & ROS) - Increase the number of fraud transactions and decrease the number of legitimate transactions. 

Synthetic Minority Over-Sampling Technique (SMOTE) - Over-sample minority class (fraud transactions) by creating synthetic fraud cases

After the sampling techiques were applied, the training data was used to train a Decision tree to classify fraud and legitimate cases.

# Results
- Breakdown of fraud vs legitamate cases in our original dataset
<img width="502" alt="image" src="https://user-images.githubusercontent.com/40481691/168497501-0377812f-013f-4269-891d-28330ac0f384.png">

- ROS dataset:
<img width="501" alt="image" src="https://user-images.githubusercontent.com/40481691/168498189-f2cae321-1bb5-40e4-b741-cb59055bb26d.png">

- RUS dataset:
<img width="503" alt="image" src="https://user-images.githubusercontent.com/40481691/168498835-c2c938e5-ad10-41a5-92e8-6881eee71101.png">

- SMOTE dataset:
<img width="502" alt="image" src="https://user-images.githubusercontent.com/40481691/168498288-51679fe2-fc3d-4ed6-85cd-8db384e8dfdb.png">


- Breakdown of decision tree. Optimized to minimize overall entropy. The weights were finalized after 15 epochs to avoid overfitting on training data.:
<img width="383" alt="Screen Shot 2022-05-15 at 5 41 55 PM" src="https://user-images.githubusercontent.com/40481691/168495059-1161f31e-b8a8-428b-bcbb-d36e8cdca33e.png">


- Confusion Matrix of model performance on testing data. The testing data, consisting of 600 transactions, was divided into three sets, each containing 200 transactions. With 100% accuracy, the model successfully identified one fraudulent case in each of the test data collections. The number of fraud cases in the test dataset was purposefully minimized to mimic real-life situations.
<img width="481" alt="Screen Shot 2022-05-15 at 5 42 46 PM" src="https://user-images.githubusercontent.com/40481691/168495073-2cbff508-0f75-433c-82d8-27fb349cffb4.png">


