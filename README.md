# SGD Mechanics and Attention Context Assigment1
This repository contains my submission for the Module 4 assignment.  
The assignment is divided into two parts:

- **Part A:** Manual computation of Stochastic Gradient Descent (SGD)
- **Part B:** Contextual word representations using self-attention

The goal of this assignment is to understand the core learning mechanisms behind neural networks, rather than model performance.

---

## File

- `m4s2assignment1.py`  
  Main Python file containing both Part A and Part B implementations. (was originally implemented in Colab)

---

## Part A: Manual Stochastic Gradient Descent (SGD)

### Objective

The objective of Part A is to demonstrate an understanding of how a neural network learns by updating its parameters using **Stochastic Gradient Descent**.

Instead of using machine learning libraries, the gradient and weight updates are computed explicitly.

---

### Model

A simple linear model with a single parameter is used:

\[
\hat{y} = x \cdot w
\]

This model allows the learning process to be observed step by step.

---

### Dataset

- Insurance dataset
- Only the **first three samples** are used, as required by the assignment

---

### Learning Procedure

For each of the first three samples, the following steps are performed:

1. **Forward pass**  
   Compute the prediction using the current weight.

2. **Loss computation**  
   Use squared error loss to measure prediction error.

3. **Gradient computation**  
   Compute the gradient of the loss with respect to the weight.

4. **Weight update (SGD)**  
   Update the weight immediately after each sample using the learning rate.

This update-after-each-sample behavior is what characterizes *Stochastic* Gradient Descent.

---

### Manual Computation and Verification

- The first sample is computed **manually** to demonstrate understanding of each step.
- The remaining steps are **verified with code** by printing intermediate values inside the training loop.
- The printed outputs match the manually computed table, confirming correctness.

---

### Key Observation

- A large gradient results in a large weight update.
- As the model learns, gradients become smaller and updates decrease.
- The learning rate controls how strongly gradients affect the weight updates.

---

## Part B: Attention and Contextual Word Representations

### Objective

The objective of Part B is to demonstrate that **word meaning depends on context**, and that self-attention can produce context-aware representations.

---

### Setup

- A homonym (**“seal”**) is used with two different meanings:
  - Animal (swimming in the ocean)
  - Action (sealing an envelope)
- Simple 2D word embeddings are assigned for clarity and visualization.

---

### Self-Attention

Self-attention is applied with:

- Queries = Keys = Values

This allows each word to incorporate information from other words in the sentence.

---

### Evaluation

- Euclidean distance is measured between the word “seal” and contextually related words.
- Distances are compared **before** and **after** applying self-attention.

---

### Key Observation

- Before attention, embeddings are static and less informative.
- After attention, embeddings move closer to contextually relevant words.
- This demonstrates how attention creates **context-dependent representations**, which is a core idea behind transformer-based models.

---

## Summary

- **Part A** illustrates how neural networks learn through gradients and parameter updates.
- **Part B** illustrates how attention mechanisms encode contextual meaning.
- Together, these parts reflect the two main themes of Module 4:
  - Optimization
  - Representation learning

---

## Notes

- Plots included in the code are for visualization purposes only and are not required by the assignment.
- The focus of this work is on understanding learning mechanics rather than achieving optimal performance.
