🍄 Mushroom Edibility Classification
📌 Overview

This project applies machine learning techniques to classify mushrooms as edible or poisonous, providing data-driven guidance for vegetarian foragers. Using the mushroom_cleaned dataset from Kaggle, we explore feature importance and predictive performance across multiple models to identify key traits associated with safe mushroom consumption.

Our goal is to create a reliable, interpretable, and scientifically grounded tool that supports safer mushroom foraging decisions.

📊 Dataset

Source: Kaggle - Mushroom Cleaned Dataset

Observations: 54,035 mushrooms

Features: 9 mushroom characteristics (cap diameter, cap shape, gill attachment, gill color, season, stem height, stem width, stem color)

Target Variable: class → 0 = Poisonous, 1 = Edible

🔍 Methodology
Data Preprocessing

Log transformation for skewed variables (stem_height, stem_width)

Dropped original skewed variables after transformation

Train-validation split (70% / 30%) with stratification

No missing values detected

Models Used

Decision Tree Classifier

Random Forest Classifier

Logistic Regression

Neural Network (MLPClassifier)

📈 Model Comparison
Model	Accuracy	ASE	Top Features	Notes
Random Forest	99.06%	0.009973	Log Stem Width, Gill Attachment, Stem Color, Cap Diameter, Log Stem Height	Best overall performance, robust results
Decision Tree	97.67%	Low	Gill Color, Stem Color, Season	Highly interpretable, good accuracy
Neural Network	74.07%	0.176319	Not directly interpretable	Captures complex patterns
Logistic Regression	62.92%	0.221959	Log Stem Height, Season, Log Stem Width	Useful for feature directionality
🌟 Key Insights for Foragers

Stem Width: Consistently the strongest predictor of edibility.

Gill Attachment & Color: Strongly associated with safe mushrooms.

Stem Color: Standard stem colors (white, cream, brown) are safer indicators.

Cap Shape: Rounded/convex caps often linked with edible mushrooms.

Seasonality: Certain seasons have higher correlation with edibility.

⚠️ Disclaimer

While these models provide scientifically grounded guidance, mushroom foraging carries inherent risks. Always cross-reference findings with expert field guides and, when possible, consult mycologists before consumption.

📂 Project Structure
mushroom-edibility-classification/
│
├── data/
│   └── mushroom_cleaned.csv
│
├── notebooks/
│   └── Mushroom_Classification.ipynb
│
├── src/
│   └── preprocessing.py
│   └── models.py
│
├── results/
│   ├── model_comparison.png
│   ├── feature_importance.png
│
├── README.md
└── requirements.txt

⚙️ Installation & Usage
# Clone the repository
git clone https://github.com/yourusername/mushroom-edibility-classification.git
cd mushroom-edibility-classification

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook notebooks/Mushroom_Classification.ipynb

📜 License

This project is licensed under the MIT License.
