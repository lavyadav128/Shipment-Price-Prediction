# 🚢 Supply Chain Shipment Price Prediction

An end-to-end Machine Learning web application predicting international and domestic shipment freight pricing using ensemble regression algorithms (CatBoost, XGBoost, Random Forest).

---

## 📌 Project Overview
Freight pricing in international supply chains is influenced by dynamic factors including shipping distance, delivery modes (Air, Ocean, Land), shipment weights, customs duties, fuel surcharges, and carrier capacity. 

This project builds an automated, data-driven pricing intelligence system that forecasts shipment freight costs with high accuracy, enabling logistics planners and procurement teams to optimize freight spend and prevent overpayment.

---

## 📊 Model Performance Comparison

Multiple regression models were trained, evaluated, and fine-tuned:

| Model Architecture | $R^2$ Score |
| :--- | :--- |
| **CatBoost Regressor** | **0.9718** |
| **XGBoost Regressor** | **0.9583** |
| **Random Forest Regressor** | **0.9563** |
| **Support Vector Regressor (SVR)** | **0.9130** |
| **Decision Tree Regressor** | **0.8990** |
| **AdaBoost Regressor** | **0.8598** |
| **K-Neighbors Regressor** | **0.8406** |
| **Linear Regression** | **0.8218** |

*CatBoost Regressor emerged as the best-performing model with an $R^2$ score of **97.18%**.*

---

## 🛠️ Tech Stack & MLOps Architecture

- **Machine Learning:** CatBoost, XGBoost, Scikit-Learn, Pandas, NumPy
- **Web Framework:** Flask (`app.py`), HTML5, CSS3, Bootstrap
- **Containerization:** Docker (`Dockerfile`)
- **CI/CD:** GitHub Actions workflows (`workflows/`)
- **Modular Pipeline:** Structured components in `shipment/` (Data Ingestion, Data Validation, Data Transformation, Model Trainer, Evaluation, Prediction)

---

## 📂 Repository Structure
```
├── config/                  # Pipeline configuration files
├── shipment/                # Core modular ML package
│   ├── components/          # Ingestion, validation, transformation, training, evaluation
│   ├── pipeline/            # Training and prediction pipelines
│   ├── entity/              # Config and artifact entity classes
│   ├── exception/           # Custom exception handling
│   └── logger/              # Execution logging
├── static/                  # Web styling and assets
├── templates/               # Flask UI templates (index.html, predict.html)
├── workflows/               # CI/CD deployment configuration
├── app.py                   # Flask web server
├── Dockerfile               # Production container definition
├── requirements.txt         # Python package dependencies
├── setup.py                 # Package setup installer
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Docker (optional, for containerized run)

### Setup & Execution
1. **Clone the repository:**
   ```bash
   git clone https://github.com/lavyadav128/Shipment-Price-Prediction.git
   cd Shipment-Price-Prediction
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the application:**
   ```bash
   python app.py
   ```
   Open `http://localhost:5000` in your web browser.

---

## 👤 Author
- **Lav Kumar Yadav**
- GitHub: [@lavyadav128](https://github.com/lavyadav128)
- LinkedIn: [Lav Kumar Yadav](https://www.linkedin.com/in/lav-yadav-90476981)