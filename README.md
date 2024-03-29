# deep-learning-challenge_REPORT
Module21Challenge


# Overview

The purpose of this analysis is to use deep learning neural networks with TensorFlow to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

# Results

## Data Preprocessing

Target Variable: The target for the model is IS_SUCCESSFUL, indicating whether the money given to an organization was used effectively.

Feature Variables: The features for the model include:
APPLICATION_TYPE: The type of application.
AFFILIATION: The affiliation of the applicant.
CLASSIFICATION: The classification of the applicant.
USE_CASE: The use case for the funds.
ORGANIZATION: The type of organization.
STATUS: The status of the applicant's organization.
INCOME_AMT: The amount of income the applicant's organization reports.
SPECIAL_CONSIDERATIONS: Any special considerations for the application.
ASK_AMT: The amount of money being asked for.

Variables to Remove: Non-target and non-feature variables removed include:
EIN and NAME, as they are identifiers and do not contribute predictive power to the model. I also removed STATUS' and 'SPECIAL_CONSIDERATIONS in AlphabetSoupCharity_Optimization_3 to see if it would have an effect. It did not. 

## Compiling, Training, and Evaluating the Model

Neurons, Layers, Activation Functions: The most sucessful neural network model (AlphabetSoupCharity_Optimization_5) was designed with two hidden layers. The first hidden layer with 100 neurons and the second with 40 neurons, both using the ReLU activation function. This configuration was chosen based on trial and error to balance complexity and computational efficiency.The output layer uses the sigmoid activation function, suitable for binary classification.

Target Model Performance: The goal was to achieve a predictive accuracy higher than 75%. No, I was not able to achieve this target model performance.

Performance Achievements and Steps Taken:
Initially, the model accuracy was approximately 53.78%. Through various optimization efforts, including adjusting the binning of INCOME_AMT and ASK_AMT, then later to CLASSIFICATION and ASK_AMT,  the model's accuracy improved to 65.75%.

Steps to Increase Performance included:
Adjusting binning strategies for CLASSIFICATION and ASK_AMT to better categorize these financial figures.Experimenting with different architectures, including adjusting the number of neurons and layers. Implementing different activation functions and regularization techniques to combat overfitting. Modifying the training process, including the number of epochs and batch size.

## Summary
The deep learning model showed promise in predicting the success of funding applications with an accuracy of up to 65.75%, which is an improvement from the initial accuracy but still below the target of 75%. This suggests there is room for further optimization and exploration of model architectures or feature preprocessing.

Recommendation for a Different Model: Given the challenges in reaching the desired accuracy with a deep learning model, a different approach using ensemble methods like Random Forest or Gradient Boosting might be beneficial. These models can handle categorical and numerical data well, are less sensitive to outliers, and can provide feature importance insights, which could be valuable for further feature engineering.

Ensemble methods are robust to overfitting, especially with a dataset that might not be very large, and they often require less preprocessing of data. They can also achieve high accuracy without the need for extensive hyperparameter tuning. Gradient Boosting, in particular, focuses on correcting the mistakes of previous models in the sequence, which can lead to a highly accurate model even with complex datasets. Exploring these models could provide a complementary approach to the deep learning model, potentially achieving higher accuracy or offering insights for further improving the neural network model.


## Credits
For this challenge, I utilized Google, ChatGPT, Stack Overflow, TA assistance, and educational resources related to the unit provided by BCS.

## License
Data for this dataset was generated by edX Boot Camps LLC and is intended for educational purposes only.
