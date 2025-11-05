<!-- 🌐 README for Phish-Blocker  -->

<div align="center" style="background: linear-gradient(135deg, #0077b6, #00b4d8, #90e0ef); padding: 30px; border-radius: 20px; box-shadow: 0 0 10px rgba(0,0,0,0.2);">
  <h1 style="color: white; font-size: 50px; margin-bottom: 10px;">🛡️ Phish-Blocker</h1>
  <h3 style="color: #f1f1f1; font-weight: 400;">An Open-Source Phishing URL Detection Tool powered by Machine Learning</h3>
  <p>
    <img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square" alt="Python Version">
    <img src="https://img.shields.io/badge/Status-Active-success?style=flat-square" alt="Status">
    <img src="https://img.shields.io/badge/Category-Cybersecurity-important?style=flat-square" alt="Category">
  </p>
</div>

---

## 🚀 Overview  
Phish-Blocker is a lightweight and intelligent system that detects and blocks phishing URLs in real time.  
It combines **URL feature extraction** with **machine learning algorithms** to accurately classify URLs as *legitimate* or *phishing*.  

This project uses the **public phishing dataset from Mendeley Data**, renamed locally as **`Dataset.csv`**:  
🔗 [Phishing Dataset for Machine Learning (Mendeley Data)](https://data.mendeley.com/datasets/vfszbj9b36/1)

Built for developers, researchers, and cybersecurity enthusiasts who value **explainable, open-source protection systems**.

---

## 🧩 Features  
<div style="margin-left:20px; line-height:1.7em; font-size:16px;">
✅ Intelligent URL feature extraction (domain, path, and query analysis)  
🤖 Machine-learning-based phishing classification  
⚙️ Supports both single and bulk URL detection  
🧠 Easy model retraining using <b>Dataset.csv</b>  
🧪 Interactive Flask-based demo interface  
🧩 Modular and extendable structure — integrate into your own apps effortlessly  
</div>

---

## 📂 Project Structure  
<pre style="background:#f8f9fa; padding:15px; border-radius:10px; border:1px solid #ddd; font-size:15px;">
Phish-Blocker/
├── main.py                   → Runs the web demo/application
├── train_model.py            → Trains ML model using Dataset.csv
├── predict.py                → Predicts if a URL is phishing or safe
├── url_feature_extractor.py  → Extracts structured features from URLs
├── db.py                     → Manages logging or database operations
├── demo.py                   → CLI / interactive demo
├── test_detection.py         → Unit tests for detection logic
├── test.py                   → Additional testing utility
├── add_missing_columns.py    → Adjusts dataset schema if needed
├── Dataset.csv               → Dataset (downloaded from Mendeley Data)
└── static/                   → Frontend assets (HTML, CSS, JS)
</pre>

---

## 🛠️ Getting Started  

### 🧱 Prerequisites  
- Python **3.8+**  
- pip (Python package manager)

### 💻 Installation  

# Clone the repository
git clone https://github.com/k-tanuj/Phish-Blocker.git
cd Phish-Blocker

# Install dependencies
pip install -r requirements.txt

▶️ Usage
1️⃣ Download the Dataset
Download the phishing dataset from Mendeley and save it as Dataset.csv in the root folder:
🔗 https://data.mendeley.com/datasets/vfszbj9b36/1

2️⃣ Train the Model
Train the phishing detection model using Dataset.csv:
python train_model.py --dataset Dataset.csv

3️⃣ Predict a Single URL
Classify whether a specific URL is phishing or safe:
python predict.py --url "http://example.com/suspicious"

4️⃣ Run the Demo Interface
Launch the local web interface for testing:
python main.py
Then open http://localhost:5000 in your browser.

🧠 How It Works
<div style="font-size:16px; line-height:1.8em;"> 1. The system accepts a URL input. 2. <code>url_feature_extractor.py</code> analyzes it and extracts measurable attributes such as: • URL and domain length • Number of dots, slashes, digits, and special symbols • Presence of redirects or subdomains 3. Extracted features are passed to the trained ML model (e.g., Random Forest, XGBoost). 4. The model predicts: <b>Safe</b> ✅ or <b>Phishing</b> 🚨. 5. The result is displayed on the web interface and optionally logged in the database. </div>
🧪 Testing
To ensure everything works as intended, run:
pytest test_detection.py

📦 Requirements
Install all dependencies using:
pip install -r requirements.txt
Contents of requirements.txt
<pre style="background:#f8f9fa; padding:15px; border-radius:10px; border:1px solid #ddd; font-size:15px;"> numpy==1.26.4 pandas==2.2.3 scikit-learn==1.5.2 joblib==1.4.2 xgboost==2.1.1 Flask==3.0.3 Flask-Cors==5.0.0 matplotlib==3.9.2 seaborn==0.13.2 pytest==8.3.3 requests==2.32.3 beautifulsoup4==4.12.3 tldextract==5.1.2 </pre>

🙏 Acknowledgements
<div style="font-size:15px; line-height:1.8em;"> - Dataset sourced from <b>Mendeley Data</b> — stored locally as <b>Dataset.csv</b>. - Inspired by traditional phishing-detection approaches enhanced with modern ML. - Built with love by <b>Tanuj Kumawat</b> ❤️ using Python and Flask. - Gratitude to all open-source libraries and contributors that made this project possible. </div>
<h3 align="center" style="margin-top:30px; font-weight:normal; color:#555;"> 💬 <i>“In cybersecurity, prevention is better than cure — let Phish-Blocker be your first line of defense.”</i> </h3>
