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

<br>
We executed a grid search. The best run had the following parameters:

Best trial: 25. Best value: 0.955495:  87%|████████▋ | 26/30 [8:32:36<1:32:44, 1391.04s/it]
[I 2026-02-17 19:19:58,582] Trial 25 finished with value: 0.9554952344394854 and parameters: {'iterations': 1233, 'depth': 5, 'learning_rate': 0.05563228358640898, 'l2_leaf_reg': 1.2388924496891942, 'border_count': 157}. Best is trial 25 with value: 0.9554952344394854.

<br>

We've sent our second submission, and we are now on the top 50%+ on Kaggle Competition!

<br>

We've runned GridSearch with Optuna for our MLPClassifier model. We got the following best set of hyperparameters:
<br>

#### [I 2026-02-18 15:01:16,452] Trial 22 finished with value: 0.9533291427951834 and parameters: {'hidden_layer_sizes': (128,), 'alpha': 5.894589851301599e-05, 'learning_rate_init': 0.0007594934857959463, 'activation': 'relu'}. Best is trial 22 with value: 0.9533291427951834.
<br>
We trained the MLPCtunned model, and used KFold to generate oof_preds. The oof_preds are stored into mlp_oof.npy.

<br>

#### We trained the LogisticRegression tunned model, at Logistic_Regression_tunned.ipynb, we've obtained the following score and best params:
Best score: 0.9526825664593407
Best params: {'C': 0.061907906899253747, 'penalty': 'l1', 'solver': 'liblinear'}
