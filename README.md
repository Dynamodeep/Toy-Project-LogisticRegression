# 🎓 Placement Prediction using Machine Learning

A machine learning project that predicts whether a student is likely to get placed based on their **CGPA and IQ score** using Logistic Regression.

## Project Overview

This project uses supervised machine learning to classify students into two categories: placed or not placed. It uses academic performance (CGPA) and IQ scores as input features to train a Logistic Regression model.

The project demonstrates the complete machine learning workflow, from data preprocessing and exploratory data analysis to model training, evaluation, and saving the trained model.

## 🎯 Objectives

- Analyze the relationship between CGPA, IQ, and student placement.
- Visualize the dataset using a scatter plot.
- Preprocess the data using feature scaling.
- Train a Logistic Regression classification model.
- Evaluate the model using accuracy score.
- Visualize the decision boundaries.
- Save the trained model using Pickle.

## 🛠️ Technologies Used

- **Python** — Programming language
- **NumPy** — Numerical computing
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Scikit-learn** — Machine learning and preprocessing
- **MLxtend** — Decision region visualization
- **Pickle** — Model serialization

## 📂 Project Structure

```text
Placement-Prediction/
│
├── placement.csv       # Dataset
├── placement.ipynb     # Jupyter Notebook
├── model.pkl           # Trained Logistic Regression model
└── README.md           # Project documentation
```

*Note: Adjust the filenames above to match your actual repository.*

## 📊 Dataset Description

The project uses a CSV dataset named `placement.csv`.

| Feature | Description |
|---|---|
| CGPA | Student's cumulative grade point average |
| IQ | Student's IQ score |
| Placement | Target variable indicating placement status |

The dataset may contain an additional unnamed index column, which is removed during preprocessing.

## ⚙️ Workflow

1. **Data Loading:** Import the dataset using Pandas.
2. **Data Cleaning:** Remove the unnecessary unnamed column.
3. **Exploratory Data Analysis:** Visualize CGPA and IQ against placement status.
4. **Feature Selection:** Select CGPA and IQ as input features and Placement as the target.
5. **Train-Test Split:** Split the dataset into training and testing sets using a 90:10 ratio.
6. **Feature Scaling:** Apply StandardScaler to standardize the input features.
7. **Model Training:** Train a Logistic Regression classifier.
8. **Model Evaluation:** Evaluate predictions using accuracy score.
9. **Decision Boundary Visualization:** Plot the decision regions using MLxtend.
10. **Model Saving:** Export the trained model as `model.pkl` using Pickle.

## 🧠 Machine Learning Algorithm

**Logistic Regression**

Logistic Regression is a supervised machine learning algorithm used for classification problems. In this project, it predicts a student's placement category based on CGPA and IQ.

The model learns patterns from the training data and uses them to classify unseen student records.

## 📈 Model Evaluation

The model is evaluated using **Accuracy Score**, which measures the proportion of correct predictions.

\[
\text{Accuracy}=\frac{\text{Correct Predictions}}{\text{Total Predictions}}
\]

The actual accuracy depends on the dataset and training-test split. The measured accuracy can be added here after running the notebook.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Dynamodeep/Placement-Prediction.git
cd Placement-Prediction
```

Replace the repository URL and folder name if your GitHub repository uses a different name.

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn mlxtend jupyter
```

### 3. Run the notebook

```bash
jupyter notebook
```

Open the notebook and execute the cells in order.

### 4. Dataset path

If you are running the notebook locally, update the dataset path:

```python
df = pd.read_csv("placement.csv")
```

This assumes that `placement.csv` is in the same directory as the notebook.

## 💾 Saving the Model

The trained model is saved using Pickle:

```python
import pickle

with open("model.pkl", "wb") as file:
    pickle.dump(model, file)
```

**Important:** The model uses standardized input features. To make predictions on new student data correctly, save and reuse the fitted `StandardScaler` along with the model.

## 🔮 Future Improvements

- Save the scaler along with the trained model.
- Build a simple web application using Flask or Streamlit.
- Allow users to enter CGPA and IQ to obtain predictions.
- Evaluate the model using a confusion matrix, precision, recall, and F1-score.
- Use stratified train-test splitting and a fixed random state for reproducibility.
- Compare Logistic Regression with other classification algorithms.
- Test the model on additional student datasets.

## ⚠️ Disclaimer

This project is intended for educational purposes. Predictions are based on the features and patterns present in the dataset and should not be treated as definitive judgments about a student's employability.

## 👨‍💻 Author

**Deepanshu Bhatt**

- GitHub: [@Dynamodeep](https://github.com/Dynamodeep)

---

⭐ If you find this project useful, consider giving the repository a star!
