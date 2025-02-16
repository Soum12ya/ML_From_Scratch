# Linear Regression using Gradient Descent

Overview

This project implements Linear Regression using Batch Gradient Descent, Stochastic Gradient Descent (SGD), and Mini-Batch Gradient Descent without using libraries like scikit-learn, TensorFlow, or PyTorch. The dataset is normalized before training, and different learning rates are tested to observe their effects on the cost function.

### Dataset Description

The dataset consists of two files:

1. linearX.csv (Independent/Predictor Variable)

2. linearY.csv (Dependent/Response Variable)

These datasets are concatenated into a single DataFrame with columns X and Y.

### Steps Performed -
1. Data Preprocessing
2. Implementing Linear Regression using Gradient Descent
3. Advantage of Averaging the Cost Function
4. Plotting Cost Function vs Iterations
5. Plotting Dataset and Regression Line
6. Testing Different Learning Rates

## Questions

#### 1. Use linear regression to fit a straight line to the given database. Set your learning rate to 0.5. What are the cost function value and learning parameters values after convergence? Also, mention the convergence criteria you used.
#### ans : 
After convergence the cost function value is 0.2781 and value of m is 0.6620 and b is 0.0000 (after 50 iteration)
<img width="278" alt="cost" src="https://github.com/user-attachments/assets/ded174f8-5459-48ed-bcc3-c15f3867c64f" />
The convergence criteria used in the code is the stabilization of the cost function.

#### 2. The cost function that we are using in this assignment is different than the one we used in class. Can you think of the advantage of averaging the cost?
#### ans : Advantages of Averaging the Cost Function -
Averaging the cost function provides several benefits in linear regression:

1. Stabilizes Gradient Updates :-
     When using batch gradient descent, averaging the cost function ensures that each update step is more stable and not dominated by extreme values. This helps prevent 
     sudden fluctuations in parameter updates, leading to smoother convergence.

2. Better Convergence Behavior :-
     Without averaging, the cost function values could become excessively large, especially when the dataset is large. Averaging prevents large gradients, making the 
     optimization process more controlled and reducing the chances of divergence.

3. Ensures Scale Independence :-
     If we did not average, the cost function would scale with the dataset size. By averaging, we make the cost function independent of the number of data points, ensuring 
     that it remains comparable across datasets of different sizes.

4. Improves Numerical Stability :-
     When working with large datasets, summing the squared error terms directly can result in numerical instability. Averaging helps in keeping the computed values within a 
     reasonable range, reducing the risk of overflow or underflow.

5. Consistency Across Different Optimization Methods :-
     Whether using batch gradient descent, stochastic gradient descent, or mini-batch gradient descent, averaging the cost function ensures consistent learning behavior 
     across different optimization techniques.

#### 3. Plot cost function v/s iteration graph for the model in question 1 for first 50 iterations.
#### ans : 
![cost_vs_iterations](https://github.com/user-attachments/assets/fbb78a09-0248-4ca2-bd86-49bf75be5990)


#### 4. Plot the given dataset on a graph and also print the straight line you obtained in question 1 to show how it fits the data.
#### ans : 
![Linear Regression Fit](https://github.com/user-attachments/assets/aaf48fba-396c-48b7-900c-22f645cea2af)


