# All-Hyper-Parameter-Optimization-
# All Techniques Of Hyper Parameter Optimization GridSearchCV RandomizedSearchCV Bayesian Optimization -Automate Hyperparameter Tuning (Hyperopt) Sequential Model Based Optimization(Tuning a scikit-learn estimator with skopt) Optuna- Automate Hyperparameter Tuning Genetic Algorithms (TPOT Classifier) 

# References 

* https://github.com/fmfn/BayesianOptimization 
* https://github.com/hyperopt/hyperopt
*  https://www.jeremyjordan.me/hyperparameter-tuning/ 
*  https://optuna.org/ 
*  https://towardsdatascience.com/hyperparameters-optimization-526348bb8e2d(By Pier Paolo Ippolito )
*   https://scikit-optimize.github.io/stable/auto_examples/hyperparameter-optimization.html  


** The main parameters used by a Random Forest Classifier are: 

criterion = the function used to evaluate the quality of a split.
max_depth = maximum number of levels allowed in each tree. max_features = maximum number of features considered 
when splitting a node. min_samples_leaf = minimum number of samples which can be stored in a tree 
leaf. min_samples_split = minimum number of samples necessary in a node to cause node splitting. n_estimators = number of trees in the ensamble. 

# Automated Hyperparameter Tuning Automated Hyperparameter
  Tuning can be done by using techniques such as  
  * Bayesian Optimization Gradient Descent Evolutionary Algorithms 
  * 
  # Bayesian Optimization Bayesian optimization uses 
  probability to find the minimum of a function. The final aim is to find the input value to a function which can gives us the lowest possible output value.
  It usually performs better than random,grid and manual search providing better performance in the testing phase and reduced optimization time.
  
  # In Hyperopt, Bayesian Optimization 
  can be implemented giving 3 three main parameters to the function 
  *fmin.  
  *Objective Function = defines the loss function to minimize.
  *Domain Space = defines the range of input values to test (in Bayesian Optimization this space creates a probability distribution for each of the used Hyperparameters).
  
  # Optimization Algorithm = defines the search algorithm to use to select the best input values to use in each new iteration.
  
  # Genetic Algorithms Genetic Algorithms tries to apply natural selection mechanisms to Machine Learning contexts.
  
  Let's immagine we create a population of N Machine Learning models with some predifined Hyperparameters.
  We can then calculate the accuracy of each model and decide to keep just half of the models (the ones that performs best). 
  We can now generate some offsprings having similar Hyperparameters to the ones of the best models so that go get again a population of N models.
  At this point we can again caltulate the accuracy of each model and repeate the cycle for a defined number of generations. In this way, 
  just the best models will survive at the end of the process.    
  
  # Optimize hyperparameters of the model using Optuna
  
  The hyperparameters of the above algorithm are n_estimators and max_depth for which we can try different values to see if the model accuracy can be improved. The objective function is modified to accept a trial object. This trial has several methods for sampling hyperparameters. We create a study to run the hyperparameter optimization and finally read the best hyperparameters.
