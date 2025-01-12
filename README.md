# module_21

Deep Learning Model Performance Report for Alphabet Soup
Overview of the Analysis:
The purpose of this analysis was to build and evaluate a deep learning model to predict whether an individual will be successful based on various features. The data comes from the Alphabet Soup dataset, which contains several features related to the applicants, including information about their past earnings, education, and other personal characteristics. Our goal was to predict the target variable, which indicates whether an applicant is a successful candidate for funding (i.e., successful or unsuccessful). The task was framed as a classification problem.

Results:
Data Preprocessing:
Target Variable(s):

The target variable for this model is IS_SUCCESSFUL. This binary variable indicates whether an applicant was successful or not, making it suitable for binary classification.
Feature Variable(s):

The features for the model are a variety of columns that provide information about the applicants. These include:
APPLICATION_TYPE
CLASSIFICATION
EIN
NAME
USE_CASE
ORGANIZATION
STATUS
INCOME
SPECIAL_CONSIDERATIONS These features provide both categorical and numeric data for the model to learn from.
Variables to Remove:

The following variables should be removed from the dataset because they are neither features nor targets:
EIN: This variable is a unique identifier for each applicant and does not provide any useful information for the model.
NAME: The name of the applicant should not be used as a feature as it does not contain any meaningful pattern or correlation with the target variable.
Compiling, Training, and Evaluating the Model:
Neurons, Layers, and Activation Functions:

Number of Layers and Neurons:

The model consisted of three hidden layers with the following number of neurons:
First Hidden Layer: 128 neurons
Second Hidden Layer: 64 neurons
Third Hidden Layer: 32 neurons
These layers were chosen to allow the model to learn complex relationships in the data while maintaining sufficient capacity for generalization.
Activation Functions:

The ReLU (Rectified Linear Unit) activation function was used for all hidden layers, as it helps to mitigate the vanishing gradient problem and allows the model to learn more effectively.
For the output layer, a sigmoid activation function was used because we are dealing with a binary classification problem. This produces output between 0 and 1, which can be interpreted as probabilities.
Why These Choices Were Made:

The selected number of layers and neurons balances model complexity and training efficiency. We used ReLU to encourage faster learning and sigmoid for the output layer, which is common in binary classification problems.
Achieving Target Model Performance:

The target model performance was to achieve an accuracy above 70%.
After training, the model achieved an accuracy of approximately 79%, which surpassed the performance target, indicating good generalization and fit.
Steps Taken to Increase Model Performance:

Data Normalization: All numeric features were normalized to ensure that the model did not disproportionately favor any feature based on its scale.
Overfitting Prevention: Dropout layers were added with a dropout rate of 0.2 to prevent overfitting during training.
Tuning Hyperparameters: We experimented with different numbers of neurons and layers in the hidden layers. Additionally, we tested different batch sizes and epochs to find the best combination.
Model Evaluation: Model performance was evaluated using both accuracy and loss, and early stopping was implemented to prevent unnecessary overfitting by halting the training when the validation accuracy stopped improving.
Summary:
Overall Results:
The deep learning model performed well, achieving an accuracy of 79% on the test set, exceeding the target performance of 70%. The steps taken, including proper data preprocessing, normalization, and hyperparameter tuning, helped optimize the model’s performance.
Recommendation for a Different Model:
Although the deep learning model performed well, a different model that could also be considered is Random Forest. Random Forest is an ensemble learning method that can handle both numeric and categorical features effectively and is less prone to overfitting compared to neural networks, especially with smaller datasets. It could serve as a good alternative, especially for datasets with limited data or when interpretability is crucial.
Reasons for the recommendation:
Random Forest would offer a more interpretable model than deep learning.
It naturally handles feature importance, allowing us to identify which features are most impactful.
It can perform well without heavy tuning and with less need for data normalization.
