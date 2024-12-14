 # Disease Predictor Using Machine Learning

## Overview
This project implements a disease prediction system using machine learning algorithms such as Decision Tree, Random Forest, and Naive Bayes. It is a GUI-based Python application that predicts diseases based on symptoms selected by the user. The system uses a dataset of diseases and their associated symptoms to train models and evaluate their performance.

## Features
- **Graphical User Interface (GUI):** A user-friendly interface built using the Tkinter library.
- **Symptom Selection:** Dropdown menus allow the user to select up to five symptoms.
- **Machine Learning Models:** Includes Decision Tree, Random Forest, and Naive Bayes for disease prediction.
- **Accuracy Display:** Prints the model accuracy on the test dataset in the console.
- **Predicted Disease Output:** Displays the predicted disease for the selected symptoms.

---

## Prerequisites
- Python 3.x
- Libraries:
  - `tkinter`
  - `numpy`
  - `pandas`
  - `sklearn`

---

## Dataset
The application uses two datasets:
1. **Training Dataset (`Training.csv`):** Contains symptoms and their associated diseases for training the machine learning models.
2. **Testing Dataset (`Testing.csv`):** Used to evaluate the model's accuracy.

The `prognosis` column in both datasets contains disease labels that are mapped to numerical values for model training and testing.

---

## Code Explanation

### Libraries and Data Preparation
The code starts by importing necessary libraries such as `numpy`, `pandas`, and machine learning modules from `sklearn`. It reads and processes the `Training.csv` and `Testing.csv` datasets, converting disease labels to numerical values using `replace()`.

### Symptoms and Diseases
A list of symptoms (`l1`) and diseases (`disease`) is predefined. The symptom list is used for creating dropdown menus, while the disease list is used to display prediction results.

### Machine Learning Models
#### Decision Tree
- A `DecisionTreeClassifier` is trained on the `Training.csv` dataset.
- Accuracy is calculated and printed using `accuracy_score` from `sklearn`.
- Predictions are displayed in the GUI.

#### Random Forest
- A `RandomForestClassifier` is trained similarly to the Decision Tree.
- The same prediction process is followed, with results displayed in the GUI.

#### Naive Bayes
- A `GaussianNB` classifier is trained.
- Follows the same accuracy calculation and prediction process as the other models.

### GUI Implementation
The GUI is created using Tkinter:
- **Labels and Input Fields:**
  - Fields for the patient’s name and symptom selection.
- **Buttons:**
  - Buttons to run each of the three models.
- **Output Fields:**
  - Text fields to display predicted disease for each model.

---

## Instructions to Run
1. **Install Required Libraries:**
   ```bash
   pip install numpy pandas scikit-learn
   ```
2. **Prepare the Dataset:**
   Ensure `Training.csv` and `Testing.csv` are in the same directory as the code.

3. **Run the Application:**
   Execute the Python script.
   ```bash
   python disease_predictor.py
   ```

4. **Use the GUI:**
   - Enter the patient's name.
   - Select up to five symptoms from the dropdown menus.
   - Click on a model button (Decision Tree, Random Forest, or Naive Bayes) to predict the disease.
   - The predicted disease will be displayed in the corresponding output field.

---

## Output
### Console Output
- Displays accuracy and the number of correct predictions for each model:
  ```
  0.95
  95
  ```
### GUI Output
- Predicted disease based on the selected symptoms.

---

## Files
- **`disease_predictor.py`**: The main Python script.
- **`Training.csv`**: Training dataset with symptoms and diseases.
- **`Testing.csv`**: Testing dataset for evaluation.

---

## Future Improvements
- Add more symptoms and diseases to the dataset.
- Implement advanced models like Neural Networks.
- Enhance the GUI for a better user experience.
- Allow users to input symptoms as free text and match them intelligently.

---

## Project By
**Shaheer Waseem**

