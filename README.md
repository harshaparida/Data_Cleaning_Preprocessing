# 📊 Data Cleaning and Preprocessing of Netflix Movies and TV Shows

This project focuses on cleaning and preprocessing a dataset containing information about Netflix Movies and TV Shows. The dataset includes features like title, type, director, cast, country, release year, rating, duration, and more.

---

## 🧹 Data Preprocessing Steps

### ✅ 1. Handling Missing Values
- Used `.isnull()` to identify missing values.
- Columns with all values missing were removed using:
  ```python
  data = data.loc[:, ~data.isnull().all()]
  ```

### ✅ 2. Removing Unnamed/Empty Columns
- Columns without any data (e.g., unnamed columns) were dropped using `.isnull().all()`.

### ✅ 3. Standardizing the `country` Column
- Converted all country names to lowercase and stripped whitespace.
- Applied standard formatting to ensure uniform country names.

### ✅ 4. Date Format Conversion
- The `date_added` column was converted to a consistent `dd-mm-yyyy` format using:
  ```python
  data['date_added'] = pd.to_datetime(data['date_added'], errors='coerce')
  ```

### ✅ 5. Renaming Column Headers
- Converted all column names to lowercase and replaced spaces with underscores for consistency.

### ✅ 6. Data Type Fixes
- `date_added`: Converted to `datetime64`.
- `rating`: Converted to `category` to optimize memory usage.

---

## 📁 Output

- The cleaned dataset is saved as: `cleaned_dataset.csv` (or `.xlsx`)
- You can find the cleaned version inside this repository.

---

## 🛠 Tools Used

- Python 🐍
- Pandas 🐼
- Jupyter Notebook / VS Code
- (Optional) Excel

---

Feel free to contribute or fork this project for your own data cleaning tasks!
