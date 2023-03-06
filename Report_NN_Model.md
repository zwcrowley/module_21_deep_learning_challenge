### Report on the Neural Network Model

1. **Overview** : The purpose of this analysis was to determine if it would be beneficial for Alphabet Soup to use a neural network model to help it select charities that would best make use of funding that it would provide. 

2. **Results**: 

- Data Preprocessing

   - What variable(s) are the target(s) for your model? 
        
        For the first model that I built using a neural network, I used all 9 features (dropping "NAME" and "EIN"). For the optimization step, I used the following 7 features for the model:
        * 'APPLICATION_TYPE'
        * 'AFFILIATION'
        * 'CLASSIFICATION'
        * 'USE_CASE'
        * 'ORGANIZATION'
        * 'INCOME_AMT'
        * 'ASK_AMT'
  
   - What variable(s) are the features for your model?
        * For this analysis, "IS_SUCCESSFUL" is the target variable.
  
   - What variable(s) should be removed from the input data because they are neither targets nor features?

        I removed the following 4 variables because they did not add meaningful information to the model, for STATUS and SPECIAL_CONSIDERATIONS I removed them on the optimization step because they did not have any real variation, only small numbers of one of two categories.
        * "EIN"
        * "NAME"
        * "STATUS"
        * "SPECIAL_CONSIDERATIONS"
  
  

- Compiling, Training, and Evaluating the Model

   - How many neurons, layers, and activation functions did you select for your neural network model, and why?
   - Were you able to achieve the target model performance?
   - What steps did you take in your attempts to increase model performance?
  
**Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.