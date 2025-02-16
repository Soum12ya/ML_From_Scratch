### Linear Regression using Gradient Descent

Overview

This project implements Linear Regression using Batch Gradient Descent, Stochastic Gradient Descent (SGD), and Mini-Batch Gradient Descent without using libraries like scikit-learn, TensorFlow, or PyTorch. The dataset is normalized before training, and different learning rates are tested to observe their effects on the cost function.

## Dataset Description

The dataset consists of two files:

1. linearX.csv (Independent/Predictor Variable)

2. linearY.csv (Dependent/Response Variable)

These datasets are concatenated into a single DataFrame with columns X and Y.

### Steps Performed

## 1. Data Preprocessing
The X values are normalized using standardization. The Y values are also normalized.

## 2. Implementing Linear Regression using Gradient Descent

Initialized parameters (m = 0, b = 0). Used Batch Gradient Descent to optimize parameters. Set learning rate to 0.5 and ran for 50 iterations. Tracked cost function values and parameter updates. Convergence Criteria: Cost function stabilization (minimal change between iterations).

## 3. Advantage of Averaging the Cost Function

Averaging the cost function ensures that the cost per data point is accounted for, preventing large-scale variations and ensuring stable gradient updates.

## 4. Plotting Cost Function vs Iterations

The cost function values for the first 50 iterations were plotted to observe the rate of convergence.

## 5. Plotting Dataset and Regression Line

The dataset points were visualized along with the regression line obtained from training.

## 6. Testing Different Learning Rates

Learning rates tested: 0.005, 0.5, 5.

Plotted cost function vs iterations for each learning rate.

## Observations:

lr = 0.005: Slow convergence.

lr = 0.5: Optimal balance between speed and stability.

lr = 5: Divergence due to large updates.

## 7. Implementing Stochastic and Mini-Batch Gradient Descent

Stochastic Gradient Descent (SGD):

Updates parameters per sample, leading to noisy but fast convergence.

Observed fluctuations in the cost function plot.

Mini-Batch Gradient Descent (to be implemented if needed):

Uses small subsets of data for each update, balancing efficiency and stability.

Comparison with Batch Gradient Descent:

Batch GD showed smoother convergence.

SGD converged faster but was less stable.
