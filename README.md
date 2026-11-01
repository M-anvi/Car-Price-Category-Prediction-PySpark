# Car Price Category Prediction Using PySpark

## 📌 Project Overview

This project uses **Apache PySpark and Machine Learning** to classify used cars into three price categories: Low, Medium, and High.

The project applies a Decision Tree Classifier using PySpark's MLlib library. It includes data loading, cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and visualization.

The objective is to understand how different vehicle characteristics influence car price categories and build a classification model that predicts the price category of a car.

## 🎯 Objectives

- Load and process car data using PySpark.
- Perform data cleaning and preprocessing.
- Conduct Exploratory Data Analysis (EDA).
- Create Low, Medium, and High price categories.
- Encode categorical features and handle missing values.
- Train a Decision Tree Classification model.
- Evaluate model performance using classification metrics.
- Visualize the results using Python visualization libraries.

## 📂 Dataset

The project uses a CarDekho used-car dataset containing **15,411 records and 14 columns**.

### Dataset Features

| Feature | Description |
|---|---|
| car_name | Name of the car |
| brand | Car manufacturer |
| model | Car model |
| vehicle_age | Age of the vehicle |
| km_driven | Distance driven |
| seller_type | Individual or dealer |
| fuel_type | Fuel category |
| transmission_type | Manual or automatic |
| mileage | Vehicle mileage |
| engine | Engine capacity |
| max_power | Maximum engine power |
| seats | Number of seats |
| selling_price | Actual selling price |


## 🛠️ Technologies Used

- Python
- Apache PySpark 3.5.5
- Spark MLlib
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## ⚙️ Project Workflow

### 1. Environment Setup
- Check Python and Java versions.
- Install the required Python libraries.
- Initialize the Spark session.

### 2. Data Loading and Inspection
- Load the CSV dataset using Spark DataFrame.
- Inspect the dataset schema and dimensions.
- Identify duplicate records and missing values.

### 3. Data Cleaning and Preprocessing
- Remove duplicate records.
- Handle blank and missing values.
- Convert numerical columns into appropriate data types.
- Remove invalid or non-positive selling prices.

### 4. Exploratory Data Analysis (EDA)
- Analyze selling price distribution.
- Explore the number of cars by fuel type.
- Examine descriptive statistics.

### 5. Price Category Creation

The selling price is divided into three categories using approximate percentile boundaries:

- **Low:** Selling price at or below the 33rd percentile.
- **Medium:** Selling price above the 33rd percentile and at or below the 67th percentile.
- **High:** Selling price above the 67th percentile.

### 6. Feature Engineering
- Apply StringIndexer to categorical variables.
- Apply OneHotEncoder for categorical feature encoding.
- Handle missing numerical values using median imputation.
- Assemble the processed features using VectorAssembler.

### 7. Model Training
- Split the dataset into 80% training and 20% testing data.
- Train a Decision Tree Classifier using PySpark MLlib.
- Use a pipeline to combine preprocessing and model training.

### 8. Model Evaluation
The model is evaluated using:
- Accuracy
- Weighted Precision
- Weighted Recall
- Weighted F1-score
A confusion matrix is also generated to examine classification performance.

### 9. Visualization and Results
- Selling price distribution.
- Car count by fuel type.
- Distribution of price categories.
- Confusion matrix.
- Feature importance.
- Actual vs. predicted category comparison.
- Example predictions.


## 📁 Project Structure

```text
Car-Price-Category-Prediction-PySpark/
│
├── data/
│   └── cardekho_dataset.csv
│
├── Car_Price_Category_Prediction_PySpark.ipynb
│
├── Car_Price_Dashboard.xlsx
│
└── README.md
```

## ▶️ How to Run the Project

### Prerequisites

- Python 3.x
- Java Development Kit (JDK)
- Jupyter Notebook
- Apache PySpark

### Install Dependencies

```bash
pip install pyspark==3.5.5 pandas numpy matplotlib seaborn
```

### Run the Notebook

1. Clone or download this repository.
2. Ensure the dataset is inside the `data` folder.
3. Open the Jupyter Notebook.
4. Run the notebook cells sequentially.
5. Review the model evaluation results and visualizations.

## 📈 Expected Outcome

The project produces a trained Decision Tree classification model capable of predicting whether a car belongs to the Low, Medium, or High selling-price category based on its vehicle characteristics.

The notebook also provides evaluation metrics, a confusion matrix, feature importance analysis, and visual comparisons of actual and predicted categories.

## 👩‍💻 Author

**Manvi**

B.Tech – Computer Science and Engineering

GitHub: [M-anvi](https://github.com/M-anvi)
