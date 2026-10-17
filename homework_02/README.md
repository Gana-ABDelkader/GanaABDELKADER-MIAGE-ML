# HW2 — Uniform Convergence and the Limits of Learning

## Overview

This homework explores the relationship between sample size, hypothesis class complexity, and generalization through probabilistic simulations.

The experiments focus on three main concepts:

- **Uniform Convergence:** The relationship between empirical risk and true risk.
- **No-Free-Lunch Principle:** The limitations of learning arbitrary target functions.
- **Inductive Bias:** How prior knowledge can improve generalization.

## Contents

The homework is organized into three parts.

### Part I — Simulating Uniform Convergence

This part studies how empirical risk behaves as the sample size increases and how the size of the hypothesis class affects uniform convergence.


### Part II — Simulating No-Free-Lunch

This part considers randomly generated target functions over a finite input domain.

The results illustrate that when target labels are completely random, observing training examples provides no information about the labels of unseen inputs.

### Part III — Introducing Prior Knowledge

This part introduces structured target functions defined by thresholds.

The results show how a suitable inductive bias can help a learner generalize beyond the observed examples.

## Technologies

- Python
- NumPy
- Matplotlib
- Jupyter Notebook

## Main Conclusions

The experiments illustrate that increasing the sample size generally improves the accuracy of empirical risk estimates and reduces generalization error. Larger hypothesis classes make uniform convergence more difficult, while theoretical bounds provide sufficient guarantees that can be conservative.

The No-Free-Lunch experiments demonstrate the limitations of learning completely random target functions. In contrast, when the target belongs to a structured family such as threshold functions, a matching hypothesis class allows ERM to exploit prior knowledge and generalize more effectively.

## Deliverable

The main deliverable is a Jupyter Notebook (`.ipynb`) containing the simulation code, visualizations, comparisons with theoretical results, and interpretations of the experiments.
