# Supervised Learning

Supervised learning involves training a model to predict an output (or target) from given inputs. This method requires labeled data, meaning each input comes with a known output (label). The goal is for the model to learn from these labeled examples, so it can make predictions on new, unseen data.

### Key Concepts

- **Training**: The process of using data to train a model.
    - **x**: Input variable, also known as a feature.
    - **y**: Output variable, also known as the target.
- **m**: The number of training examples.
- **(x, y)**: A single training example.
- **(xⁱ, yⁱ)**: The i-th training example (1st, 2nd, 3rd, etc.). This is not exponentiation.

### Regression

Regression is used when the output is a continuous value, meaning it can take any value within a range, often referred to as an infinitely large set of possible outputs.

The process for regression is as follows:
- **x** → input feature
- **f** → model or function that learns the relationship between x and y
- **ŷ** → the predicted value of y based on the model's function

The model will generate predictions as follows:
\[ \hat{y} = f_{w,b}(x) = wx + b \]
Where:
- **w** and **b** are parameters that influence the prediction of **ŷ** based on **x**.

#### Cost Function

The cost function measures how well the model's predictions match the actual data. It helps adjust the model's parameters (**w** and **b**) to improve prediction accuracy.

- **w**: The slope of the line. It determines how steep the regression line is.
    - The slope is calculated as:
    \[
    w = \frac{y_2 - y_1}{x_2 - x_1}
    \]
    or \(\Delta y / \Delta x\).
- **b**: The bias term, also known as the y-intercept, shifts the regression line up or down.

The goal is to minimize the difference between the predicted values (**ŷ**) and actual values (**y**) by adjusting **w** and **b**.

#### Squared Error Cost Function

The squared error cost function computes the average squared difference between predicted and actual values, serving as a measure of the model's accuracy.

\[
J(w, b) = \frac{1}{2m} \sum_{i=1}^{m} (\hat{y}^{(i)} - y^{(i)})^2
\]

This function helps optimize the model by finding the best parameters (**w** and **b**) that minimize the prediction error.