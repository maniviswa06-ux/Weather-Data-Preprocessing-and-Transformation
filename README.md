# Weather Data Preprocessing and Transformation

## Project Overview

This project demonstrates the complete data preprocessing and transformation workflow using Python, Pandas, and Scikit-learn.

The project uses environmental weather data to perform data inspection, data cleaning, missing value treatment, data type conversion, and categorical feature encoding.

The main objective is to convert raw, inconsistent environmental data into a clean and machine-learning-ready dataset.

## Objectives

- Understand the structure and characteristics of the dataset.
- Identify and analyze missing values.
- Remove unnecessary columns.
- Handle missing values using appropriate techniques.
- Convert categorical and numerical data into appropriate data types.
- Perform Label Encoding on categorical features.
- Perform One-Hot Encoding to convert categorical variables into numerical features.
- Prepare the dataset for future machine learning applications.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Scikit-learn | Feature encoding |
| Jupyter Notebook | Interactive development |

## Project Workflow

### 1. Data Loading and Understanding
- Imported the required Python libraries.
- Loaded the environmental dataset using Pandas.
- Examined dataset dimensions and column names.
- Inspected data types and statistical summaries.
- Identified unnecessary columns.

### 2. Data Preprocessing

**Missing Value Analysis**

Identified missing values in the following features:

- Ozone
- Solar.R
- Weather

**Handling Missing Values**

- Removed the Ozone column because approximately 24% of its values were missing.
- Used group-wise mean imputation to handle missing Solar.R values based on Weather categories.
- Removed rows containing missing values in the Weather column.

**Data Type Conversion**

- Replaced the text value `May` with `5` in the Month column.
- Converted the Month column into an integer data type.

### 3. Data Transformation

**Label Encoding**

- Used Scikit-learn's LabelEncoder.
- Converted categorical Weather values into numerical labels.
- Created a separate copy of the preprocessed dataset.

**One-Hot Encoding**

- Used Pandas `get_dummies()`.
- Converted the Weather feature into separate binary columns.
- Generated the following encoded features:
  - Weather_C
  - Weather_PS
  - Weather_S

## Dataset Information

- Dataset: Environmental Weather Data
- Initial shape: 158 rows × 10 columns
- Features include Ozone, Solar.R, Wind, Month, Day, Year, Temp, and Weather.
- The dataset contains environmental and weather-related observations.

## Project Structure

```text
Weather-Data-Preprocessing-and-Transformation/
│
├── Data Preprocessing & Transformation.ipynb
├── environmental_data.csv
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation and Execution

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Weather-Data-Preprocessing-and-Transformation.git
```

### Step 2: Navigate to the project folder

```bash
cd Weather-Data-Preprocessing-and-Transformation
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

### Step 5: Open the notebook

Open `Data Preprocessing & Transformation.ipynb` and execute the cells sequentially.

Make sure `environmental_data.csv` is available in the project directory.

## Key Learning Outcomes

- Understanding real-world data quality issues.
- Identifying and treating missing values.
- Applying group-wise mean imputation.
- Performing data type conversion.
- Understanding categorical feature encoding.
- Differentiating Label Encoding and One-Hot Encoding.
- Preparing datasets for machine learning workflows.

## Future Improvements

- Add exploratory data analysis (EDA) with visualizations.
- Compare different missing value imputation techniques.
- Perform outlier detection and treatment.
- Apply feature scaling using StandardScaler, MinMaxScaler, and RobustScaler.
- Build supervised machine learning models using the cleaned dataset.
- Develop a reusable preprocessing pipeline using Scikit-learn.

## Author

**Your Name**

GitHub: https://github.com/YOUR-USERNAME

---

If you find this project useful, feel free to star ⭐ the repository.
