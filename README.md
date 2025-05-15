
# Logistic Regression Classifier

This repository contains a simple implementation of Logistic Regression using Python and the `scikit-learn` library. The classifier is trained and tested on a dataset of social network ads to predict user purchase behavior based on age and estimated salary.

## Dataset

The dataset used is `Social_Network_Ads.csv`, which should be placed in the same directory as the code. It includes the following columns:

- Age
- Estimated Salary
- Purchased (Target Variable)

## Requirements

- Python 3.x
- NumPy
- pandas
- Matplotlib
- scikit-learn

Install the required packages with:

```bash
pip install numpy pandas matplotlib scikit-learn
```

## Steps

### 1. Importing Libraries

The code begins by importing necessary libraries: NumPy, pandas, Matplotlib, and scikit-learn.

### 2. Loading the Dataset

```python
dataset = pd.read_csv('Social_Network_Ads.csv')
X = dataset.iloc[:, :-1].values
y = dataset.iloc[:, -1].values
```

### 3. Splitting the Dataset

Split into training and test sets using an 75-25 ratio.

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, random_state=0)
```

### 4. Feature Scaling

Standardize features using `StandardScaler`.

### 5. Training the Model

Train a `LogisticRegression` model using the training set.

### 6. Evaluating the Model

- Predict the test set results
- Compute and print the confusion matrix and accuracy

### 7. Visualizing the Results

- Plot decision boundary and data points for training set
- Plot decision boundary and data points for test set

## Output

- Confusion matrix and accuracy score printed to the console.
- Visualizations for both training and test set classifications.

![Image](https://github.com/user-attachments/assets/53352fb4-3475-4889-87d0-c92c6aed4419)

![Image](https://github.com/user-attachments/assets/b5ab8843-a3a3-4691-ae3b-5c990e86d2e7)

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! If you'd like to improve this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

Please make sure your code follows the existing style and includes appropriate documentation and tests.
