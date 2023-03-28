[Back to Portfolio](index)

---
## **Predicting customer defaulting on a loan: Home Credit Group classification algorithms analysis**

### Summary

Given Home Credit's default risk data, this project aims to build a classification algorithm that will predict whether or not a client will default on a loan. Secondly, due to the business nature of the problem, the project also aims to analyze different models to try and explain their financial implications when optimizing for different metrics. Finally, the project will aim to not only optimize statistical performance but also computing power efficiency: a marginal improvement in accuracy may not be an overall gain given the time the model takes to perform.

As the objective of the project is only to predict, at no point will we touch on output interpretability nor try to point out the most prominent features that drive defaulting on a loan.

In order to accomplish this we will use Python and in particular Scikit learn 1.1.3 for both data processing as well as model implementation. For Gradient Boosted Trees, we will use the LightGBM package.

Because we do know that the data is very imbalanced (over 90% of the observations are negative), the performance metric of interest will not be accuracy as is: just by always predicting negative we would be right most of the time. Instead we will focus on ROC Area Under the Curve, which is a far more balanced metric.

1: &emsp;24825&nbsp;&nbsp;&emsp;(Defaulted)<br>
0: &emsp;282686&emsp;(Did not default)



It is important to use such a metric which combines elements from both the true positive rate as well as the true negative rate: if we were to flag accurately all the defaulting loans (recall) we may avoid the costs of the default, however at the expense of missing on plenty of customers who would have paid their loans and interest back. As we do not know the associated benefits and costs of these two cases, ROC Area Under the Curve is the best we can do for this imbalanced dataset. We will also keep track of accuracy and runtime of each model, just not trying to optimize it as this could be done on the best model when deploying on the cloud if its performance warrants it.

These were the models that were fitted:

1. Logistic Regression
2. Lasso Regression (L1)
3. Support Vector Machines
4. Decision Trees

Ensemble Models<br>

5. Random Forest
6. LightGBM (Gradient Boosted Algorithm)

These were the results:




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>roc_auc</th>
      <th>accuracy</th>
      <th>runtime</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>LGBM</th>
      <td>0.790970</td>
      <td>0.920126</td>
      <td>1788.541508</td>
    </tr>
    <tr>
      <th>random_forest</th>
      <td>0.758290</td>
      <td>0.919271</td>
      <td>1005.142762</td>
    </tr>
    <tr>
      <th>SVC</th>
      <td>0.752688</td>
      <td>0.915304</td>
      <td>12.469002</td>
    </tr>
    <tr>
      <th>logistic_regression_full</th>
      <td>0.696794</td>
      <td>0.909928</td>
      <td>30.610333</td>
    </tr>
    <tr>
      <th>decision_tree</th>
      <td>0.617587</td>
      <td>0.897792</td>
      <td>78.623214</td>
    </tr>
    <tr>
      <th>logistic_regression_l1</th>
      <td>0.481147</td>
      <td>0.919271</td>
      <td>33.661335</td>
    </tr>
  </tbody>
</table>
</div>



Ignoring runtime for a second, it can be clearly seen that Lightweight Gradient Boosting Model (LGBM) results are the clear winners: The model captures effectively those clients who will default while not rejecting those who would not default if given the loan better than any other model.

This would be a massive improvement over the default of assuming every client will pay back: it will be as accurate as that one, but better in that this one will actually avoid a lot of the costs associated with a client defaulting. The other default assumption would be to assume that no client would ever pay back and not hand out any loans, which of course would result in the bank closing. Deploying this model would strike a great balance which would allow the bank to collect interest and principal on the loans they give while reducing the risk of giving loans that will not be paid back.

The model does have some limitations and setbacks that should be addressed when implementing on a larger scale.

* Ideally, some more feature engineering should be conducted to further feed information to the model as to how defaulting really works.
* Because of the large nature of the data, this model is likely not perfectly tuned: when getting access to the adequate computing power, the model can and should be modified to improve performance.
* Speaking about computing power, given that we did not have access to GPU resources, we did not try to implement more powerful models, such as XGBoost. That model would very likely perform better than LGBM, and should be tried if possible. Any improvement, even if marginal, would implicate massive savings in costs for the bank when scaled to thousands of transactions.

### References

* [Data](https://www.kaggle.com/competitions/home-credit-default-risk/data)
* [LightGBM](https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMClassifier.html#lightgbm.LGBMClassifier)
* [Full Project](https://github.com/roberto-andrade22/loan_default_classification)

---
[Back to Portfolio](index)
