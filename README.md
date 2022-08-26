
# Wheat Kernel Classification

three different varieties of wheat: Kama, Rosa and Canadian, 70 elements each, randomly selected for the experiment. High quality visualization of the internal kernel structure was detected using a soft X-ray technique.

## Attribute Information

To construct the data, seven geometric parameters of wheat kernels were measured:
1. area A,
2. perimeter P,
3. compactness C = 4*pi*A/P^2,
4. length of kernel,
5. width of kernel,
6. asymmetry coefficient
7. length of kernel groove.
All of these parameters were real-valued continuous.

## Data

https://archive.ics.uci.edu/ml/datasets/seeds#

## Train and Test score without StandardScaler
| S No.|model_name | train_score | test_score |
| --- | --- | --- | --- |
| 1. | LogisticRegression(penalty='l1',solver='saga',tol=0.004,fit_intercept=False,) | 0.9345 | 0.9286 |
| 2. | RidgeClassifierCV() | 0.9762 | 0.9762 |
| 3. | PCA+LogisticRegression() | 0.8988 | 0.9286 |
| 4. | LDA+LogisticRegression() | 0.9762 | 0.9524 |

## Train and Test score with StandardScaler
| S No.|model_name | train_score | test_score |
| --- | --- | --- | --- |
| 1. | LogisticRegression(penalty='l1',solver='saga',tol=0.004,fit_intercept=False,) | 0.9524 | 0.9524 |
| 2. | RidgeClassifierCV() | 0.9702 | 0.9524 |
| 3. | PCA+LogisticRegression() | 0.9345 | 0.8810 |
| 4. | LDA+LogisticRegression() | 0.9762 | 0.9524 |
