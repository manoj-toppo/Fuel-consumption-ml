End-to-End Machine Learning project predicting car **fuel efficiency (MPG)** using the UCI Auto MPG dataset. Follows Harshit Tyagi's tutorial series—covers EDA, pipelines, model training, evaluation, and Flask deployment.

## 🎯 Business Problem

**Predict MPG** (continuous target) from car specs like `weight`, `horsepower`, `cylinders`.  
**Best Model**: Random Forest (RMSE **4.72**, R² **~0.85**) after GridSearchCV. [web:16]

| Top Features | Importance |
|--------------|------------|
| weight       | ~35%      |
| horsepower   | ~30%      |
| displacement | ~15%      | [web:16]

## 🚀 Quick Start

```bash
# Clone & install
git clone <your-repo>
cd auto-mpg-predictor
pip install -r requirements.txt

# Run EDA notebook
jupyter notebook notebooks/01_EDA_and_Splitting.ipynb

# Train best model
python src/train_final_model.py

# Launch Flask API
python app.py
curl "http://localhost:5000/predict?weight=3000&horsepower=130"

| Model             | Test RMSE |
| ----------------- | --------- |
| Linear Regression | 7.89      |
| Decision Tree     | 7.64      |
| Random Forest     | 4.72      |
| SVM               | 6.34      |
