# Student Performance Predictor

🔗 **Live Demo:** [Perdormance Predictor](https://performance-predictor-ee9q.onrender.com)

This project is an end-to-end Machine Learning application that predicts a student's math score based on various personal and academic factors. The model is deployed as a web application using Flask.

> **Note:** This project was developed as a learning exercise to understand and implement the complete lifecycle of a machine learning project. While functional, it serves primarily as a demonstration of these concepts.

---


## 🚀 Features

* **Interactive Web Interface:** A user-friendly web form to input student data.
* **ML-Powered Predictions:** Utilizes a trained regression model to predict math scores in real-time.
* **Data Preprocessing Pipeline:** A robust Scikit-Learn pipeline handles data cleaning, imputation, and feature scaling.
* **Model Training & Evaluation:** The project includes scripts for training multiple models and selecting the best one based on performance.

---

## 🛠️ Tech Stack

* **Backend:** Python, Flask
* **Machine Learning:** Scikit-Learn, Pandas, NumPy, CatBoost, XGBoost
* **Frontend:** HTML, Tailwind CSS
* **Deployment:** The application is ready to be deployed on any platform that supports WSGI applications.

---

## ⚙️ Setup and Installation

To run this project locally, please follow these steps:

### Prerequisites

* Python 3.9+
* pip (Python package installer)

### 1. Clone the Repository

Clone this repository to your local machine:
```bash
git clone [https://github.com/TaherBatterywala/your-repo-name.git](https://github.com/TaherBatterywala/your-repo-name.git)
cd your-repo-name
```

### 2. Create a Virtual Environment

It is highly recommended to create a virtual environment to manage project dependencies.
```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

Install all the required packages using the `requirements.txt` file.
```bash
pip install -r requirements.txt
```

---

## 📈 Usage

### 1. Run the Training Pipeline

Before you can run the web application, you need to train the model and generate the necessary artifact files (`preprocessor.pkl` and `model.pkl`).

Run the following command from the root directory of the project:
```bash
python src/components/data_ingestion.py
```
This command will execute the entire pipeline: data ingestion, data transformation, model training, and will save the artifacts in the `artifacts` directory.

### 2. Start the Flask Application

Once the training pipeline has completed successfully, you can start the web server:
```bash
python app.py
```

The application will be running at **http://127.0.0.1:5000**. Open this URL in your web browser to use the application.

---

## 📂 Project Structure

```
.
├── artifacts/              # Stores the trained model and preprocessor
├── logs/                   # Stores application logs
├── notebook/               # Jupyter notebooks for experimentation
├── src/                    # Source code
│   ├── __init__.py
│   ├── components/         # Data ingestion, transformation, model training
│   ├── pipeline/           # Prediction pipeline
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── templates/              # HTML files for the web interface
│   ├── index.html
│   └── home.html
├── app.py                  # Main Flask application file
├── requirements.txt        # Project dependencies
└── README.md
