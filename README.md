# Parameter Optimisation of SVM

## Introduction
This assignment illustrates a way of finding the optimal hyperparameter of Support Vector Classifier. The data set used here is Letter Recognition Data Set from UCI repository.


## Dataset
The data used contains 17 columns and 20,000 rows. Various parameters are used to predict the letter from A-Z 

## Methodology
The dataset is split into training and testing set for 10 times and the following SVC classifier hyperparameter are selected for best accuracy:
- **Kernel** - Selected from RBF, Polynomial, Linear and Sigmoid
-  **C (Regularisation parameter)** - Random integer values from 1 to 7
- **Gamma (Kernel coefficient)** - Random integer values from -1 to 7. If the value is less than 1, then gamma is randomly set as auto or scale. It is used only by rbf, poly and sigmoid kernel.
- **Degree** - Random integer from 1 to 5. It is only used by poly kernel and represent the degree of polynomial kernel function.

The above hyperparameters are randomly selected from the given values for 100 iterations. The parameters that gave the best accuracy for each sample are shown in table below:
| Sample | Kernel | c | gamma | degree | Accuracy |
|--------|--------|---|-------|--------|----------|
| 1      | rbf    | 6 | scale | 4      | 0.967500 |
| 2      | rbf    | 7 | auto  | 5      | 0.971167 |
| 3      | rbf    | 7 | auto  | 7      | 0.964500 |
| 4      | rbf    | 7 | scale | 2      | 0.967333 |
| 5      | rbf    | 5 | auto  | 4      | 0.964667 |
| 6      | rbf    | 7 | auto  | 6      | 0.967000 |
| 7      | rbf    | 7 | auto  | 1      | 0.968333 |
| 8      | rbf    | 5 | auto  | 7      | 0.963000 |
| 9      | rbf    | 6 | auto  | 4      | 0.963833 |
| 10     | rbf    | 7 | auto  | 5      | 0.968667 |

The following Convergence graph shows the accuracy of sample 8 (maximum accuracy) over the 100 iterations:

![output](https://user-images.githubusercontent.com/71625050/233223546-83f8a074-0058-4f54-8070-8a47cff390d5.png)

## Result
The best parameters of SVC for the given dataset are:
- Kernel : rbf
- C : 7
- Gamma : auto
- Degree : 5

The above parameter gave a maximum accuracy of 0.971167.
