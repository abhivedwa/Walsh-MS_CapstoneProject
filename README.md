# Walsh MS Capstone Project

## Project Overview
This repository contains the MS Capstone project work focused on financial data analysis and machine learning modeling. The project appears to analyze stock market data, particularly focusing on quarterly results, price movements, and sector-specific analysis.

## Project Structure

### 📁 Root Directory
- **`data/`** - Contains raw and processed data files
- **`images/`** - Generated visualizations and charts organized by analysis cells
- **`reports/`** - Interim and final project reports
- **`src/`** - Source code and notebooks organized by functionality

### 📊 Data Directory (`data/`)
```
data/
├── raw/                                    # Original raw data files
│   └── MS_Capstone_Final_Raw_Dump.xlsx
└── raw_processed/                          # Cleaned and processed data
    └── MS_Capstone_Final_Clean.xlsx
```

### 🖼️ Images Directory (`images/`)
Organized by analysis cells (cell_5 through cell_11), containing:
- **Correlation analysis** (Pearson, Spearman, mutual information)
- **Sector-specific analysis** (Auto, FMCG, IT/Technology, Pharma, BFSI)
- **Statistical visualizations** (box plots, scatter plots, heatmaps)
- **Outlier analysis** and summary tables
- **Seasonal and quarterly analysis** charts

### 📋 Reports (`reports/`)
- **`QM 640 Interim Report_old.docx`** - Previous interim report
- **`QM 640 Interim Report-Abhi Vedwa .pdf`** - Current interim report
- **`QM 640 Interim Report-Abhi Vedwa Draft V1.docx`** - Draft version

### 🔧 Source Code (`src/`)

#### Data Cleaners & EDA (`src/notebooks/Data_Cleaners_EDA/`)
- **`Data_Quality_Check_Summary.ipynb`** - Data quality assessment notebook -- used in Report
- **`EDA_Draft_code.ipynb`** - Draft exploratory data analysis WIP
- **`EDA_Master.ipynb`** - Master EDA notebook -- used in Report
- **`images/`** - Organized visualizations by analysis cells

#### Data Extractors (`src/notebooks/Data_Extractors/`)
- **`getQuaterlyPriceData.ipynb`** - Quarterly price data extraction
- **`getQuaterlyResults.ipynb`** - Quarterly results data extraction
- **`Merge_Price_Results.ipynb`** - Data merging operations
- **`Price_data_AV_API.ipynb`** - API-based price data extraction

#### Models (`src/notebooks/Models/`)

##### Final Models (`src/notebooks/Models/Final Models/`)
- **`Optimised_Models.ipynb`** - Optimized machine learning models
- **`RQ3.ipynb`** - Old one Research Question 3 analysis -  Refer Sector Specific MPA
- **`Sector Specific MPA.ipynb`** - Sector-specific model performance analysis
- **`images/`** - Model performance visualizations
- **`rq3_analysis_results/`** - RQ3 specific analysis outputs
- **`rq3_outputs/`** - RQ3 model outputs

##### Other Model Work (`src/notebooks/Models/Other Model Work/`)
- **`Final_BaseLine_Models.ipynb`** - Baseline model implementations
- **`LR.ipynb`** - Logistic regression specific work

## Analysis Structure

The project is organized into analysis "cells" (cell_5 through cell_11), each focusing on specific aspects:

- **Cell 5**: Correlation analysis, collinearity assessment, feature selection
- **Cell 6**: Seasonal analysis, quarterly patterns, fiscal quarter returns
- **Cell 7**: Sector-specific correlations, financial margin analysis
- **Cell 8**: Outlier detection, distribution analysis, influential observations
- **Cell 9**: Sector-specific fundamental analysis, movement patterns
- **Cell 10**: Capitalization analysis, sector ranking, correlation vs. return analysis
- **Cell 11**: Skewness analysis, distribution characteristics

## Key Features

- **Comprehensive EDA**: Extensive exploratory data analysis across multiple dimensions
- **Sector Analysis**: Deep dive into specific sectors (Auto, FMCG, IT, Pharma, BFSI)
- **Machine Learning Models**: Multiple model implementations with optimization
- **Statistical Analysis**: Correlation analysis, outlier detection, seasonal patterns
- **Data Quality**: Systematic data quality assessment and cleaning procedures

## Technologies Used

- **Python**: Primary programming language
- **Jupyter Notebooks**: Interactive analysis and documentation
- **Pandas/NumPy**: Data manipulation and analysis
- **Matplotlib/Seaborn**: Data visualization
- **Scikit-learn**: Machine learning models
- **XGBoost**: Advanced gradient boosting models

## Getting Started

1. Navigate to the appropriate notebook in `src/notebooks/`
2. Ensure all dependencies are installed
3. Start with the EDA notebooks for understanding the data
4. Review the model notebooks for implementation details

## Project Status

This appears to be an active MS Capstone project with ongoing development and analysis. The structure suggests a comprehensive approach to financial data analysis with both exploratory and predictive modeling components.

---

*Last Updated: 24-08-2025*
*Project Lead: Abhi Vedwa*
*Course: WAlsh MS Capstone*
    

