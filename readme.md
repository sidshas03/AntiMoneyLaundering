# 🕵️‍♂️ Anti Money Laundering Detection using Transaction Data

This project analyzes synthetic banking transactions to detect patterns associated with money laundering. Using a Kaggle dataset, we perform exploratory data analysis and prepare the ground for classification modeling.

## 📂 Dataset

- **Source:** [Kaggle – Synthetic Transaction Monitoring Dataset](https://www.kaggle.com/datasets/berkanoztas/synthetic-transaction-monitoring-dataset-aml)
- **File:** `SAML-D.csv` (~996MB)
- **Key Columns:**
  - `Time`, `Date`: Transaction timestamp
  - `Sender_account`, `Receiver_account`: Pseudonymous account IDs
  - `Amount`: Monetary value of transaction
  - `Payment_type`: Type of transaction (e.g., CASH_OUT, TRANSFER)
  - `Is_laundering`: Target flag (1 = laundering, 0 = legitimate)

## 🛠️ Tech Stack

- Python 3
- Google Colab
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (for metrics and modeling)

## 📊 Exploratory Data Analysis

We analyze trends in:
- Frequency of laundering by `Payment_type`
- Amount patterns in laundering vs normal cases
- Group-wise statistical summaries

### Sample Insights:
- Certain payment types (e.g., TRANSFER) have higher laundering rates.
- Laundering transactions often involve higher maximum and average amounts than regular ones.

## 🚀 How to Run (Colab)

1. Open `Anti_Money_Laundering.ipynb` in Google Colab.
2. Upload your `kaggle.json` API key.
3. Run the cell to authenticate and download the dataset.
4. Execute the EDA blocks and modify or extend as needed.

## 📈 Planned Extensions

- Train machine learning models (Logistic Regression, XGBoost)
- ROC-AUC and confusion matrix evaluations
- Integrate anomaly detection
- Convert pipeline into real-time dashboard

## 📁 Project Structure
├── Anti_Money_Laundering.ipynb # Main analysis notebook
└── README.md # Project documentation


## 🧠 Author's Note

This is a synthetic dataset, but it reflects realistic fraud detection challenges. The aim is to develop interpretable workflows for financial surveillance.

## 📩 Contact

**Likhit Babu**  
📧 Email: sp8004@nyu.edu  
🔗 LinkedIn: [Siddharthan P S](https://www.linkedin.com/in/ssiddharthan/)
- 📘 Medium Article: [Detecting Money Laundering with Python and AML Dataset](https://medium.com/@siddharthanps.1/%EF%B8%8F-detecting-money-laundering-using-python-my-hands-on-attempt-5e772aef6e8c)  


## ✅ Tip
To reduce RAM usage in Colab:
- Use `usecols` to load selective columns
- Downcast numeric types with `pd.to_numeric(..., downcast=)`
