# Neural_Network_Charity_Analysis

## Overview of the analysis: 

Using knowledge of machine learning and neural networks, use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results: 

### Data Preprocessing

- What variable(s) are considered the target(s) for your model? 

Verified if the target was marked as successful in the DataFrame, which was an indicator that it was funded successfully by AlphabetSoup.

- What variable(s) are considered to be the features for your model?

The IS_SUCCESSFUL column is the feature chosen for this dataset.

- What variable(s) are neither targets nor features, and should be removed from the input data?

To improve code efficiency, columns EIN and NAME can be removed because they will not  increase the accuracy of the model. 

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

When looking at the optimized model, layer 1 started with 110 neurons with a relu activation. Layer 2, dropped to 80 neurons and continued with the relu activation. Then, the sigmoid activation seemed to be the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).

![image](https://user-images.githubusercontent.com/107759305/225812734-4251f1e2-bd04-4d5b-99bf-183903e5eab1.png)

- Were you able to achieve the target model performance?

The target for the model was 75%, but the best the model could produce was 72.7%.

![image](https://user-images.githubusercontent.com/107759305/225812849-fed4df32-ef69-45e3-a716-a403152d558f.png)

- What steps did you take to try and increase model performance?

First columns were reviewed. Then, STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy. Then, the linear activation produced the worst accuracy, around 28%. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.

## Summary: 

The relu and sigmoid activations gave us a 72.7% accuracy, consequently it is the best the model that can produce using various number of neurons and layers. Recommendation: we could try the random forest classifier as it is less influenced by outliers.




