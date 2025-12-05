# IMDB Movie Reviews – Data Preprocessing & EDA

## 🎯 Objective
Use the IMDB 50K movie reviews dataset to:
- Perform basic data preprocessing  
- Do exploratory data analysis (EDA)  
- Understand the distribution of sentiments and review lengths  

---

## 📂 Dataset
- **Source**: IMDB Dataset of 50K Movie Reviews (Kaggle)  
- **File**: `IMDB Dataset.csv`  
- **Columns**:
  - `review` – text of the movie review  
  - `sentiment` – label (`positive` or `negative`)  

---
## File Structure
imdb-ml-intro/
│── IMDB Dataset.csv
│── imdb_eda.ipynb        # your notebook
│── REPORT.md             # the markdown report
│── README.md             # short project description

---

## 🧹 Data Preprocessing

Steps performed:

1. **Loaded** the CSV using `pandas.read_csv()`
2. **Checked for missing values** using `isnull().sum()`
3. **Removed duplicate reviews** based on the `review` column  
4. Created a new feature:
   - `review_length` – number of characters in each review  
5. Optionally converted reviews to lowercase (`clean_review`) for easier text processing

---

## 📊 Exploratory Data Analysis (EDA)

### 1️⃣ Sentiment Distribution
- Counted how many reviews are **positive** vs **negative**
- Plotted a bar chart using `seaborn.countplot`

**Insight:**
- The dataset is approximately balanced between positive and negative reviews.

### 2️⃣ Review Length
- Calculated summary statistics of `review_length`
- Plotted a histogram of review lengths

**Insight:**
- Most reviews have a medium to long length.
- There are some very long reviews, which appear as a long tail in the histogram.

### 3️⃣ Review Length vs Sentiment
- Created a boxplot of `review_length` grouped by `sentiment`

**Insight:**
- On average, positive and negative reviews have similar length distributions.
- There might be a slight trend of one sentiment having slightly longer reviews, but they overlap strongly.

---

## 📈 Visualizations Included
- Bar chart of sentiment distribution  
- Histogram of review length  
- Boxplot of review length vs sentiment  

These visualizations were created using **Matplotlib** and **Seaborn**.

---

## 🛠 Tools & Libraries
- **Python**
- **Pandas** – for data loading and preprocessing  
- **Matplotlib** & **Seaborn** – for visualizations  
- **Jupyter Notebook / Google Colab** – for interactive analysis  

---

## Conclusion
The IMDB 50K reviews dataset is a clean and balanced dataset for basic NLP and ML tasks.  
With simple preprocessing and EDA, we can understand:

- How reviews are distributed by sentiment  
- How long movie reviews tend to be  
- That the dataset is suitable for building a binary sentiment classifier in future work.


