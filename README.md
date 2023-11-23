# ML Model Analyzer

A Flask web app for automated Exploratory Data Analysis (EDA) and quick ML model comparison, with secure server-rendered previews and exports.

## 🚀 Features

- Automated EDA: dataset size, dtypes, missingness, duplicates, memory usage
- Smart target detection and problem-type inference (binary/multiclass vs regression)
- One-click training and comparison across multiple sklearn models
- Feature importance visualization and downloadable model package (model + preprocessors)
- CSV export of model comparison results
- Secure, server-generated HTML for data preview to minimize XSS attack surface

## 🏃 Quick Start

```bash
git clone https://github.com/codestreamhubio/ML-model-analyzer.git
cd ML-model-analyzer

python3 -m venv .venv
source .venv/bin/activate

python -m pip install --upgrade pip
pip install -r requirements.txt

python app.py
```

## 📦 Installation

Prerequisites:
- Python 3.8+
- pip

Steps:
1) Clone the repository
2) Create and activate a virtual environment
3) Install dependencies: `pip install -r requirements.txt`
4) Run the app: `python app.py`

Optional verification:
```bash
python -c "import flask, pandas, sklearn; print('Deps OK')"
```

## 💡 Usage

1) Upload a CSV/XLSX/XLS (max 50MB) to see a safe, server-generated preview
2) Click Analyze to compute EDA (stats, missingness, correlations)
3) Choose the target and confirm problem type (auto-detected; you can override)
4) Start training to compare models; the best model is selected automatically
5) Review metrics and feature importance; export CSV or download the model package
