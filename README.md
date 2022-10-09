# Unit 21 Homework: Charity Funding Predictor

## Background

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

 **Results**: Using bulleted lists and images to support your answers, address the following questions.

<h3> Data Preprocessing </h3>

1) What variable(s) are the target(s) for your model?
-I decided to use the variable of "IS_SUCCESSFUL" because it is a simple binary variable, and would make my model predict the success or failure of money used.

2) What variable(s) are the features for your model?
-The variables I featured were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS,and ASK_AMT.

3) What variable(s) should be removed from the input data because they are neither targets nor features?
-I removed two variables, "EIN" and "NAME" because they would have no impact on the model as they were simply identification values.
  
<h3> Compiling, Training, and Evaluating the Model </h3>

1) How many neurons, layers, and activation functions did you select for your neural network model, and why? Were you able to achieve the target model performance? What steps did you take in your attempts to increase model performance?

-For my initial model, I used the starter code setup as a benchmark to work from. This model utilized two hidden layers (one with 80 and one with 30 neurons). The activation for both was set to the ReLu function. My output layer utilized the sigmoid activitation. 

-For my most successful model, I wanted to start with subtle changes to assess where I could make the biggest impact on my model accuracy. I did not want to add additional layers because I feared that would complicate my model to start. I used the same number of layers (3) as was in my starter code, but for this optimization I only had the initial hidden layer use the ReLu activation function, and I set the middle hidden layer and output layer both to sigmoid activation. This dramatically improved the model's accuracy (from 73% in the first model to 99% in the second model with minimal loss.)

<h3>Summary</h3>

1) Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

-Overall, I was able to create a model that achieved the requested threshold accuracy of 75% in predicting the target variable of "IS_SUCCESSFUL." Initially I was concerned that I created a vanishing gradient problem by using sigmoid functions in both the middle hidden layer and output layer, given that the sigmoid function squashes the input between 0 and 1. Therefore, a large change in the input of the sigmoid function will cause a small change in the output. Despite this potential issue, I also understood that the sigmoid function could handle complex data better than the ReLu function, despite the ReLu fuction reducing the vanishing gradient issues. I also reduced the vanishing gradiant issue by not adding addional layers that would make the model hard to train. Because of the above, I think the optimization of my model is legitimate. Going forward, I would be curious to try out a random forest model on this dataset, given that a large majority of it is categorical variables. 

- - -

## Rubric

[Unit 21 Homework Rubric](https://docs.google.com/document/d/1SLOROX0lqZwa1ms-iRbHMQr1QSsMT2k0boO9YpFBnHA/edit?usp=sharing)

- - - 

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.	

