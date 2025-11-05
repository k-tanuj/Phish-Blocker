<!-- 🌐 README for Phish-Blocker  -->

<!-- HEADER -->
<div align="center" style="background: linear-gradient(135deg, #0077b6, #00b4d8, #90e0ef); padding: 35px; border-radius: 18px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
  <img src="https://cdn-icons-png.flaticon.com/512/906/906334.png" alt="Shield Icon" width="110"/>
  <h1 style="color: white; font-size: 50px; margin: 10px 0;">🛡️ Phish-Blocker</h1>
  <h3 style="color: #f1f1f1; font-weight: 400; margin-bottom: 15px;">An Open-Source Phishing URL Detection Tool Powered by Machine Learning</h3>
  <p>
    <img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square">
    <img src="https://img.shields.io/badge/Status-Active-success?style=flat-square">
    <img src="https://img.shields.io/badge/Category-Cybersecurity-important?style=flat-square">
  </p>
</div>

---

## 🚀 Overview  
Phish-Blocker intelligently identifies and blocks phishing URLs before they harm users.  
It combines **URL feature extraction** and **machine learning models** to classify sites as *legitimate* or *phishing* in milliseconds.

<div align="center" style="margin: 15px 0;">
  <img src="https://cdn-icons-png.flaticon.com/512/901/901175.png" width="90" alt="Data Icon"/>
  <p><i>Dataset-driven intelligence for smarter security.</i></p>
</div>

This project uses the **public phishing dataset from Mendeley Data**, renamed locally as **`Dataset.csv`**:  
🔗 [Phishing Dataset for Machine Learning (Mendeley Data)](https://data.mendeley.com/datasets/vfszbj9b36/1)

---

## 🧩 Features  
<div style="margin-left:20px; font-size:16px; line-height:1.8em;">
✅ Advanced URL feature extraction (domain, path, query)  
🤖 ML-based phishing detection with Random Forest / XGBoost  
⚙️ Single or bulk classification support  
🧠 Retrainable with <b>Dataset.csv</b> or your own data  
🧪 Flask web demo for quick live testing  
🧩 Modular architecture for integration in other security systems  
</div>

---

## 📂 Project Structure  
<pre style="background:#f8f9fa; padding:15px; border-radius:10px; border:1px solid #ddd; font-size:15px;">
Phish-Blocker/
├── main.py                   → Launches Flask web app
├── train_model.py            → Trains ML model using Dataset.csv
├── predict.py                → Predicts if a URL is phishing or safe
├── url_feature_extractor.py  → Extracts URL-level features
├── db.py                     → Database/log handler
├── demo.py                   → CLI demo
├── test_detection.py         → Unit tests
├── test.py                   → Extra utilities
├── add_missing_columns.py    → Dataset adjustment tool
├── Dataset.csv               → Dataset (from Mendeley Data)
└── static/                   → Frontend assets (HTML, CSS, JS)
</pre>

---

## 🛠️ Getting Started  

### 🧱 Prerequisites  
- Python **3.8+**  
- pip  

### 💻 Installation  

# Clone the repository
git clone https://github.com/k-tanuj/Phish-Blocker.git
cd Phish-Blocker

# Install dependencies
pip install -r requirements.txt


▶️ Usage
1️⃣ Download Dataset
Download and rename your dataset as Dataset.csv
🔗 Mendeley Dataset Link

2️⃣ Train the Model
python train_model.py --dataset Dataset.csv

3️⃣ Predict a URL
python predict.py --url "http://example.com/suspicious"

4️⃣ Run the Web Demo
python main.py
Then visit http://localhost:5000


🧠 How It Works
<div align="center" style="margin: 10px 0;"> <img src="https://cdn-icons-png.flaticon.com/512/864/864685.png" width="90" alt="Process Icon"/> </div>
User Input:
The system accepts a URL from the interface or CLI.

Feature Extraction:
url_feature_extractor.py analyzes and extracts:

URL and domain length

Number of dots, slashes, digits, symbols

Presence of redirects or subdomains

Model Classification:
Extracted features are fed to a trained ML model (Random Forest / XGBoost).

Prediction:

✅ Safe → Legitimate website

🚨 Phishing → Malicious or suspicious site

Output Display:
Results appear on the Flask web interface and can be logged in the database.

<div align="center" style="margin-top:15px;"> <img src="https://github.com/edent/SuperTinyIcons/raw/master/images/svg/python.svg" width="60"> <img src="https://cdn-icons-png.flaticon.com/512/841/841364.png" width="60"> <img src="https://cdn-icons-png.flaticon.com/512/906/906324.png" width="60"> <p><i>Machine Learning workflow simplified.</i></p> </div>


🧪 Testing
pytest test_detection.py


📦 Requirements
<pre style="background:#f8f9fa; padding:15px; border-radius:10px; border:1px solid #ddd; font-size:15px;"> numpy==1.26.4 pandas==2.2.3 scikit-learn==1.5.2 joblib==1.4.2 xgboost==2.1.1 Flask==3.0.3 Flask-Cors==5.0.0 matplotlib==3.9.2 seaborn==0.13.2 pytest==8.3.3 requests==2.32.3 beautifulsoup4==4.12.3 tldextract==5.1.2 </pre>


🙏 Acknowledgements
<div style="font-size:15px; line-height:1.8em;"> - Dataset from <b>Mendeley Data</b> — saved as <b>Dataset.csv</b> - Built by <b>Tanuj Kumawat</b> 🧠 with inspiration from real-world phishing detection systems - Made possible thanks to open-source Python libraries and the global developer community </div>

<h3 align="center" style="margin-top:30px; font-weight:normal; color:#555;"> 💬 <i>“In cybersecurity, prevention is better than cure — let Phish-Blocker be your first line of defense.”</i> </h3> 
