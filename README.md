# Heart Discease model
Developing a model to predict heart atack on people and stabilish what factors are more likely to induct it
<br>
This far, we have already done a analysis of outliars, correlation, merging categories that are just too equal, and verified the relation of all our vars with target. Now, we shall start our first ML model, what we start in 'first_ML.ipynb', where we will use a ML Classifier to take a overview on our problem. We won't use any solution or GridSearch now, neither use Cross Validation...
<br>
<br>
### We know started do implement KFold and are pretending to use it to stack a model with LinearRegression. KFold is implemented in 2nd_ML.ipynb and stack shall be implemented in first_stack_model.ipynb ASAP, after we train other models to use on it's stacking. We are know considering MLPClassifier

#### Conclusion: we have trained our first k-fold model with CBClassifier. We shall know train a MLPClassifier to add to our stack.

<br>
A new organizaition feature has been add. Every model shall have their pretended use at the end, so. 2nd_ML_stack1 means that will be the first CBC (catboost_classifier) model we will use to stack a LR model, by example.
