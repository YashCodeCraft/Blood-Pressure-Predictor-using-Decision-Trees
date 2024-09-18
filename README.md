# Blood Pressure Predictor using Decision Trees

This project implements a decision tree classifier to predict Blood Pressure based on patient characteristics such as age, sex, cholesterol levels, and sodium-to-potassium ratio. The dataset contains patient data, and the classifier uses a decision tree model to classify blood pressure levels.

## Dataset

The dataset used in this project is in CSV format (`drug200.csv`). It includes the following columns:
- `Age`: The patient's age.
- `Sex`: The patient's gender (M or F).
- `BP`: The patient's blood pressure level (High, Low, or Normal).
- `Cholesterol`: The patient's cholesterol level (High or Normal).
- `Na_to_K`: The sodium-to-potassium ratio in the patient's blood.
- `Drug`: The drug prescribed.

## Requirements

To install the required dependencies, run:

```bash
pip install -r requirements.txt
```

## Instructions
1. Place the dataset (drug200.csv) in the appropriate directory.
2. Run the script, and it will train a decision tree classifier based on the data.
3. The model predicts the blood pressure (BP) of patients, and the performance metrics like accuracy and confusion matrix will be displayed.
   
## How It Works
1. Data Preprocessing: Categorical data such as Sex, BP, Cholesterol, and Drug are label-encoded into numerical values.
2. Model Training: The dataset is split into training and testing sets. A decision tree model is trained on the training data.
3. Hyperparameter Tuning: Grid search is used to optimize the model parameters (`criterion`, `max_depth`, `max_leaf_nodes`).
4. Evaluation: The trained model is evaluated using accuracy scores, classification reports, and confusion matrices.
5. Visualization: The project includes a visualization of the decision tree and correlation heatmaps.

## Model
The Decision Tree model is built with the following configuration:

- `criterion`: Gini or Entropy
- `max_depth`: Ranges from 1 to 6
- `max_leaf_nodes`: Ranges from 1 to 6
The model is fine-tuned using grid search to find the optimal hyperparameters for better accuracy.

## Usage
To make predictions using the trained model:

```python
model.predict([[40, 1, 0, 16, 1]])  # Example input (Age, Sex, Cholesterol, Na_to_K, Drug)
```
This will output the predicted blood pressure category (0-low, 1-Normal, 2-High)

## Output
- The model outputs a confusion matrix, classification report, and the accuracy score of the predictions.
- It also visualizes the decision tree structure, showing how the model makes predictions based on patient data.
  
## Future Improvements
- Experiment with other classifiers like Random Forest or SVM to compare performance.
- Enhance data preprocessing by handling missing values and outliers.
- Apply more feature engineering techniques to improve model accuracy.
  
## Conclusion
This project demonstrates how a decision tree classifier can be used for drug prediction based on patient characteristics. The model provides useful insights into the factors influencing drug prescriptions and offers opportunities for further exploration in medical data classification.

