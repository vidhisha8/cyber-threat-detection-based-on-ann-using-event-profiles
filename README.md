# Cyber Threat Detection Based on ANN Using Event Profiles

## What is this project about?
This was my third-year B.Tech project focused on applying Machine Learning and Deep Learning to cybersecurity.

Traditional rule-based security systems generate massive volumes of false alarms, causing security analysts to waste time investigating benign alerts. The goal of this project was to build an AI-assisted SIEM (Security Information and Event Management) prototype capable of separating actual cyber threats from background noise with high precision.

## What I built
A full-stack **Django** web application that:
1. Ingests raw security event logs (~10,000 records) and preprocesses them into structured numerical event profiles using **TF-IDF feature extraction**.
2. Trains and benchmarks **5 traditional Machine Learning classifiers** against **Deep Learning architectures (ANN/FCNN and LSTM)** using an 80/20 stratified train-test split.
3. Provides an interactive web dashboard allowing users to upload datasets, trigger model training/evaluation modules, and compare performance metrics (Accuracy, Precision, Recall, and F1-Score).

## Model Benchmarking Results
I evaluated 7 classification models on the processed event profiles:

| Model Category | Algorithm | Performance Summary |
| :--- | :--- | :--- |
| **Deep Learning** | **LSTM (Long Short-Term Memory)** | **Best — 94% Accuracy** (Highest Precision, Recall & F1-Score) |
| **Deep Learning** | **ANN / FCNN (Fully Connected Network)** | **Second Best** — Strong baseline neural performance |
| **Machine Learning** | **Random Forest** | Competitive ensemble performance |
| **Machine Learning** | **Support Vector Machine (SVM)** | Moderate classification accuracy |
| **Machine Learning** | **K-Nearest Neighbors (KNN)** | Moderate performance on high-dimensional vectors |
| **Machine Learning** | **Naive Bayes** | Lower accuracy due to feature independence assumptions |
| **Machine Learning** | **Decision Tree** | Prone to overfitting on raw log features |

The **LSTM** architecture outperformed conventional baselines across accuracy, precision, recall, and F-measure by effectively capturing sequential patterns across the vectorized event logs.

## Dataset Overview
* **Volume:** ~10,000 network security event log records
* **Validation Strategy:** 80/20 Train-Test Split (~8,000 training records / 2,000 testing records)

## Tech Stack
* **Programming Language:** Python
* **Web Framework:** Django (HTML/CSS Frontend, Python Backend)
* **Deep Learning:** TensorFlow / Keras (LSTM, ANN / Multi-Layer Perceptron)
* **Machine Learning:** Scikit-Learn (Random Forest, SVM, KNN, Naive Bayes, Decision Tree)
* **Data Processing & Feature Extraction:** Pandas, NumPy, Scikit-Learn (`TfidfVectorizer`)
* **Visualization:** Matplotlib

## How to Run Locally

```bash
# 1. Clone the repository
git clone [https://github.com/vidhisha8/cyber-threat-detection-ann.git](https://github.com/vidhisha8/cyber-threat-detection-ann.git)
cd cyber-threat-detection-ann

# 2. Install required dependencies
pip install -r requirements.txt

# 3. Run database migrations (if running for the first time)
python manage.py migrate

# 4. Start the Django development server
python manage.py runserver

# 5. Open in your browser
# [http://127.0.0.1:8000](http://127.0.0.1:8000)
