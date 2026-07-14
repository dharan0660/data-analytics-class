# Real Datasets Setup Guide

## 🚀 Quick Start

Follow these steps to download and analyze real datasets from Kaggle:

### Step 1: Install Kaggle API
```bash
pip install kaggle
```

### Step 2: Set Up Kaggle Credentials
1. Go to https://www.kaggle.com/settings/account
2. Scroll to "API" section
3. Click "Create New API Token"
4. This downloads `kaggle.json`
5. Place it in `~/.kaggle/` folder

**For Windows:**
- Place `kaggle.json` in `C:\Users\<YourUsername>\.kaggle\`

**For Mac/Linux:**
- Place `kaggle.json` in `~/.kaggle/`

### Step 3: Download Datasets

**Option A: Using Python Script**
```bash
python real-datasets/download_datasets.py
```

**Option B: Using Bash Script**
```bash
bash real-datasets/download_datasets.sh
```

**Option C: Manual Download from Kaggle**
- Healthcare: https://www.kaggle.com/datasets/hmanglani/healthcare-dataset
- E-Commerce: https://www.kaggle.com/datasets/carrie1/ecommerce-data

### Step 4: Analyze the Data

**Healthcare Analysis:**
```bash
python real-datasets/analysis_scripts/healthcare_analysis.py
```

**E-Commerce Analysis:**
```bash
python real-datasets/analysis_scripts/ecommerce_analysis.py
```

## 📊 Dataset Information

### Healthcare Dataset
- **Size:** Medium (1000-5000+ rows)
- **Columns:** Patient ID, Age, Medical Conditions, Hospital Stays, Treatment Costs, etc.
- **Perfect for:** Cost analysis, patient segmentation, trend analysis
- **URL:** https://www.kaggle.com/datasets/hmanglani/healthcare-dataset

### E-Commerce Sales Dataset
- **Size:** Medium (5000-10000+ rows)
- **Columns:** Invoice No, Customer ID, Product, Quantity, Price, Date, Country, etc.
- **Perfect for:** Sales analysis, customer behavior, revenue forecasting
- **URL:** https://www.kaggle.com/datasets/carrie1/ecommerce-data

## 📁 Folder Structure After Download

```
real-datasets/
├── healthcare/
│   ├── *.csv (downloaded dataset files)
│   └── processed/ (for your processed data)
├── ecommerce/
│   ├── *.csv (downloaded dataset files)
│   └── processed/ (for your processed data)
├── analysis_scripts/
│   ├── healthcare_analysis.py
│   └── ecommerce_analysis.py
├── analysis_notebooks/ (create Jupyter notebooks here)
├── download_datasets.py
├── download_datasets.sh
└── DATASETS.md
```

## 🔍 What's in Each Dataset

### Healthcare Data Includes:
- Patient demographics (age, gender, location)
- Medical conditions and diagnoses
- Hospital stays duration
- Treatment types and costs
- Insurance information
- Blood type and medical history

**Analysis Ideas:**
- Average cost by medical condition
- Hospital stay duration analysis
- Age group distribution
- Cost trends over time
- Patient segmentation

### E-Commerce Data Includes:
- Transaction details (Invoice number, date)
- Customer information (ID, country)
- Product details (name, quantity, price)
- Financial information (unit price, total amount)
- Temporal data (transaction dates)

**Analysis Ideas:**
- Sales trends by month/year
- Top selling products
- Customer lifetime value
- Geographic sales distribution
- Revenue analysis by country
- Customer segmentation

## 💡 Next Steps After Download

1. **Explore Data:**
   ```bash
   python real-datasets/analysis_scripts/healthcare_analysis.py
   python real-datasets/analysis_scripts/ecommerce_analysis.py
   ```

2. **Create Jupyter Notebooks:**
   - Create `.ipynb` files in `analysis_notebooks/` folder
   - Load data with pandas
   - Create visualizations with matplotlib/seaborn

3. **Data Cleaning:**
   - Handle missing values
   - Remove duplicates
   - Data type conversions
   - Save cleaned data to `processed/` folder

4. **Analysis:**
   - Descriptive statistics
   - Trends and patterns
   - Customer segmentation
   - Predictive modeling

## ⚠️ Important Notes

- **License:** All datasets are CC0 (Public Domain)
- **Attribution:** Always cite the original Kaggle dataset in your work
- **Data Privacy:** This data is anonymized/synthetic
- **Size:** Medium-sized datasets for educational purposes

## 🐛 Troubleshooting

**Issue: "Kaggle API not found"**
- Solution: `pip install kaggle`

**Issue: "403 - Authentication failed"**
- Solution: Check if `kaggle.json` is in correct location
- Run: `kaggle config view` to verify

**Issue: "Dataset not found"**
- Solution: Dataset may have been removed from Kaggle
- Check alternative links in DATASETS.md

**Issue: "Permission denied" on shell script**
- Solution: Run `chmod +x real-datasets/download_datasets.sh`

## 📚 Resources

- Kaggle Datasets: https://www.kaggle.com/datasets
- Pandas Documentation: https://pandas.pydata.org/docs/
- Data Analysis Tutorial: https://www.kaggle.com/learn

---

Happy analyzing! 🎉
