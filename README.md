# Neural_Network_Charity_Analysis

# Project Overview
By implementing a Neural Network Model we developed a tool that assist us in identifying non-profit organizations that are worth donating to and which are high risk.

## Resources
- Dataset: [Charity Data](https://github.com/harg74/Neural_Network_Charity_Analysis/blob/main/resources/charity_data.csv)
- Software: Pyton 3.7, scikit-learn 1.0.1, scipy 1.7.1, numpy 1.20.3, tensorflow 2.6.2

## Results
### Data Preprocessing
- Target Variable: ´´´IS_SUCCESSFUL´´´ is the variable that we are interested and determine if an application will be successful or not. 

- Feature Variables: AFFILIATION, APPLICATION_TYPE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, USE_CASE, CLASSIFICATION and ASK_AMT. (The categorical columns were encoded using OneHotEncoder)
    
- Removed Variables: EIN, NAME and STATUS. These columns were deleted because they don't add any type of value to our model.

### Compiling, Training, and Evaluating the Model
- The final neural network model consisted of 3 hidden layers, that cointains of 100, 50, and 20 neurons, respectively. Each hidden layer employed the tanh function. Whereas the model's output layer utilized the sigmoid activation function.

![image](https://user-images.githubusercontent.com/78564912/153693603-c6b47596-71be-4f50-b591-42adfc56855f.png)

- The model did not achieve the target model performance of 75%. The model's performance was 72.3%.

![image](https://user-images.githubusercontent.com/78564912/153693628-b41c5b60-f505-443a-b736-3419a18e5d82.png)

- The steps that were implemented to try to increase the model performance included: removing noisy varibales (STATUS); adding additional neurons and hidden layers; and changing the activation function of the hidden layers from relu to tanh.

## Summary

- The accuracy of the "optimized" model remained significatively unchanged compared with the initial model at 72.3% (The initial model's accuracy was 72.4%). We can confirm that not because we add more and more layers our model will perform better.

- It would interesting to implement a Random Forest Model as classification model, which it would be capable to achieve similar accuracy with less code and therefore in much less time compared with the implementation time of a neural network.