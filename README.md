<h1 align="center">Credit Card Fraud Detection & Risk Management System</h1>

<p align="center">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
    <img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python Version">
    <img src="https://img.shields.io/badge/Streamlit-1.25.0-red.svg" alt="Streamlit Version">
    <img src="https://img.shields.io/badge/scikit--learn-1.3.0-orange.svg" alt="Scikit-learn Version">
</p>

## 📖 About The Project

This project is a comprehensive system for detecting fraudulent credit card transactions and managing associated risks. It uses a combination of machine learning models, advanced feature engineering, and a real-time dashboard to provide a powerful tool for financial institutions. The interactive Streamlit dashboard allows for real-time monitoring, anomaly detection, balance forecasting, and model performance evaluation.

## ✨ Key Features

*   **Real-time Fraud Detection:** Utilizes an ensemble of machine learning models (Isolation Forest and Random Forest) to detect fraudulent transactions in real-time.
*   **Advanced Feature Engineering:** Creates sophisticated features to improve model accuracy, such as transaction velocity, time-based features, and merchant analysis.
*   **Balance Forecasting:** Predicts future account balances using Facebook's Prophet model to identify accounts at risk of overdraft.
*   **Model Explainability:** Provides insights into why a transaction is flagged as fraudulent using SHAP (SHapley Additive exPlanations).
*   **Interactive Dashboard:** A Streamlit-based dashboard for monitoring key metrics, detecting anomalies, forecasting balances, and evaluating model performance.
*   **End-to-End Pipeline:** A complete data pipeline for ingestion, transformation, model training, and storage using a SQLite database.

## 🛠️ Built With

This project is built with a modern Python stack for machine learning and data science.

*   **Backend:** Python
*   **Machine Learning:** scikit-learn, Prophet, SHAP
*   **Data Manipulation:** Pandas, NumPy
*   **Dashboard:** Streamlit
*   **Visualization:** Plotly, Seaborn, Matplotlib
*   **Orchestration:** Apache Airflow
*   **Database:** SQLite, SQLAlchemy

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

Ensure you have Python 3.9 or higher installed. You can download it from [python.org](https://www.python.org/downloads/).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/Credit-Card-Fraud-Detection-Risk-Management-System.git
    cd Credit-Card-Fraud-Detection-Risk-Management-System
    ```
2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

To use the application, follow these steps:

1.  **Download the data:**
    ```bash
    python scripts/download_data.py
    ```
2.  **Run the main data pipeline:**
    ```bash
    python scripts/main_pipeline.py
    ```
3.  **Launch the dashboard:**
    ```bash
    streamlit run fraud_detection_dashboard.py
    ```
    Navigate to `http://localhost:8501` in your web browser.

## 📂 Project Structure

```
├── data/
├── models/
├── src/
│   ├── ingestion/
│   ├── features/
│   ├── models/
│   ├── evaluation/
│   ├── explainability/
│   └── utils/
├── scripts/
├── training_models/
├── fraud_detection_dashboard.py
├── requirements.txt
└── README.md
```

## 🤖 Model & Pipeline

The project employs a sophisticated pipeline and a variety of models to ensure accurate fraud detection and risk management.

*   **Fraud Detection Models:**
    *   **Isolation Forest:** An unsupervised algorithm for anomaly detection.
    *   **Random Forest:** A supervised model trained on labeled transaction data.
    *   **Ensemble Approach:** Combines the strengths of both models for enhanced accuracy.
*   **Balance Forecasting Model:**
    *   **Prophet:** A time-series forecasting model from Facebook used for predicting account balances.
*   **Data Pipeline:**
    *   The pipeline starts with data ingestion from CSV files into a SQLite database.
    *   It then proceeds with feature engineering, creating new variables for the models.
    *   Finally, it trains the models and stores the artifacts for use in the dashboard.

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
