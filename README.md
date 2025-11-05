<!-- 🌐 README for Phish-Blocker  -->

<!-- HEADER -->
<div align="center" style="background: linear-gradient(135deg, #0077b6, #00b4d8, #90e0ef); padding: 35px; border-radius: 18px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
  <img src="https://cdn-icons-png.flaticon.com/512/1055/1055646.png" alt="Phishing Detection Icon" width="110" style="filter: drop-shadow(0 0 4px rgba(255,255,255,0.5)); border-radius: 10px;"/>

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
  <img src="https://cdn-icons-png.flaticon.com/512/4149/4149684.png" width="90" alt="Data Analysis Icon" style="filter: drop-shadow(0 0 6px rgba(255,255,255,0.7)); border-radius:12px; margin-top:5px;"/>
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


<!-- ======================== -->
<!-- 💡 HOW IT WORKS SECTION -->
<!-- ======================== -->
<div style="max-width:850px; margin:40px auto; padding:25px; background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(0,0,0,0.15)); border-radius:16px; box-shadow:0 6px 20px rgba(0,0,0,0.25); border:1px solid rgba(255,255,255,0.08); font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,Helvetica,Arial,sans-serif;">

  <h2 style="color:#e6f7ff; font-size:28px; font-weight:800; margin-bottom:15px; letter-spacing:0.3px;">🧠 How It Works</h2>

  <div align="center" style="margin: 10px 0;">
    <img src="https://cdn-icons-png.flaticon.com/512/2103/2103827.png" width="95" alt="How It Works Icon" style="filter: drop-shadow(0 0 6px rgba(255,255,255,0.6)); border-radius: 14px;"/>
    <p><i style="color: #9cc9ff;">Machine Learning workflow — from URL input to prediction.</i></p>
  </div>

  <ol style="color:#d7e9ff; font-size:15px; line-height:1.8em; margin-left:20px;">
    <li><b>User Input:</b>  The system accepts a URL from the interface or CLI.</li>
<ol style="color:#d7e9ff; font-size:15px; line-height:1.8em; margin-left:20px;">
  <li style="margin-bottom:12px;">
    <strong>User Input:</strong>
    <div style="margin-top:6px; color:#cfefff;">The system accepts a URL from the interface or CLI.</div>
  </li>

  <li style="margin-bottom:12px;">
    <strong>Feature Extraction:</strong>
    <div style="margin-top:8px; color:#cfefff;">
      The <code style="background:rgba(255,255,255,0.05); padding:2px 6px; border-radius:6px;">url_feature_extractor.py</code> module analyzes and extracts:
      <ul style="margin-top:8px; margin-bottom:6px; color:#dff6ff;">
        <li>URL and domain length</li>
        <li>Number of dots, slashes, digits, and special symbols</li>
        <li>Presence of redirects or subdomains</li>
      </ul>
    </div>
  </li>

  <li style="margin-bottom:12px;">
    <strong>Model Classification:</strong>
    <div style="margin-top:6px; color:#cfefff;">
      Extracted features are fed to a trained ML model (e.g., <strong>Random Forest</strong> or <strong>XGBoost</strong>).
    </div>
  </li>

  <li style="margin-bottom:12px;">
    <strong>Prediction:</strong>
    <div style="margin-top:8px; color:#cfefff;">
      The model outputs a label:
      <ul style="margin-top:8px; margin-bottom:6px; color:#dff6ff;">
        <li>✅ <strong>Safe</strong> — legitimate website</li>
        <li>🚨 <strong>Phishing</strong> — malicious or suspicious site</li>
      </ul>
    </div>
  </li>

  <li style="margin-bottom:6px;">
    <strong>Output Display:</strong>
    <div style="margin-top:6px; color:#cfefff;">Results appear on the Flask web interface and can be logged in the database for auditing.</div>
  </li>
</ol>

  </ol>

  <div align="center" style="margin-top:25px;">
    <img src="https://github.com/edent/SuperTinyIcons/raw/master/images/svg/python.svg" width="60" style="margin:0 6px;">
    <img src="https://cdn-icons-png.flaticon.com/512/841/841364.png" width="60" style="margin:0 6px;">
    <img src="https://cdn-icons-png.flaticon.com/512/906/906324.png" width="60" style="margin:0 6px;">
    <p style="color:#a8d8ff; font-style:italic; margin-top:6px;">Machine Learning workflow simplified.</p>
  </div>
</div>

<!-- ================== -->
<!-- 🔬 TESTING SECTION -->
<!-- ================== -->
<div style="max-width:850px; margin:40px auto; padding:25px; background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(0,0,0,0.15)); border-radius:16px; box-shadow:0 6px 20px rgba(0,0,0,0.25); border:1px solid rgba(255,255,255,0.08); font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,Helvetica,Arial,sans-serif;">
  <h2 style="color:#e6f7ff; font-size:28px; font-weight:800; margin-bottom:12px;">🧪 Testing</h2>
  <pre style="background:rgba(0,0,0,0.65); color:#e8faff; padding:10px 14px; border-radius:8px; font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,'Roboto Mono','Courier New',monospace; font-size:14px;">pytest test_detection.py</pre>
</div>

<!-- ===================== -->
<!-- 📦 REQUIREMENTS BLOCK -->
<!-- ===================== -->
<div style="max-width:850px; margin:40px auto; padding:25px; background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(0,0,0,0.15)); border-radius:16px; box-shadow:0 6px 20px rgba(0,0,0,0.25); border:1px solid rgba(255,255,255,0.08); font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,Helvetica,Arial,sans-serif;">
  <h2 style="color:#e6f7ff; font-size:28px; font-weight:800; margin-bottom:12px;">📦 Requirements</h2>
  <pre style="background:rgba(0,0,0,0.65); color:#dff6ff; padding:15px 18px; border-radius:8px; border:1px solid rgba(255,255,255,0.05); font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,'Roboto Mono','Courier New',monospace; font-size:14px; line-height:1.6em;">
numpy==1.26.4
pandas==2.2.3
scikit-learn==1.5.2
joblib==1.4.2
xgboost==2.1.1
Flask==3.0.3
Flask-Cors==5.0.0
matplotlib==3.9.2
seaborn==0.13.2
pytest==8.3.3
requests==2.32.3
beautifulsoup4==4.12.3
tldextract==5.1.2
  </pre>
</div>

<!-- ====================== -->
<!-- 🙏 ACKNOWLEDGEMENTS -->
<!-- ====================== -->
<div style="max-width:850px; margin:40px auto; padding:25px; background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(0,0,0,0.15)); border-radius:16px; box-shadow:0 6px 20px rgba(0,0,0,0.25); border:1px solid rgba(255,255,255,0.08); font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,Helvetica,Arial,sans-serif;">
  <h2 style="color:#e6f7ff; font-size:28px; font-weight:800; margin-bottom:15px;">🙏 Acknowledgements</h2>
  <ul style="color:#cde7ff; font-size:15px; line-height:1.9em;">
    <li>Dataset from <b>Mendeley Data</b> — saved as <b>Dataset.csv</b>.</li>
    <li>Built by <b>Tanuj Kumawat</b> 🧠 with inspiration from real-world phishing detection systems.</li>
    <li>Made possible thanks to open-source Python libraries and the global developer community.</li>
  </ul>
</div>

<!-- ================= -->
<!-- 💬 FINAL QUOTE -->
<!-- ================= -->
<h3 align="center" style="max-width:750px; margin:50px auto; font-weight:700; color:#ffffff; background:#0077b6; padding:16px 24px; border-radius:14px; box-shadow:0 4px 14px rgba(0,0,0,0.25);">
💬 <i>“In cybersecurity, prevention is better than cure — let Phish-Blocker be your first line of defense.”</i>
</h3>

