# 🛡 Keylogger Detection System

**Multi-layer detection of malicious keyloggers** combining:
- 🖥 Real-time process & file monitoring
- 🐍 Simulated keylogger for adversarial testing
- 🤖 Machine Learning classification (LogReg, Random Forest, Gradient Boosting)
- 🌐 Web-scraped process dataset for training

---

## 🚀 How It Works
1. **Heuristic Monitor** — watches running processes, suspicious file creation, and clipboard anomalies (`keylogger/py1`).
2. **Simulated Keylogger** — generates malicious behavior for testing (`keylogger/py2`).
3. **Machine Learning** — trains models on labeled process data (`keylogger_ml/ml_integration.py`).
4. **Data Collection** — captures process snapshots & scrapes processlibrary.com for benign samples.

---

## 📂 Project Structure
```plaintext
keylogger/         # Heuristic monitor & simulated keylogger
keylogger_ml/      # ML training & evaluation pipeline
task_manager.py    # Process snapshot tool
web_scraping.py    # Process name scraper
process_data.csv   # Labeled dataset (malicious / benign)
```

---

## 🛠 Tech Stack
Python, psutil, pynput, cryptography, scikit-learn

Data Handling: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Scraping: BeautifulSoup4, lxml

Windows APIs: win32clipboard, ImageGrab

## 🎯 Future Goals
Integrate trained model into live monitor for real-time detection

Expand features beyond process names (e.g., behavioral metrics)

Add model persistence & dashboard alerts

---

**Disclaimer:** This project includes a simulated keylogger component for educational and research purposes only. Do **not** deploy on systems without explicit permission.

