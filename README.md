# ATT&CK TTP Extractor

## 📌 Project Overview

### 🔍 What is this project?

\#️⃣ **ATT&CK TTP Extractor**

This project is an **ATT&CK TTP Extractor**, designed to **scrape, preprocess, balance, and fine-tune** threat intelligence data using **MITRE ATT&CK techniques**. It also provides a **Flask API** and a **web interface** for extracting and analyzing threat techniques from security reports and uploaded documents. 🛡️

### 💡 Why these components?

- **🕵️‍♂️ Data Scraping**: MITRE ATT&CK data is scraped from online sources to create a dataset of attack techniques and threat intelligence. This ensures up-to-date cyber threat information.
- **🛠️ Data Preprocessing**: Cleans and transforms the dataset to extract meaningful features, ensuring better model training by removing unnecessary characters and stopwords.
- **⚖️ Balancing Data**: Uses **TF-IDF and Random Forest-based MultiOutputClassifier** to handle dataset imbalances, ensuring fair training for all techniques.
- **🔄 Converting CSV to JSON**: Converts the dataset into **JSONL (JSON Lines) format** for fine-tuning **GPT-Neo 125M**.
- **🧠 Fine-tuning LLM**: Trains **GPT-Neo 125M** to predict relevant MITRE ATT&CK techniques from security reports.
- **🔗 Flask API**: Lightweight and efficient API to analyze uploaded security reports.
- **🌐 Web Interface**: A user-friendly front-end for uploading files and analyzing reports.

---

## 📂 Project Structure

This project contains **10 main folders**:

1. 📁 **Dataset** - Original dataset files.
2. 📁 **Preprocessed Dataset** - Cleaned datasets.
3. 📁 **Scraping Data** - Scripts for MITRE ATT&CK data scraping.
4. 📁 **Preprocessing Scraped Dataset** - Cleaning and processing scripts.
5. 📁 **Balancing Datasets** - Techniques to balance data distribution.
6. 📁 **Cleaning Balanced Datasets** - Final dataset cleanup.
7. 📁 **Converting CSV to JSON** - Convert CSV to JSONL format.
8. 📁 **Fine-tuning** - Fine-tune the model for better predictions.
9. 📁 **Flask** - API backend for analysis.
10. 📁 **Interface** - Web-based UI for interaction.

---

## 🚀 How to Run

### 🔧 Prerequisites

Ensure you have the following installed:

- ✅ Python 3.x
- ✅ Flask
- ✅ PyTorch
- ✅ Transformers (Hugging Face)
- ✅ pandas, scikit-learn, nltk
- ✅ BeautifulSoup (for web scraping)

### 📥 Installation Steps

1️⃣ Clone the repository:

```sh
git clone https://github.com/j4ik2i5x0/ATT-CK-Ext.git
cd attack-ttp-extractor
```

2️⃣ Install dependencies:

```sh
pip install -r requirements.txt
```

3️⃣ Run the **Flask API**:

```sh
cd flask
python app.py
```

4️⃣ Open the **Web Interface**:

- Open `interface/index.html` in a browser.
- Upload a security report (PDF/TXT) and analyze it.

5️⃣ Fine-tune the model (optional, if retraining is required):

```sh
cd fine-tuning
python training_with_llm.py
```

### ✅ Expected Output

- 📝 JSON response with threat analysis via Flask API.
- 📊 A summarized report highlighting extracted **MITRE ATT&CK techniques** on the web interface.

---

## 🔮 Future Improvements

- 🔄 Enhance dataset diversity.
- 📡 Add more scraping sources.
- 🎯 Improve model accuracy with additional fine-tuning.

### 🤖 Why **GPT-Neo 125M**?

GPT-Neo 125M was chosen as it provides a **lightweight, efficient alternative** to large-scale models like GPT-3, while maintaining effectiveness for **cybersecurity analysis**. Fine-tuning ensures **accurate ATT&CK technique mapping** from security reports. 🔐

### 📄 Why JSON format for fine-tuning?

- JSONL format is **structured for NLP-based training**, allowing the model to process **system prompts, user queries, and responses in a structured manner**.
- This helps map **security reports to MITRE techniques** more effectively.

### ⚖️ Why preprocess and balance datasets?

- **Security datasets are often imbalanced**, where some attack techniques appear more frequently than others.
- Applying **TF-IDF vectorization** and **synthetic oversampling** ensures **fair learning across all techniques**.

📌 *This project aims to improve threat intelligence extraction and enhance cybersecurity analysis using advanced NLP techniques.* 🔥

