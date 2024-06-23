# ML_Salary_prediction
Prediction engine to predict data job salaries for Data related jobs

## Project Overview
This project aims to design and implement a prediction engine to predict data job salaries in the United States. The dataset used for this project is sourced from Kaggle and contains detailed information on various data job roles, including job titles, salaries, experience levels, locations, and more.

## Dataset
- **Source**: Kaggle
- **Link**: [Data Jobs Salaries](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries)
- **Contents**: The dataset includes job titles, salaries, experience levels, locations, and other relevant details.

## Project Steps

### 1. Data Acquisition
The dataset was acquired from Kaggle and contains information on data job roles in the United States.

### 2. Data Understanding and Cleaning
- **Observations**:
  - 11 columns, 15965 rows.
  - Three numeric columns: `work_year`, `salary_in_usd`, `remote_ratio`, `salary`.
  - Six categorical columns: `experience_level`, `employment_type`, `job_title`, `employee_residence`, `company_location`, `company_size`, `salary_currency`.
  - No null values.
  - Dropped duplicate rows and unnecessary salary columns.

### 3. Data Analysis
- Analyzed categorical columns to understand their distributions and relationships.
- Analyzed numerical columns to understand their statistical properties.

### 4. Handling Outliers and Inconsistencies
- Used boxplots to detect outliers.
- Calculated upper and lower bounds using the Interquartile Range (IQR) method.
- Set thresholds and removed outliers accordingly.

### 5. Feature Engineering
- **Encoding**: Encoded categorical features using appropriate techniques.
- **Feature Selection**: Selected relevant features for model training.
- **Scaling and Splitting**: Scaled the dataset and split it into training and test sets.

### 6. Model Selection, Training, and Evaluation

#### Linear Regression Model
- **R_Score**: 0.25 (25% accuracy)
- **Mean Squared Error (MSE)**: 2813280687.593782

#### Linear Regression Model – Visualization
- **Coefficient**: [22277.45939177 -297.48595147 2243.82203775 -1997.98687361 10264.38174577 14126.97736321]
- **Intercept**: 139811.22298095864

#### L2 (Lasso) Regression / Cross-Validation (K-Fold) / Hyperparameter Tuning
- **R_Score**: 0.25
- **MSE**: 2652750059.0700665

#### Other Models Tested: Decision Tree Regressor, Random Forest, Gradient Boosting
- **R_Score**: 0.37 (38% accuracy)
- **MSE**: 2339850754.1546235

### 7. Result Summary
- Improvement in model accuracy and reduction in MSE with different techniques and models.

### 8. Conclusion
- The models show moderate accuracy.
- Further improvements are necessary for better performance.

### 9. Areas of Improvement
- Explore more feature engineering techniques (e.g., Rare Encoder).
- Test other models that perform well with categorical data.
- Enhance data cleaning and feature transformation.
- Aim to increase accuracy and reduce MSE.

## Usage

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/predicting-data-job-salaries.git
   cd predicting-data-job-salaries
   ```

2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

3. Run the project:
   ```sh
   python main.py
   ```

## Repository Structure
```
predicting-data-job-salaries/
│
├── data/
│   ├── raw/                 # Raw data files
│   └── processed/           # Processed data files
│
├── notebooks/               # Jupyter notebooks for data exploration and analysis
│
├── src/
│   ├── data_preprocessing.py # Scripts for data cleaning and preprocessing
│   ├── feature_engineering.py # Scripts for feature engineering
│   ├── model_training.py     # Scripts for model training and evaluation
│
├── requirements.txt         # List of dependencies
├── README.md                # Project overview and instructions
└── main.py                  # Main script to run the project
```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or suggestions.

## License
This project is licensed under the MIT License.

## Acknowledgements
- Kaggle for providing the dataset.
- Open-source libraries used in this project.

---

Feel free to customize the above sections as per your project details and preferences. This README file provides a comprehensive overview of your project, including its purpose, steps taken, usage instructions, and more.
