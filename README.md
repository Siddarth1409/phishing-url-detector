#  Phishing URL Detector Web App

A machine learning-powered web application that detects whether a given URL is legitimate or a phishing attempt.
Built using Python, Flask, and scikit-learn, this tool provides a simple web interface and keeps a log of all URL predictions.

---

##  Features

-  Detect if a URL is phishing or safe using a trained ML model
-  Logs all prediction results with date & time to `history.csv`
-  View past predictions in a user-friendly table
-  Built with Flask and trained using scikit-learn’s Random Forest

---

##  Machine Learning Details

- **Model**: RandomForestClassifier  
- **Training script**: `train_model.py`  
- **Dataset**: URLs labeled as phishing or legitimate (`dataset.csv`)  
- **Features extracted** (from `features.py`):
  - Length of URL
  - Presence of `@`, `//`, `-`
  - Count of dots, hyphens
  - Use of HTTPS
  - Domain properties, etc.

---

##  Tech Stack

- Python 3
- Flask (for web app)
- Pandas & scikit-learn (for model)
- HTML + Bootstrap (for frontend)
- CSV (for logging)

---

##  Getting Started

1. Clone the repo:

   git clone https://github.com/Siddarth1409/phishing-url-detector.git
   cd phishing-url-detector

2. Install dependencies:

pip install -r requirements.txt

3. Train the model:
python train_model.py

4. Run the Flask app:

python app.py




PROJECT STRUCTURE 

phishing-url-detector/
│
├── app.py                 # Flask application
├── classify_url.py        # Prediction logic
├── train_model.py         # Model training script
├── features.py            # URL feature extraction logic
├── dataset.csv            # Dataset used for training
├── history.csv            # Logged URL prediction history
├── requirements.txt       # Python dependencies
├── templates/
│   ├── index.html         # Home UI
│   └── history.html       # Logs page
└── phishing_model.pkl     # Trained ML model (not uploaded to GitHub)




NOTE : 
The phishing_model.pkl file is not included in the GitHub repo because it exceeds 100MB. To generate your own model file:


python train_model.py


 Author
Siddarth Loni
sdt.loni@gmail.com
🔗 GitHub - Siddarth1409
