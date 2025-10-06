# 🛒 Shopping Behavior Prediction

This project implements a **machine learning classifier** to predict whether a user will make a purchase during an online shopping session based on session data.

---

## 📖 Overview

The project uses a dataset of user sessions (`shopping.csv`) with approximately 12,000 rows. Each row represents a user session with **17 features** describing user activity, browser, system, and session metrics, as well as the target label (`Revenue`) indicating whether the user made a purchase.

### Features

- **Administrative**: Number of administrative pages visited (int)  
- **Administrative_Duration**: Time spent on administrative pages (float)  
- **Informational**: Number of informational pages visited (int)  
- **Informational_Duration**: Time spent on informational pages (float)  
- **ProductRelated**: Number of product-related pages visited (int)  
- **ProductRelated_Duration**: Time spent on product-related pages (float)  
- **BounceRates**, **ExitRates**, **PageValues**: Metrics from Google Analytics (float)  
- **SpecialDay**: Proximity to a special day (float)  
- **Month**: Month of the session (int 0–11)  
- **OperatingSystems**, **Browser**, **Region**, **TrafficType**: User and system info (int)  
- **VisitorType**: 1 for returning visitors, 0 otherwise (int)  
- **Weekend**: 1 if session was on a weekend, 0 otherwise (int)  

**Label:** `Revenue` – 1 if user made a purchase, 0 otherwise.

---

## 🛠️ Project Files

```text
shopping-predictor/
│
├── shopping.csv         # User session data
├── shopping.py          # Main program: data loading, model training, evaluation
├── requirements.txt     # Dependencies
├── LICENSE              # MIT License
└── README.md            # Documentation (this file)
```
## ▶️ Usage

1. Clone the repository:
```python
git clone https://github.com/yourusername/shopping-predictor.git
cd shopping-predictor
```
2. Install dependencies:
```python
pip install -r requirements.txt
```
3. Run the predictor:
```python
python shopping.py
```
The program will:

1. Load and preprocess the dataset.
2. Split data into training and testing sets.
3. Train a 1-Nearest Neighbor (1-NN) classifier.
4. Evaluate the model using sensitivity and specificity metrics.

## 🔧 Dependencies / Requirements
- Python 3.8 or higher
- pandas – for CSV data handling
- scikit-learn – for K-Nearest Neighbor classifier
Example `requirements.txt`:
```python
pandas>=1.5.0
scikit-learn>=1.2.0
```
## 📈 Evaluation Metrics
- Sensitivity (True Positive Rate):
  Proportion of actual buyers correctly predicted as buyers.
- Specificity (True Negative Rate):
  Proportion of non-buyers correctly predicted as non-buyers.

## 🏁 Credits
Educational purpose: Demonstrates data preprocessing, feature encoding, and KNN classifier usage for supervised machine learning tasks.
Dataset is synthetic and based on online shopping session behaviors.

## 📄 License
```text
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
