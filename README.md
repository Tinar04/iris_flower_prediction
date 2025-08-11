# Iris Flower Classification using Logistic Regression 🌸

This project demonstrates a complete machine learning pipeline for classifying Iris flowers into their respective species using a **Logistic Regression** model. The process involves data preparation, model training, and performance evaluation.

## 💾 Dataset
The dataset used is the **Iris dataset**, a classic machine learning benchmark. It contains 150 samples of Iris flowers from three species: `setosa`, `versicolor`, and `virginica`. Each sample has four features: `sepal length`, `sepal width`, `petal length`, and `petal width`.

-   **Features**: `sepal length (cm)`, `sepal width (cm)`, `petal length (cm)`, `petal width (cm)`
-   **Target**: `setosa` (0), `versicolor` (1), `virginica` (2)

## 🛠️ Process

1.  **Data Preparation and Exploration**:
    -   The `load_iris` function from scikit-learn is used to load the dataset.
    -   A pandas DataFrame is created to organize the features and the target variable, and its first few rows are displayed.
    -   The dataset is confirmed to have **no missing values**.
    -   The DataFrame has a shape of `(150, 5)`, with 150 samples and 5 columns (4 features + 1 target).
    -   The target column is perfectly balanced, with **50 samples** for each of the three species.

2.  **Data Splitting**:
    -   The data is split into features (`X`) and the target (`y`).
    -   The data is further divided into a **training set** and a **testing set** using `train_test_split`.
    -   **20%** of the data is reserved for testing the model's performance on unseen data.

3.  **Model Training**:
    -   A **Logistic Regression** model is initialized with `max_iter` set to 1000 to ensure convergence.
    -   The model is trained (`fit`) on the training data (`X_train` and `y_train`). The model converged in **93 iterations**.

4.  **Prediction and Evaluation**:
    -   The trained model makes predictions on the `X_test` data.
    -   The predicted labels are compared to the actual labels to evaluate performance.
    -   A **test accuracy score of 1.0 (100%)** is achieved, indicating the model perfectly classified all 30 flowers in the test set.
    -   **Cross-validation** with `cv=5` is performed to get a more robust estimate of the model's performance. The scores range from **0.933 to 1.0**, confirming the model's reliability.

5.  **Custom Prediction**:
    -   The model is used to predict the species of a new, unseen flower with specific measurements (`[5.1, 3.5, 1.4, 0.2]`).
    -   The model correctly predicts the species as **'setosa'**.

## ✅ Outcome

The **Logistic Regression** model proved to be highly effective for this classification task. It achieved perfect accuracy on the test set and demonstrated consistent performance through cross-validation. The model is capable of accurately classifying new Iris flowers based on their sepal and petal dimensions.
