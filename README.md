# Landslide Susceptibility Mapping using Machine Learning

This project focuses on predicting landslide susceptibility by analyzing various geospatial and environmental factors. By leveraging machine learning models, specifically XGBoost and Random Forest, this study aims to identify areas prone to landslides, which can be crucial for disaster management and land-use planning.

## Table of Contents

- Project Objective

- Dataset

- Methodology

    - Data Preparation and Preprocessing

    - Exploratory Data Analysis (EDA)

    - Model Training and Evaluation

- Results

- How to Reproduce the Results

- Technologies Used

## Project Objective

The primary goal of this project is to develop a robust model for landslide susceptibility mapping. This involves:

  - Identifying and preparing key factors that contribute to landslides.
  - Analyzing the relationships between these factors and landslide occurrences.
  - Training and evaluating machine learning models to accurately predict landslide-prone areas.

## Dataset

The dataset used for this analysis is a combination of landslide and non-landslide data points, each associated with a set of environmental and geographical attributes. The key features in the dataset include:

  - **Slope:** The steepness of the terrain.
  - **Curvature:** The rate of change of slope.
  - **Aspect:** The direction the slope faces.
  - **Elevation:** The altitude of the location.
  - **Land Use:** The type of land cover (e.g., forest, agricultural, urban).
  - **Geology:** The underlying rock and soil type.
  - **NDVI (Normalized Difference Vegetation Index):** A measure of vegetation density.
  - **Rainfall:** The amount of precipitation in the area.
  - **Distance to River:** The proximity to a river.
  - **Distance to Road:** The proximity to a road.
  - **Distance to Fault:** The proximity to a geological fault line.

The data is organized into several CSV files located in the `Data/` directory, including `Landslide.csv`, `No_Landslide.csv`, and the combined `Final_Data.csv`.

## Methodology

The project follows a systematic approach, divided into three main stages:

### 1\. Data Preparation and Preprocessing

This stage, detailed in the `Preparing_Data.ipynb` notebook, involves:

  - **Loading and Merging:** Reading the `Landslide.csv` and `No_Landslide.csv` datasets.
  - **Data Cleaning:** Handling any missing or inconsistent data.
  - **Feature Engineering:** Creating a binary `Target` variable (1 for landslide, 0 for no landslide).
  - **Data Normalization:** Scaling the features to a common range to ensure that no single feature dominates the model training process.

### 2\. Exploratory Data Analysis (EDA)

The `Analysing_Data.ipynb` notebook covers the EDA phase, which includes:

  - **Statistical Summary:** Generating descriptive statistics for each feature.
  - **Data Visualization:** Creating various plots like histograms, box plots, and correlation matrices to understand the distribution of the data and the relationships between different features.
  - **Feature Importance:** Analyzing which factors have the most significant impact on landslide occurrences.

### 3\. Model Training and Evaluation

The core of the machine learning implementation is in the `XGB-RF.ipynb` notebook. The steps include:

  - **Data Splitting:** Dividing the dataset into training and testing sets.
  - **Model Selection:** Choosing two powerful ensemble models:
      - **XGBoost (Extreme Gradient Boosting):** A decision-tree-based ensemble Machine Learning algorithm that uses a gradient boosting framework.
      - **Random Forest:** An ensemble learning method for classification that operates by constructing a multitude of decision trees at training time.
  - **Model Training:** Training both models on the prepared training data.
  - **Performance Evaluation:** Assessing the models' performance using various metrics, such as:
      - Accuracy
      - Precision
      - Recall
      - F1-Score
      - ROC Curve and AUC Score
      - Confusion Matrix

## Results

The machine learning models, particularly XGBoost and Random Forest, demonstrated high accuracy in predicting landslide susceptibility. The key findings from the analysis highlight the significant influence of factors like slope, rainfall, and geology on the likelihood of a landslide. The model evaluation metrics provide a quantitative measure of the models' effectiveness, showcasing their potential for real-world application in risk assessment.

## How to Reproduce the Results

To run this project and reproduce the results, follow these steps:

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/landslide-susceptibility-mapping.git
    cd landslide-susceptibility-mapping
    ```
2.  **Install the required dependencies:**
    ```sh
    pip install pandas numpy scikit-learn matplotlib seaborn jupyter xgboost
    ```
3.  **Run the Jupyter Notebooks:**
      - Start with `Preparing_Data.ipynb` to process the raw data.
      - Then, run `Analysing_Data.ipynb` for exploratory data analysis.
      - Finally, execute `XGB-RF.ipynb` to train and evaluate the machine learning models.

## Technologies Used

  - **Python:** The core programming language used for the project.
  - **Jupyter Notebook:** For interactive data analysis and modeling.
  - **Pandas:** For data manipulation and analysis.
  - **NumPy:** For numerical operations.
  - **Matplotlib & Seaborn:** For data visualization.
  - **Scikit-learn:** For machine learning tasks like data splitting, model training, and evaluation.
  - **XGBoost:** For implementing the XGBoost algorithm.