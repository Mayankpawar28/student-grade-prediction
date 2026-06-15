# Student Grade Prediction

A simple machine learning project that predicts a student's final percentage and corresponding grade based on their attendance, assignment marks, mid-term marks, and end-semester marks, using Linear Regression.

## Overview

This project uses historical student performance data to train a Linear Regression model. Given a student's attendance percentage and marks from assignments, mid-terms, and end-semester exams, the model predicts their likely final percentage and maps it to a grade.

## Features

- Predicts final percentage using Linear Regression
- Converts predicted percentage into a letter grade (O, A+, A, B+, B, C, P, F)
- Simple command-line interface for entering new student data
- Trained and evaluated using an 80/20 train-test split

## Tech Stack

- Python 3
- Pandas
- Scikit-learn

## Dataset

The model is trained on `student_data.csv`, which should contain the following columns:

| Column            | Description                          |
|-------------------|---------------------------------------|
| Attendance        | Student's attendance percentage       |
| Assignment        | Assignment marks                      |
| MidTerm           | Mid-term exam marks                   |
| EndSem            | End-semester exam marks               |
| FinalPercentage   | Final overall percentage (target)     |

## Grading Scale

| Percentage Range | Grade |
|-------------------|-------|
| >= 90             | O     |
| 80 - 89           | A+    |
| 70 - 79           | A     |
| 60 - 69           | B+    |
| 50 - 59           | B     |
| 40 - 49           | C     |
| 30 - 39           | P     |
| < 30              | F     |

## How It Works

1. Load the dataset from `student_data.csv`
2. Select `Attendance`, `Assignment`, `MidTerm`, and `EndSem` as input features (X) and `FinalPercentage` as the target (y)
3. Split the data into training (80%) and testing (20%) sets
4. Train a Linear Regression model on the training data
5. Take new input values from the user and predict the final percentage
6. Map the predicted percentage to a corresponding grade

## Installation

```bash
git clone <your-repo-url>
cd <repo-folder>
pip install pandas scikit-learn
```

## Usage

1. Place your `student_data.csv` file in the project directory
2. Run the notebook or script:
   ```bash
   jupyter notebook Grade_Prediction.ipynb
   ```
3. When prompted, enter:
   - Attendance
   - Assignment Marks
   - Mid-Term Marks
   - End-Sem Marks
4. The model will output the predicted percentage and grade

## Future Improvements

- Add model evaluation metrics (R² score, MAE, RMSE)
- Try other regression models (Random Forest, XGBoost) and compare performance
- Add data visualization for feature importance and correlations
- Build a simple web interface using Flask/Streamlit
- Add input validation for user-entered marks

## License

This project is open source and available under the MIT License.
