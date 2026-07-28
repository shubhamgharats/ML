# Placement Prediction using Logistic Regression

## Overview
This notebook builds a **Logistic Regression** model to predict whether a student gets placed based on two features:
- **CGPA**
- **IQ**

---

## Workflow

### 1. Import Libraries
Import the required Python libraries such as:
- pandas
- numpy
- matplotlib
- scikit-learn

---

### 2. Load the Dataset
Read the `placement.csv` file into a Pandas DataFrame and inspect the data.

```python
df = pd.read_csv("placement.csv")
```

---

### 3. Data Preprocessing
- Remove the unnecessary index column.
- Select the required features.

**Input Features (X):**
- CGPA
- IQ

**Target (y):**
- Placement (0 or 1)

---

### 4. Visualize the Data
Create a scatter plot to understand how the data points are distributed.

This helps us see whether the classes can be separated.

---

### 5. Split the Dataset
Split the data into:
- **Training Set (90%)**
- **Testing Set (10%)**

This allows us to evaluate the model on unseen data.

---

### 6. Feature Scaling
Standardize the input features using `StandardScaler`.

Feature scaling helps Logistic Regression perform better because all features are brought to the same scale.

---

### 7. Train the Model
Create and train the Logistic Regression model.

```python
clf = LogisticRegression()
clf.fit(X_train, Y_train)
```

---

### 8. Make Predictions
Use the trained model to predict placement on the test dataset.

```python
Y_pred = clf.predict(X_test)
```

---

### 9. Evaluate the Model
Calculate the model's accuracy.

```python
accuracy_score(Y_test, Y_pred)
```

A higher accuracy indicates better prediction performance.

---

### 10. Visualize the Decision Boundary
Use `plot_decision_regions()` to visualize how Logistic Regression separates the two classes.

---

### 11. Save the Model
Save the trained model using Pickle so it can be reused later without retraining.

```python
pickle.dump(clf, open("model.pkl", "wb"))
```

---

## Files Used

- `placement.csv` – Dataset
- `model.pkl` – Saved trained model

---

## Libraries Used

- pandas
- numpy
- matplotlib
- scikit-learn
- mlxtend
- pickle

---

## Outcome

A Logistic Regression model is trained to predict student placement based on **CGPA** and **IQ**, evaluated using accuracy, visualized with a decision boundary, and saved for future use.