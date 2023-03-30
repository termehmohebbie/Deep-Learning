# Deep Learning
### Alphabet Soup Charity Model

#### Overview of the analysis: 

In this analysis we're using real world dataset containing data from more than 35000 organizations, funded by Alphabet Soup in the past. With the help of this data, the aim of the analysis is to create a deep learning neural network model to predict the success/failure of the future funds.

#### Results: 

##### Data Preprocessing

* The "IS_SUCCESSFUL" column is target of this model.  
* During optimization attempts, different feature sets were used to understand their effects on the loss and accuracy.

##### Compiling, Training and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

The main model has two hidden layers with 80 and 30 neurons respectively. The hidden layes used "relu" activation function while the output layer used "sigmoid" activation function. In this analysis, the epochs number was 100. 

* Were you able to achieve the target model performance?

The main model could not achieve the target model performance which is 75%. The accuracy of this model was around 73% and the loss was 56%.

* What steps did you take in your attempts to increase model performance?

  Three different attempts were made to optimize the model:
  
    * **Attempt #1**
      * Number of epoches was increased to 150 from 100.     
      * A new hidden layer was added with 60 neurons.
      
      Results : 73% accuracy (same) / 58% loss (increased)
      
    * **Attempt #2**
      * Two more variables were dropped ('STATUS' and 'SPECIAL_CONSIDERATION'). 
      * Binning structures of 'APPLICATION_TYPE' and 'CLASSIFICATION' variables have been changed.
      * A new hidden layer was added with 60 neurons. 
      
      Results : 73% accuracy (same) / 58% loss (increased)

    * **Attempt #3**
      * Two more dense layers were added.
     
    Results : 73% accuracy (same) / 58% loss (increased)


#### Summary: 

None of the optimization attempts had achieved increase in accuracy, instead they were cause to increase in loss. Since there are a lot of categorical data in our dataset, may be trying decision trees or random forrest methods to get better results.
