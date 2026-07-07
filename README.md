# Medical Insurance Cost Prediction

A machine learning project that predicts medical insurance costs using a **Linear Regression** model.  
The project includes exploratory data analysis, data preprocessing, model training, prediction testing, and regression model evaluation.

## Project Overview

The goal of this project is to predict the `charges` column in the insurance dataset based on customer information such as:

- Age
- Sex
- BMI
- Number of children
- Smoking status
- Region

The project focuses on building an interpretable baseline model using Linear Regression and evaluating its performance using regression metrics.

## Dataset

The dataset used in this project is `insurance.csv`.

### Features

| Column | Description |
|---|---|
| `age` | Age of the insurance beneficiary |
| `sex` | Gender of the beneficiary |
| `bmi` | Body Mass Index |
| `children` | Number of children covered by insurance |
| `smoker` | Smoking status |
| `region` | Residential region |
| `charges` | Medical insurance cost |

## Project Workflow

1. Import required libraries.
2. Load the insurance dataset.
3. Perform exploratory data analysis.
4. Check missing values and duplicate rows.
5. Visualize the distribution of medical charges.
6. Analyze relationships between features and the target.
7. Encode categorical variables using `LabelEncoder`.
8. Split the data into training and testing sets.
9. Train a Linear Regression model.
10. Test the model using predictions.
11. Evaluate the model using regression metrics.

## Exploratory Data Analysis

The notebook includes several visualizations:

- Medical charges distribution
- Box plots for categorical features
- Pairplot for numerical relationships
- Correlation heatmap
- Prediction vs. actual values
- Residual distribution

The visualizations were styled with a consistent purple theme to improve presentation quality.

## Model

The model used is:

```text
Linear Regression
```

### Train/Test Split

```text
Training data: 80%
Testing data: 20%
Random state: 42
```

## Model Performance

The final model achieved the following results:

| Metric | Value |
|---|---:|
| MAE | 4,182.35 |
| MSE | 35,493,102.61 |
| RMSE | 5,957.61 |
| R² | 0.8068 |

### Interpretation

The model explains approximately **80.68%** of the variation in medical insurance charges.

The MAE indicates that predictions differ from actual charges by around **4,182** on average.  
The RMSE is higher than the MAE, which means the model still has some larger prediction errors, especially for high-cost medical cases.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook

## Repository Structure

```text
medical-insurance-cost-prediction/
│
├── data/
│   └── insurance.csv
│
├── notebook/
│   └── Medical_Insurance_Prediction_Styled_80_20.ipynb
│
├── README.md
├── requirements.txt
└── LICENSE
```

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/your-username/medical-insurance-cost-prediction.git
```

2. Navigate to the project folder:

```bash
cd medical-insurance-cost-prediction
```

3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook
```

5. Run all cells in the notebook.

## Key Insights

- Smoking status is the strongest predictor of medical insurance charges.
- Age and BMI have a positive relationship with charges.
- Some high-cost observations are difficult for a simple Linear Regression model to predict.
- Linear Regression provides a strong and interpretable baseline model.

## Future Improvements

- Use one-hot encoding for nominal categorical features such as `region`.
- Apply a logarithmic transformation to the skewed `charges` target.
- Add interaction features such as `bmi x smoker`.
- Compare Linear Regression with more advanced models such as Random Forest and Gradient Boosting.
- Use cross-validation for more reliable performance estimation.

## Author

**Samer Gharbi**

Data Science | Data Analysis | Machine Learning
