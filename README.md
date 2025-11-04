# 🛍️ Mall Customer Segmentation Data Cleaning & Analysis Project

[![Python](https://img.shields.io/badge/python-3.8+-green.svg)](https://www.python.org/downloads/)
[![Excel](https://img.shields.io/badge/Excel-2016%2B-blue?logo=microsoft-excel&logoColor=white)
](https://excel.cloud.microsoft/en-gb/)
[![Pandas](https://img.shields.io/badge/pandas-1.5.0+-green.svg)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()

> A comprehensive data cleaning and preprocessing project demonstrating professional data wrangling techniques on mall customer dataset.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Steps to Convert Raw CSV Data into Columns in Excel](#-steps-to-convert-raw-csv-data-into-columns-in-excel)
- [Project Objectives](#-project-objectives)
- [Technologies Used](#-technologies-used)
- [Installation](#-installation)
- [Data Cleaning Workflow](#-data-cleaning-workflow)
- [Results & Insights](#-results--insights)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Project Overview

This project demonstrates a complete data cleaning and preprocessing pipeline for a mall customer dataset. The project showcases industry-standard practices for handling real-world data quality issues including missing values, duplicates, data type inconsistencies, and outliers.

### What This Project Does:
- ✅ Cleans raw customer data with multiple quality issues
- ✅ Handles missing values using appropriate imputation strategies
- ✅ Corrects invalid and inconsistent data entries
- ✅ Standardizes column names and data formats
- ✅ Performs comprehensive distribution analysis
- ✅ Generates professional visualizations
- ✅ Creates detailed data quality reports

---

## 📊 Dataset Description

### Original Dataset
- **Source**: Mall Customer Raw Data
- **Records**: 200 customer entries
- **Features**: 8 columns
- **Format**: CSV file

### Columns:
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| CustomerID | Integer | Unique customer identifier |
| Gender | String | Customer gender (Male/Female) |
| Age | Integer | Customer age in years |
| Annual Income (k$) | Float | Annual income in thousands of dollars |
| Spending Score (1-100) | Integer | Customer spending score (1-100 scale) |
| Membership Type | String | Membership tier (Gold/Silver/Bronze) |
| Email | String | Customer email address |
| Phone Number | String | Customer phone number |

### Data Quality Issues Identified:
- ❌ 3 missing age values (NULL/NA strings)
- ❌ 4 negative age values (-28, -19, -45, -67)
- ❌ 3 extreme age values (150, 250 years)
- ❌ 17 missing membership types
- ❌ 19 missing email addresses
- ❌ 20 missing phone numbers
- ❌ Inconsistent column naming
- ❌ Mixed data types

---

## 📂 Steps to Convert Raw CSV Data into Columns in Excel

Before starting the Python-based data cleaning, you may need to convert raw CSV data into properly formatted columns in Excel. Follow these steps:

### Step 1: Copy the Raw CSV Data
Copy the entire text containing comma-separated records from your source.

### Step 2: Open Excel & Paste Data
1. Open a new Excel workbook
2. Paste the data into the first column (Column A)

### Step 3: Select the Entire Data
Press `Ctrl + A` to select all data in the worksheet.

### Step 4: Use Text to Columns
Use either method:
- Navigate to `Data` → `Text to Columns`
- Press keyboard shortcut `ALT + A + E`

### Step 5: Choose Conversion Type
1. Select **✅ Delimited**
2. Click **Next**

### Step 6: Choose the Delimiters
1. Check the following delimiters:
   - ✅ **Comma**
   - ✅ **Tab** (if applicable)
2. Preview the data in the bottom pane
3. Click **Next**

### Step 7: Select Data Format
1. Choose **✅ General** (recommended for most cases)
2. Click **Finish**

### Step 8: Validate Column Separation
Your data should now be split into individual columns such as:
- CustomerID
- Gender
- Age
- Annual Income
- Spending Score
- Membership Type
- Email
- Phone Number

### Step 9: Clean Data (Optional but Recommended)
After column separation, perform data quality checks:
- ✔️ Handle missing values
- ✔️ Correct invalid age values (e.g., negative / unrealistic ages)
- ✔️ Standardize phone numbers & emails
- ✔️ Validate membership types

### Step 10: Save the File
Save the cleaned data file in Excel format:
1. Go to `File` → `Save As`
2. Choose `.xlsx` format
3. Name your file appropriately

### 📊 Example Output

**Before Conversion:**
```
CustomerID,Gender,Age,Annual Income,Spending Score,Membership Type
1001,Male,25,50000,75,Gold
1002,Female,30,60000,82,Platinum
```

**After Conversion:**
| CustomerID | Gender | Age | Annual Income | Spending Score | Membership Type |
|------------|--------|-----|---------------|----------------|-----------------|
| 1001       | Male   | 25  | 50000         | 75             | Gold            |
| 1002       | Female | 30  | 60000         | 82             | Platinum        |

---

## 🎯 Project Objectives

### Primary Goals:
1. **Data Quality Improvement**: Transform raw, messy data into clean, analysis-ready format
2. **Missing Value Treatment**: Apply appropriate strategies for handling missing data
3. **Data Standardization**: Ensure consistency across all data fields
4. **Outlier Detection**: Identify and handle anomalous data points
5. **Distribution Analysis**: Understand the statistical properties of numeric variables
6. **Visualization**: Create informative plots to communicate data insights

### Learning Outcomes:
- Master pandas for data manipulation
- Implement data validation rules
- Apply statistical methods for data analysis
- Create professional visualizations
- Document data cleaning workflows

---

## 💻 Technologies Used

### Core Libraries:
- **Python 3.8+**: Primary programming language
- **Pandas 1.5.0+**: Data manipulation and analysis
- **NumPy 1.23.0+**: Numerical computing
- **Matplotlib 3.6.0+**: Data visualization
- **Seaborn 0.12.0+**: Statistical visualization
- **SciPy 1.9.0+**: Statistical functions

### Development Tools:
- Jupyter Notebook / Python IDE
- Git for version control
- GitHub for collaboration

---

## 🚀 Installation

### Prerequisites:
- Python 3.8 or higher
- pip package manager

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/mall-customer-data-cleaning.git
cd mall-customer-data-cleaning
```

### Step 2: Create Virtual Environment (Optional but Recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Verify Installation
```bash
python -c "import pandas; import numpy; import matplotlib; print('All packages installed successfully!')"
```

---

## 🔧 Data Cleaning Workflow

### **Step 1: Import Necessary Libraries**

The first step involves importing all required Python libraries for data manipulation, analysis, and processing. Key libraries include:

- **pandas**: For data manipulation and analysis
- **numpy**: For numerical operations and handling missing values
- **warnings**: To suppress unnecessary warning messages during execution

This foundational step ensures all tools are available for the subsequent cleaning operations.

---

### **Step 2: Data Exploratory Analysis**

Initial data exploration helps understand the structure, content, and quality of the raw dataset. This step involves:

- **Loading the dataset** from the CSV file
- **Inspecting dataset dimensions** (rows and columns)
- **Viewing column names** and their current format
- **Checking data types** for each column
- **Displaying sample rows** to understand data structure
- **Generating summary statistics** for numerical columns
- **Identifying obvious data quality issues** at first glance

**Key Findings:**
- Dataset contains 200 customer records
- 8 columns with mixed data types
- Several columns have naming inconsistencies
- Presence of NULL values as text strings
- Negative and unrealistic age values detected

---

### **Step 3: Check Missing Values**

Comprehensive assessment of missing data across all columns to determine the extent of data quality issues.

**Activities:**
- Count null values in each column using appropriate methods
- Calculate percentage of missing data per column
- Identify empty strings that aren't detected as null values
- Check for text representations of null ('NULL', 'NA')
- Create a summary report of missing data patterns

**Missing Values Identified:**
- **Age Column**: 3 NULL text values + outliers
- **Email Column**: 19 missing entries
- **Phone Number Column**: 20 missing entries  
- **Membership Type**: 17 missing/empty values
- **Annual Income**: 1 NULL value

---

### **Step 4: Standardize Column Names**

Transform inconsistent column headers into a clean, uniform naming convention.

**Standardization Rules Applied:**
- Convert all column names to lowercase
- Replace spaces with underscores (snake_case format)
- Remove special characters (parentheses, dollar signs)
- Ensure names are descriptive and programming-friendly

**Transformations:**
- `CustomerID` → `customer_id`
- `Annual Income (k$)` → `annual_income_k`
- `Spending Score (1-100)` → `spending_score`
- `Membership Type` → `membership_type`
- `Phone Number` → `phone_number`

**Result**: Clean, consistent column names following best practices for data analysis and programming.

---

### **Step 5: Clean Age Column**

Address multiple data quality issues in the Age column, which is critical for customer segmentation analysis.

**Issues Identified:**
- Text null values ('NULL', 'NA') instead of numeric nulls
- Negative ages (e.g., -28, -19, -45, -67, -33)
- Unrealistic ages (e.g., 150, 250)
- Mixed data types (numeric and text)

**Cleaning Actions:**
1. Replace text nulls ('NULL', 'NA') with actual NaN values
2. Convert column to numeric data type
3. Identify negative age values
4. Identify unrealistic ages (greater than 120 years)
5. Replace all invalid ages with NaN
6. Calculate median age from valid values
7. Fill all missing ages with the median value
8. Convert final column to integer type

**Outcome**: All age values are now realistic, numeric, and within valid range (18-72 years).

---

### **Step 6: Clean Annual Income**

Ensure the Annual Income column contains only valid numeric values suitable for analysis.

**Cleaning Process:**
1. Check for NULL text values or empty strings
2. Convert column to numeric data type using safe conversion
3. Identify any missing or invalid income values
4. Calculate median income from valid entries
5. Fill missing values with median income
6. Convert to integer type for consistency
7. Validate income range is realistic

**Result**: Annual Income column now contains clean numeric data with no missing values, ranging from 15k to 140k.

---

### **Step 7: Standardize Gender**

Ensure consistent formatting of gender values across all records.

**Standardization Process:**
1. Remove leading and trailing whitespace
2. Standardize capitalization to Title Case
3. Map any abbreviations to full words (M → Male, F → Female)
4. Verify only valid gender values exist
5. Check for any unusual or invalid entries

**Final Format**: All gender values are standardized as 'Male' or 'Female' with proper capitalization.

---

### **Step 8: Clean Membership Type**

Handle missing membership classifications and standardize existing values.

**Cleaning Actions:**
1. Identify empty strings and replace with NaN
2. Check for text nulls ('NULL', '', ' ')
3. Determine the most common membership type (mode)
4. Fill missing values with mode or 'Unknown' placeholder
5. Standardize text format (Title Case)
6. Trim whitespace from all entries
7. Verify valid membership categories (Gold, Silver, Bronze)

**Result**: All customers now have a valid membership type designation with consistent formatting.

---

### **Step 9: Clean Email Column**

Address missing email addresses while maintaining data integrity.

**Processing Steps:**
1. Identify completely missing email values
2. Check for empty strings masquerading as valid data
3. Replace empty strings with NaN for consistency
4. Convert all emails to lowercase for standardization
5. Trim whitespace from email addresses
6. Fill missing emails with placeholder: 'not_provided@unknown.com'
7. Validate email format consistency

**Outcome**: Email column is clean with standardized format and no missing values.

---

### **Step 10: Clean Phone Number Column**

Standardize phone number format and handle missing values appropriately.

**Cleaning Process:**
1. Detect missing phone numbers (null and empty strings)
2. Replace empty strings with NaN
3. Trim whitespace from existing phone numbers
4. Fill missing values with placeholder: '000-0000'
5. Ensure consistent format across all entries
6. Validate phone number patterns

**Result**: Phone numbers are standardized with placeholders for missing data.

---

### **Step 11: Check for Duplicates**

Identify and remove any duplicate customer records to ensure data integrity.

**Duplicate Detection Process:**
1. Check for exact duplicate rows across all columns
2. Identify duplicate Customer IDs
3. Review duplicate records if found
4. Remove duplicates keeping the first occurrence
5. Report number of duplicates removed
6. Verify unique customer count

**Finding**: No duplicate records detected in the dataset. Data integrity confirmed.

---

### **Step 12: Validate Data Types**

Ensure all columns have appropriate data types for analysis and modeling.

**Type Validation:**
1. **customer_id**: Convert to integer (unique identifier)
2. **gender**: Keep as object/string (categorical)
3. **age**: Convert to integer (numeric)
4. **annual_income_k**: Convert to integer (numeric)
5. **spending_score**: Convert to integer (numeric)
6. **membership_type**: Keep as object/string (categorical)
7. **email**: Keep as object/string (text)
8. **phone_number**: Keep as object/string (text)

**Final Data Type Summary:**
- Integer columns: customer_id, age, annual_income_k, spending_score
- Object (string) columns: gender, membership_type, email, phone_number

**Verification**: All data types are now appropriate for their intended use in analysis.

---

### **Step 13: Final Quality Check**

Comprehensive validation to ensure all cleaning operations were successful.

**Quality Assurance Checks:**

1. **Missing Values Audit**
   - Confirm zero missing values remain
   - Verify all NaN values have been handled
   - Check for empty strings in text columns

2. **Data Range Validation**
   - Age: 18-72 years (realistic range)
   - Annual Income: 15k-140k (reasonable range)
   - Spending Score: 1-100 (within defined scale)

3. **Categorical Value Review**
   - Gender: Only 'Male' and 'Female'
   - Membership: Gold, Silver, Bronze (standardized)

4. **Statistical Summary**
   - Generate descriptive statistics
   - Review distribution of values
   - Identify any remaining outliers

5. **Record Count Verification**
   - Confirm 200 records maintained
   - Verify no data loss during cleaning

6. **Display Sample Data**
   - Show first 10 cleaned records
   - Verify formatting and values look correct

**Quality Metrics:**
- ✅ Zero missing values
- ✅ Zero duplicates
- ✅ All outliers handled
- ✅ Consistent data types
- ✅ Standardized text formats
- ✅ Valid data ranges

---

### **Step 14: Save Cleaned Data**

Export the cleaned dataset in multiple formats for future use.

**Export Operations:**
1. **CSV Format**: Save as `mall_customer_cleaned.csv`
   - Standard format for data analysis
   - Compatible with all analysis tools
   - Preserves data structure

2. **Excel Format** (Optional): Save as `mall_customer_cleaned.xlsx`
   - User-friendly format for business users
   - Supports formatting and formulas
   - Easy to share and review

3. **Generate Cleaning Report**: Create `data_cleaning_summary.txt`
   - Documents all cleaning actions
   - Lists issues found and resolved
   - Provides before/after statistics
   - Includes quality metrics

**Files Created:**
- ✅ `mall_customer_cleaned.csv` - Clean dataset for analysis
- ✅ `data_cleaning_summary.txt` - Detailed cleaning report
- ✅ (Optional) `mall_customer_cleaned.xlsx` - Excel version

---

## 📊 Results & Insights

### Data Quality Improvements

| Metric | Before Cleaning | After Cleaning | Improvement |
|--------|----------------|----------------|-------------|
| Missing Values | 60 (7.5%) | 0 (0%) | ✅ 100% |
| Invalid Ages | 10 | 0 | ✅ 100% |
| Duplicate Records | 0 | 0 | ✅ Maintained |
| Standardized Columns | 0% | 100% | ✅ Complete |

### Key Statistics (Cleaned Data)

- **Total Customers**: 200
- **Age Range**: 18-72 years
- **Income Range**: $15,000 - $140,000
- **Average Spending Score**: 50.2
- **Gender Distribution**: 112 Female, 88 Male
- **Membership Types**: Gold (40%), Silver (35%), Bronze (25%)

---

## 🚀 Use Cases

Once your data is properly cleaned, you can:

- ✔️ Perform customer segmentation analysis
- ✔️ Build predictive models for spending behavior
- ✔️ Create interactive dashboards in Power BI/Tableau
- ✔️ Generate targeted marketing campaigns
- ✔️ Conduct statistical analysis and hypothesis testing
- ✔️ Develop machine learning models

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improving this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## 📄 License

This project is available under the MIT License. Feel free to use and share.

---

## 👤 Author

Created to help data analysts, business professionals, and students master data cleaning techniques.

---

## 🌟 Acknowledgments

Special thanks to the data science community for continuous support and feedback.

---

**Happy Data Cleaning! 📈**

If you found this project helpful, please ⭐ star this repository!
