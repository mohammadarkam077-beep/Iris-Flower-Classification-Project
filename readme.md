Running Iris Classification Project in VS Code
📌 Overview

This project can be executed fully in Visual Studio Code using a Python environment.
The code is compatible with both .py scripts and Jupyter Notebooks inside VS Code.

🧰 Prerequisites

Make sure the following are installed on your system:

Python 3.8 or higher

Visual Studio Code

VS Code Extensions:

Python (by Microsoft)

Jupyter (optional but recommended)

📁 Project Files
├── Iris.csv                  # Dataset (optional)
├── iris_classification.py    # Main Python script / Notebook code
├── final_iris_model.pkl      # Saved trained model
├── iris_scaler.pkl           # Saved feature scaler
├── README.md                 # Documentation

⚙️ Step 1: Create & Activate Python Environment (Recommended)
Using Conda
conda create -n iris_env python=3.9
conda activate iris_env

OR Using venv
python -m venv iris_env
iris_env\Scripts\activate   # Windows
source iris_env/bin/activate  # macOS/Linux

📦 Step 2: Install Required Libraries

Run this in VS Code terminal:

pip install numpy pandas matplotlib seaborn scikit-learn joblib

▶️ Step 3: Run the Project
Option A: Run as Python Script
python iris_classification.py

Option B: Run as Jupyter Notebook (Inside VS Code)

Open the .py or .ipynb file

Select Python Interpreter (top-right)

Run cells using ▶️ or Shift + Enter

📊 Outputs Generated

Data visualizations (EDA plots)

Model evaluation metrics

Confusion matrices

Feature importance plot

Saved model files:

final_iris_model.pkl

iris_scaler.pkl

🔍 Model Used

Final Model: Random Forest Classifier

Why: High accuracy, stability, interpretability

🔁 Reusing the Saved Model in VS Code
import joblib
import numpy as np

model = joblib.load("final_iris_model.pkl")
scaler = joblib.load("iris_scaler.pkl")

sample = np.array([[5.1, 3.5, 1.4, 0.2]])
sample_scaled = scaler.transform(sample)
prediction = model.predict(sample_scaled)

print("Predicted Class:", prediction)

❗ Common Issues & Fixes
Issue: ModuleNotFoundError

✔ Solution:

pip install <missing-package>

Issue: Plots not displaying

✔ Solution:

plt.show()

🚀 Optional: Flask Deployment (Advanced)

A basic Flask API snippet is included in the code and can be run as:

python app.py

✅ VS Code Compatibility Status

✔ Fully compatible
✔ Beginner-friendly
✔ Production-ready structure

👤 Author

Md Arkam
M.Pharm | Data Analytics | Machine Learning