### Report on the Neural Network Model

1. **Overview** : The purpose of this analysis was to determine if it would be beneficial for Alphabet Soup to use a neural network model to help it select charities that would best make use of funding that it would provide. 

2. **Results**: 

- Data Preprocessing

   - What variable(s) are the target(s) for your model? 
        * For this analysis, "IS_SUCCESSFUL" is the target variable.

   - What variable(s) are the features for your model?
       
        For the first model that I built using a neural network, I used 9 features (dropping "NAME" and "EIN"). For the optimization step, I used the following 7 features for the model:
        * 'APPLICATION_TYPE'
        * 'AFFILIATION'
        * 'CLASSIFICATION'
        * 'USE_CASE'
        * 'ORGANIZATION'
        * 'INCOME_AMT'
        * 'ASK_AMT'
  
   - What variable(s) should be removed from the input data because they are neither targets nor features?

        I removed the following 4 variables because they did not add meaningful information to the model, for STATUS and SPECIAL_CONSIDERATIONS I removed them on the optimization step because they did not have any real variation, only small numbers of one of the two categories of both were present.
        * "EIN"
        * "NAME"
        * "STATUS"
        * "SPECIAL_CONSIDERATIONS"
  
  

- Compiling, Training, and Evaluating the Model

   - How many neurons, layers, and activation functions did you select for your neural network model, and why?
       - For the original model: I used 3 hidden layers with the following neurons and activation functionsl: Layer 1: relu, 8 neurons; Layer 2: relu and 5 neurons; Layer 3: sigmoid and 1 neuron.  
    ![Alt text](images/original_model.png?raw=true "Original Model")

    #### Optimization:
    - For the best performing of the three optimization models that I created: I used 5 hidden layers with the following neurons and activation functionsl: 
        - Layer 1: relu, 9 neurons 
        - Layer 2: relu and 7 neurons
        - Layer 3: relu and 7 neurons
        - Layer 4: tanh and 5 neurons
        - Layer 5: sigmoid and 1 neuron 
    ![Alt text](images/opt_model_1.png?raw=true "Opt Model 1")
    ![Alt text](images/opt_model_2.png?raw=true "Opt Model 1")

   - Were you able to achieve the target model performance? 
       - I was not able to make the model reach target performance, after 3 attempts in the optimazation notebook, the best I could do was reach:
       - 72.52% accuracy. 
        ![Alt text](images/opt_accuracy.png?raw=true "Opt Accuracy")

   - What steps did you take in your attempts to increase model performance? 
       - I changed the number of features from 9 to 7, I changed the number of layers from 3 to 5 and back to 3, 5 layers performed slightly better. I changed all of the activation functions of the layers, I changed the number of epochs from 100 to 120, 100 performed the best.
      
**Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Overall, the neural network model that I created to classify the binary outcome variable of IS_SUCCESSFUL was just over 72% accurate. This is better than random chance so it could helpful to Alphabet Soup to get money to organizations that could do a better than average chance to put the money to good use. However, the model could be improved by adding more features that could greatly increase model performance. 

Another approach that I would recommend was to create a model using cluster analysis to find different levels of organizations to give more or less money to, that way a lot more organizations get some money but the most likely to be successful/ use the money in a better way will get the most money.