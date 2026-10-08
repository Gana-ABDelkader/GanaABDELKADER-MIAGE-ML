# HW1 – Introduction and Learnability

## Statistical and Machine Learning

This homework experimentally illustrates the difference between **PAC** and **Agnostic PAC** learning using **Empirical Risk Minimization (ERM)** with threshold classifiers.

The experiments are implemented in Python using a Jupyter Notebook.

## Objective

The objective is to study how the performance of a threshold classifier changes depending on:

- the size of the training dataset
- the presence or absence of label noise
- the empirical error and true error
- the probability of having a true error greater than $\epsilon$.

The homework considers two settings:

- **Realizable (PAC) setting:** training labels are generated directly from the target function.
- **Agnostic PAC setting:** labels are independently flipped with a fixed probability, introducing noise into the training data.


## Experiments

The notebook contains the following experiments:

### 1. Data Generation

Training datasets are generated for different sample sizes:

$$
m \in \{5, 10, 20, 50, 100, 200\}
$$

At least one generated dataset is visualized.

### 2. ERM Implementation

An ERM algorithm is implemented for threshold classifiers.

### 3. Performance Evaluation

For each training sample size, the following are evaluated:

- **Empirical error:** error of the learned hypothesis on the training data.
- **True error:** error estimated using a large, independently generated test set.

### 4. PAC Verification

The experiment is repeated multiple times for each training sample size.

The probability

$$
P(L(h) > \epsilon)
$$

is estimated to study how the probability of failure changes as the number of training examples increases.

### 5. Agnostic PAC

The same experiments are repeated after introducing label noise.

The results from the realizable and noisy settings are compared to investigate:

- whether the empirical error can still reach zero
- whether more training examples improve generalization
- how label noise affects the learning process

## Main Observations

The experiments show that increasing the training sample size generally decreases the probability that the learned hypothesis has a true error greater than $\epsilon$.

In the realizable setting, the training data is noise-free, allowing ERM to achieve an empirical error of zero.

In the Agnostic PAC setting, label noise makes the learning problem more difficult. The empirical error is not necessarily zero, and the probability of failure is generally higher, particularly for smaller training sets.

However, increasing the amount of training data still improves generalization in both settings.

## Conclusion

Overall, the experiments illustrate the main difference between the PAC and Agnostic PAC settings: **label noise makes learning more difficult, but increasing the amount of training data improves generalization in both cases.**

## Technologies

- Python
- NumPy
- Matplotlib
- Jupyter Notebook

No machine learning libraries such as scikit-learn are used for the learning algorithm.