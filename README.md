# Wood Surface Defect Detection

This project focuses on automating wood surface defect detection using computer vision and machine learning techniques. By leveraging bounding box annotations and image data, the goal is to classify and localize defects to improve quality control processes in the wood industry.

## Project Overview

- **Dataset**: The dataset includes 4000 images and corresponding bounding box annotations, reduced to 100 for demonstration purposes.
- **Models Evaluated**:
  - **Random Forest**: Best overall performance with an F1-score of 0.49.
  - **SVC**: Competitive but slightly lower F1-score of 0.48.
  - **Logistic Regression**: Least effective with an F1-score of 0.45.
- **Business Impact**: The Random Forest model shows potential for semi-automated defect detection but requires further improvement in precision and recall for underrepresented defect classes.

## Key Features

1. **Data Preparation**:
   - Resized images to a uniform size of `(224, 224)` for consistency in model training.
   - Adjusted bounding box annotations to match resized image dimensions.
   - Processed images and bounding box data saved for further analysis.

2. **Model Training**:
   - Implemented feature scaling using `StandardScaler`.
   - Used `GridSearchCV` for hyperparameter tuning.
   - Applied stratified cross-validation to ensure balanced splits.

3. **Evaluation Metrics**:
   - Focused on F1-score, precision, and recall for imbalanced datasets.
   - Visualized confusion matrices to analyze model performance on each class.

4. **Recommendations**:
   - Improve data quality by collecting more diverse and balanced data.
   - Deploy a human-in-the-loop system for semi-automated defect detection.
   - Use feedback from production to iteratively improve the model.