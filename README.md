# 📊 Netflix-Data-Analysis-python

## 🔍 Project Overview

Netflix, being a data-driven company, relies heavily on insights from data to optimize its **recommendation engine**, **content strategy**, and **user engagement**. This project involves analyzing a dataset containing **9,827 Netflix movie records**. The objective was to perform **data preprocessing**, **exploratory analysis**, and **insight generation** to support business decisions.

---

## 📁 Dataset Overview

- **Total Rows:** 9,827  
- **Total Columns:** 9  

### 🔑 Key Columns:

- `Title` – Movie title  
- `Release_Date` – Date of release  
- `Popularity` – Popularity score  
- `Vote_Count` – Total number of user votes  
- `Vote_Average` – Average rating  
- `Genre` – Movie genres (comma-separated)  
- Other columns dropped during analysis: `Overview`, `Original_Language`, `Poster_Url`  

---

## 📚 Libraries Used

The following Python libraries were used in this project:

| Library         | Purpose |
|----------------|---------|
| **pandas**     | Data manipulation and analysis |
| **numpy**      | Numerical operations and array handling |
| **matplotlib** | Data visualization (basic plots, histograms) |
| **seaborn**    | Statistical data visualization (barplots, countplots) |

---

## 🛠️ Data Cleaning and Preprocessing

- ✅ No null values and no duplicates were found.
- ✅ **Date Formatting:**
  - Converted `Release_Date` from object to datetime.
  - Extracted **year** from the date for trend analysis.
- ✅ **Dropped Columns:**
  - Removed `Overview`, `Original_Language`, and `Poster_Url` as they were not relevant.
- ✅ **Vote_Average Binning:**
  - Created quartile-based categories:
    - `not_popular`
    - `below_avg`
    - `avg`
    - `popular`
- ✅ **Genre Cleaning:**
  - Split `Genre` values into lists.
  - Used `.explode()` to normalize into one row per genre per movie.
- ✅ **Category Casting:**
  - Converted `Genre` and `Vote_Average` into `category` types for memory efficiency and improved analysis.

---

## 📈 Data Analysis & Insights

### ✅ 1. Most Frequent Genre

- **Top Genre:** Drama  
- Followed by: **Comedy** and **Thriller**  
- **Visualization:** Bar plot using `seaborn.catplot()` clearly shows genre distribution.

### ✅ 2. Vote Category Distribution

- Highest number of movies fall under the **"not_popular"** category.

| Category      | Movie Count |
|---------------|-------------|
| not_popular   | 2,467       |
| below_avg     | 2,398       |
| avg           | 2,412       |
| popular       | 2,450       |

### ✅ 3. Most Popular Movie

- 🎬 **Movie:** *Spider-Man: No Way Home*  
- 💥 **Popularity Score:** 5083.954  
- 🎭 **Genres:** Action, Adventure, Science Fiction  

### ✅ 4. Least Popular Movies

Two titles had the **lowest popularity score** of **13.354**:

1. **The United States vs. Billie Holiday**  
   - Genres: Music, Drama, History  
2. **Threads**  
   - Genres: War, Drama, Science Fiction  

### ✅ 5. Year with Most Releases

- **Year:** 2020  
- Notable spike likely due to the **COVID-19 pandemic** and streaming demand surge.

---

## 📌 Final Thoughts

This analysis provided several actionable business insights:

- **Drama** is the dominant genre — could be due to user preference or content availability.
- Highly popular titles are often in **Action**, **Adventure**, or **Sci-Fi** genres.
- Many titles have **low average ratings**, suggesting room for **content quality improvements**.
- **Yearly trends** help track content growth phases (e.g., the spike in 2020).

---

## 🔚 Conclusion

This project successfully:

- ✅ Cleaned and transformed the dataset  
- ✅ Explored genre distribution, rating patterns, and popularity metrics  
- ✅ Built clear visualizations for storytelling and decision-making  

<!-- ### 🚀 Future Work

- Build a **content-based recommendation system**  
- Apply **clustering** to group similar movies  
- Explore **user-behavior segmentation** for personalization  

--- -->



