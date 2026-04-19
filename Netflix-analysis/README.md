# 🎬 Netflix Data Analysis

## 📌 Project Overview

This project explores the Netflix titles dataset to uncover trends, patterns, and insights about the platform’s content library. The analysis focuses on content distribution, growth over time, genres, ratings, and production trends.

---

## 📂 Dataset

* Source: Netflix Titles Dataset
* Contains information on movies and TV shows including:

  * Title
  * Type (Movie/TV Show)
  * Director, Cast
  * Country
  * Date Added
  * Release Year
  * Rating
  * Duration
  * Genre (`listed_in`)

---

## 🧹 Data Cleaning & Preparation

The dataset required several preprocessing steps before analysis:

* Handled missing values by filling categorical columns with `"Unknown"`
* Converted `date_added` to datetime format
* Extracted new features:

  * `year_added`
  * `month_added`
* Cleaned and separated the `duration` column into:

  * Numerical values (`duration_int`)
  * Type (`minutes` or `seasons`)
* Split multi-value columns (`country`, `listed_in`) and used `.explode()` for detailed analysis
* Removed duplicate records

---

## 📊 Exploratory Data Analysis

### 🔹 Content Growth Over Time

* Netflix content increased significantly after 2015
* Reflects global expansion and investment in original content

### 🔹 Movies vs TV Shows

* Movies dominate the platform, with roughly twice as many titles as TV shows
* Indicates a stronger focus on film content

### 🔹 Top Producing Countries

* The United States is the leading content producer
* Followed by other major contributors like India and the UK

### 🔹 Popular Genres

* Content spans diverse genres
* International Movies and Dramas are among the most common categories

### 🔹 Content Release Trends

* Content is added consistently throughout the year
* Suggests a steady release strategy rather than seasonal spikes

### 🔹 Movie Duration

* Most movies are between 90–120 minutes
* Aligns with standard feature-length expectations

### 🔹 TV Shows Duration

* Most TV shows have 1–2 seasons
* Indicates a preference for shorter series formats

### 🔹 Ratings Distribution

* Majority of content is rated **TV-MA and TV-14**
* Suggests a focus on mature and teenage audiences

---

## 📌 Key Insights

* Netflix has experienced rapid content growth in recent years
* The platform prioritizes movies over TV shows
* Content production is heavily dominated by the United States
* A wide variety of genres supports a global audience
* Shorter TV series and standard-length movies are most common
* Content is released consistently throughout the year
* Audience targeting leans toward mature and teen viewers

---

## 📈 Tools & Technologies

* Python
* Pandas
* Matplotlib
* Jupyter Notebook

---

## 🚀 Conclusion

This analysis highlights Netflix’s strategy of maintaining a large, diverse content library with a strong emphasis on movies and mature audience engagement. The platform’s steady release pattern and global content distribution reflect its position as a leading streaming service.

---

## 📎 Future Work

* Analyze trends by genre over time
* Compare growth of Movies vs TV Shows
* Build a recommendation system based on content features
