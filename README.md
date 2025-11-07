# Real Estate Price Prediction Project

## Overview

This project focuses on predicting real estate prices using machine learning techniques. The goal is to build an accurate regression model that can estimate property prices based on various features such as location, property characteristics, and market conditions. The project demonstrates a complete machine learning pipeline from data preprocessing to model deployment.

## Key Features

- **Comprehensive Data Analysis**: Exploratory data analysis to understand relationships between variables
- **Advanced Feature Engineering**: Creation of meaningful features from raw data
- **Multiple Model Comparison**: Evaluation of various regression algorithms
- **Hyperparameter Tuning**: Optimization using GridSearchCV for best performance
- **Robust Model Selection**: XGBoost Regressor chosen for its outlier resistance

## Technologies Used

### Programming & Data Analysis
- **Python 3.8+**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization

### Machine Learning Libraries
- **Scikit-learn** - Machine learning algorithms and utilities
- **XGBoost** - Gradient boosting framework
- **Category Encoders** - Encoding categorical variables

### Model Development
- **Scikit-learn** - For traditional ML models (Linear Regression, Random Forest, etc.)
- **XGBoost** - For advanced gradient boosting
- **Joblib** - Model serialization and persistence

## Key Learning Points

### Feature Engineering Applied
- **Temporal Features**: Extraction of time-based patterns from date columns
- **Geospatial Features**: Creation of location-based aggregations and clusters
- **Polynomial Features**: Generation of interaction terms between important variables
- **Binning**: Transformation of continuous variables into categorical ranges
- **Domain-Specific Features**: Creation of property-specific metrics like price per square foot
- **Missing Value Imputation**: Advanced strategies for handling NaN values

### Feature Selection
- **Correlation Analysis**: Identification of highly correlated features for removal
- **Recursive Feature Elimination (RFE)**: Systematic elimination of least important features
- **Feature Importance**: Using tree-based models to rank feature relevance
- **Variance Threshold**: Removal of low-variance features
- **Domain Knowledge**: Manual selection based on real estate expertise

### Model Choice Rationale
The project evaluated multiple algorithms:
- **Linear Regression** - Baseline model
- **Random Forest Regressor** - For handling non-linear relationships
- **Gradient Boosting Regressor** - For sequential improvement
- **XGBoost Regressor** - **Selected as final model** due to:
  - Superior handling of outliers
  - Built-in regularization to prevent overfitting
  - Ability to capture complex patterns
  - Consistent performance across validation sets

### Hyperparameter Tuning with GridSearch
- **Systematic Search**: Exhaustive parameter combination testing
- **Cross-Validation**: 5-fold cross-validation to ensure robustness
- **Key Parameters Tuned**:
  - Learning rate and number of estimators
  - Tree depth and minimum child weight
  - Subsample and column sample ratios
  - Regularization parameters (L1, L2)
- **Performance Metrics**: Optimized for RMSE and R² scores

### XGBoost's Outlier Handling
XGBoost Regressor demonstrated exceptional performance in controlling outlier influence through:
- **Gradient-based Learning**: Less sensitive to extreme values
- **Tree Splitting Criteria**: Focuses on overall distribution patterns
- **Regularization**: Penalizes complex trees that might overfit to outliers
- **Robust Loss Functions**: Options like Huber loss for outlier resistance

## Results
The final XGBoost model achieved:
- **R² Score**: 0.90 on test data
- **RMSE**: $45,200
- **Mean Absolute Error**: $32,100

The model demonstrates strong predictive power while effectively handling the challenges of real estate data, including outliers and complex feature interactions.

## Future Improvements
- Integration of external data sources (economic indicators, school ratings)
- Implementation of deep learning models
- Development of ensemble methods

## Installation & Usage
```bash
# Clone repository
git clone https://github.com/iKebb/Ironhack-Project03_IronKaggle.git

# Run training pipeline
python src/main.ipynb
```

## Contributors
- [Keberth José Rodríguez Albino]
- [Rafael Rocha, Natasha Silvestre]

## License
This project is licensed under the MIT License - see the LICENSE file for details.