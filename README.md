# sensor_impact_FDD
This is an NREL public repository used for sensor impact evaluation and verification project funded by DOE. Specifically, the function of repository can evaluate the sensor impact, including sensor accuracy and sensor selection, on fault detection and diagnostics (FDD) performance.

The run of the modules in this repo relies on the fault building simulation data that calibrated on Oak Ridge National Laboratory's Flexible Research Platform. Check the Data section for download information.

This project is a work-in-progress and is temporarily in a personal repository, which in the future will be moved to https://github.com/NREL/sensor_impact_FDD after the account is set up by NREL's Information Technology Support team.

Authors: Liang Zhang, Matt Leach, National Renewable Energy Laboratory, January 18, 2021

## Installation
Download and install the latest version of [Conda](https://docs.conda.io/en/latest/) (version 4.4 or above)
Create a new conda environment:

`$ conda create -n <name-of-repository> python=3.8 pip`

`$ conda activate <name-of-repository>`

(If you’re using a version of conda older than 4.4, you may need to instead use source activate <name-of-repository>.)

Make sure you are using the latest version of pip:

`$ pip install --upgrade pip`

Install the environment needed for this repository:

`$ pip install -e .[dev]`

## Data
This module is developed based on the fault building simulation data that calibrated on Oak Ridge National Laboratory's Flexible Research Platform.
The data include 22 fault types data under seven weathers from different climate zones. The details of physics-based modeling of the faulty buildings are introduced in [this paper](https://www.mdpi.com/2075-5309/9/11/233/htm).

Downloading data is mandatory to use the classes in the repo,

The data can be downloaded [here](https://docs.conda.io/en/latest/). Please contact Liang.Zhang@nrel.gov if there is any download issues.

## Modules
The base.py and SIE.py provide modules to realize sensor impact evaluations. This repo contains three sub-classes that realize three modules used for sensor impact evaluation in FDD.

### Module 1: Sensor Accuracy Impact on FDD Performance
Sub-Class Name: sensor_accuracy_impact_FDD or SAIF

### Module 2: Sensor Selection and Impact on FDD Performance
Sub-Class Name: sensor_selection_impact_FDD or SSIF

### Module 3: Sensor Accuracy Impact on Sensor Selection and FDD Performance
Sub-Class Name: sensor_accuracy_impact_sensor_selection or SAISS

## Machine Learning Algorithms
### Linear Models
[Classifier using Ridge regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RidgeClassifier.html#sklearn.linear_model.RidgeClassifier)

[Logistic regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html#sklearn.linear_model.LogisticRegression)

[Stochastic Gradient Descent - SGD](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDClassifier.html#sklearn.linear_model.SGDClassifier)

[Passive Aggressive Algorithms](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.PassiveAggressiveClassifier.html#sklearn.linear_model.PassiveAggressiveClassifier)

[Perceptron](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Perceptron.html#sklearn.linear_model.Perceptron)

### Linear and Quadratic Discriminant Analysis
[Linear Discriminant Analysis](https://scikit-learn.org/stable/modules/generated/sklearn.discriminant_analysis.LinearDiscriminantAnalysis.html#sklearn.discriminant_analysis.LinearDiscriminantAnalysis)

[Quadratic Discriminant Analysis](https://scikit-learn.org/stable/modules/generated/sklearn.discriminant_analysis.QuadraticDiscriminantAnalysis.html#sklearn.discriminant_analysis.QuadraticDiscriminantAnalysis)

### Support Vector Machines
[C-Support Vector Classification](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html#sklearn.svm.SVC)

[Nu-Support Vector Classification](https://scikit-learn.org/stable/modules/generated/sklearn.svm.NuSVC.html#sklearn.svm.NuSVC)

[Linear Support Vector Classification](https://scikit-learn.org/stable/modules/generated/sklearn.svm.LinearSVC.html#sklearn.svm.LinearSVC)

### Nearest Neighbors
[Classifier implementing the k-nearest neighbors vote](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html#sklearn.neighbors.KNeighborsClassifier)

[Nearest centroid classifier](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.NearestCentroid.html#sklearn.neighbors.NearestCentroid)

[Gaussian process classification (GPC) based on Laplace approximation](https://scikit-learn.org/stable/modules/generated/sklearn.gaussian_process.GaussianProcessClassifier.html#sklearn.gaussian_process.GaussianProcessClassifier)

### Naive Bayes
[Gaussian Naive Bayes](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html#sklearn.naive_bayes.GaussianNB)

[Naive Bayes classifier for multivariate Bernoulli models](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.BernoulliNB.html#sklearn.naive_bayes.BernoulliNB)

[Naive Bayes classifier for multinomial models](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html#sklearn.naive_bayes.MultinomialNB)

### Decision Trees
[Decision Tree Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html#sklearn.tree.DecisionTreeClassifier)

### Ensemble methods
[Random Forest Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html#sklearn.ensemble.RandomForestClassifier)

[Extra-Trees Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.ExtraTreesClassifier.html#sklearn.ensemble.ExtraTreesClassifier)

[AdaBoost classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostClassifier.html#sklearn.ensemble.AdaBoostClassifier)

[Histogram-based Gradient Boosting Classification Tree](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.HistGradientBoostingClassifier.html#sklearn.ensemble.HistGradientBoostingClassifier)

[Gradient Boosting for classification](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html#sklearn.ensemble.GradientBoostingClassifier)

### Neural Network
[Multi-layer Perceptron classifier](https://scikit-learn.org/stable/modules/generated/sklearn.neural_network.MLPClassifier.html#sklearn.neural_network.MLPClassifier)
