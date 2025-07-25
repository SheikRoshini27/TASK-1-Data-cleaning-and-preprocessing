# TASK-1-Data-cleaning-and-preprocessing
# 📊 Netflix Movies and TV Shows Dataset – Data Cleaning

This project involves cleaning and preprocessing the **Netflix Movies and TV Shows dataset**, commonly found on Kaggle, to make it suitable for analysis or visualization.

---

## ✅ Objective

Clean and prepare a raw dataset by:
- Removing duplicates
- Handling missing values
- Standardizing column names and formats
- Converting date and text fields into consistent formats

---

## 📁 Dataset

- **Original File**: `archive.zip` containing `netflix_titles.csv`
- **Cleaned File**: `netflix_titles_cleaned.csv`

---

## 🛠️ Tools Used

- Google Colab (Python 3)
- Libraries: `pandas`, `zipfile`, `os`, `google.colab.files`

---

## 🔧 Cleaning Steps Performed

1. **Unzipped the dataset** and read `netflix_titles.csv`
2. **Standardized column names** to lowercase with underscores (e.g., `release_year`)
3. **Removed duplicates** using `.drop_duplicates()`
4. **Converted date format** of `date_added` to proper `datetime` using `pd.to_datetime()`
5. **Dropped rows** with missing `title` or `type` (essential fields)
6. **Standardized text fields** like `country` using `.str.strip().str.title()`
7. **Checked data types** for consistency (e.g., `release_year` as integer)
8. **Saved the cleaned dataset** as `netflix_titles_cleaned.csv`

---

## 📉 Missing Values (After Cleaning)

| Column       | Missing |
|--------------|---------|
| director     | 2634    |
| cast         | 825     |
| country      | 831     |
| date_added   | 98      |
| rating       | 4       |
| duration     | 3       |
| (others)     | 0       |

Note: Non-critical missing values were **not imputed**, allowing for flexibility in downstream use.

---

## 🚀 How to Use

1. Open the Colab notebook: `netflix_cleaning_colab.ipynb`
2. Upload your `archive.zip` file when prompted
3. Run all cells
4. Download `netflix_titles_cleaned.csv` when processing is complete

---

## 📌 Future Improvements (Optional)
- Impute missing values (e.g., replace missing `director` with `"Unknown"`)
- Split `duration` into two columns: `duration_int`, `duration_type`
- Perform language or genre normalization

---

## 🧑‍💻 Author

Sheik Roshini Tabassum  
Task: Data Cleaning & Preprocessing – Netflix Dataset  
Tool: Google Colab (Python + Pandas)

---
