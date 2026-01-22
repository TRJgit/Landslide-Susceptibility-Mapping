# Landslide Susceptibility Mapping

A project that implements machine learning models to predict landslide susceptibility based on geographical features. It uses Random Forest and XGBoost classifiers to analyze spatial data and identify areas prone to landslides.

## Project Structure

-   **Data Processing & Analysis:**
    -   `Preparing_Data.ipynb`: Preprocesses raw data, merges landslide and non-landslide datasets, handles missing values, and normalizes features.
    -   `Analysing_Data.ipynb`: Performs Exploratory Data Analysis (EDA) to understand feature distributions and correlations.

-   **Modeling:**
    -   `RF.ipynb`: Implements a Random Forest Classifier with hyperparameter tuning using GridSearchCV. Includes model evaluation metrics like ROC-AUC and Confusion Matrix.
    -   `XGBoost.ipynb`: Implements an XGBoost Classifier for improved predictive performance, also evaluating with standard classification metrics.

-   **Data:**
    -   `Data/`: Contains the datasets used in the project.
        -   `Landslide.csv` / `No_Landslide.csv`: Raw data files.
        -   `Final_Data.csv`: Processed dataset used for model training, containing features: `Slope`, `Elevation`, `Corina` (Land Cover), and `Target`.
        -   `Normalized_data.csv`: Normalized version of the final dataset.
        -   `Target.csv`: Target variable labels.

## Dependencies

The project requires the following Python libraries:

-   `pandas`
-   `numpy`
-   `matplotlib`
-   `seaborn`
-   `scikit-learn`
-   `xgboost`

## Usage

1.  **Data Preparation**: Run `Preparing_Data.ipynb` to process raw datasets into a format suitable for training.
2.  **Analysis**: Run `Analysing_Data.ipynb` to visualize data characteristics.
3.  **Model Training**:
    -   Run `RF.ipynb` to train and evaluate the Random Forest model.
    -   Run `XGBoost.ipynb` to train and evaluate the XGBoost model.

## Features

The models predict landslide occurrence based on the following key features:
-   **Slope**: The steepness of the terrain.
-   **Elevation**: Height above sea level.
-   **Corina**: Corine Land Cover classification (e.g., bare rocks, vegetation).

## Results

Both models are evaluated using metrics such as Accuracy, Precision, Recall, F1-Score, and ROC-AUC. Detailed performance reports and confusion matrices are generated within the respective notebooks.