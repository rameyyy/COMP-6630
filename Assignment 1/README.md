# Assignment 1 - COMP 5630/6630
## Introduction to Machine Learning

---

## Question 1 [20 points]

Suppose that you are conducting a scientific experiment where you are observing the effects of one variable (`x_train.npy` and `x_test.npy`) on the output (`y_train.npy` and `y_test.npy`). On visualizing the relationship between the variables, you see a plot.

### Objective

Your goal is to come up with a **linear regression model** that can take the training data (`x_train.npy` and `y_train.npy`) and model the relationship between the variables x and y.

**Important:** You should implement your own version of linear regression either using:
- Gradient descent, OR
- Normal equations

> You **SHOULD NOT** use any pre-packaged library such as Sci-Kit Learn.

### Guidelines

1. Try to plot this relationship on your own using matplotlib. You can also visualize the test data to see if it gives you any clues about the underlying relationship between the variables.

2. Use your knowledge gleaned from the previous step to answer the following question:
   - What are some functions that you can try to map the relation between x and y? Plot each of them individually to verify!

### Deliverables

You will need to write a short report detailing:
- Your thought process
- The code you wrote in Python to implement the linear regression model
- The equation that models the relationship between x and y that you found
- Evidence that corroborates your final statement (plots, prediction errors, etc.)

---

## Question 2 [20 points]

Imagine that you are a realtor in Auburn. You have data points (see Excel file - last column is the target variable) that correspond to the recent sales of different houses in and around Auburn.

### Objective

Your goal is to help estimate the prices of houses that one can use to sell or buy listings. Use your knowledge of linear regression to find the best regression model.

**Use your implementation from Question 1 (without any basis functions) to answer the following questions:**

1. What is the average least squares error for the given data using your simple linear regression model?

2. Which factor has the **most effect** on the final value? How do you know this? Can you use only this feature to predict the price?

3. Which factor has the **least effect** on the final value? How do you know this? What effect does removing this feature have on the performance?

---

## Submission Requirements

Submit the following as a **single IPYNB file**:

1. Use the "text cells" on Colab to write your report
2. Include a cell with **README instructions** at the top of your notebook to note any dependencies required to run your code

---

## Important Notes

1. **Code Execution:** If your code does not run on Colab, you will not get any credit for the code segment. We will only grade what is in your report.
   - This includes any syntax errors due to indentation, unnamed/unknown libraries that were not listed in the README file, etc.

2. **Python Only:** Please submit code only in Python and in the IPython notebook format. You can write your answers as part of the notebook if you do not want a separate report file, but it must be comprehensive.
   - Any code not in Python will not be graded at all.

3. **GenAI Declaration:** Please declare any use of GenAI usage. Your points will not be deducted for declaration. But if the TA or instructor discovers GenAI usage and you don't declare, then your points will be deducted.
